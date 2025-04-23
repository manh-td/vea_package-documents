





Change the URL for tags and authors









































---


A taxonomy classified things based on a common relation. Ghost uses two taxonomies to classify posts: **authors** and **tags**. The authors taxonomy groups posts by their author.

For example, Ghost automatically makes all posts by Jane Austen available at `sitename.com/author/jane-austen/`. Similarly, the tags taxonomy groups posts by their tag, and Ghost automatically makes all posts tagged with `podcast` available at `sitename.com/tag/podcast/`.

These taxonomies save you the trouble of creating archive pages for every author and tag, and, most of the time, they’re exactly what you need.

But what if you want to customize these taxonomies? What if, instead of post authors, you have post *contributors*? Instead of tags, you have *topics*?

In this tutorial, we’ll show you how to define custom taxonomies, transforming `/author/` and `/tag/` into new terms, with a few lines of code ⚡

**Define your taxonomies in the `routes.yaml` file**
----------------------------------------------------

Download your `routes.yaml` file from the **Settings** → **Labs** in Ghost Admin.

This file is split into three sections, and for this tutorial, you’ll be using the “taxonomies” section. Read more about [dynamic routing](https://ghost.org/docs/themes/routing/?ref=ghost.org)for an overview of the rest of the file.

This is the default taxonomy configuration:

```
taxonomies:
  tag: /tag/{slug}
  author: /author/{slug}

```

By changing the permalink structure – updating the values to the right of the colon –  you can customize the taxonomy to suit your publication’s needs:

```
taxonomies:
  tag: /topic/{slug}
  author: /contributor/{slug}

```

Save this file and upload it to your Ghost site. Your new taxonomy is now live! For example, posts tagged with `travel` now show up at `site.com/topic/travel/`, rather than `/tag/travel`. Similarly, author pages now show up at `site.com/contributor/author-slug/`, rather than `/author/author-slug`.

Pretty neat, right?

Summary
-------

You’ve successfully updated your taxonomies and permalinks for tags and authors on your Ghost publication 🥳

Be sure to share your sweet new taxonomies over on our [Forum](https://forum.ghost.org/?ref=ghost.org) – our community is always excited to see how people are using Ghost.

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









