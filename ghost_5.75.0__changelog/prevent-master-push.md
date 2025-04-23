


GIT Hack: Prevent pushing to master






































Git has this great feature whereby you can execute arbitrary scripts whenever *something* happens on your git repository. A common use case for this is a `pre-receive` hook on the remote repository which prevents people with access from doing destructive actions, like force pushing, which are incredibly easy to do by accident.

Many projects use GitHub as their remote repository, and as GitHub is a service, they do not permit you to upload arbitrary scripts to run on their servers. Makes sense, but how then can you protect your codebase?

Turns out, from [version 1.8.2](https://raw.githubusercontent.com/git/git/master/Documentation/RelNotes/1.8.2.txt?ref=ghost.org), Git has a new `pre-push` hook that lets you do the same thing on your local repository. It's not as handy as setting it up on the remote for all your users, but it does allow you the developer to protect yourself from... yourself.

### Setup the hook

For any repository you want to protect, you need to create a new file called `pre-push` in the `.git/hooks` directory and make sure the file has permission to be executed. Inside the file, you'll add the script you want to run, here's the one I use:

```
#!/bin/bash

protected_branch='master'
current_branch=$(git symbolic-ref HEAD | sed -e 's,.*/\(.*\),\1,')

if [ $protected_branch = $current_branch ]
then
    read -p "You're about to push master, is that what you intended? [y|n] " -n 1 -r < /dev/tty
    echo
    if echo $REPLY | grep -E '^[Yy]$' > /dev/null
    then
        exit 0 # push will execute
    fi
    exit 1 # push will not execute
else
    exit 0 # push will execute
fi

```

This checks if the current branch is `master`, and if so it will prompt you to confirm what you're doing. It doesn't detect whether you're doing a normal push, or a force push, as I prefer to have the confirmation on any push to master. This script is borrowed heavily from scripts by [pixelhandler](https://gist.github.com/pixelhandler/5718585?ref=ghost.org) and [Itty Bitty Labs](https://blog.ittybittyapps.com/blog/2013/09/03/git-pre-push/?ref=ghost.org). For anyone wondering, the weird use of grep is so that this [works on Windows](https://stackoverflow.com/questions/15510083/syntax-error-operator-in-msysgit-bash?ref=ghost.org) as well as \*nix systems.

Once you've added this script to your `.git/hooks/pre-push` file, any push command which operates on the master branch will require confirmation. Simple, but very effective.

**Note:** If the confirmation doesn't appear for you, please check that you have a git version higher than 1.8.2 (run `git --version` on the command line) and also check that the `pre-push` file is executable (run `chmod +x pre-push` on the command line) and try again :)


### Get notified when we ship new features.






 
### You might also like...

Apr

08


![Custom content for every subscriber](/changelog/content/images/size/w750/2025/04/Ghost-Call-to-action-card.png)

Custom content for every subscriber
-----------------------------------

Calls to Action got an upgrade, now you can fine-tune the design and who sees them in more detail.
Apr 8, 2025


New





 
Apr

01


![Social web (beta)](/changelog/content/images/size/w750/2025/04/image--1-.png)

Social web (beta)
-----------------

Increase your reach by connecting your publication to the Fediverse
Apr 1, 2025


Beta





 





 
















 






