





How to add a table of contents to your Ghost site









































---


Having a table of contents on your site is a nice creature comfort for post readers – having one that's automatically generated and always up to date is nice for post authors. In this tutorial, we’ll show you how to add an automatically generated table of contents to your Ghost site in a few quick steps.

Here's an example of what we'll build:

0:00/

Tocbot
------

To help us add the table of contents, we’re going to use a JavaScript (JS) library called [Tocbot](https://tscanlin.github.io/tocbot/?ref=ghost.org). This library does the heavy lifting for us, which includes finding out the post’s headings, creating links to those sections, and showing the reader where they are on the page. It’s a super cool library!

💡Tocbot works by looking at your post’s heading tags like `<h2>`. Create a heading in Ghost by selecting your heading text and clicking the `H` icon in the popup editor.

There are two parts to the Tocbot library: 1) a JS file that handles functionality and 2) a CSS file that handles basic styling. Both need to be loaded into your Ghost theme.

In this tutorial, we’ll be using Ghost’s default theme, [Casper](https://demo.ghost.io/?ref=ghost.org). While the steps apply to any Ghost theme, you'll need to modify the code to work with your particular theme.

Edit default.hbs
----------------

Open `default.hbs` in [a code editor](https://ghost.org/tutorials/open-a-theme-in-a-code-editor/). In this file, add the Tocbot script and styles as explained below.

🚧At the time of writing, Tocbot is on version 4.12.3. When installing it on your site, use the latest version by updating the version number in the URLs above. Advanced developers can install Tocbot directly from npm.
### Add the CSS

Near the top of the `default.hbs` file, in the `head` tag and right before `{{ghost_head}}`, add the Tocbot CSS:

```
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/tocbot/4.12.3/tocbot.css">
```
### Additional styles

We'll add some additional styles to a `style` tag directly after the CSS we just loaded in `default.hbs`.

These styles will help Tocbot look right at home in our theme. While what's shared below is specific to Casper, you can adapt the style to work with whatever theme you’re using.

Our goal for the TOC is for it to be present alongside article content on larger screens but above it on smaller ones.

```
<style>
.gh-content {
    position: relative;
 }

.gh-toc > .toc-list {
    position: relative;
}

.toc-list {
    overflow: hidden;
    list-style: none;
}

@media (min-width: 1300px) {
     .gh-sidebar {
        position: absolute; 
        top: 0;
        bottom: 0;
        margin-top: 4vmin;
        grid-column: wide-start / main-start; /* Place the TOC to the left of the content */
    }
   
    .gh-toc {
        position: sticky; /* On larger screens, TOC will stay in the same spot on the page */
        top: 4vmin;
    }
}

.gh-toc .is-active-link::before {
    background-color: var(--ghost-accent-color); /* Defines TOC   accent color based on Accent color set in Ghost Admin */
} 
</style>
```
### Add the JS

In `default.hbs`, now near the end of the file and right before `{{ghost_foot}}`, add the Tocbot script:

```
<script src="https://cdnjs.cloudflare.com/ajax/libs/tocbot/4.12.3/tocbot.min.js"></script>
```
### Initialize the Tocbot script

Having loaded the Tocbot script, we now need to initialize it, which tells Tocbot where on the page we want our table of contents and what we want to add to it.

Add this script right after the code from the last step:

```
{{! Initialize Tocbot after you load the script }}
<script>
    tocbot.init({
        // Where to render the table of contents.
        tocSelector: '.gh-toc',
        // Where to grab the headings to build the table of contents.
        contentSelector: '.gh-content',
        // Which headings to grab inside of the contentSelector element.
        headingSelector: 'h1, h2, h3, h4',
        // Ensure correct positioning
        hasInnerContainers: true,
    });
</script>
```
💡The classes (`gh-content`, `gh-toc`) used in this tutorial are based on the Casper theme. You’ll need to change `gh-content` to match the container class (what wraps around your post content) of your theme. `gh-toc` can be anything you want – you just need to ensure that the class in the initialization script matches the one in the template (as shown in the next step).

Edit post.hbs
-------------

Let's define where we want the table of contents to show up in our theme.

In `post.hbs`, add the following code snippet right before the `{{content}}` helper:

```
<aside class="gh-sidebar"><div class="gh-toc"></div></aside> {{! The TOC will be inserted here }}
```

🔥 Fire up your table of contents
--------------------------------

You've made some sweet progress: Tocbot is installed and you’ve hooked it up to your Ghost theme.

As a final check, your `default.hbs` and `post.hbs` files should look like this:

```
<!DOCTYPE html>
<html lang="{{@site.locale}}"{{#match @custom.color_scheme "Dark"}} class="dark-mode"{{else match @custom.color_scheme "Auto"}} class="auto-color"{{/match}}>
<head>

    {{!-- Basic meta - advanced meta is output with {ghost_head} below --}}
    <title>{{meta_title}}</title>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="HandheldFriendly" content="True" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    {{!-- Theme assets - use the {asset} helper to reference styles & scripts,
    this will take care of caching and cache-busting automatically --}}
    <link rel="stylesheet" type="text/css" href="{{asset "built/screen.css"}}" />
    
    {{!-- TOC styles --}}
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/tocbot/4.12.3/tocbot.css">
    
    <style>
    .gh-content {
        position: relative;
    }

    .gh-toc > .toc-list {
        position: relative;
    }

    .toc-list {
        overflow: hidden;
        list-style: none;
    }

    @media (min-width: 1300px) {
        .gh-sidebar {
            position: absolute; 
            top: 0;
            bottom: 0;
            margin-top: 4vmin;
            grid-column: wide-start / main-start; /* Place the TOC to the left of the content */
        }
    
        .gh-toc {
            position: sticky; /* On larger screens, TOC will stay in the same spot on the page */
            top: 4vmin;
        }
    }

    .gh-toc .is-active-link::before {
        background-color: var(--ghost-accent-color); /* Defines TOC accent color based on Accent color set in Ghost Admin */
    } 
    </style>

    {{!-- This tag outputs all your advanced SEO meta, structured data, and other important settings,
    it should always be the last tag before the closing head tag --}}
    {{ghost_head}}

</head>
<body class="{{body_class}}{{#match @custom.title_font "=" "Elegant serif"}} has-serif-title{{/match}}{{#match @custom.body_font "=" "Modern sans-serif"}} has-sans-body{{/match}}{{#if @custom.show_publication_cover}} has-cover{{/if}}{{#is "home"}}{{#unless @custom.show_logo_in_navigation}} no-logo{{/unless}}{{/is}}">
<div class="viewport">

    <header id="gh-head" class="gh-head outer">
        <nav class="gh-head-inner inner">

            <div class="gh-head-brand">
                <a class="gh-head-logo{{#unless @site.logo}} no-image{{/unless}}" href="{{@site.url}}">
                    {{#if @site.logo}}
                        <img src="{{@site.logo}}" alt="{{@site.title}}" />
                    {{else}}
                        {{@site.title}}
                    {{/if}}
                </a>
                <a class="gh-burger" role="button">
                    <div class="gh-burger-box">
                        <div class="gh-burger-inner"></div>
                    </div>
                </a>
            </div>
            <div class="gh-head-menu">
                {{navigation}}
            </div>
            <div class="gh-head-actions">
                <div class="gh-social">
                    {{#if @site.facebook}}
                        <a class="gh-social-link gh-social-facebook" href="{{facebook_url @site.facebook}}" title="Facebook" target="_blank" rel="noopener">{{> "icons/facebook"}}</a>
                    {{/if}}
                    {{#if @site.twitter}}
                        <a class="gh-social-link gh-social-twitter" href="{{twitter_url @site.twitter}}" title="Twitter" target="_blank" rel="noopener">{{> "icons/twitter"}}</a>
                    {{/if}}
                </div>
                {{#if @site.members_enabled}}
                    {{#unless @member}}
                        <a class="gh-head-button" href="#/portal/signup" data-portal="signup">Subscribe</a>
                    {{else}}
                        <a class="gh-head-button" href="#/portal/account" data-portal="account">Account</a>
                    {{/unless}}
                {{/if}}
            </div>
        </nav>
    </header>

    <div class="site-content">
        {{!-- All other templates get inserted here, index.hbs, post.hbs, etc --}}
        {{{body}}}
    </div>

    {{!-- The global footer at the very bottom of the screen --}}
    <footer class="site-footer outer">
        <div class="inner">
            <section class="copyright"><a href="{{@site.url}}">{{@site.title}}</a> &copy; {{date format="YYYY"}}</section>
            <nav class="site-footer-nav">
                {{navigation type="secondary"}}
            </nav>
            <div><a href="https://ghost.org/" target="_blank" rel="noopener">Powered by Ghost</a></div>
        </div>
    </footer>

</div>
{{!-- /.viewport --}}


{{!-- Scripts - handle member signups, responsive videos, infinite scroll, floating headers, and galleries --}}
<script
    src="https://code.jquery.com/jquery-3.5.1.min.js"
    integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0="
    crossorigin="anonymous">
</script>
<script src="{{asset "built/casper.js"}}"></script>
<script>
$(document).ready(function () {
    // Mobile Menu Trigger
    $('.gh-burger').click(function () {
        $('body').toggleClass('gh-head-open');
    });
    // FitVids - Makes video embeds responsive
    $(".gh-content").fitVids();
});
</script>

{{!-- Tocbot script --}}
<script src="https://cdnjs.cloudflare.com/ajax/libs/tocbot/4.12.3/tocbot.min.js"></script>

{{! Initialize Tocbot after you load the script }}
<script>
    tocbot.init({
        // Where to render the table of contents.
        tocSelector: '.gh-toc',
        // Where to grab the headings to build the table of contents.
        contentSelector: '.gh-content',
        // Which headings to grab inside of the contentSelector element.
        headingSelector: 'h1, h2, h3, h4',
        // Ensure correct positioning
        hasInnerContainers: true,
    });
</script>

{{!-- Ghost outputs required functional scripts with this tag - it should always be the last thing before the closing body tag --}}
{{ghost_foot}}

</body>
</html>
```

default.hbs

```
{{!< default}}

{{!-- The tag above means: insert everything in this file
into the {body} tag of the default.hbs template --}}


{{#post}}
{{!-- Everything inside the #post block pulls data from the post --}}

<main id="site-main" class="site-main">
<article class="article {{post_class}} {{#match @custom.post_image_style "Full"}}image-full{{else match @custom.post_image_style "=" "Small"}}image-small{{/match}}">

    <header class="article-header gh-canvas">

        <div class="article-tag post-card-tags">
            {{#primary_tag}}
                <span class="post-card-primary-tag">
                    <a href="{{url}}">{{name}}</a>
                </span>
            {{/primary_tag}}
            {{#if featured}}
                <span class="post-card-featured">{{> "icons/fire"}} Featured</span>
            {{/if}}
        </div>

        <h1 class="article-title">{{title}}</h1>

        {{#if custom_excerpt}}
            <p class="article-excerpt">{{custom_excerpt}}</p>
        {{/if}}

        <div class="article-byline">
        <section class="article-byline-content">

            <ul class="author-list">
                {{#foreach authors}}
                <li class="author-list-item">
                    {{#if profile_image}}
                    <a href="{{url}}" class="author-avatar">
                        <img class="author-profile-image" src="{{img_url profile_image size="xs"}}" alt="{{name}}" />
                    </a>
                    {{else}}
                    <a href="{{url}}" class="author-avatar author-profile-image">{{> "icons/avatar"}}</a>
                    {{/if}}
                </li>
                {{/foreach}}
            </ul>

            <div class="article-byline-meta">
                <h4 class="author-name">{{authors}}</h4>
                <div class="byline-meta-content">
                    <time class="byline-meta-date" datetime="{{date format="YYYY-MM-DD"}}">{{date}}</time>
                    {{#if reading_time}}
                        <span class="byline-reading-time"><span class="bull">&bull;</span> {{reading_time}}</span>
                    {{/if}}
                </div>
            </div>

        </section>
        </div>

        {{#match @custom.post_image_style "!=" "Hidden"}}
        {{#if feature_image}}
            <figure class="article-image">
                {{!-- This is a responsive image, it loads different sizes depending on device
                https://medium.freecodecamp.org/a-guide-to-responsive-images-with-ready-to-use-templates-c400bd65c433 --}}
                <img
                    srcset="{{img_url feature_image size="s"}} 300w,
                            {{img_url feature_image size="m"}} 600w,
                            {{img_url feature_image size="l"}} 1000w,
                            {{img_url feature_image size="xl"}} 2000w"
                    sizes="(min-width: 1400px) 1400px, 92vw"
                    src="{{img_url feature_image size="xl"}}"
                    alt="{{#if feature_image_alt}}{{feature_image_alt}}{{else}}{{title}}{{/if}}"
                />
                {{#if feature_image_caption}}
                    <figcaption>{{feature_image_caption}}</figcaption>
                {{/if}}
            </figure>
        {{/if}}
        {{/match}}

    </header>

    <section class="gh-content gh-canvas">
        <aside class="gh-sidebar"><div class="gh-toc"></div></aside> {{! The TOC will be inserted here }}
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
{{#if @site.members_enabled}}
{{#unless @member}}
{{#if access}}
    <section class="footer-cta outer">
        <div class="inner">
            {{#if @custom.email_signup_text}}<h2 class="footer-cta-title">{{@custom.email_signup_text}}</h2>{{/if}}
            <a class="footer-cta-button" href="#/portal" data-portal>
                <div class="footer-cta-input">Enter your email</div>
                <span>Subscribe</span>
            </a>
            {{!-- ^ This looks like a form element, but it's just a link to Portal,
            making the form validation and submission much simpler. --}}
        </div>
    </section>
{{/if}}
{{/unless}}
{{/if}}


{{!-- Read more links, just above the footer --}}
{{#if @custom.show_recent_posts_footer}}
    {{!-- The {#get} helper below fetches some of the latest posts here
    so that people have something else to read when they finish this one.

    This query gets the latest 3 posts on the site, but adds a filter to
    exclude the post we're currently on from being included. --}}
    {{#get "posts" filter="id:-{{id}}" limit="3" as |more_posts|}}

        {{#if more_posts}}
            <aside class="read-more-wrap outer">
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

post.hbs

You’re now ready to [upload your changes](https://ghost.org/tutorials/download-and-upload-a-theme/#upload) to your Ghost site. Activate your new theme, refresh a post, and watch your own little table-of-contents robot work its magic 🤖

![](https://ghost.org/tutorials/content/images/2022/05/table-of-contents.png)

Summary
-------

In this tutorial, you installed a third-party JS library, modified a Ghost theme template, and added custom CSS. You’re well on your way to becoming a Ghost pro. Keep on leveling up your Ghost skills by checking out more of our tutorials or head on over to [our Forum](https://forum.ghost.org/?ref=ghost.org) to share how you built your table of contents.

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

[### A complete guide to code snippets

4 min read](/tutorials/code-snippets-in-ghost/)

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









