





How to install Ghost locally










































---


In this tutorial, we’ll walk you through the steps of installing Ghost locally on your machine.

Running Ghost locally is essential for custom theme development because it allows you to:

⌚ Make and preview changes to your theme in real-time

🧑‍🔬 Quickly test out new ideas

🤩 Ensure your theme is free of bugs and ready for primetime

⚠️Installing Ghost locally requires that Node be installed on your machine. See [our tutorial for a guide to installing it on Mac OS, Windows, and Linux](https://ghost.org/tutorials/node/).

Install Ghost CLI
-----------------

Ghost CLI (command-line interface) is a tool for installing and configuring Ghost. It assists you in installing Ghost locally. To install the tool, open a terminal and run:

```
npm install ghost-cli@latest -g

```

This command tells `npm` (Node Package Manager) to install the latest version of Ghost CLI. The `-g` flag means “globally” and ensures that you’re able to access the tool anywhere on your machine.

Confirm that Ghost CLI is installed correctly by running `ghost help` in the terminal. The tool will output a list of all available commands. It’s a handy way to see everything the Ghost CLI can do!

 
![email letter on fire](https://ghost.org/tutorials/content/images/size/w1000/2023/04/flames-of-knowledge.jpg)

Install Ghost locally
---------------------

You’re now ready to install Ghost. In the terminal, navigate to an empty directory. The directory can have any name you want.

Run the install command:

```
ghost install local

```

This command uses the Ghost CLI tool installed in the previous step. The `local` argument means that you’re going to run Ghost locally, that is, on your computer and not exposed to the internet. This local installation of Ghost makes testing and development easier.

Once the installation finishes, the CLI tool will output the URL for your Ghost site. By default, it’ll be `http://localhost:2368`.

Open the link in your browser to go through Ghost’s onboarding flow. Access Ghost Admin at any time via `http://localhost:2368/ghost`.

0:00/

That’s it. You’re done! Your local Ghost site is ready for use 🖥️

5 Ghost CLI commands to know
----------------------------

Ghost runs in a separate background process and remains running until you stop it or restart your computer. So you may find these commands useful for taming it:

```
ghost stop
```

Run this command from your installation directory. It will stop the currently running Ghost instance.

```
ghost start
```

Run this command from your installation directory to start your local instance of Ghost. It’s necessary to run `ghost start` after you restart your computer.

```
ghost ls
```

Run this command from anywhere on your machine to list your Ghost installs. It shows where you installed them, whether they’re running, and their URL. You can install multiple Ghost publications on your machine, which is helpful if you want to test out different content, debug something without messing with your current setup, or develop several themes at once.

```
ghost update
```

Run this command from your installation directory to update Ghost.

```
ghost help
```

Run this command from anywhere to show all available commands. [Also, find a deep dive and full explanation of all Ghost CLI commands in the docs.](https://ghost.org/docs/ghost-cli/?ref=ghost.org)

Summary
-------

In this tutorial, you learned how to install Ghost locally. You began by installing the Ghost CLI globally. Now, you can run `ghost install local` in any empty directory to launch a full-fledged Ghost publication on your computer!

You’re now in the perfect place to start creating a custom Ghost theme. Jump into our [developer theme documentation](https://ghost.org/docs/themes/?ref=ghost.org) to learn how to get started or visit us on the [official Ghost forum](https://forum.ghost.org/?ref=ghost.org), where we talk about all things Ghost.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Essential concepts to know when building a Ghost theme

7 min read](/tutorials/essential-concepts/)

[### Open a theme in a code editor

1 min read](/tutorials/open-a-theme-in-a-code-editor/)

[### How to add social media icons to your site

4 min read](/tutorials/add-social-media-icons/)

[### How to add an offer banner

4 min read](/tutorials/offer-banners/)

[### How to build CSS files

2 min read](/tutorials/build-css-files/)







Be the first to know.
---------------------

Join the Ghost developer community — sign up to get early access to the latest features, developer tools, and tutorials.



No spam. Once a month. Unsubscribe any time.
[![](https://ghost.org/tutorials/assets/img/most-helpful.jpg?v=235936095d)

Most helpful
------------

Essential tutorials to get you started](https://ghost.org/tutorials/most-helpful/)
[![](https://ghost.org/tutorials/assets/img/fundamentals.jpg?v=235936095d)

Funda­mentals
-------------

The basics of Ghost theme development](https://ghost.org/tutorials/fundamentals/)
[![](https://ghost.org/tutorials/assets/img/level-up.jpg?v=235936095d)

Level up
--------

Next-level development techniques](https://ghost.org/tutorials/level-up/)
[![](https://ghost.org/tutorials/assets/img/do-more.jpg?v=235936095d)

Do more
-------

Ideas & inspiration for whatever comes next](https://ghost.org/tutorials/do-more/)









