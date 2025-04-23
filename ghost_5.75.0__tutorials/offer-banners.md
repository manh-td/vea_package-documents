





How to add an offer banner to a Ghost site










































---


📰Ghost now includes a [native announcement bar feature](https://ghost.org/changelog/announcement-bar/?ref=ghost.org), which is easy to use and includes loads of customizations. It may be a better fit for your publication than the solution presented below!

Offers in Ghost provide a full-featured system to encourage new member signups with special discounts.

[Creating offers and discountsThe offers system in Ghost allows you to convert more paid customers by offering shareable discounts to your audience. Creating an offerThe offers page appears in Ghost Admin when you have an active Stripe connection in place. Offers can be created for any plan or tier, using a percentage or![](https://ghost.org/help/favicon.png)Ghost Help CenterTeam Ghost![](https://ghost.org/help/content/images/2020/12/topography-1.svg)](https://ghost.org/help/offers/?ref=ghost.org)

This tutorial will walk you through the process of adding a stunning offer bannerto your site's theme.

We’ll use the Ghost theme, [Headline](https://headline.ghost.io/?ref=ghost.org), as our starting point. However, all the steps below will work for most themes.

Here's a preview of what we're going to create.

![Website with banner offer at the top](https://ghost.org/tutorials/content/images/2022/05/banner-tutorial.png)

Add the banner to your theme
----------------------------

From a local copy of the Headline theme, open `default.hbs` in your code editor. Add the following code block [after the opening `<body>` tag](https://github.com/TryGhost/Headline/blob/32d941209008622da1074caefbb8d35f094afcbe/default.hbs?ref=ghost.org#L23).

```
<a class="gh-banner" href="https://YOUR-OFFER-URL" style="background-image: url({{asset "images/banner-background.jpg"}})">
    <div class="gh-banner-inner">
        <div class="gh-banner-left">
            <p class="gh-banner-headline">Support independent media</p>
            <p class="gh-banner-cta">Limited-time offer for new subscribers</p>
        </div>
        <div class="gh-banner-right">
            <p class="gh-banner-button">Learn more</p>
        </div>
    </div>
</a>
```

This code block contains the blueprint for your offer. Here's a reference of what it will look like on the page.

![Banner announcing a limited time offer](https://ghost.org/tutorials/content/images/2022/05/banner.png)

Looks pretty good, right? To make the banner your own, replace `https://YOUR-OFFER-URL` with your own offer URL from Ghost Admin and update the banner copy to suit your publication's identity.

 
![email letter on fire](https://ghost.org/tutorials/content/images/size/w1000/2023/04/flames-of-knowledge.jpg)

Add the background image
------------------------

The last edit to make is to add the background image. Add the image to the theme's `assets/images` folder. Update the code snippet so that `banner-background.jpg` matches your image's filename.

![](https://ghost.org/tutorials/content/images/2022/05/news-bg-1.jpg)

banner-background.jpg

Creating a banner background image that works on a variety of screen sizes can be a challenge. For reference, our banner background image is 1257 by 90 px.

You can omit the background image altogether by removing `style="background-image: url({{asset "images/banner-background.jpg"}})"` from the code snippet above. The banner will fall back to the background color defined in the next section.

That's all the changes that need to be made to the theme 💪 Zip up the theme folder and upload it to your Ghost site.

Style the banner via Code Injection
-----------------------------------

To style the banner, add the following `style` tag to **Code Injection → Site Header**. After adding in the styles, click `Save`.

```
<style>
.gh-banner {
  display: block;
  height: 90px;
  padding: 0 var(--gap);
  line-height: 1.3;
  background-color: #eeeff1; /* Banner background color */
  background-repeat: no-repeat;
  background-position: center;
}

.gh-banner-inner {
  display: flex;
  flex-direction: row;
  gap: 0.5em;
  align-items: center;
  justify-content: space-between;
  max-width: 1200px;
  height: 100%;
  margin: 0 auto;
}

.gh-banner-right {
  flex-shrink: 0;
}

.gh-banner-headline {
  font-size: 120%;
  font-weight: 700;
}

.gh-banner-button {
  padding: 0.35em 0.65em;
  font-weight: 700;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 3px;
  transition: background-color 0.3s;
}

.gh-banner:hover .gh-banner-button {
  background-color: var(--ghost-accent-color);
}

@media (max-width: 500px) {
  .gh-banner {
    font-size: 1.4rem;
  }

  .gh-banner-inner {
    flex-direction: column;
    justify-content: center;
  }
}

@media (max-width: 768px) {
  .gh-banner {
    position: relative;
    color: #fff;
  }

  .gh-banner::after {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    content: "";
    background: rgba(0 0 0 / 50%);
  }

  .gh-banner-inner {
    position: relative;
    z-index: 1;
  }
}
    
.is-head-open .gh-banner {
    display: none;
    }

/* Override Headline theme defaults */
.gh-banner:hover {
  opacity: 1 !important;
}

.gh-head-menu::before {
  top: 170px !important;
}

.gh-head-menu::after {
  top: 226px !important;
}
</style>
```

Now, an offer banner appears on every page of your site ✨

![Banner on post page](https://ghost.org/tutorials/content/images/2022/05/banner-on-mars.png)

Summary
-------

Offers are an effective tool to grow your paid membership by providing visitors an extra incentive to sign up. In this tutorial, you learned how to customize your theme to add an offer banner. Truth be told, the hardest part of all is likely coming up with the banner design and copy. We often talk about these kinds of things in [the Ghost Forum](https://forum.ghost.org/?ref=ghost.org), so come on over to share your creativity and find some inspiration 🌈

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

[### How to add social media icons to your site

4 min read](/tutorials/add-social-media-icons/)

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









