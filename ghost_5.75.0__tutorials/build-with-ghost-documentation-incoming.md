





📝 Build with Ghost: Documentation incoming









































---


Let's turn this one up to #11. Here's what this issue is rocking:

* Documentation in two shakes of a lamb's tail
* This site will provide plenty of inspiration for your next theme
* Philippe made `ts-ghost` and it's awesome
* Airtable works great with Ghost (and publishes with us, too)

🏋️****Pro tip:****We shared some top-tier tips and tricks on [this recent Forum thread](https://forum.ghost.org/t/community-question-of-the-week-1-share-your-tips-tricks/42676?ref=ghost.org).

Ghost & Raycast: Search our docs fast
-------------------------------------

[Raycast](https://www.raycast.com/?ref=ghost.org) is an extendable launcher for MacOS. It's a successor to Alfred and a replacement for Spotlight. In a nutshell, it's a super efficient way to open files and apps, manage windows, jump into your next meeting, convert and transform values, and so much more.

Ghost is now part of that "so much more."

We recently shipped a Raycast plugin to provide fuzzy, typeahead search across all of our documentation.


0:00
/0:16









That means you have instant access to our [help center](https://ghost.org/help/?ref=ghost.org), [developer docs](https://ghost.org/docs/?ref=ghost.org), [tutorials](https://ghost.org/tutorials/), [changelog](https://ghost.org/changelog/?ref=ghost.org), and [publisher resources](https://ghost.org/resources/?ref=ghost.org). You can also narrow your search to only return results from a particular source.

Head over to the [Raycast store](https://www.raycast.com/ryan_feigenbaum/ghost-docs?ref=ghost.org) to install the extension.

😪At the moment, Raycast is only available on MacOS, so if you're on a different OS, [you'll need to sit tight](https://www.raycast.com/faq?ref=ghost.org).

**Just shipped 🚢**
------------------

* [Emoji autocomplete](https://ghost.org/changelog/emoji-picker/?ref=ghost.org): The Ghost editor now streamlines your emoji input. Type a colon `:` and some text to search for emojis and use them in your text 😄

![Emoji autocomplete in Ghost](https://ghost.org/changelog/content/images/2023/11/CleanShot-2023-11-15-at-13.40.46@2x-1.png)

Ideas and tools 🛠️
------------------

* [Site Inspire](https://www.siteinspire.com/?ref=ghost.org) provides a filterable gallery of beautiful websites. It's a fantastic resource for finding design inspiration (as the name implies).
* The annual [State of JavaScript survey is out](https://stateofjs.com/en-US?ref=ghost.org). It tracks responses from the developer community to report feature and framework usage, trends, and demographics. Also, because it's a survey built by developers, it's chockablock with some sweet bells and whistles.
* Web Dev Simplified recently published [this YouTube video](https://youtu.be/mSBnJvHtgD0?si=usgVU5-JSZB5dXqy&ref=ghost.org) about lesser-known JS array methods like `groupBy` and `with`. How many of these do you know?
* This interactive tutorial by fffuel.co teaches you [how to create an SVG spinner](https://fffuel.co/svg-spinner/?ref=ghost.org). And their whole site has loads of helpful tools like noise and grain generators.

From the community
------------------

We recently caught up with Philippe on his amazing [`ts-ghost` library](https://ts-ghost.dev/?ref=ghost.org). It's a collection of tools for interacting with Ghost. These tools, written in Typescript, provide convenience, validation, and, of course, types when working with the Ghost Admin and Content APIs.

![the homepage for ts-ghost](https://ghost.org/tutorials/content/images/2023/12/CleanShot-2023-12-07-at-16.49.16.png)

A huge benefit of this library, even if you're not using Typescript, is clever autocomplete in your code editor. For example, rather than having to check the docs for the properties available on the post object, `ts-ghost` will let you know it's `feature_image`, not ~~`featured-image`~~.

But things don't end there.

Philippe shared his favorite aspects of the library, too. For instance, he uses a cool library called [Zod](https://zod.dev/?ref=ghost.org) to validate expressions like `filter` and `order`. For example, trying to get all posts tagged with `art` by using the incorrect filter, `category:art`, generates a validation error right in your editor. (It should be `tag:art`.) This feat of engineering is accompanied by other details that make using this library an absolute joy 😍


0:00
/0:58









ts-ghost in action




Philippe was inspired to build this library because he often works with the Ghost API in combination with other JS frameworks. He's the author of the [Ghost/Astro](https://github.com/PhilDL/astro-starter-ghost?ref=ghost.org) integration and uses a combination of Remix and Ghost for his learning platform, Coding Dodo.

[Coding Dodo - Odoo, Python & JavaScript TutorialsOdoo, ERP, and Python Tutorials. Real-world examples and useful code snippets on all Odoo versions covered but focus on the latest releases. Join us!![](https://codingdodo.com/content/images/size/w256h256/2021/04/small-logo.png)Coding Dodo - Odoo, Python & JavaScript TutorialsPhilippe L’ATTENTION![](https://codingdodo.com/content/images/2021/04/codingdodo-facebook-post.png)](https://codingdodo.com/?ref=ghost.org)

Philippe is currently a software engineer who works on B2B ERP (enterprise resource planning) web apps and contributes to open source in his free time. He's also a jazz musician (his original passion), and we're hoping his next contribution will be an album titled: *Music to write Ghost blogs to*.

Until then, find Philippe on [GitHub](https://github.com/PhilDL?ref=ghost.org), [X](https://twitter.com/_philDL?ref=ghost.org), and be sure to try out [`ts-ghost`](https://ts-ghost.dev/?ref=ghost.org).

Featured site: Airtable
-----------------------

Airtable is cloud-based software that combines elements of a database with the user-friendly experience of a spreadsheet. [It pairs well](https://ghost.org/integrations/airtable/?ref=ghost.org) with Ghost if you want a no-code way to present complex data.

Airtable also runs their product blog, [For the Record](https://blog.airtable.com/?ref=ghost.org), on Ghost.

![Airtable home page](https://ghost.org/tutorials/content/images/2023/12/CleanShot-2023-12-08-at-14.57.19@2x.png)

The design is clean and elegant, providing a comfortable reading experience. The blog communicates product updates, new features, best practices, and represents a perfect example of how businesses can [strategically use Ghost for content marketing](https://ghost.org/business?ref=ghost.org).

![Post page from Airtable](https://ghost.org/tutorials/content/images/2023/12/CleanShot-2023-12-08-at-14.59.45@2x.png)

---

Sites featured in the Build with Ghost newsletter are discovered through our creator network, [Ghost Explore](https://ghost.org/explore/?ref=ghost.org). It’s a way for creators and readers alike to discover their favorite new publications. Anyone running a Ghost site can add themselves to Explore to be featured throughout the wider Ghost ecosystem. If you’d like to be featured in this newsletter, add your site to Explore and reply to this email.

Thanks for building with us.
============================

Have an idea for a Ghost tutorial? Reply to this email and let us know ❤️

Looking for other creators and developers working with Ghost? Join the [official Ghost Forum](https://forum.ghost.org/?ref=ghost.org), where we talk about all things Ghost!

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









