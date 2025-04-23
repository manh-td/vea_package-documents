





Install Node on macOS, Windows, and Linux









































---


As the saying goes, "Every journey begins with a single step." In the world of web development, that first step is often Node. This tutorial explains what Node is and how to install it on your system. Once installed, you’ll be ready to run Ghost locally and begin your journey of creating a custom Ghost theme.

What’s Node?
------------

Usually, JavaScript runs in your browser, but in 2009, Ryan Dahl had the idea to create a runtime — Node — so that JavaScript could run independently of it. Today, nearly all modern web development uses Node in some way. Ghost runs entirely on Node, and, fun fact, when Ghost first came out in 2013, it ran on Node v0.10. Not even version 1!

******************************************Node Package Manager****************************************** (NPM) is included with every installation of Node. It’s a command-line tool for installing, managing, and sharing JavaScript code. For example, use NPM to [install Ghost](https://ghost.org/docs/install/local/?ref=ghost.org) or [any of these other 3 million-plus packages](https://www.npmjs.com/?ref=ghost.org).

Install Node on macOS
---------------------

To install Node on macOS, open up a browser and navigate to [the official Node website](https://nodejs.org/?ref=ghost.org).

Click on the **LTS** version on the left and download the installer.

![Choose macOS installer on Node js website](https://ghost.org/tutorials/content/images/2023/04/install-node-on-mac.png)

Run the installer, choosing the default options.

![The node js installer on macos](https://ghost.org/tutorials/content/images/2023/04/node-installer-macos.png)

After the installer completes, confirm Node is installed by opening a terminal and running `node -v`. The terminal will output the current version of Node that’s installed.

![Console showing the installed version of node](https://ghost.org/tutorials/content/images/2023/04/node-installed-on-mac-os.png)

That’s all there is to it. You’re now ready to start using Node 🥳

🏋️If you’re looking for more control over your Node installation or foresee wanting to switch Node versions, check out the [instructions for using `nvm` in the Linux section below](#install-node-on-linux).

Install Node on Windows
-----------------------

[Go to Node’s official page.](https://nodejs.org/?ref=ghost.org) Click on the **LTS** version on the left and download the installer.

![Choose the windows installer on the node js website](https://ghost.org/tutorials/content/images/2023/04/install-node-on-windows.png)

Follow the installer prompts. It’s recommended to check “Yes” on the **Tools for Native Modules** screen to ensure you don’t run into potential compatibility issues in the future. Checking this box runs an additional installation script.

![Check yes on the Tools for native modules screen](https://ghost.org/tutorials/content/images/2023/04/windows-install-node-js-optional.png)

After installation, confirm that Node is installed correctly by opening your terminal and running `node -v`. The command will output Node’s version number to the console.

![Terminal showing the node version](https://ghost.org/tutorials/content/images/2023/04/windows-node-installed.png)

You’re now ready to start using Node 🥳

 
![email letter on fire](https://ghost.org/tutorials/content/images/size/w1000/2023/04/flames-of-knowledge.jpg)

Install Node on WSL
-------------------

Windows users have another option for installing Node: [Windows Subsystem for Linux or WSL](https://learn.microsoft.com/en-us/windows/wsl/install?ref=ghost.org). WSL allows you to run a Linux environment on your Windows machine. Because most web development happens in Linux environments, the benefits of using WSL are that you’ll have fewer problems, an easier time following tutorials, and more tools at your disposal. The downside is that it takes a few additional steps to configure and install.

Open a terminal as an **************************administrator************************** by right-clicking on the application and choosing “Run as administrator.”

![Use run as admin to open the terminal](https://ghost.org/tutorials/content/images/2023/04/teminal-run-as-admin.png)

In the terminal, run:

```
wsl --install
```

Windows will install WSL. After installation is complete, restart your machine. Open your terminal and select **Ubuntu**, the WSL distribution installed by default.

![Use Ubuntu in the windows terminal](https://ghost.org/tutorials/content/images/2023/04/wsl-ubunut-terminal.png)

You’re now on Linux on Windows. Pretty cool! To install Node, follow the instructions in the next section.

Install Node on Linux
---------------------

The best way to install Node on Linux is to use ******************************************[Node version manager](https://github.com/nvm-sh/nvm?ref=ghost.org)****************************************** [(nvm)](https://github.com/nvm-sh/nvm?ref=ghost.org). It’s a script that makes it easy to install up-to-date Node versions and switch between them.

Open a terminal and run:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

Close your terminal and reopen it. Check that nvm is installed correctly by running `command -v nvm`. This command should output `nvm`.

Finally, [check which version of Node Ghost currently supports](https://ghost.org/docs/faq/node-versions/?ref=ghost.org). Install it with the following command:

```
nvm install 18
```

Once installation is complete, close and reopen your terminal. Check that Node is installed correctly with `node -v`.  If it returns the current version installed, then you’re in business and ready to start using Node 🥳

⚠️`nvm` works great when using Ghost locally, but it's not recommended for production. [See our FAQ for more info.](https://ghost.org/docs/faq/using-nvm/?ref=ghost.org)

Summary
-------

It’s hard to overstate how omnipresent Node is in the current web development ecosystem. Name a website or app and somewhere along the line, they’re probably using Node. Installing it on your system is the first step in creating an amazing app or a super sick custom Ghost theme.

Your next step is to install Ghost locally, which should be a breeze now that Node is installed 😉

[How to install Ghost locally on Mac, PC or LinuxA detailed local install guide for how to install the Ghost publishing platform on your computer running Mac, PC or Linux. Ideal for Ghost theme development.![](https://ghost.org/favicon.ico)Ghost - The Professional Publishing Platform![](https://ghost.org/images/meta/ghost-docs.png)](https://ghost.org/docs/install/local/?ref=ghost.org)

And we have lots more resources to help you build a custom theme:

* [The official Ghost docs](https://www.notion.so/070a4e323c154a81b60595285e583ab6?ref=ghost.org)
* [Tutorials](https://www.notion.so/379479fa194b496ca4b917a0f8f77afb?ref=ghost.org)
* [Videos](https://www.youtube.com/@TryGhost?ref=ghost.org)
* [The official Ghost Forum](https://www.notion.so/Ghost-Starter-Theme-update-3ca13b3e81994e97beb7e5497bdb67e5?ref=ghost.org)
* [Build with Ghost Newsletter](https://ghost.org/tutorials/#/portal/signup/free)

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Build a custom sign-up form

7 min read](/tutorials/form/)

[### Custom settings are the ultimate power-up for themes

6 min read](/tutorials/custom-settings/)

[### The art of the post template

12 min read](/tutorials/post-template/)

[### A complete guide to partials

10 min read](/tutorials/partials/)

[### A comprehensive guide to the index template

9 min read](/tutorials/index/)

[### A comprehensive guide to the default template

9 min read](/tutorials/default/)

[### Essential concepts to know when building a Ghost theme

7 min read](/tutorials/essential-concepts/)

[### How to install Ghost locally

3 min read](/tutorials/local-ghost/)

[### How to create a read-next section

10 min read](/tutorials/read-next/)

[### How to build a custom homepage

11 min read](/tutorials/custom-homepage/)

[### Create a custom post template

4 min read](/tutorials/create-a-custom-post-template/)

[### Implementing redirects

5 min read](/tutorials/implementing-redirects/)

[### Show reading time & progress

3 min read](/tutorials/reading-time/)

[### How to build CSS files

2 min read](/tutorials/build-css-files/)

[### How to make a podcast RSS feed

4 min read](/tutorials/custom-rss-feed/)







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









