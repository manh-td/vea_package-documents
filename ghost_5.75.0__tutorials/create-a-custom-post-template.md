





Create a custom post template in Ghost









































---


It likely doesn't surprise you, but every article you publish looks the same. Because each one, without fail, uses the same post template. And, 99% of the time – that's precisely what you want: consistent styling across your publication.

But what about that 1%? What if you publish a limited-run series that needs bespoke styling? What if you want to omit the author or other metadata from certain posts? Or what if you want to load a library to show graphs and charts?

Ghost makes it easy to create custom templates for just such occasions. This tutorial will walk you through the steps to create them.

Create a template file
----------------------

Our publication, *History & Design*, is launching a limited-run series on Midcentury modern design to promote a forthcoming book on the subject. To make these posts stand out from our usual ones, we're going to create a custom template.

![Midcentury Modern custom template example](https://ghost.org/tutorials/content/images/2022/05/mcm-custom-post.jpeg)

The first step is to open your theme in a code editor. Rather than creating a new file from scratch, jumpstart the custom template creation process by copying the existing `post.hbs` file. This way, we'll have a base from which to start.

Rename the file `custom-midcentury-modern.hbs`.

```
.
├── LICENSE
├── README.md
├── assets
├── author.hbs
├── custom-midcentury-modern.hbs
├── default.hbs
├── error-404.hbs
├── error.hbs
├── gulpfile.js
├── index.hbs
├── package.json
├── page.hbs
├── partials
├── post.hbs
├── tag.hbs
└── yarn.lock
```

Theme files with custom template

**The filename is essential.** The `custom-` prefix tells Ghost that the file is a custom template, which makes it selectable in the Ghost Editor. Everything after the initial hyphen `-` specifies what authors see in the Editor's **Template** dropdown menu. In this example, our custom template appears as "Midcentury Modern."

![Ghost editor sidebar with template option highlighted](https://ghost.org/tutorials/content/images/2022/05/custom-template-select.jpg)

Now, the author can easily choose our big splashy custom template for these special posts.

Designing the custom template
-----------------------------

Because we just copied our current post template for our custom one, we don't actually yet have our new design.

Let's leverage Ghost's Header card to help us make the custom template. The full-width Header card features customizable sizes, text, backgrounds, and an optional call-to-action button.

This is a Header card
---------------------

### It really catches your attention, right?

[Learn more](https://ghost.org/changelog/headers/?ref=ghost.org)

By substituting our existing post header with the Header card, we'll get an easy, eye-catching custom template

### Editing the post template

For this example, we'll use the [default Ghost theme Casper](https://demo.ghost.io/?ref=ghost.org), but you can adapt this technique for any theme.

Open `custom-midcentury-modern.hbs` in a code editor and remove the entire `<header>` element.

To remove the gap between the navbar and Header card, add `style="padding-top: 0"` to the `<article>` tag.

The complete custom template now looks like this:

```
{{!< default}}

{{!-- The tag above means: insert everything in this file
into the {body} tag of the default.hbs template --}}


{{#post}}
{{!-- Everything inside the #post block pulls data from the post --}}

<main id="site-main" class="site-main">
    <article class="article {{post_class}} {{#match @custom.post_image_width "Full"}}image-full{{else match @custom.post_image_width "=" "Small"}}image-small{{/match}}" style="padding-top: 0;">

        <section class="gh-content gh-canvas">
            {{content}}
        </section>

        {{!--
        <section class="article-comments gh-canvas">
            If you want to embed comments, this is a good place to paste your code!
        </section>
        --}}

    </article>
</main>

{{!-- A signup call to action is displayed here, unless viewed as a logged-in member --}}
{{#match @custom.email_signup_for_logged_out_visitors "!=" "None"}}
{{#unless @member}}{{#if access}}
    <section class="footer-cta {{#match @custom.email_signup_for_logged_out_visitors "Bottom of post"}}cta-alt{{/match}}">
        <div class="inner">
            {{#if @custom.email_signup_text}}<h2>{{@custom.email_signup_text}}</h2>{{/if}}
            <a class="footer-cta-button" href="#/portal" data-portal>
                <div class="footer-cta-input">Enter your email</div>
                <span>Subscribe</span>
            </a>
            {{!-- ^ This looks like a form element, but it's just a link to Portal,
            making the form validation and submission much simpler. --}}
        </div>
    </section>
{{/if}}{{/unless}}
{{/match}}


{{!-- Read more links, just above the footer --}}
{{#if @custom.show_recent_posts}}
    {{!-- The {#get} helper below fetches some of the latest posts here
    so that people have something else to read when they finish this one.

    This query gets the latest 3 posts on the site, but adds a filter to
    exclude the post we're currently on from being included. --}}
    {{#get "posts" filter="id:-{{id}}" include="authors" limit="3" as |more_posts|}}

        {{#if more_posts}}
            <aside class="read-more-wrap">
                <div class="read-more inner">
                    {{#foreach more_posts}}
                        {{> "post-card"}}
                    {{/foreach}}
                </div>
            </aside>
        {{/if}}

    {{/get}}
{{/if}}

{{/post}}
```

custom-midcentury-modern.hbs

Just zip up your theme files and upload them to Ghost. On any post, you'll now have the option of selecting your custom template. Create your Header card in the post editor and your custom template is ready for publication 🥳

Summary
-------

From limited-run series, as in our example, to tweaks, additions, and complex integrations, custom templates are an easy, elegant solution that you now know how to implement 💪

Because the possibilities for custom templates are seemingly limitless, we'd love to see what you've created. Come show and tell with the whole Ghost community over [on our Forum](https://forum.ghost.org/?ref=ghost.org). It's a fantastic place to get help and meet fellow Ghost users.

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

[### Implementing redirects

5 min read](/tutorials/implementing-redirects/)

[### Show reading time & progress

3 min read](/tutorials/reading-time/)

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









