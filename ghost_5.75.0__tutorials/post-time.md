





👩‍🎨 Build with Ghost: The art of the post template









































---


Welcome to Issue #8! Some of what we have in store:

* Our new tutorial shows you how to showcase your content by building the perfect post template
* Updates to CSS that will blow your mind 🤯
* Taking Ghost headless with Thimira

The art of the post template
----------------------------

![post header digram showing header elements and how they're represented in code](https://ghost.org/tutorials/content/images/2023/08/header--2--1.png)

It's the heart and soul of your theme. It's where authors bring their creative content to life, and where readers immerse themselves in these narratives.

It's the post template, and, in our latest tutorial, we cover everything you need to know to build one. We focus on the following:

* The basic anatomy of a post template
* Understanding the data available in the post context
* Steps to designing a captivating post header
* Bringing in your content
* Tips & tricks for creating a beautiful reading experience

Check it out 👉

[The art of the post template in GhostCreating gorgeous post layouts has never been easier in Ghost. Dive into our step-by-step guide to learn everything you need to know about creating a custom post template.![](https://ghost.org/favicon.ico)TutorialsTeam Ghost![](https://ghost.org/tutorials/content/images/2023/08/post-2.jpg)](https://ghost.org/tutorials/post-template/)

But wait! There's more.

We also released tutorials on using custom settings and building custom sign-up forms.

[Custom settings are the ultimate power-up for Ghost themesWant to elevate your Ghost theme? Dive into custom settings with this complete guide. Choose typefaces, color schemes, and more. Your theme, your rules!![](https://ghost.org/favicon.ico)TutorialsTeam Ghost![](https://ghost.org/tutorials/content/images/2023/08/custom-1.jpg)](https://ghost.org/tutorials/custom-settings/)
🏋️****Pro tip:****When adding custom settings to your theme, use the new [description key to communicate the setting's purpose](https://ghost.org/docs/themes/custom-settings/?ref=ghost.org#setting-a-description) to your users
[How to build custom sign-up forms in GhostLearn to create a custom sign-up form with Ghost. This guide covers all steps, including HTML integration, CSS styling, and user engagement strategies.![](https://ghost.org/favicon.ico)TutorialsTeam Ghost![](https://ghost.org/tutorials/content/images/2023/08/signup.jpg)](https://ghost.org/tutorials/form/)

Did you know we have [a YouTube channel](https://youtube.com/@TryGhost?ref=ghost.org)? Our most recent video includes a complete guide to using partials in Ghost. Don't forget to like and subscribe 😜

**Just shipped 🚢**
------------------

* [Header cards](https://ghost.org/changelog/header-card-improvements/?ref=ghost.org) got a massive upgrade, giving you more power to create beautiful pages and posts. (Header cards are full-width cards perfect for creating a division between sections or making a large call to action.)
* In the same spirit, it's now possible [to hide the title and feature image for pages](https://ghost.org/changelog/create-landing-pages/?ref=ghost.org), making it possible to build radically different landing pages.

🚧Custom theme developers will need to update their themes to support the [new @page helper](https://ghost.org/docs/themes/helpers/page?ref=ghost.org) that makes toggling the title and feature image possible.

Ideas and tools 🛠️
------------------

* Meta recently launched Threads, its ~~Twitter~~ X competitor. Ahmad Shadeed took the launch as an opportunity to [dive deeply into their CSS](https://ishadeed.com/article/threads-app-css/?ref=ghost.org).
* Core Web Vitals is a set of Google metrics for measuring your site's user experience. [Harry Roberts discusses their implications for SEO](https://csswizardry.com/2023/07/core-web-vitals-for-search-engine-optimisation/?ref=ghost.org).
* Probably more than you want to know about [using emoji on the web](https://fullystacked.net/posts/using-emoji-on-the-web/?ref=ghost.org) 🫥 🍾🪤
* [View transitions](https://twitter.com/argyleink/status/1683897409410334720?ref=ghost.org) (or incredibly cool ways of showing and hiding content) are coming to the browser. Get ahead of the curve on this new API.
* Animating on scroll used to be a JavaScript-only affair. No longer! Check out [scroll progress animations in CSS](https://developer.mozilla.org/en-US/blog/scroll-progress-animations-in-css/?ref=ghost.org).

Getting technical with Thimira
------------------------------

Thimira Thenuwara recently relaunched [Android Wedakarayo](https://androidwedakarayo.com/?ref=ghost.org), a Sinhala publication about technology based in Sri Lanka. The relaunch is notable because Thimira shifted to using Ghost headlessly, implementing a Nuxt frontend with Tailwind styling, oAuth sign-in, and Algolia search. We'll explain all of this in a minute, but let's start at the beginning.

![Homepage of Android Wedakarayo](https://ghost.org/tutorials/content/images/2023/08/CleanShot-2023-08-18-at-09.54.27.png)

Android Wedakarayo

By day, Thimira is a Deputy Manager of Finance for a group of companies in Sri Lanka. By night, [certified Ghost Expert](https://ghost.org/experts/thimira-thenuwara/?ref=ghost.org) 🦸

His foray into Ghost development began when Android Wedakarayo transitioned from WordPress to Ghost. At first, the publication used stock Casper (always a good place to start). Here and there, Thimira began customizing it to suit the publication's needs, eventually developing a totally bespoke theme.

Before hacking on his Ghost theme, Thimira didn't know web development at all! He taught himself HTML, CSS, and JS and says, "The platform taught me the ropes of web design." He also had a great support network to help him: another Ghost Expert, [Kasun Jayarathna](https://ghost.org/experts/kasun-jayarathna/?ref=ghost.org), got him up to speed on Ghost, Srilal Sachintha taught him Linux servers, and his fiancée, Shenaya Hewagama, cheered him on throughout.

Ghost is truly a fantastic gateway to learning web development. The cost of entry is low and the payoff is high: a totally customized, beautiful publication. Just be careful because before you know it, you'll be building a headless Ghost site with Nuxt, Algolia, oAuth, and a handful of other custom features 😏 Let's talk about what all this means.

Running Ghost headlessly means using Ghost's API with a frontend other than Ghost's native theme layer. While it enables advanced functionality, [headless is **not** the way to go for most users](https://ghost.org/docs/jamstack/?ref=ghost.org). Ghost's theme layer, for example, includes the metadata that optimizes your site for SEO. Going headless means you need to code that functionality yourself.

Using a framework like [Nuxt](https://nuxt.com/?ref=ghost.org) (based on [Vue](https://vuejs.org/?ref=ghost.org)) for your frontend can ease some of the burden by providing plugins and packages to help you rebuild features from Ghost's theme layer.

[Algolia](https://www.algolia.com/?ref=ghost.org) is an advanced search-as-a-service. It can be used with any Ghost site, and we use it on our [Tutorials](https://ghost.org/tutorials/) site. [Learn more about setting up Algolia on Ghost in our docs](https://ghost.org/docs/themes/search/?ref=ghost.org#create-an-advanced-search-index-using-algolia).

oAuth (open authorization) is a protocol that allows third-party apps to access user data without exposing user credentials. A common example, and the one Thimira implemented, is using Google or Apple to sign into a third-party website.

To see the whole thing in action, go check out [Android Wedakarayo](https://androidwedakarayo.com/?ref=ghost.org). We'd also be remiss if we didn't mention [Thimira's Apple-inspired personal site](https://thimirathenuwara.com/?ref=ghost.org), which has lots of clever animations.

![Thimira's personal website](https://ghost.org/tutorials/content/images/2023/08/CleanShot-2023-08-18-at-13.56.22.png)

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









