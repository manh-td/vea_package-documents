





✅ Remind me to change this title









































---


Welcome to #14. In this issue, we share:

* Our new TK reminders feature
* Investigations into ActivityPub (we need your help!)
* Design and code tips and tricks
* Our interview with TechHut Media on all things Linux

🏋️****Pro tip:****Quickly access the ****Settings**** menu from the dashboard with the keyboard shortcut `⌘ + ,` (MacOS) or `CTRL + ,` (Windows).

Ghost is open source
--------------------

Since our beginning as a [Kickstarter](https://www.kickstarter.com/projects/johnonolan/ghost-just-a-blogging-platform?ref=ghost.org) project in 2013, we've been open source, meaning all our code is freely available for you to inspect, run, and modify in pretty much whatever way you like. It also means that [hundreds of contributors](https://github.com/TryGhost/Ghost/graphs/contributors?ref=ghost.org) have helped and continue to help build Ghost 💪

[GitHub - TryGhost/Ghost: Independent technology for modern publishing, memberships, subscriptions and newsletters.Independent technology for modern publishing, memberships, subscriptions and newsletters. - TryGhost/Ghost![](https://github.githubassets.com/assets/pinned-octocat-093da3e6fa40.svg)GitHubTryGhost![](https://opengraph.githubassets.com/64ce676dbaee61925c45ec25dd56fd90cbb3ed6b20d762a36980cb891a5e2d6c/TryGhost/Ghost)](https://github.com/TryGhost/Ghost?ref=ghost.org)

But, if you're reading this newsletter, there's a good chance, you already knew all that 🤓

Just shipped 🚢
--------------

* One of our top requested features is federating over **ActivityPub**, the protocol used by Mastodon, PixelFeed, and, recently, Threads. We're investigating adding protocol support to Ghost but we need your help. [Please take a minute and tell us a bit about how you imagine this working](https://tally.so/r/m67X4P?ref=ghost.org) 🙏
* 🆕 **TK Reminders**. Ever wanted to leave yourself a reminder to update something before publishing? We've now got your back. Type `TK` in the editor and Ghost will remind you to add that missing image or update a statistic. [See how this new feature works in our changelog.](https://ghost.org/changelog/tk-reminders/?ref=ghost.org)
* On 1 March 2024, we rolled out some minor style changes to Ghost's editor cards. The gist of these changes is that we transitioned from `em` units to `px` units for `font-size`. We made these changes to make it easier to create custom themes without unexpected consequences. [Learn more in our Forum post](https://forum.ghost.org/t/upcoming-style-changes-to-editor-cards-in-ghost/45381?ref=ghost.org).

Ideas and tools 🛠️
------------------

* Do your readers like to print out your articles? No? Well, if they did, here's a nice guide to [writing CSS for print](https://voussoir.net/writing/css_for_printing?ref=ghost.org).
* [Stack Sorted](https://stacksorted.com/?ref=ghost.org) brings together a curated collection of the web's best designs sorted by elements.
* Did you know that CSS has `system colors` that are automatically updated based on your color preference? [Stefan Judis shares more about how to use these colors in your styles](https://www.stefanjudis.com/today-i-learned/css-defines-color-values-that-follow-system-preferences/?ref=ghost.org).
* Matt Pocock — as always — brings some clarity to Typescript by [explaining how to type a](https://www.totaltypescript.com/how-to-type-array-reduce?ref=ghost.org) reduce method.
* Looking for some design inspiration? Check out [this monster list](https://muz.li/blog/top-twitter-accounts-every-designer-should-follow?ref=ghost.org) by Muzli for some sweet follows.

TechHut Media
-------------

TechHut Media dives deep into the world of open source, making it the ideal spot for enthusiasts and newbs alike. We caught up with the team behind the scenes, Brandon and Nicco, to learn more about the publication and how they use Ghost.

[TechHut MediaYour source for technology reviews, marketing, and content production services.![](https://www.techhut.tv/favicon.ico)TechHut MediaNiccolò Venerandi![](https://www.techhut.tv/content/images/size/w720/2024/02/desktop.png)](https://www.techhut.tv/?ref=ghost.org)
### Meet the authors

Before there was a publication, there was a YouTube channel. Two, to be precise.

Brandon's channel, [TechHut](https://www.youtube.com/@TechHut?ref=ghost.org), focuses on various tech products and software with an overall goal of influencing people towards open-source alternatives and self-hosting.

Nicco started his channel, [Nicco Loves Linux](https://www.youtube.com/@niccoloveslinux?ref=ghost.org), as a way to explain how KDE works, and now covers other topics in the Linux world.

Watching either channel, it's obvious that both creators are passionate and knowledgeable about Linux, and they're both great sources for keeping up with all that's new in open source.

### Learn about Linux distros

When talking about Linux, a favorite topic is distros. A distro (short for distribution) refers to the complete operating system built around the Linux kernel.

There are hundreds of [Linux distros](https://distrowatch.com/?ref=ghost.org), each with its unique purpose and style. The proliferation of distros can be overwhelming, so we asked Nicco and Brandon about some of their favorites.

As mentioned, Nicco loves KDE, and, in particular, [Kubuntu](https://kubuntu.org/?ref=ghost.org). This distro pairs Ubuntu with the desktop environment, KDE Plasma. Ubuntu, a key piece in [the recommended production tech stack for Ghost](https://ghost.org/docs/install/ubuntu/?ref=ghost.org), is built on Debian.

![A desktop with the Plasma desktop environment featuring an illustrated wallpaper of forest and the sun](https://kde.org/announcements/megarelease/6/desktop.png)

[KDE Plasma 6](https://kde.org/announcements/megarelease/6/?ref=ghost.org)

Even if some terms in the last section are new to you, they highlight the essence of open source: a collaborative environment where each piece of software evolves from its predecessors, leading to innovative creations. This continuous cycle of improvement and reinvention is unique to the open-source community, a process not found in the proprietary software world.

Oh, and for development purposes, Nicco also uses Arch, btw 😉

![A login and neofetch output of a Arch Linux base installation on a virtual machine.](https://upload.wikimedia.org/wikipedia/commons/e/ed/Arch_Linux_Base_Neofetch_output.png)

Neofetch output for Arch Linux

Brandon prefers yet another distro, [Fedora](https://fedoraproject.org/?ref=ghost.org), which uses the [GNOME](https://www.gnome.org/?ref=ghost.org) desktop environment. Well, to be precise, he's running an optimized version of Fedora called [Nobara](https://nobaraproject.org/?ref=ghost.org) that he dual boots with Windows 11.1.

Windows, of course, is not an open-source distro, but it is possible to run [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/about?ref=ghost.org) (WSL), which allows you to run Linux distros on Windows. That's pretty cool, and, when using Windows, [we recommend this approach for](https://ghost.org/tutorials/node/#install-node-on-wsl) Ghost theme development.

![Ubuntu Linux desktop featuring a jellyfish](https://res.cloudinary.com/canonical/image/fetch/f_auto,q_auto,fl_sanitize,w_2557,h_1321/https://assets.ubuntu.com/v1/acdf946a-Screenshot+from+2022-04-18+13-05-17.png)

Ubuntu Linux desktop

If this is all new to you, but your curiosity is piqued and you'd like to try a Linux distro yourself, Brandon recommends [Ubuntu](https://ubuntu.com/desktop?ref=ghost.org), as it's the easiest to get up and going.

If this *isn't* your first rodeo, then Brandon and Nicco think the most exciting Linux developments are being made with desktop environments. Of note, [KDE Plasma 6](https://kde.org/announcements/megarelease/6/?ref=ghost.org) just came out and the brand-new [COSMIC desktop](https://blog.system76.com/post/cosmic-the-road-to-alpha?ref=ghost.org) for [Pop!\_OS](https://pop.system76.com/?ref=ghost.org) (yep, another distro) is nearing its alpha release.

### Open-source news

The [TechHut newsletter](https://www.techhut.tv/?ref=ghost.org), powered by Ghost and rocking the [Headline theme](https://github.com/tryghost/headline/?ref=ghost.org), is a great way to keep up on all these exciting developments. Brandon chose Ghost for the newsletter because of its integrated membership features, ease of use, and, of course, because Ghost is open source.

---

Sites featured in the Build with Ghost newsletter are discovered through our creator network, [Ghost Explore](https://ghost.org/explore/?ref=ghost.org). It’s a way for creators and readers alike to discover their favorite new publications. Anyone running a Ghost site can add themselves to Explore to be featured throughout the wider Ghost ecosystem. If you’d like to be featured in this newsletter, add your site to Explore and reply to this email.

[![](https://ghost.org/tutorials/content/images/2023/04/image-1.png)](https://ghost.org/explore/?ref=ghost.org)

Thanks for building with us.
============================

Have an idea for a Ghost tutorial? Reply to this email and let us know ❤️

Looking for other creators and developers working with Ghost? Join the [official Ghost Forum](https://forum.ghost.org/?ref=ghost.org), where we talk about all things Ghost!

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### 💌 Build with Ghost: Email is changing in a big way

3 min read](/tutorials/email-is-changing/)

[### 🎁 Build with Ghost: Wrapped 2023

2 min read](/tutorials/build-with-ghost-wrapped-2023/)

[### 📝 Build with Ghost: Documentation incoming

4 min read](/tutorials/build-with-ghost-documentation-incoming/)

[### ➕ Build with Ghost: Recommendations for the open web

5 min read](/tutorials/we-recommend-this-newsletter/)

[### ⦿ Build with Ghost: Meet our new official theme

6 min read](/tutorials/build-with-ghost-meet-our-new-official-theme/)

[### 👩‍🎨 Build with Ghost: The art of the post template

5 min read](/tutorials/post-time/)

[### 🥯 Build with Ghost: A partial guide to everything

5 min read](/tutorials/partial-guide/)

[### 🧠 Build with Ghost: Do you know these essential concepts?

4 min read](/tutorials/3-things/)

[### 🏗️ Build with Ghost: First steps for creating a custom theme

5 min read](/tutorials/build-with-ghost-the-first-for-creating-a-custom-theme/)

[### 💻 Build with Ghost: Themes made easy

5 min read](/tutorials/themes-made-easy/)

[### 📖 4 ways to build a read-next section in Ghost

4 min read](/tutorials/how-to-build-a-read-more-section/)

[### 🐛 How to debug your Ghost theme once and for all

3 min read](/tutorials/how-to-debug-your-ghost-theme/)

[### 🏎️ Build Ghost themes more quickly with our new VS Code extension

5 min read](/tutorials/build-ghost-themes-more-quickly-with-our-new-vs-code-extension/)







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









