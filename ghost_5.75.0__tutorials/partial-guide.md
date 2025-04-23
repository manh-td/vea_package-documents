





🥯 Build with Ghost: A partial guide to everything









































---


Welcome to issue #7! Seven is the most popular lucky number in the world, so this issue is packed with a whole lot of good fortune 🥠

Here's what else this issue includes:

* Build beautiful themes with **three new tutorials** to help you
* Grow engagement with **new signup cards** and embeddable forms
* Gain insights from **Erin Mikail Staples**, a renowned developer advocate, tech educator, and comedian, as she shares the secrets behind her vibrant, stylish Ghost site

🏋️

****Pro tip:**** Bring up the card menu in the editor by typing `/` on a new line. Start typing to filter card types and quickly find the one you want 🎴

Use partials to simplify your theme development
-----------------------------------------------

Partials are an essential tool for quick, maintainable theme development. These partial templates encompass bits of code that you can use throughout your theme. Typical use cases include [cards](https://github.com/TryGhost/Casper/blob/fa76f770064ad3b4a29b3a7d286d757fb110db26/partials/post-card.hbs?ref=ghost.org), [CTAs](https://github.com/TryGhost/Digest/blob/944a3683c39903d1f7bfbc87effdab8863157e5c/partials/content-cta.hbs?ref=ghost.org), [headers](https://github.com/TryGhost/Episode/blob/21970de0bcf00c424227568a5a58cd58ba580157/partials/components/header.hbs?ref=ghost.org), [navbars](https://github.com/TryGhost/Taste/blob/1d9dd0fb8b66a1f3732e75f1bc637e5293a12d3e/partials/components/navbar.hbs?ref=ghost.org), or any other elements you find yourself using repeatedly. (Those links all point to real-world examples in official Ghost themes.)

[A complete guide to partials in GhostLearn partials in Ghost for better code maintenance and consistency. This tutorial will teach you what a partial is, how it’s used, and some advanced tips and tricks.![](https://ghost.org/tutorials/content/images/size/w256h256/2022/05/ghost-logo-orb.png)Team GhostTutorials![](https://ghost.org/tutorials/content/images/2023/06/partials.jpg)](https://ghost.org/tutorials/partials/)

Our new tutorial lays out everything you need to know about partials, from the very basics to advanced properties. In particular, we use a partial to create a card for a fictional music publication, *Of Record*, and walk through every line of code that makes it work.

![Example of a partial. A card with a young woman looking at records and the title and author byline of the article](https://ghost.org/tutorials/content/images/2023/06/hover-card.png)

This tutorial complements two others we just released:

[A comprehensive guide to Ghost’s index templateLearn to create and customize your Ghost theme’s index template in this comprehensive tutorial. Understand the index template functionality, the power of the post loop, and bonus theme customization techniques.![](https://ghost.org/tutorials/content/images/size/w256h256/2022/05/ghost-logo-orb.png)Team GhostTutorials![](https://ghost.org/tutorials/content/images/2023/06/index.jpg)](https://ghost.org/tutorials/index/)
[A comprehensive guide to Ghost’s default templateDiscover the secrets of Ghost’s default.hbs template. Learn how to optimize your site’s common elements and become an efficient theme-creation machine 🤖![](https://ghost.org/tutorials/content/images/size/w256h256/2022/05/ghost-logo-orb.png)Team GhostTutorials![](https://ghost.org/tutorials/content/images/2023/06/Default-3.jpg)](https://ghost.org/tutorials/default/)

**Just shipped 🚢**
------------------

We've recently shipped two related, exciting features: [signup cards](https://ghost.org/changelog/signup-cards/?ref=ghost.org) and [embeddable signup forms](https://ghost.org/changelog/embeddable-signup-forms/?ref=ghost.org).

**Signup cards**, available to users on the [beta editor](https://ghost.org/changelog/editor-beta/?ref=ghost.org), give you new ways to grow your audience. Add them to a post by selecting the Signup card from the card menu or by typing `/` on a new line. Customize the card to fit your publication.

🚨

****Important note for theme developers.**** Signup cards require updates to a theme's CSS to display properly. In particular, cards that are full-width or have a split layout with a contained image add a `kg-content-wide` class that requires styling. Additionally, the container for post content may also need to be updated. [See our docs for more info](https://ghost.org/docs/themes/content/?ref=ghost.org#signup-card). All official themes have been updated, so they are also a great resource for understanding these changes.

Whereas signup cards are for use across your Ghost publication, **embeddable signup forms** can be used anywhere on the web. Customize the form and use the provided code to grow your audience on any platform.

Ideas and tools 🛠️
------------------

* The modern web is responsive by default. That responsivity is powered (in large part) by media queries. [Here's everything you need to know](https://engineering.kablamo.com.au/posts/2023/media-queries-and-responsive-design/?ref=ghost.org).
* Out of the loop on modern CSS? [Stephanie Eckles has got you covered](https://moderncss.dev/modern-css-for-dynamic-component-based-architecture/?ref=ghost.org). This article is just ❤️‍🔥
* 🍱 One hot new web design trend is bento grids. [See how these beautiful sites are using it](https://bentogrids.com/?ref=ghost.org).
* [Seven pro tips for working with fonts in Figma](https://pimpmytype.com/figma-typography-tips/?ref=ghost.org). These tips are actually really helpful 💁
* Learn how to make shiny, rotating cards using this [fantastic set of CSS techniques](https://www.smashingmagazine.com/2023/07/shines-perspective-rotations-css-3d-effects-images/?ref=ghost.org).

Erin Mikail is here for the rise of the personal blog (again)
-------------------------------------------------------------

![Erin Mikail's personal website with a bright pink background and cards with posts, twitter info, description, and more](https://ghost.org/tutorials/content/images/2023/07/screely-1689113132022.png)

As the Sr. Developer Community Advocate at HumanSignal, Erin empowers the open-source community behind the Label Studio project. Working from NYC, Erin creates educational materials like tutorials, speaks at events, runs workshops, and maintains community channels to improve user experience.

While doing all of that, Erin also has a kick-ass Ghost site! It's rocking a slightly modified version of the [Groovy theme](https://ghost.org/themes/groovy/?ref=ghost.org), which showcases some clever uses of partials and an engaging index template.

Erin has been on Ghost for a while because, as an open-source platform, it provides flexibility and control over content and appearance. Also, the fact that Ghost is a nonprofit aligns with Erin's values. She says, "Ghost.org offers a genuine commitment to the public good rather than focusing on creating profits for shareholders. They reinvest their revenue into their platform, continually improving and upgrading. This has given me the confidence that they truly value their community, not a group of external investors" ❤️

![A cute dog at a desk doing important work](https://ghost.org/tutorials/content/images/2023/07/q64tI7xuvdpZ_yCr1e2gaoL3EAp5p3C-AEn0yt9Ikia2yE36ktS7vfT89Oogvf2MDUBdbtuM2d36jABNzrNWKIX-79BSGr1t-kFfWDAnx1mHPcfVV2Ib3cHg5Eg_reAdQuEfDqIwR9Sy2rvsumC_AGg.png)

Meet Erin's coding partner, Q

If Erin could pass on one bit of advice when working with Ghost, it's not to be afraid to ask for help. Ghost's [Forum](https://forum.ghost.org/?ref=ghost.org) and [GitHub](https://github.com/tryghost/?ref=ghost.org) are open and responsive. They're full of people willing to help. Erin says she has found the answer she needed on the Forum too many times to count.

> done > perfect

And, when possible, Erin says to remember that done is better than perfect. Rather than letting posts linger as drafts, "embrace the joy of constantly improving and being a work in progress." Amen!

[👉 Follow Erin (and Q) on the web](https://poplme.co/erinmikail?ref=ghost.org)

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

[### ✅ Remind me to change this title

5 min read](/tutorials/tk/)

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









