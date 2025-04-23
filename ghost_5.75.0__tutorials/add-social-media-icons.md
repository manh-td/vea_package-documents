





How to add social media icons to your Ghost theme











































---


Add any social media icon to your Ghost site from Ghost Admin. This tutorial will walk you through the process, step by step.

📢This tutorial uses the default Ghost theme, [Source](https://source.ghost.io/?ref=ghost.org), as a working example. The techniques presented below can also be applied to other Ghost themes.![Casper with new icons](https://ghost.org/tutorials/content/images/2024/05/art-times-social-media-icon-demo.png)

Add your social media links
---------------------------

Go to **Settings** → **Navigation**. To the **Primary Navigation** area, add a new item for every social media network you want to include. The label must be the name of the social media network. For example, to add a link to your Threads profile, use "Threads" as the navigation label.

![Ghost Admin navigation area](https://ghost.org/tutorials/content/images/2024/05/navigation-1.png)

Code generator
--------------

Follow the rest of the tutorial for a step-by-step guide on how to write the code for your theme — or take a shortcut and use our generator to create the code for you automatically.

Choose your official Ghost theme and the social media icons you want. Then, copy the code and paste it into **Settings** → **Code Injection** → **Site Header**. Click **Save** and you're done 🥳 Remember that you still need to add the navigation items, as explained in the previous step.

To see how to add the icons manually or learn more about the process, continue the tutorial below.


Choose your social media networks
























Generated code

```

Choose your theme and social media networks to get started...
```



Add the icon library
--------------------

We're going to use [FontAwesome](https://fontawesome.com/?ref=ghost.org) as our icon library. Let's load it on our Ghost site. Go to **Settings** → **Code Injection** → **Site Header**.

Paste in the following line of code and click **Save**.

```
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/brands.min.css" integrity="sha512-+oRH6u1nDGSm3hH8poU85YFIVTdSnS2f+texdPGrURaJh8hzmhMiZrQth6l56P4ZQmxeZzd2DqVEMqQoJ8J89A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
```
![Add FontAwesome to your Ghost site](https://ghost.org/tutorials/content/images/2024/05/code-injection-social-media-script.png)

Add the base styles
-------------------

Next, add the base icon styling right after the line of code from the previous step.

```
<style>
    :where(.nav, .gh-head-menu) .nav-behance a,
    :where(.nav, .gh-head-menu) .nav-dribbble a,
    :where(.nav, .gh-head-menu) .nav-mastodon a,
    :where(.nav, .gh-head-menu) .nav-threads a,
    :where(.nav, .gh-head-menu) .nav-x a,
    :where(.nav, .gh-head-menu) .nav-youtube a {
        font-size: 0 !important;
    }

    :where(.nav, .gh-head-menu) .nav-behance a::before,
    :where(.nav, .gh-head-menu) .nav-dribbble a::before,
    :where(.nav, .gh-head-menu) .nav-mastodon a::before,
    :where(.nav, .gh-head-menu) .nav-threads a::before,
    :where(.nav, .gh-head-menu) .nav-x a::before,
    :where(.nav, .gh-head-menu) .nav-youtube a::before {
        font-family: "Font Awesome 6 Brands";
        display: inline-block;
        font-size: 20px;
        font-style: normal;
        font-weight: normal;
        font-variant: normal;
        text-rendering: auto;
        -webkit-font-smoothing: antialiased;
    }
</style>
```

Notice that the styles include the names of the social media networks. If the social media network you want to use is already included, then copy these styles as is. Otherwise, update them to include the new social media network. For example, for LinkedIn, you would add: `:where(.nav, .gh-head-menu) .nav-linkedin a` and `:where(.nav, .gh-head-menu) .nav-linkedin a::before`.

Add the social media icons
--------------------------

The final step is to add styling that pulls in the actual icon for each social media network. Here's the code for the icons listed above. Again, add it to the **Site Header**.

```
<style>
  :where(.nav, .gh-head-menu) .nav-behance a::before {content: "\f1b4"}
  :where(.nav, .gh-head-menu) .nav-dribbble a::before {content: "\f17d"}
  :where(.nav, .gh-head-menu) .nav-mastodon a::before {content: "\f4f6"}
  :where(.nav, .gh-head-menu) .nav-threads a::before {content: "\e618"}
  :where(.nav, .gh-head-menu) .nav-x a::before {content: "\e61b"}
  :where(.nav, .gh-head-menu) .nav-youtube a::before {content: "\f167"}
</style>
```

All together, **Code Injection** looks like this:

![Code Injection with base styles](https://ghost.org/tutorials/content/images/2024/05/code-injection-social-media.png)

Copy the unicode (the value after `content`) from [FontAwesome's website](https://fontawesome.com/icons/linkedin?s=&f=brands&ref=ghost.org) for additional social media icons. Then, follow the pattern above to create a new CSS rule.

![](https://ghost.org/tutorials/content/images/2024/05/font-awesome-1.png)

For example, add a LinkedIn icon with the following CSS rule:

```
:where(.nav, .gh-head-menu) .nav-linkedin a::before { 
    content: "\f08c";
}
```

Save your styles in **Code Injection**,refresh your homepage, and revel in your new, beautiful social media icons ✨

![Ghost website with custom icons](https://ghost.org/tutorials/content/images/2024/05/art-times-social-media-icon-demo-1.png)

Summary
-------

By adding FontAwesome and some CSS to **Code Injection**, you now have a customized Ghost site that puts your social media icons front and center. This approach has the benefit of being maintenance-free, meaning that you can continue to install the latest version of your theme without having to worry about reincorporating this code.

We're eager to see your custom social media icons. Come share your site with the whole Ghost community over on [our official Forum](https://forum.ghost.org/?ref=ghost.org). It’s also a fantastic place to get help and meet other people using Ghost.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Essential concepts to know when building a Ghost theme

7 min read](/tutorials/essential-concepts/)

[### How to install Ghost locally

3 min read](/tutorials/local-ghost/)

[### Open a theme in a code editor

1 min read](/tutorials/open-a-theme-in-a-code-editor/)

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










