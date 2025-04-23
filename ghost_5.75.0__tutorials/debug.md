





How to debug your Ghost theme with the log helper









































---


Like a behind-the-scenes look at your favorite film, Ghost’s {{log}} helper lets you see the data that’s behind your theme, empowering you to debug your theme like a pro. In this tutorial, we’ll follow Jamie, as they work on their new Ghost site, *Cats in Art*. Using real-world examples, we'll show you everything you need to know about the log helper, from getting started to traversing contexts.

[Ghost Handlebars Theme Helpers: logDebug your custom Ghost theme with this handy handlebars helper for Ghost theme developers ⚡️ Read more about Ghost themes!![](https://ghost.org/favicon.ico)Ghost - The Professional Publishing Platform![](https://ghost.org/images/meta/ghost-docs.png)](https://ghost.org/docs/themes/helpers/log/?ref=ghost.org)

Start Ghost in development mode
-------------------------------

To use the `{{log}}` helper, start Ghost in development mode. In a terminal, navigate to the directory where Ghost is [locally installed](https://ghost.org/docs/install/local/?ref=ghost.org) and run `ghost run -D`. This command tells Ghost to start and output logging information to the console.

```
ghost run -D
```

Open a browser and navigate to your local Ghost site. For every page load, requests for the page and its assets (like images) now appear in the console. Refresh the page to see the data logged in real-time. (Hit `ctrl + c` in the terminal to stop Ghost’s development mode.)

0:00/

The log helper in action

Open Ghost Admin, navigate to ****************Settings****************, and set your theme. You’re now ready to start using the `{{log}}` helper 🏃‍♀️

🗃️To see real-time changes, be sure your theme folder is located in (or linked to) Ghost’s `content/themes` folder.

Use the {{log}} helper
----------------------

The `{{log}}` helper shows which data is available at a particular place in your theme. *Cats in Art* is a site ***********—*********** you guessed it — featuring cats in art. It uses Ghost’s default theme, [Casper](https://demo.ghost.io/?ref=ghost.org).  As we follow Jamie’s use of the `{{log}}` helper, know that the same techniques shown below work with all Ghost themes.

Log specific data
-----------------

Jamie added a sweet gradient to use as the background image to their author profile, but the image isn’t appearing on the site. They open the `author.hbs` file, which Casper uses to render author profile pages, and find the [code for the background image](https://github.com/TryGhost/Casper/blob/a007415d8909bf0acf8fdab20747611e1f0cb333/author.hbs?ref=ghost.org#L16):

```
<img class="post-card-image"
        srcset="{{img_url feature_image size="s"}} 300w,
                {{img_url feature_image size="m"}} 600w,
                {{img_url feature_image size="l"}} 1000w,
                {{img_url feature_image size="xl"}} 2000w"
        sizes="(max-width: 1000px) 400px, 800px"
        src="{{img_url feature_image size="m"}}"
        alt="{{name}}"
/>
```
![Image not found on Jamie's site](https://ghost.org/tutorials/content/images/2023/01/image-404.png)

By running in development mode, Jamie already has a vague clue about what’s causing the bug. There’s a 404 error that tells them the image file isn’t being found.

![The terminal shows a 404 response for the requested image](https://ghost.org/tutorials/content/images/2023/01/image-404-console.png)

💡 Click the image to expand

Use the log helper by combining the log keyword with the property to be logged:  `{{log property_to_logged}}`. To help investigate their missing image, Jamie log’s the value of `feature_image` by adding the log helper to the template and refreshing the page in the browser.

```
{{log feature_image}}
<img class="post-card-image"
        srcset="{{img_url feature_image size="s"}} 300w,
                {{img_url feature_image size="m"}} 600w,
                {{img_url feature_image size="l"}} 1000w,
                {{img_url feature_image size="xl"}} 2000w"
        sizes="(max-width: 1000px) 400px, 800px"
        src="{{img_url feature_image size="m"}}"
        alt="{{name}}"
/>
```
![The terminal shows undefined](https://ghost.org/tutorials/content/images/2023/01/log-undefined.png)

`undefined` now appears in the log. From here, Jamie guesses that they're likely not using the right image property, which is why the image is not coming through. To be sure, Jamie annotates the log helper with static text. This technique is particularly useful when using multiple log helpers.

```
{{log "feature image:" feature_image}}
```
![The console shows feature image: undefined](https://ghost.org/tutorials/content/images/2023/01/feature-image.png)

Adding this bit of text confirms that the feature\_image property is undefined — Jamie’s bummed the property value is wrong but relieved to know what the bug is 😅

### Log all available data

If `feature_image` isn’t the right property, then what is? Jamie uses `{{log this}}` to show all available data in a context.

```
{{log this}}
```

Think of `log this` as saying “log *this* data right here.” Jamie now gets this output:

![Log this shows author data in the console](https://ghost.org/tutorials/content/images/2023/01/log-this.png)
```
{
  slug: 'jamie',
  id: '1',
  name: 'Jamie Larson',
  profile_image: null,
  cover_image: 'http://localhost:2368/content/images/2023/01/mesh-gradient.png',
  bio: null,
  website: null,
  location: 'Berlin',
  facebook: null,
  twitter: '@jamie',
  meta_title: null,
  meta_description: null,
  url: 'http://localhost:2368/author/jamie/'
}
```

Each of the properties listed here — `name`, `slug`, `url`, `bio`, etc. — can be used in the theme template. For example, `{{name}}` renders as “Jamie Larson” on the live site.

Looking through the available data, the error becomes clear. `feature_image` is not the right property. It’s actually `cover_image`. Jamie can tell that’s the property they need because of its name (cover image) and because it’s the only one with an image URL.

Changing the property to `cover_image` returns Jamie’s author page with their sweet gradient image loading as expected!

![Jamie successfully loads his gradient background image](https://ghost.org/tutorials/content/images/2023/01/cover-image-loaded.png)😹You might be thinking that Jamie could’ve figured out their bug much quicker by just reading the [docs for the author's context](https://ghost.org/docs/themes/contexts/author/?ref=ghost.org). That’s probably true, but Jamie’s mischievous cat had chewed through the ethernet cable, leaving Jamie without internet and without access to the docs. `{{log}}` was their saving grace.

Doing more with the log helper
------------------------------

Now that Jamie has a good handle on how the `log` helper works, they take it for a spin to see what else it can do.

### Logging post data

Jamie opens their post template (`post.hbs`). Inside the post context, they add `{{log this}}` and save the file.

```
{{#post}}
...
{{log this}}
...
{{/post
```

Loading a post outputs lots of data to the terminal, probably too much to fit on the screen all at once. This data represents everything available to use in the theme when inside the post context.

![Logging post data to the terminal](https://ghost.org/tutorials/content/images/2023/01/logging-a-post.png)

Jamie sees familiar properties like `title` and `feature_image` and a whole lot more.

But Jamie's really only interested in seeing the tags for the post. They update the log helper with the property name and annotate it to make it easier to recognize in the logs:

```
{{log "tags:" tags}}
```
![Tags logged to the console](https://ghost.org/tutorials/content/images/2023/01/log_tags.png)

In the terminal, Jamie sees that this post has one tag associated with it, “Print.” (On *Cats in Art*, each artwork is tagged with which kind of art it is.) They also see all the available tag data, which is editable on the tag page in Ghost Admin.

Jamie notices that each tag has an `accent_color` property, which gives them the idea of color-coding tags in a future design 🎨

### Switching contexts

Jamie’s feeling pretty good now. There’s nothing they can’t log 💪

But just as they’re ready to sign off for the day, Jamie thinks it would be cool to include the number of posts they’ve written about cats in art on their author page.

They log author data only to see that publication count isn’t included. Jamie thinks about where this data might be available.

The author template (`author.hbs`) renders a collection of posts — everything an author’s published. In Ghost, this collection is paginated by default. The pagination object includes lots of useful data like the current page number, the number of posts per page, and the total number of posts available. This `total` property is exactly what Jamie needs: the total number of posts they’ve published about cats in art.

[Ghost Handlebars Theme Helpers: paginationDefine the pagination for your Ghost theme using the pagination Handlebars helper. Read more about Ghost themes! 👻![](https://ghost.org/favicon.ico)Ghost - The Professional Publishing Platform![](https://ghost.org/images/meta/ghost-docs.png)](https://ghost.org/docs/themes/helpers/pagination/?ref=ghost.org)

Jamie updates the author template to include this data, wrapped in a `span` to make it easier to style.

```
<header class="post-card-header">
  <h2 class="post-card-title">{{name}} <span class="author-post-count">{{pagination.total}}</span></h2>
</header>
```

They refresh the page, hoping to see their post count, but it doesn’t work. Jamie then tries logging it:

```
{{log "post count:" pagination.total}}
```
![Terminal shows post count undefined](https://ghost.org/tutorials/content/images/2023/01/post-count-undefined.png)

Undefined!? Jamie’s now been at this awhile, racking their brain for why this isn’t working, and just about ready to hurl their laptop out the window into the evening breeze. But instead, they pet their mischievous cat and get back to it.

Jamie knows they’re currently in the `#author` context, but pagination data is only available in the top-level context. That means Jamie needs to exit the current context and go up a level to get the post count, like if you were on the main floor but what you needed to get was upstairs.

Jamie goes up a level by prefixing the property with `../`, similar to how you navigate the file system in the terminal. The `log` helper now looks like this:

```
{{log "post count:" ../pagination.total}}
```
![Post count correctly logged to the terminal](https://ghost.org/tutorials/content/images/2023/01/post-count-correct.png)

In the terminal, the helper now logs the post count as 100. That’s promising. Jamie updates their template with this new syntax.

```
<header class="post-card-header">
  <h2 class="post-card-title">{{name}} <span class="author-post-count">{{../pagination.total}}</span></h2>
</header>
```
![Jamie's author page shows 100 posts](https://ghost.org/tutorials/content/images/2023/01/100-post-jamie.png)

Aw, yeah. Looking great! Post count now displays correctly, and Jamie contemplates whether to write post 101 or to call it a night, for real this time.

Whatever Jamie decides, changing context is an indispensable tool when developing Ghost themes, and using it with the `log` helper gives the developer the ability to see which data is available, no matter where they are in the theme.

Summary
-------

In this tutorial, you followed Jamie in their use of the `log` helper to output specific data, all available data by using `this`, and data from different contexts.

Knowing how to use the `log` helper unlocks a whole new perspective for custom theme development. You now have direct access to the data your templates are rendering. This new superpower will boost your ability to squash bugs and amplify your creative possibilities 🌈

Let us know what you find, what you create, and whether you’re getting stuck [on our official Forum](https://forum.ghost.org/?ref=ghost.org), where we talk about all things Ghost.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Create a Google News sitemap

4 min read](/tutorials/create-a-google-news-sitemap/)

[### Change the URL for tags and authors

1 min read](/tutorials/change-taxonomy-url/)

[### A complete guide to code snippets

4 min read](/tutorials/code-snippets-in-ghost/)

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









