





How to use Code Injection in Ghost









































---


Code Injection offers an interface for easily adding analytics, styles, custom fonts, meta tags, and scripts to a Ghost site. It's also the perfect tool for making minor edits to your theme or adding some cool effects with JavaScript. In this tutorial, learn how as well as everything you need to know about using Code Injection in Ghost.

What's Code Injection?
----------------------

As the name hints, Code Injection injects code into your Ghost site. Access Code Injection from **Settings → Code Injection**.


![Ghost Settings page with Code Injection option highlighted](https://ghost.org/tutorials/content/images/2024/05/code-injection-1.png)

On the **Code Injection** page, there are two areas: **Site Header** and **Site Footer**. Ghost injects any text entered into these boxes onto every page of your site.

💡Code Injection is also available on a per post basis via the Ghost Editor's sidebar. It works the same way as explained above but is only added to that particular post's page.

**Site Header** code is injected into the `<head>` tag. **Site Footer** code is injected before the closing `</body>` tag. Both are added after other styles and scripts used by your theme.

```
<html>
  <head>
    <title>Page Title</title>
      
    <!-- Code Injection Site Header added here -->  
  </head>
  <body>
  <!-- Your beautiful content -->

  <!-- Code Injection Site Footer added here -->    
  </body>
</html>
```

Add CSS to the Site Header
--------------------------

One of the most common use cases for Code Injection is to add CSS to your Ghost site to customize the look and feel of your theme.

Let's say we had a site about animals using the Casper theme.

![Casper theme with animal posts](https://ghost.org/tutorials/content/images/2022/05/animals-w-regular-fonts.jpeg)

Everything's looking pretty good, but let's add some fun by using a custom typeface from [Google Fonts](https://fonts.google.com/?ref=ghost.org). Find the font you want to use – for our animals site, we're going to use a font called "Luckiest Guy." Go to the typeface's page and click **Get font**.

![Google Fonts page with numbers indicating steps](https://ghost.org/tutorials/content/images/2024/05/fonts-2.png)

Then, click **Get embed code**.

![Google Fonts Use on the web box](https://ghost.org/tutorials/content/images/2024/05/get-embed.png)

Copy the `<link>` tags and paste them into the **Site Header**.

![Google Fonts embed code](https://ghost.org/tutorials/content/images/2024/05/head-code.png)
```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Luckiest+Guy&display=swap" rel="stylesheet">
```



Code Injection → Site Header



Next, add the CSS rules. **Whenever you add CSS rules to the Site Header, wrap them in a `<style>` tag.** We only want our wacky new font to affect our headings, so we'll only apply it to them. And, since this font only has a single weight, we'll specify that, too.

```
<style>
    h1, h2, h3, h4, h5, h6 {
        font-family: 'Luckiest Guy', sans-serif;
        font-weight: 400;
    }
</style>
```



Code Injection → Site Header



That's it! The **Code Injection** is ready to be saved.

![Code Injection Site Header with custom Google Font](https://ghost.org/tutorials/content/images/2024/05/code-injection-header.png)

And so is our animals site – but now with a funky new font 💅

![Ghost animals site with funky new font](https://ghost.org/tutorials/content/images/2022/05/animals-2.jpeg)

Add JS to the Site Footer
-------------------------

The second most common use case for **Code Injection** is to add JavaScript to a Ghost site. When adding JS, add it to the **Site Footer** so that it loads properly.

As an example, let's add a typewriter effect to our animals site. To help us along, we'll use the open-source [TypewriterJS library](https://github.com/tameemsafi/typewriterjs?ref=ghost.org).

Load the main script into the **Site Footer**.

```
<script src="https://unpkg.com/typewriter-effect@latest/dist/core.js"></script>
```



Code Injection → Site Footer



Next, configure the TypewriterJS script and start it on the page. **Whenever you add JS via Code Injection, wrap it in a `<script>` tag.**

```
<script>
    const app = document.querySelector('.site-title + p');

    const typewriter = new Typewriter(app, {
      loop: true,
      delay: 75,
    });

    typewriter
      .typeString('356 of the best <strong>monkeys</strong>')
      .pauseFor(1000)
      .deleteChars(7)
      .typeString('<strong>parrots</strong>')
      .pauseFor(750)
      .deleteChars(7)
      .typeString('<strong>sharks</strong>')
      .pauseFor(500)
      .deleteChars(6)
      .typeString('<strong>snakes</strong>')
      .pauseFor(500)
      .deleteChars(7)
      .typeString('<strong>animals</strong> on the web')
      .pauseFor(1500)
      .deleteAll(50)
      .start();
</script>
```



Code Injection → Site Footer



All set! The **Site Footer** is ready to be saved.

![Ghost Code Injection Site Footer example](https://ghost.org/tutorials/content/images/2024/05/footer.png)

And our animals site just got a little wilder 🦁


0:00
/0:16









Summary
-------

**Code Injection** is a powerful and convenient tool for quickly adding CSS, JS, and more to your Ghost site.

Many of Ghost's best **Integrations** rely on Code Injection – and now that you're an expert with it – you're more than ready to add one to your publication.

[Ghost integrations – official apps, plugins & toolsGhost plugins, tools & apps to integrate withh your Ghost site for automation, analytics, marketing, support and much more! 👉![](https://ghost.org/favicon.ico)Ghost - The Professional Publishing Platform![](https://ghost.org/images/meta/ghost-integrations.png)](https://ghost.org/integrations/?ref=ghost.org)
**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Send a custom welcome email

5 min read](/tutorials/welcome-email/)

[### Open a theme in a code editor

1 min read](/tutorials/open-a-theme-in-a-code-editor/)

[### Download a code editor

1 min read](/tutorials/download-a-code-editor/)

[### Download and upload a theme

5 min read](/tutorials/download-and-upload-a-theme/)

[### The complete guide to comments

3 min read](/tutorials/adding-comments/)

[### How to add social media icons to your site

4 min read](/tutorials/add-social-media-icons/)

[### How to add an offer banner

4 min read](/tutorials/offer-banners/)







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










