





Show reading time & progress in your Ghost theme










































---


In this tutorial, we’ll see how to add reading times to your Ghost theme and use JavaScript (JS) to update the reader’s progress in real-time. (Just look at the top of this page while you're reading for a demo.)

**Reading time**
----------------

Letting your readers know how long it’ll take to read an article is quite simple in Ghost. The `reading_time` helper outputs a customizable, calculated reading time of your content.

![Post card showing a 55 min reading time](https://ghost.org/tutorials/content/images/2022/05/reading-time.jpeg)

Add `{{reading_time}}` to your Ghost template to output `x min read`.

```
{{! Ensure you're in a post context }}
{{#post}}
	{{reading_time}}
	{{! outputs: 3 min read }}
{{/post}}
```

It’s also possible to customize the helper’s output.

```
{{! Ensure you're in a post context }}
{{#post}}
	{{reading_time minute="Only a minute" minutes="Takes % minutes"}}
	{{! outputs: Takes 3 minutes }}
{{/post}}
```

The `minute` attribute defines the value to use when reading time is calculated to be one minute or less. `minutes` defines the value to use when reading time is greater than a minute. (`%` is a variable that will be replaced with the number of minutes.)

And that’s all there is to it – you’re now an expert with the `reading_time` helper 🤓

Our docs are a great reference for the reading time helper and include some extra information about how reading time is calculated – for example, images count toward the reading time! You can also check out how [we use reading time in the Casper theme](https://github.com/TryGhost/Casper/blob/ff4e4226c0b5ddbe627adbcdbf0a2bb8135fc1cb/partials/post-card.hbs?ref=ghost.org#L55).

[Ghost Handlebars Theme Helpers: reading\_timeRender the estimated reading time of a post in your Ghost publication with this handlebars helper ⚡️ Read more about Ghost themes!![](https://ghost.org/favicon.ico)Ghost - The Professional Publishing Platform![](https://ghost.org/images/meta/ghost-docs.png)](https://ghost.org/docs/themes/helpers/reading_time/?ref=ghost.org)

**Show reading progress**
-------------------------

With reading time, the reader knows how long it will likely take to read your post, but what if we could provide real-time status as they read the article? By adding some custom HTML, CSS, and JS – this is also possible.

### Add the progress bar element

The first step is to add the `<progress>` element to the post template. We’ll add a class to make it easier to style in the next step. In `post.hbs`, add the following code block after `{{!< default}}`:

```
<progress class="reading-progress" value="0" max="100" aria-label="Reading progress"></progress>

```

The [progress element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress?ref=ghost.org) shows the completion status of a task. It could be the progress of a file upload, for example. In our case, it’s the reader's progress through the article.

### Style the progress bar

By default, the progress bar will be styled by the user’s browser. To maintain a consistent design, we’ll add some CSS to style the progress bar.

In **Code Injection** → **Site Header**, add this code:

```
<style>
.reading-progress {
  position: fixed;
  top: 0;
  z-index: 999;
  width: 100%;
  height: 5px; /* Progress bar height */
  background: #c5d2d9; /* Progress bar background color */
  -webkit-appearance: none;
     -moz-appearance: none;
          appearance: none; /* Hide default progress bar */
}

.reading-progress::-webkit-progress-bar {
  background-color: transparent;
}

.reading-progress::-webkit-progress-value {
  background: var(--ghost-accent-color); /* Progress bar color */
}
</style>
```

Comments above indicate the options you’d most likely want to change. The progress bar's color is set to the accent color as defined in Ghost Admin.

### Make the progress bar dynamic

The final component is to add the JS that will dynamically update the progress bar as the reader scrolls through the article. Add this code to `default.hbs` right before `ghost_foot`:

```
{{#is "post"}}
  <script>
    const progressBar = document.querySelector('.reading-progress');

    function updateProgress() {
      const totalHeight = document.body.clientHeight;
      const windowHeight = document.documentElement.clientHeight;
      const position = window.scrollY;
      const progress = position / (totalHeight - windowHeight) * 100;
      progressBar.setAttribute('value', progress);
      requestAnimationFrame(updateProgress);
    }

    requestAnimationFrame(updateProgress);
  </script>
{{/is}}
```

default.hbs

That’s it! Zip up your theme and upload it to your Ghost site. Hop on over to a post and start scrolling to see your real-time progress bar in action 💥

Demo
----

0:00/

Summary
-------

This tutorial walked through two ways to let readers know just how long (or short) that post is on your Ghost site. Being able to add reading time and progress to a theme means you're well on you're way to becoming a top-notch Ghost developer.

We’re eager to see your progress (bars), so come on over to [our Forum](https://forum.ghost.org/?ref=ghost.org) to show off 😉

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Build a custom sign-up form

7 min read](/tutorials/form/)

[### Custom settings are the ultimate power-up for themes

6 min read](/tutorials/custom-settings/)

[### The art of the post template

12 min read](/tutorials/post-template/)

[### A complete guide to partials

10 min read](/tutorials/partials/)

[### A comprehensive guide to the index template

9 min read](/tutorials/index/)

[### A comprehensive guide to the default template

9 min read](/tutorials/default/)

[### Essential concepts to know when building a Ghost theme

7 min read](/tutorials/essential-concepts/)

[### How to install Ghost locally

3 min read](/tutorials/local-ghost/)

[### Install Node on macOS, Windows, and Linux

4 min read](/tutorials/node/)

[### How to create a read-next section

10 min read](/tutorials/read-next/)

[### How to build a custom homepage

11 min read](/tutorials/custom-homepage/)

[### Create a custom post template

4 min read](/tutorials/create-a-custom-post-template/)

[### Implementing redirects

5 min read](/tutorials/implementing-redirects/)

[### How to build CSS files

2 min read](/tutorials/build-css-files/)

[### How to make a podcast RSS feed

4 min read](/tutorials/custom-rss-feed/)







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










