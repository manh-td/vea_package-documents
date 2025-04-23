





➕ Build with Ghost: Recommendations for the open web









































---


Welcome to issue #10! Here's what's cooking:

* Get to know our newest feature: recommendations
* Design inspo, advanced layouts, and pathfinding algos
* A behind-the-scenes look at how we optimize Ghost
* We found 404 Media and didn't go blind

🏋️****Pro tip:****Our [video tutorials on YouTube](https://www.youtube.com/@tryghost?ref=ghost.org) teach you everything you need to know to build awesome custom themes.

Recommendations
---------------

We just released an exciting new feature: recommendations. Now, it's possible to recommend your favorite sites, no matter where they live on the web. Likewise, other publications can recommend you 🤝

Access recommendations from the updated **Settings** page. Recommendationsshow you not only how many clicks or subscriptions you've referred to recommended sites, but also how many signups have been sent your way. Read the [Changelog](https://ghost.org/changelog/recommendations/?ref=ghost.org)for more about the new feature, visit the [Help center](https://ghost.org/help/recommendations/?ref=ghost.org) to understand how it works, and [check out these recommendations](#/portal/recommendations) to see the feature in action.

![](https://ghost.org/changelog/content/images/2023/10/recs.png)

But this is Build with Ghost, so we're going to get just a bit more technical.

### Under the hood

One of the most exciting aspects of recommendations is that it's [built on an open standard called Webmentions](https://ghost.org/docs/recommendations?ref=ghost.org). By building it this way, Ghost's recommendation feature escapes walled gardens and vendor lock-in, operating, instead, across the entirety of the internet. That means you can recommend publications on other platforms — and they can recommend you 💪

### 1-click subscriptions

Recommendations have another trick up their sleeve. As its name implies, 1-click subscriptions streamline the membership process by allowing readers to sign up for a publication with *a single click*.

Currently, 1-click subscriptions are only supported between Ghost publications. However, we're eager to help other platforms implement this 1-click functionality, and [Micro.blog](https://micro.blog/?ref=ghost.org) and [Steady](https://steadyhq.com/en?ref=ghost.org) have already expressed interest. **If you're a platform that wants to build 1-click subscriptions for the open web, get in touch.**

### Recommendations & themes

The recommendations feature brings two new theme helpers with it.

**`{{recommendations}}`**

The `recommendations` helper outputs a list of your recommended sites. Highly customizable, this helper is a great way to share your favorite publications with readers. Below is the default template Ghost uses to output your recommendations (but you can create a totally customized template, too).

![](https://ghost.org/tutorials/content/images/2023/11/ray-so-export.png)

Check out the docs for all the [details on this new helper](https://ghost.org/docs/themes/helpers/recommendations/?ref=ghost.org) and see how [it's already implemented in our Source theme](https://github.com/TryGhost/Source/blob/946e06311787f864cd347678fb9012f6d3abab22/partials/components/post-list.hbs?ref=ghost.org#L105-L111).

**`{{readable_url}}`**

The `readable_url` helper outputs a human-readable URL. When linking to a recommended site, instead of showing `https://www.google.com?foo=bar&dog=love`, it'll just show `google.com`. In short, it's a glow-up for your URLs and works beautifully with the `recommendations` helper mentioned above.

[See the docs to learn more about this helper.](https://ghost.org/docs/themes/helpers/readable_url/?ref=ghost.org)

**Just shipped 🚢**
------------------

* **Recommendations** are a [simple cross-promotion mechanism for every publisher](https://ghost.org/changelog/recommendations/?ref=ghost.org), on any platform (i.e., what we're talking about above).
* The **Settings** menu got a big refresh. [Browse all settings at a glance. Find any setting with a simple search](https://ghost.org/changelog/refreshed-settings/?ref=ghost.org).
* The **new Ghost editor**, built from the ground up, reached GA. It's the same editor you love but [now faster, more resilient, and ready for the future](https://ghost.org/changelog/new-editor/?ref=ghost.org). *The new editor relies on a new format for storing content called Lexical, meaning the previous format, Mobiledoc, is now deprecated. [Learn more about this breaking change.](https://ghost.org/docs/changes/?ref=ghost.org#mobiledoc-deprecation)*
* Did you know [Ghost has a **Chrome extension**](https://ghost.org/changelog/bookmarker/?ref=ghost.org)? It makes curating links from around the web easy as 🥧
* We built a time machine or, at least, the next best thing. With [**post history**](https://ghost.org/changelog/post-history/?ref=ghost.org), travel back in time to restore that paragraph that was, on second thought, actually really good.
* Ghost got a [full-featured **image editor**](https://ghost.org/changelog/image-editor/?ref=ghost.org). Make quick crops or advanced changes all without leaving the editor.

Ideas and tools 🛠️
------------------

* The newest version of the Web Content Accessibility Guidelines (WCAG 2.2) was recently published. [Hidde de Vries runs through all the relevant changes](https://hidde.blog/new-in-wcag22/?ref=ghost.org).
* Need ideas for your next theme? This [web design inspiration catalog](https://www.curated.design/?ref=ghost.org) is sick and sure to give you some ideas.
* Kevin Powell's videos are always bangers, and [the latest on container queries and subgrid is no exception](https://youtu.be/Zddz_R1RnfM?si=KiIdwsgsToC39Eff&ref=ghost.org). These advanced techniques are perfect for building complex layouts in CSS.
* Ever wondered how Google Maps charts your route? This [interactive map animates pathfinding algorithms](https://honzaap.github.io/Pathfinding/?ref=ghost.org) in real-time.
* One more algorithm story: This madlad performed [a bubble sort only using CSS](https://dev.to/grahamthedev/bubble-sortin-pure-css-no-js-3bb1?ref=ghost.org).

From the community
------------------

[Ghost Forum](https://forum.ghost.org/?ref=ghost.org) user, Jannis, has created [Myrtle, a tool to add mock data to your Ghost site using OpenAI's API.](https://github.com/betschki/ghost-myrtle?ref=ghost.org)

Jannis explains the tool best:

> See, as somebody who loves good design, I hate it when it’s destroyed by Lorem Ipsum content. So, I always try to put realistic content onto my theme demo sites. Something that tells a story – and actually demonstrates how it can be used.

We used Myrtle to create this mock site, *Delicious Curry*. The story it tells: we're hungry. If you're looking for a tool to whip up some stand-in content, this works great 🍛

![A food website showing different elaborate articles on curry](https://ghost.org/tutorials/content/images/2023/11/myrtle-example.png)🔑****Friendly reminder:**** While we love celebrating community innovations, we also prioritize your safety. Please remember, when using software found online, especially those involving API keys, exercise caution. Always verify the source and understand the permissions you're granting.

Behind the scenes
-----------------

Our DevOps engineer, Sam, recently wrote an article on some work he did to [optimize Playwright tests in Ghost](https://samlord.me/optimising-playwright-tests-in-ghost/?ref=ghost.org) by making them run 185% faster 🏎️

In a nutshell, this means Ghost engineers can spend less time waiting for tests to run and more time building cool features, and we all get a more resilient, bug-free Ghost.

Featured site: 404 Media
------------------------

Formed by four journalists previously at VICE's Motherboard, [404 Media](https://www.404media.co/?ref=ghost.org) is a publication committed to sustainable, society-shifting tech journalism. They recently got to the top of Hacker News by publishing a story about how attendees at a Bored Ape NFT owners conference went blind with searing eye pain. Yes, you read that right.

[‘Couldn’t See Anymore:’ Bored Ape Conference Attendees Wake Up With Searing Eye Pain, Vision Loss“Been to lots of concerts, festivals, Burning Man, and never have I ever experienced fucked eyes like this.”![](https://www.404media.co/content/images/size/w256h256/format/png/2023/08/favicon-3.svg)404 MediaSamantha Cole![](https://www.404media.co/content/images/2023/11/yugalabs.jpeg)](https://www.404media.co/bored-ape-yacht-club-conference-eye-pain-vision-loss-yuga-labs/?ref=ghost.org)

Aside from the important, captivating journalism like "[In Defense of RAM](https://www.404media.co/in-defense-of-ram-on-apple-silicon/?ref=ghost.org)" and "[Mastodon is the Good One](https://www.404media.co/mastodon-is-the-good-one/?ref=ghost.org)," 404 Media has a simply gorgeous custom theme. The typography, layout, and post elements will make you swoon and provide some inspiration for your future themes.

[![404 media homepage](https://ghost.org/tutorials/content/images/2023/11/404.png)](https://www.404media.co/?ref=ghost.org)

---

Sites featured in the Build with Ghost newsletter are discovered through our creator network, [Ghost Explore](https://ghost.org/explore/?ref=ghost.org). It’s a way for creators and readers alike to discover their favorite new publications. Anyone running a Ghost site can add themselves to Explore to be featured throughout the wider Ghost ecosystem. If you’d like to be featured in this newsletter, add your site to Explore and reply to this email.

Thanks for building with us.
============================

Have an idea for a Ghost tutorial? Reply to this email and let us know ❤️

Were you spending all your time looking for other Ghost creators and developers on Omegle? Unfortunately, [you may need to look somewhere else](https://www.omegle.com/?ref=ghost.org). Come and join us on the [official Ghost Forum](https://forum.ghost.org/?ref=ghost.org), where we talk about all things Ghost!

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









