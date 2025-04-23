





Essential concepts to know when building a Ghost theme










































---


Ever get to the end of a project and thought, “I wish I knew this before I started.” Like every time, right? Well, this tutorial will give you that knowledge and insight *before* you start building a Ghost theme. Specifically, we’ll cover three areas:

* Ghost’s **templating** language Handlebars (and what’s a templating language anyways?)
* The **structure** of a Ghost theme and the three files essential to it
* Accessing the right data at the right time with **contexts**

By learning these three essential concepts, not only will you gain a fantastic overview of how a Ghost theme works, but you'll also be extremely well prepared to start building your very own custom theme.

What’s a templating language anyways?
-------------------------------------

Let’s first get clear on what a templating language is, and then we can get into Ghost’s specific templating language, Handlebars.

Like a mold for a cake, a template is a mold for your site’s data. You use one template for outputting the homepage and another for a post page. At its core, then, creating a Ghost theme is the creation of a set of templates, and the way you write the templates is with Handlebars, Ghost’s templating language. Handlebars files are easy to spot: they have the extension `.hbs`.

0:00/
### The basics of Handlebars

When creating a Handlebars template, you’ll write most of it in standard HTML. It’s the familiar markup under the hood of pretty much every website ever made. Handlebars comes into the picture wherever you need to render dynamic data in your theme. Dynamic data refers to the values you enter in Ghost Admin and the editor, everything from your site’s title to navigation items to the content of a post. Here’s a simple example of how to display your site’s title using HTML and Handlebars.

```
<h1>{{ @site.title }}</h1>
```

Let’s explain each part of this code.

* `<h1></h1>` are the HTML open and closing tags for a top-level heading. Nothing special here.
* `{{` and `}}` are the opening and closing tags for Handlebars. They tell Ghost that work needs to be done with the data inside. The tags are also the reason the language is called “Handlebars” — because they look like the mustache of the same name. And, just like it’d look pretty strange to have only one side of the mustache `{{`, you always need to close your Handlebars code with `}}`.
* `@site.title` is a special data object, available when writing a Ghost theme. It renders the template with the actual site title. “Render” is a fancy way of saying replace. If your site is called *Delicious Cakes*, then Ghost will render the template `<h1>{{@site.title}}</h1>` with `<h1>Delicious Cakes</h1>`. The beauty of this workflow is that if you ever change your site’s title, maybe to *Delicious Cakes and Cookies*, the new title will be rendered automatically, without having to update the template.

Before discussing all the exciting things Handlebars can do, let’s take a step back and summarize what we’ve covered so far.

1. A Ghost theme is primarily made up of Handlebars templates.
2. These files are rendered by Ghost with data from your site into HTML that's understandable by the browser.
3. Your audience knows none of this and just loves your beautiful site.

Here’s another take on the earlier visualization, with a bit more detail based on what you’ve learned.

0:00/
### Happy little helpers

Ghost provides several *helpers* to — well — help you create your theme. These helpers output data, control flow, translate, paginate, get additional data, and more. To get a sense of everything that’s possible when building a Ghost theme, it’s worthwhile to check out the full list of helpers:

[Ghost Handlebars Themes - Functional HelpersDiscover how to work with the full range of functional helpers in a custom Ghost theme. Learn more about Handlebars themes!![](https://ghost.org/favicon.ico)Ghost - The Professional Publishing Platform![](https://ghost.org/images/meta/ghost-docs.png)](https://ghost.org/docs/themes/helpers/?ref=ghost.org)

Let’s look at an example of a helper in action. Suppose you’re on your post page. Sometimes you add a feature image but sometimes not. The `{{#if}}` helper lets you account for each case.

```
{{#if feature_image}}
  Code to display if there is a feature image
{{/if}}

```

Use the helper by entering `#if` followed by the value to be checked. If the value is true or exists, then all the markup between the Handlebars tags (`{{#if}}{{/if}}`) will be rendered. If the value is false or doesn’t exist, then it won't. The idea here is to account for each possibility in the theme, so the content looks good, no matter the situation. [Check out a real-world example from Casper.](https://github.com/TryGhost/Casper/blob/ba0b3d08cca796d29dc3c96f25f6420557059591/post.hbs?ref=ghost.org#LL63C9-L80C16)

The `if` helper is one of many Ghost provides. Using these helpers enables you to build resilient themes and explore creative possibilities. In the next section, we’ll see how these helpers come together in template files that structure a theme.

The structure of a Ghost theme
------------------------------

0:00/

A real-world Ghost theme will be made up of several different kinds of files, but only three are required for it to work:

* `index.hbs`
* `post.hbs`
* `package.json`

It’s possible to zip these files up, upload the resulting file to Ghost, and have a fully functioning Ghost theme. Therefore, learning what these three files do serves as an essential introduction to the structure of a Ghost theme. Let’s summarize the purpose of each one.

### index.hbs is a theme’s front door

We’ll start with `index.hbs` because it serves as the entry point for your website. By default, this template file outputs your site’s homepage. Like a book’s index that points to the location of different topics, `index.hbs` points to the location of your posts. By modifying the `index.hbs` template, you control how the list of posts appears on your Ghost site.

`index.hbs` is also used for all pages that have a collection of posts. This includes your homepage and subsequent pages, as well as tag and author pages. Ghost is flexible, so it’s also possible (and common) to create unique templates for each of these pages.

[Here’s the `index.hbs` template for Casper.](https://github.com/TryGhost/Casper/blob/ba0b3d08cca796d29dc3c96f25f6420557059591/index.hbs?ref=ghost.org)

### post.hbs is where the content is

The second required file is `post.hbs`. It renders all individual posts and pages. By modifying this template, you change how post content appears on your site.

The key difference between a post and a page is that a post always belongs to a collection but a page doesn’t. This means that a post will be included in your homepage’s list of posts but a page won’t. In typical usage, posts include your articles, whereas pages are used for content like about and contact pages.

[Here’s the `post.hbs` template for Casper.](https://github.com/TryGhost/Casper/blob/ba0b3d08cca796d29dc3c96f25f6420557059591/post.hbs?ref=ghost.org)

### package.json is the brains of the operation

The final required file is `package.json`. Those [familiar with Node.js](https://ghost.org/tutorials/node/) will recognize this JSON file as providing metadata relevant to the project, that is, the Ghost theme. This metadata includes the theme’s name, version, scripts, dependencies, license, and more.

Ghost also uses `package.json` to configure aspects of the publication. The three most common properties configured include:

* **Posts per page:** This property tells Ghost how many posts to include in a collection. For example, setting this to 15 means that 15 posts will show up on the homepage.
* **Image sizes:** Ghost can automatically optimize your theme images, and this property instructs Ghost which image sizes to generate.
* **Custom settings:** These extend your theme’s functionality by allowing users to configure different options from Ghost Admin. In Casper, for example, [one custom setting](https://github.com/TryGhost/Casper/blob/ba0b3d08cca796d29dc3c96f25f6420557059591/package.json?ref=ghost.org#L109-L115) allows users to choose whether the body font is serif or sans serif.

These three files form the structure of your theme. The first two are built, as we saw earlier, with HTML and Handlebars. Context is the glue that holds everything together and what we’ll look at next.

 
![email letter on fire](https://ghost.org/tutorials/content/images/size/w1000/2023/04/flames-of-knowledge.jpg)

Getting the right data to the right template with context
---------------------------------------------------------

The final concept to understand when working with a Ghost theme is **************context**************. Every page in a Ghost theme belongs to a context, which determines the template used and the data available.

This explanation may seem a little abstract, so let’s consider a real-world example. The *Delicious Cakes* publication from above has an article on chocolate cake (and not just any chocolate cake but the most delicious chocolate cake you’ve ever had). A single post like this belongs to the *post* context. That means that it’ll be rendered by the `post.hbs` template and have all the post data available to it, like its title, author, tags, and more.

Here’s an overview of all available pages, contexts, and templates in Ghost. Two things to note about the table:

* The homepage has more than one index. Likewise, whenever you’re ********not******** on the first page of a collection, the `paged` context is included. On `/page/2/` of your site, the context will be `paged` and `index`.
* When a specific template isn’t available (like `author.hbs`), Ghost will fall back to a template that is guaranteed to be present.

| Page | Context(s) | Template | Fallback template | Data |
| --- | --- | --- | --- | --- |
| Homepage | home, index | home.hbs | index.hbs | Collection of posts |
| Post | post | post.hbs | - | Post data |
| Page | page | page.hbs | post.hbs | Page data |
| Author | author | author.hbs | index.hbs | Author data and post collection |
| Tag | tag | tag.hbs | index.hbs | Tag data and post collection |

To reiterate, contexts are important to understand because they play a big part in building a Ghost theme. In addition to determining the available data and what template to render, contexts also interact with Handlebars helpers.

For more on contexts and to see what data is available in each one, check out the [official docs](https://ghost.org/docs/themes/contexts/?ref=ghost.org).

Summary
-------

In this tutorial, you learned three concepts essential to understanding the meaning of life, or, rather, the foundations of a Ghost theme.

* Handlebars is Ghost's templating language and is used to create templates.
* Three required files — `index.hbs`, `post.hbs`, and `package.json` — contribute to a theme's structure.
* Contexts connect your site's data with the right template.

If all of this seems a bit theoretical, like learning to swim by reading a book, a great next step is to jump right in and try building a custom theme or making some simple modifications to an existing one. See our tutorial on [installing Ghost locally](https://ghost.org/tutorials/local-ghost/) to help you get started. Our [tutorials](https://ghost.org/tutorials/) and [docs](https://ghost.org/docs/themes/?ref=ghost.org) are also fantastic resources, and [our Forum](https://forum.ghost.org/?ref=ghost.org) is a welcoming place to come and ask questions.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### How to install Ghost locally

3 min read](/tutorials/local-ghost/)

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









