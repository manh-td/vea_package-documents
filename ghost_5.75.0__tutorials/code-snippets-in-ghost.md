





A complete guide to code snippets









































---


While we can’t fix the bugs in your code, we can show you how to make it look spectacular. In this tutorial, learn how to create code blocks in Ghost and beautify them using the [Prism syntax highlighting library](https://prismjs.com/?ref=ghost.org).

Create a code block
-------------------

Before we highlight our code, we need some code to highlight. To add a block of code to a post or page, type three backticks (**```**) followed by the name of the coding language and hit `tab` or `enter`. For example, to add a block of javascript, write: **```javascript**. (You can also add a language after the fact by typing it into the top right corner of the code block.)


0:00
/0:48









Add syntax highlighting
-----------------------

Syntax highlighting applies styling to your code based on its meaning. It’s not just an aesthetic improvement – it also improves readability 🤓

We’ll use the Prism library to add syntax highlighting using two different techniques: **Code Injection** and **theme customization**. While both techniques yield the same result, the second, more complicated one offers more options for customization and optimization.

### Add Prism via Code Injection

To function, Prism requires JavaScript and CSS. The JS parses your code blocks and the CSS styles theme. Below, we'll load these resources via **Code Injection** using a CDN.

With the CDN, Prism recommends using their `autoloader` script, which automatically loads the needed languages. For example, if you have JavaScript and Python code snippets, the autoloader only loads the code needed to parse those languages.

Add the snippet below to **Settings** → **Code injection** → **Site header**:

```
<script src="https://cdn.jsdelivr.net/npm/prismjs/prism.min.js" defer></script>
<script src="https://cdn.jsdelivr.net/npm/prismjs/plugins/autoloader/prism-autoloader.min.js" defer></script>
```

Prism offers several [color themes](https://github.com/PrismJS/prism/tree/59e5a3471377057de1f401ba38337aca27b80e03/themes?ref=ghost.org). Choose the theme you want to use and load its CSS. In the code below, we use the default theme. However, if you wanted to use the Twilight theme, change the filename from `prism.min.css` to `prism-twilight.min.css`.

Again, add the following code to **Code injection** → **Site header**:

```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/prismjs/themes/prism.min.css">
```
![Code Injection fields in Ghost Admin Settings](https://ghost.org/tutorials/content/images/2024/04/syntax-highlighting-code-1.png)

Save – and that’s it! Add a code block to the editor and publish. Your code snippets will now be looking gorgeous 💅

![Code with syntax highlighting looking so good](https://ghost.org/tutorials/content/images/2024/04/example-of-syntax-highlighting.png)
### Add Prism via theme customization

By adding Prism directly to your theme files, you have more options for styling the syntax highlighting and more opportunities for optimization.

Go to the [Prism download page](https://prismjs.com/download.html?ref=ghost.org). Choose a theme and the languages you want to support. Scroll to the bottom of the page and download the JS and CSS files.

We'll add these files to the Source theme, but the process can be adapted to work with any Ghost theme.

#### Add the CSS

Add the downloaded CSS file, `prism.css`, to the `assets/css` folder.

Open `screen.css` in your code editor and import the new CSS file. Put the import statement at the top of the file.

```
@import "prism.css";
```
#### Add the JS

Add the downloaded JS file, `prism.js`, to `assets/js/lib`.

#### Upload the customized theme

Help differentiate your customized theme from the default version by renaming. In `package.json`, change the `name` field to `source-with-prism` or whatever name you want.

Recompile your assets by running `yarn zip` or `npm run zip`. (If you haven’t already installed the theme’s dependencies, you’ll need to run `yarn` or `npm install` first.)

Finally, upload the theme zip file — find it in the `dist` folder — to your site. Add a code block, publish, and bask in all your syntax-highlighted glory!

### Style Prism

Because you’re loading the styles for Prism yourself, you have two options for customization.

First, you can edit the `prism.css` file and update values to better match your aesthetic. For example, here's the rule for formatting booleans, numbers, and functions.

```
.token.boolean,
.token.number,
.token.function {
     color: #f08d49;
 }

```

Currently, it’s set to render as royal orange. You can update the color to whatever value you want.

💡On the Prism download page, check `Development version` at the top of the page to get an unminified CSS file that’s easier to edit.

Second, by self-loading, you also have access to a wider selection of themes made by the Prism community. To use one, just copy the CSS into your `prism.css` file, recompile, and upload your theme.

[GitHub - PrismJS/prism-themes: A wider selection of Prism themesA wider selection of Prism themes. Contribute to PrismJS/prism-themes development by creating an account on GitHub.![](https://github.com/fluidicon.png)GitHubPrismJS![](https://opengraph.githubassets.com/bdcf184886acdf32914e147d2048e208a2184e2f498ce656db74e4d377d89dce/PrismJS/prism-themes)](https://github.com/PrismJS/prism-themes?ref=ghost.org)

For example, here’s the Synthwave ‘84 theme. (Sometimes, you may need to modify your theme’s styling so it doesn’t conflict with Prism’s.)

![Syntax highlighted code with the Synthwave theme](https://ghost.org/tutorials/content/images/2022/05/synthwave.png)

Summary
-------

You now know two techniques for adding syntax highlighting to your Ghost site, so nothing is stopping you from showing off your tech skills to the world. What’s more, Prism offers a [full library of plugins](https://prismjs.com/?ref=ghost.org#plugins) that you can use to extend its functionality: highlight specific lines, add a copy button, and more.

Are you a developer writing about Ghost? We’d love to read it. [Come over to our Forum](https://forum.ghost.org/?ref=ghost.org) and share your beautiful code snippets with the community.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### How to debug your theme

8 min read](/tutorials/debug/)

[### Create a Google News sitemap

4 min read](/tutorials/create-a-google-news-sitemap/)

[### Change the URL for tags and authors

1 min read](/tutorials/change-taxonomy-url/)

[### How to add a table of contents

9 min read](/tutorials/adding-table-of-contents/)

[### Change the order of posts

3 min read](/tutorials/change-post-order/)

[### Building content collections

3 min read](/tutorials/content-collections/)







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









