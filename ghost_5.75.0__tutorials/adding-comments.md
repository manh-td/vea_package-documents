





The complete guide to adding comments in Ghost









































---


🥳Comments are now part of Ghost. [Learn more about the new feature](https://ghost.org/help/commenting/?ref=ghost.org). This tutorial is still good for people who want to use a third-party comment solution with Ghost.

Give the people a voice and let them reply to your article directly with comments.

Ghost integrates with a variety of commenting platforms so that you can find a platform that meets your publication’s needs. Check out our [Community Integration page](https://ghost.org/integrations/?tag=community&ref=ghost.org) to find guides on integrating your chosen platform with Ghost.

This tutorial will cover the steps you’ll take to connect most commenting platforms to your Ghost site.

![Comment fields on a blog post page](https://ghost.org/tutorials/content/images/2022/05/comments-1.jpeg)

Using Disqus commenting platform on Casper

Add the code
------------

Open a copy of your theme in the code editor and go to the `post.hbs` file.

🚁Need help? See our guides on [downloading a theme](https://ghost.org/tutorials/download-and-upload-a-theme/) and [opening it in a code editor](https://ghost.org/tutorials/open-a-theme-in-a-code-editor/).

If you’re using [Casper](https://demo.ghost.io/?ref=ghost.org), you’ll see the following section of code (beginning at line 76):

```
{{!--
  <section class="article-comments gh-canvas">
    If you want to embed comments, this is a good place to paste your code!
  </section>
--}}
```

Other themes might do things differently. For example, [Ghost’s Ease theme](https://ease.ghost.io/?ref=ghost.org) uses a `partial` called `comment.hbs`. No matter these differences, the takeaway here is that *you’re looking for the spot on your post page where you want your comments to appear*. Generally, this will be after your main content.

The next step is to add the code for your commenting platform to this location in `post.hbs`. Navigate to the tool you want to use within our **[Community Integrations](https://ghost.org/integrations/?tag=community&ref=ghost.org)** for more details on how to do this or follow the instructions provided by your commenting platform.

Once the commenting code is added, zip up your theme files and upload them to your Ghost site.

Connect and verify
------------------

Verify that the commenting tool works by testing it yourself. Navigate to one of your published posts and submit a comment – maybe something about how great your publication is 😉 – if the comment appears as expected, you’re all good to go!

Members only
------------

With Ghost, not only can you add the commenting platform of your choice, but you can also restrict access to your publication’s members. All in one extra line of code.

Wrapping your comments section with the `access` helper will restrict comments to members only.

```
{{#if access}}
  <!-- Your commenting service -->
{{else}}
  <p>You're missing out on the conversation. Become a member and join in.</p>
  <a href="#/portal/">Subscribe</a>
{{/if}}
```

Demo
----

In this demo, we added Disqus comments to Casper:

[Post with CommentsCall me Ishmael. Some years ago—never mind how long precisely—having little or no money in my purse, and nothing particular to interest me on shore, I thought I would sail about a little and see the watery part of the world. It is a way I have of![](https://ghost-with-comments.ghost.io/favicon.ico)Comment DemoGhost![](https://images.unsplash.com/photo-1617925109341-2b99305cdee2?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDN8fHdoYWxlfGVufDB8fHx8MTY1MjcyMzMxNQ&ixlib=rb-1.2.1&q=80&w=2000)](https://ghost-with-comments.ghost.io/post-with-comments/?ref=ghost.org)

Summary
-------

Woop! You’ve now added commenting to your Ghost site, and even found a way to scope commenting to your closed group of members. And, if you’re eager to keep on commenting, come over to [our Forum](https://forum.ghost.org/?ref=ghost.org), where the conversation is nothing short of lively.

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

[### How to use Code Injection

4 min read](/tutorials/use-code-injection-in-ghost/)

[### Download a code editor

1 min read](/tutorials/download-a-code-editor/)

[### Download and upload a theme

5 min read](/tutorials/download-and-upload-a-theme/)

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









