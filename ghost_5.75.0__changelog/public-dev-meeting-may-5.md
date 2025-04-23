


Public Dev Meeting May 5











































Each of the past few weeks, the [Ghost Slack](https://forum.ghost.org/?ref=ghost.org) community has continued to grow. This has been great to see and really benefits the community as a whole. There are a lot of people are stepping in to help others with problems and no one is left hanging waiting to see if anyone is around, which would sometimes happen in the irc. If you haven't yet joined, feel free to join our [Slack channel](https://forum.ghost.org/?ref=ghost.org) and say hi!

### New Features

As for Ghost itself, two major additions were merged in this week. One is the long awaited [post preview](https://github.com/TryGhost/Ghost/pull/5200?ref=ghost.org) ([#5200](https://github.com/TryGhost/Ghost/pull/5200?ref=ghost.org)). You can now view your post as you're writing, the same way that you would see it on your blog once the post is published. Definitely a good, and much needed, feature.

![](https://ghost.org/changelog/content/images/2021/01/Screen-Shot-2015-05-05-at-17-49-03.png)

The ability to password protect your blog has also been merged in ([#5103](https://github.com/TryGhost/Ghost/pull/5103?ref=ghost.org)). This allows admins the ability to protect the entire blog with a password to let specific people view it without opening it up to the general public.

![](https://ghost.org/changelog/content/images/2021/01/Screen-Shot-2015-05-05-at-17-53-36.png)![](https://ghost.org/changelog/content/images/2021/01/Screen-Shot-2015-05-05-at-17-54-44-1.png)
### Minor Changes/Bug Fixes

Some of the code injection styles were a little hard to read, so some changes were made to the styling to make it easier to read, and fit the overall style better ([#5196](https://github.com/TryGhost/Ghost/pull/5196?ref=ghost.org)).

A few of the bower dependencies were also updated, partially because a lot of repos are now adopting bower as a standard, so the full git links are no longer needed ([#5198](https://github.com/TryGhost/Ghost/pull/5198?ref=ghost.org)).

A bug was also fixed that would not update the word count for not ASCII characters ([#5208](https://github.com/TryGhost/Ghost/pull/5208?ref=ghost.org)). A new library was added to Ghost which will fix this problem, and any similar problems that might have crept up in the future.

### Progress for Future Features

One other pull request was merged in this week that was a refactor of the front end controller ([#5129](https://github.com/TryGhost/Ghost/pull/5219?ref=ghost.org)). This refactored the code that generates the list of posts for the index, tag, and author pages so that it is now one function. This is very important, and a great first step towards creating [Channels](https://github.com/TryGhost/Ghost/wiki/Channels-101?ref=ghost.org).

Morficus has also created a [proof of concept](https://gist.github.com/morficus/e2fabf24b44ff94978a7?ref=ghost.org) for multi-language in the admin panel. Definitely give that a look if you have some time and provide any feedback you have as multi-language is a feature that has been wanted for quite some time.

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1430843982005208?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 12th May, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-05-12,270,6bj).

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





 





 
















 






