





💻 Build with Ghost: Themes made easy









































---


Issue #4 of the **********************************Build with Ghost********************************** newsletter has sprung. Welcome back!

In this month’s issue:

* Speed up your theme development process with the latest updates to the Starter theme.
* A peek inside the latest features and developer tools in the Ghost ecosystem.
* Explore the world of generative art with this week’s featured publication, Gorilla Sun.

🏋️**Pro tip**: Navigate Ghost Admin more quickly with `cmd/ctrl` + `[` and `cmd/ctrl` + `]`.![Code in the rollup configuration file](https://ghost.org/tutorials/content/images/2023/03/rollup.png)

Building a custom theme just got easier
---------------------------------------

If you’ve been thinking about creating a custom Ghost theme, now is a great time, as we’ve just made the process a little bit easier and a whole lot more fun by updating the [Starter theme](https://starter.ghost.io/?ref=ghost.org).

The fundamental idea behind the Starter theme is to accelerate your theme development by taking care of the basics, offering some guidance, and providing the under-the-hood machinery. We’ve taken care of the *mise en place*, so you can get right to cooking the meal. Here’s an overview of everything that’s new:

🧑‍🏫 **********************************************A master******************************************** ********************************************class in itself**********************************************  
Learn the syntax and structure of a theme from the theme itself. Annotations throughout the code explain what each part of the theme is doing. Paired with our [VS Code extension](https://marketplace.visualstudio.com/items?itemName=TryGhost.ghost&ref=ghost.org), you can learn everything almost all you need to know without ever leaving your editor.

**🔁 Live reloading**  
Out of the box, you can make changes to your CSS, JS, and Handlebars files and see your changes reflected on your local site in real time. Having continuous feedback while you build out your Ghost theme makes the development process much quicker and makes testing a breeze.

🚀 **Modern syntax**  
The Starter theme makes it possible to use cutting-edge JS and CSS syntax and features. Under the hood, [Rollup](https://rollupjs.org/?ref=ghost.org), [Babel](https://babeljs.io/?ref=ghost.org), and [PostCSS](https://postcss.org/?ref=ghost.org) transpile your code so it runs everywhere. Long story short, coding your theme is a lot more convenient without sacrificing compatibility.

👟 **********Fast everywhere**********  
Rollup builds your assets quickly so your development flow is never interrupted. Once your theme is shipped, your visitors will benefit from fast site speeds, because your CSS and JS are optimized and minified automatically.

➕ **Extensible**  
The theme build process is powered by [Rollup](https://rollupjs.org/?ref=ghost.org) and [PostCSS](https://postcss.org/?ref=ghost.org). This means that you can easily add any of the plugins from their rich ecosystem into your theme. Lookout [Tailwind](https://tailwindcss.com/?ref=ghost.org), [Three.js](https://threejs.org/?ref=ghost.org), and [Chart.js](https://www.chartjs.org/?ref=ghost.org).

👻 ******************************Tuned for Ghost******************************  
All of the tools you need are included, like using `[gscan](https://gscan.ghost.org/?ref=ghost.org)` to test your theme’s compatibility and [Ghost’s GitHub Deploy Action](https://github.com/TryGhost/action-deploy-theme?ref=ghost.org) to automatically update your site with new versions of your theme.

[GitHub - TryGhost/Starter: A development starter theme for GhostA development starter theme for Ghost. Contribute to TryGhost/Starter development by creating an account on GitHub.![](https://github.com/fluidicon.png)GitHubTryGhost![](https://opengraph.githubassets.com/223fa4faa516d9ad9367935ce79f29d5624de9c84df061bce34345b461e9a6fa/TryGhost/Starter)](https://github.com/tryghost/starter?ref=ghost.org)

Just shipped 🚢
--------------

* Deliver simple emails or marketing announcements with these [minimal email design settings](https://ghost.org/changelog/minimalist-newsletter-settings/?ref=ghost.org)
* [Spark the conversation](https://ghost.org/changelog/comment-cta/?ref=ghost.org) by adding a comments call-to-action directly in your newsletters
* The *[Create a read-next section](https://ghost.org/tutorials/read-next)* tutorial now has [video 📼](https://youtu.be/cZBQKUfv8cI?ref=ghost.org)
* Self-hosters who run high-load sites with complicated templates may benefit from the [new built-in Redis cache adapter](https://ghost.org/docs/config/?ref=ghost.org#adapters)

Ideas and tools 🛠️
------------------

* Keen to start building your custom theme? Brush up on your CSS with [some excellent videos by Kevin Powell](https://www.youtube.com/kevinpowell?ref=ghost.org)
* [Glyphy](https://glyphy.io/?ref=ghost.org) is a great resource when you’re looking for that obscure symbol  𓆱 or cͦͮr̲a̓̕z̪̍y̎ f̵̉o̷̘̼nt̸ͬ͘
* A whole host of new features around color just dropped. Adam Argyle walks through some of the highlights in the “[High Definition CSS Color Guide](https://developer.chrome.com/articles/high-definition-css-color-guide/?ref=ghost.org)”

Exploring the possibilities of code-based art
---------------------------------------------

![Sun Gorilla article page](https://ghost.org/tutorials/content/images/2023/03/CleanShot-2023-03-27-at-14.28.05.png)

*[Gorilla Sun](https://www.gorillasun.de/?ref=ghost.org)* is a publication run by Ahmad Moussa featuring deep dives into creative coding and generative art. Ahmad showcases, teaches, and shares how to use interesting algorithms to create art. It seems the artist isn’t safe from learning math after all!

Having recently migrated to Ghost from a static-site generator, Ahmad shares some details about the decision to switch to Ghost and what the migration entailed:

[Goodbye JekyllI’ve been thinking about moving away from Jekyll for a while now. Don’t get me wrong, I love the static site generator, I really do, it’s served me well for over two years, but certain aspects of my workflow have become very clunky, and overall I haven’t been able to be as efficient…![](https://www.gorillasun.de/content/images/size/w256h256/2023/03/icon-1.png)Gorilla SunAhmad Moussa![](https://www.gorillasun.de/content/images/2023/03/Red-Boats-Argenteuil-scaled.jpg)](https://www.gorillasun.de/blog/goodbye-jekyll/?ref=ghost.org)

One of Ahmad’s most popular articles, “An Algorithm for Polygon Intersections”, details the method for determining the intersection between polygons for the purpose of generative art.

[An Algorithm for Polygon IntersectionsIn this post we’ll work our way towards an algorithm that can compute convex polygon intersections. We’ll also a method for intersections between axis-aligned rectangles, a function that can determine the intersection of two line segments, as well as a point in polygon test.![](https://www.gorillasun.de/content/images/size/w256h256/2023/03/icon-1.png)Gorilla SunAhmad Moussa![](https://www.gorillasun.de/content/images/2023/03/thumb2.png)](https://www.gorillasun.de/blog/an-algorithm-for-polygon-intersections/?ref=ghost.org)

*Gorilla Sun’s* publication is beautifully designed and graphically lush. The artworks keep you glued to the screen. Here are two of Ahmad’s faves:

![](https://ghost.org/tutorials/content/images/2023/03/PJNW29O3.jpg)![](https://ghost.org/tutorials/content/images/2023/03/9N-Fq6Dx.jpg)

---

Sites featured in the Build with Ghost newsletter are discovered through our creator network, [Ghost Explore](https://ghost.org/explore/?ref=ghost.org). It’s a way for creators and readers alike to discover their favorite new publications. Anyone running a Ghost site can add themselves to Explore to be featured throughout the wider Ghost ecosystem. If you’d like to be featured in this newsletter, add your site to Explore and reply to this email.

[![](https://ghost.org/tutorials/content/images/2023/03/explore-1.jpg)](https://ghost.org/explore/?ref=ghost.org)

Thanks for building with us
---------------------------

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

[### 🥯 Build with Ghost: A partial guide to everything

5 min read](/tutorials/partial-guide/)

[### 🧠 Build with Ghost: Do you know these essential concepts?

4 min read](/tutorials/3-things/)

[### 🏗️ Build with Ghost: First steps for creating a custom theme

5 min read](/tutorials/build-with-ghost-the-first-for-creating-a-custom-theme/)

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









