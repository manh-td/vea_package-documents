





Building content collections in Ghost









































---


Imagine you have a cooking website called Delicious that organizes recipes according to their cuisines.

It might look something like this:

![Example of a cooking website called Delicious](https://ghost.org/tutorials/content/images/2022/05/home.jpeg)

But what if, instead of a list of posts on the homepage, you wanted to present readers with cuisine collections?

![Website showing cuisine collections](https://ghost.org/tutorials/content/images/2022/05/collections.jpeg)

Using custom routing, it's possible to create content collections just like this. In this tutorial, we'll show you the delicious ins and outs of building content collections in Ghost.

**Define a content collection with tags**
-----------------------------------------

Adding tags to posts is the easiest way to define a content collection in Ghost.

![Tag dropdown in the Ghost Editor](https://ghost.org/tutorials/content/images/2022/05/tags-1.jpg)

Whenever you tag a post, Ghost [automatically creates an archive](https://ghost.org/help/organising-content/?ref=ghost.org#tag-archives) for that tag. By default, tagging this post `French` creates an archive at `sitename.com/tag/french/`.

Though they are both groups of posts, a collection is different from a tag archive: collections are **exclusive** but archives are not.

Exclusivity here means that a post lives in only one collection at a time: a post in the French collection will no longer show up on the homepage, Ghost's default collection. This exclusivity gives you much greater control over collections than you get with tag archives.

In the next section, we’ll see the tools at your disposal for building collections.

Create a collection
-------------------

Creating a collection begins by downloading your `routes.yaml` file from Ghost Admin (**Settings** → **Labs**). It’s helpful to open the file in a code editor like [VS Code](https://code.visualstudio.com/download?ref=ghost.org).

🚧The format for the routes.yaml file is YAML, which is ****whitespace sensitive.**** That means that precise indentation spacing is essential to the file working properly.

The default routes file for Ghost has three main sections: `routes`, `collections`, and `taxonomies`.

```
routes:

collections:
  /:
    permalink: /{slug}/
    template: index

taxonomies:
  tag: /tag/{slug}/
  author: /author/{slug}/
```



routes.yaml default configuration



In the file, you’ll find the default Ghost collection:

```
collections:
  /:
    permalink: /{slug}/
    template: index

```

This collection is defined as `/:`. It’s mapped to the permalink `/{slug}/`, which means that every post is collected on the homepage (or root) of your site, and the URL for those posts is defined by their slugs. For example, the post, “Hello World,” appears at `sitename.com/hello-world/`. The `template` option specifies the template (`index.hbs`) used to render the collection.

To create a new French cuisine collection, we add it to the file:

```
collections:
  /french/:
    permalink: /french/{slug}/
    template: index
  /:
    permalink: /{slug}/
    template: index
```

Now, any posts in the French collection will appear at `sitename.com/french/post-slug/`. And, the page, `sitename.com/french/` will use the `index.hbs` template to render the collection. Define a custom template like this:

```
collections:
  /french/:
    permalink: /french/{slug}/
    template: cuisine
```

With this change, Ghost will render the French cuisine collection with the `cuisine.hbs` template.

### **Filtering posts**

As it stands, our `routes.yaml` file is incomplete. We haven’t yet told Ghost what should be in the collection. Use the `filter` property to select certain posts based on criteria like tags, publication date, featured status, author, and [much more](https://ghost.org/docs/content-api/?ref=ghost.org#filtering).

Let's apply the filter to our collection:

```
collections:
  /french/:
    permalink: /french/{slug}/
    template: cuisine
    filter: tag:french
  /:
    permalink: /{slug}/
    template: index
    filter: tag:-[french]
```

This filter tells Ghost to collect all posts tagged `French` and place them on the `/french/` route. Inversely, it excludes all those posts from the homepage.

Repeat the process for each cuisine. Update the default collection with each cuisine to be excluded: `tag:-[french,italian]`. Upload the updated `routes.yaml` file to your Ghost site.

Now, when navigating from the homepage to a cuisine page like `yoursite.com/french/`, you'll find the custom collection of recipes.

![Custom collection of French recipes](https://ghost.org/tutorials/content/images/2022/05/collection-cuisine.jpeg)

Summary
-------

Congrats! You now know how to create a content collection in Ghost. The technique is a powerful one, not only because it can be used to create awesome custom themes, but also because anyone can use it to enhance a theme that already exists.

Beyond a recipe site, the application of custom collections in Ghost is extensive:

* create politics, sports, and art collections for a news website
* create Apple, Windows, and Android collections for a tech review website
* create city, nature, and sea collections for a travel website
* and so on...

To learn more about building collections, see our [docs on custom routing](https://ghost.org/docs/themes/routing/?ref=ghost.org) and visit us in [the Forum](https://forum.ghost.org/?ref=ghost.org), where creators and developers chat about all things Ghost.

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

[### How to add a table of contents

9 min read](/tutorials/adding-table-of-contents/)

[### Change the order of posts

3 min read](/tutorials/change-post-order/)







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









