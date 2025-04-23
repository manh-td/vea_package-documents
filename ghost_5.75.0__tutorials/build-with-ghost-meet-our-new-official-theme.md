





⦿ Build with Ghost: Meet our new official theme









































---


October is a month of change 🍂, and we've got some big ones to share in this month's issue:

* **Source** has launched! Our new default theme brings customization to a whole new level 🚀
* Can you spot an **AI-generated image**? How much do you know about Unicode (and why does it matter)? All this and more in our "Ideas and tools" section.
* This month's featured site, **OpenSauced**, combines two of our favorite things: pizza and open-source software 🍕 💻

🏋️****Pro tip:****Ever wondered where to find all the available keyboard shortcuts? They're now included right in the Editor. Look for ****Keyboard shortcuts**** in the sidebar.

Meet Source, Ghost's new default theme
--------------------------------------

[![Source: Our new default theme](https://ghost.org/changelog/content/images/size/w960/2023/10/source-theme-1.png)](https://source.ghost.io/?ref=ghost.org)

That's right! Casper is no longer Ghost's default theme. (But don't sweat, it's still available from the Ghost Marketplace.)

The goal of Source is to offer a highly configurable theme that can accommodate almost any publication style — all without having to write a line of code. By turning some knobs and dials, authors can achieve radically different layouts and identities, as seen in the screenshots below:

![Highlight Layout for Ghost source theme](https://ghost.org/changelog/content/images/2023/10/Screenshot-2023-10-02-at-10.28.26@2x.png)

Highlight Layout

![Magazine Layout for source Ghost theme](https://ghost.org/changelog/content/images/2023/10/Screenshot-2023-10-02-at-14.10.47@2x.png)

Magazine Layout

![Landing Page Layout for Source Ghost theme](https://ghost.org/changelog/content/images/2023/10/Screenshot-2023-10-02-at-10.28.02@2x.png)

Landing Page Layout

But that's not all. Source brings some new features for theme developers, too.

### Custom setting visibility

With custom setting visibility, theme developers can show custom settings to their users *only when those settings are relevant*. This ability makes your theme easier to navigate and the user experience more intuitive.

---

If you're unfamiliar with how custom settings work in Ghost, check out our tutorial for everything you need to know.

[Custom settings are the ultimate power-up for Ghost themesWant to elevate your Ghost theme? Dive into custom settings with this complete guide. Choose typefaces, color schemes, and more. Your theme, your rules!![](https://ghost.org/favicon.ico)TutorialsTeam Ghost![](https://ghost.org/tutorials/content/images/2023/08/custom-1.jpg)](https://ghost.org/tutorials/custom-settings/)

---

While custom setting visibility makes the user experience more intuitive, this feature itself might be a little unintuitive. Keeping with our pizza theme, here's an explanation.

Your user orders a pizza, so you show them the toppings option. They can choose mushrooms, pepperonis, or if they're a genius, pineapple. Showing the toppings option makes sense because they chose pizza. However, if they chose salad, showing the toppings option wouldn't make sense 🙅

![slice of pizza](https://ghost.org/tutorials/content/images/2023/10/pizza.jpg)

Custom setting visibility works the same way. You control which settings are visible depending on the values users choose. Let's look at a real-world example to see this concept in action.

In Source, it's possible to toggle the background image on and off — but only when the **Header style** option is **Landing**or **Search.**

![Search layout with background image](https://ghost.org/tutorials/content/images/2023/10/w-bg.png)

Search layout with background image

![Search layout without background image](https://ghost.org/tutorials/content/images/2023/10/CleanShot-2023-10-10-at-15.07.44.png)

Search layout without background image

For other layouts, this option doesn't make sense because there isn't a background image to toggle, like in the **Magazine**layout below.

![Magazine layout](https://ghost.org/tutorials/content/images/2023/10/magazine.png)

Magazine layout

Setting visibility ensures that the background-image toggle is only available when the option is relevant. The graphic below shows precisely how options change depending on the value of **Header style**:

![Custom settings shown in a variety of states. All of them show different options depending on the value of the first option, header style](https://ghost.org/tutorials/content/images/2023/10/Template-explainers.png)

Now that you have a handle on custom setting visibility, [learn how to implement it in your theme](https://ghost.org/docs/themes/custom-settings/?ref=ghost.org#setting-visibility) and provide a more refined, intuitive experience for your users 🤵

### More custom settings

Custom settings were limited to 15. Now it's 20.

### Go straight to the Source

The best way to learn how to build a Ghost theme is by checking out the open-source code that powers our official themes. This has never been more true than for Source. Not only does Source show you how to build a highly customizable theme using best practices, but it also includes lots of comments along the way that explain exactly what its code is doing.

[GitHub - TryGhost/Source: The default theme for GhostThe default theme for Ghost. Contribute to TryGhost/Source development by creating an account on GitHub.![](https://github.githubassets.com/pinned-octocat.svg)GitHubTryGhost![](https://opengraph.githubassets.com/a0b9627001117a913d3f81b80efa8fe613ecb437239733859d092407de45fa43/TryGhost/Source)](https://github.com/TryGhost/Source?ref=ghost.org)

Ideas and tools 🛠️
------------------

* Ahmad Shadeed talks about [rebuilding TechCrunch's layout](https://ishadeed.com/article/rebuilding-techcrunch-modern-css/?ref=ghost.org) with modern CSS. His article discusses the nuances of building complex layouts for content-heavy sites.
* The [State of HTML survey](https://survey.devographics.com/en-US/survey/state-of-html/2023?ref=ghost.org) just launched. It's a fantastic way to get up to speed on new features coming to HTML, and the survey design itself is just gorgeous.
* These are the greatest hits ... of [foundational web development blog posts](https://esif.dev/?ref=ghost.org). Look back on the articles that have shaped the internet we use today.
* Everypixel Journal, a blog on AI, estimates that [AI-generated images already outnumber all images taken by photographers over the past 150 years](https://journal.everypixel.com/ai-image-statistics?ref=ghost.org). Also, check out their guide on [how to spot AI-generated images](https://journal.everypixel.com/how-to-spot-ai-generated-images?ref=ghost.org).
* The world runs on Unicode. It guarantees the text you're reading right now is ǝʅqᴉᵷǝʅ. [Here's the minimum](https://tonsky.me/blog/unicode/?ref=ghost.org) a developer needs to know about this standard.

---

![](https://ghost.org/tutorials/content/images/2023/10/open-sauce-pizza.png)

All about open source at OpenSauced
-----------------------------------

[OpenSauced.pizza](https://opensauced.pizza/?ref=ghost.org) is not only a delicious domain name, but also a haven for open-source enthusiasts. We chatted with Bekah from OpenSauced about the company, its mission, and why they use Ghost for their [newsletter about open source](https://news.opensauced.pizza/?ref=ghost.org).

OpenSauced embraces the expansive world of open source, emphasizing that it's not just about code. Their perspective? Everyone can contribute to the open-source sphere, whether through detailed bug reports, insightful blog articles, or fostering community connections.

For those looking to get into the world of open-source software (OSS), OpenSauced offers a cool searchable database of repositories, featuring codebases that are trending and popular.

[OpenSauced InsightsThe open-source intelligence platform for contributors and maintainers. Unlock the power of open source with project insights by the slice.![](https://insights.opensauced.pizza/favicon.ico)OpenSauced Insights![](https://insights.opensauced.pizza/_next/static/media/Sauce.ea18edd9.svg)](https://insights.opensauced.pizza/?ref=ghost.org)

Ghost, too, is proudly open source. OpenSauced's decision to use Ghost for their newsletter was motivated by this fact. Bekah also notes Ghost's low barrier to entry that lets folks get started quickly, as well as more advanced approaches like using markdown, which makes her happy 🙂

Above all, we agree with OpenSauced that OSS is a great uniter, bringing people together from around the world to build "something bigger than individual projects." As Developer Experience Lead, Bekah is focused on enhancing the journey for both contributors and maintainers. Want to hear more from Bekah? Check out her recent video for deeper insights:




---

Sites featured in the Build with Ghost newsletter are discovered through our creator network, [Ghost Explore](https://ghost.org/explore/?ref=ghost.org). It’s a way for creators and readers to discover their favorite new publications. Anyone running a Ghost site can add themselves to Explore to be featured throughout the wider Ghost ecosystem. If you’d like to be featured in this newsletter, add your site to Explore and reply to this email.

[![](https://ghost.org/tutorials/content/images/2023/04/image-1.png)](https://ghost.org/explore/?ref=ghost.org)

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

[### 📝 Build with Ghost: Documentation incoming

4 min read](/tutorials/build-with-ghost-documentation-incoming/)

[### ➕ Build with Ghost: Recommendations for the open web

5 min read](/tutorials/we-recommend-this-newsletter/)

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









