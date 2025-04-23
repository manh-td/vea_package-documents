





Change the order of posts in Ghost









































---


By default, Ghost displays posts on index pages in reverse chronological order – that’s newest to oldest. In this tutorial, we’ll find out how to edit your `routes.yaml` to customize the order your posts, including reverse order, by title, and more.  


Download `routes.yaml`
----------------------

The first step is to download your `routes.yaml` file from **Settings** → **Labs** → **Routes** → **Download current routes.yaml**.

![Download prompt in Ghost admin](https://ghost.org/tutorials/content/images/2022/05/routes.png)

Open the file in your code editor.

Define a custom route
---------------------

Imagine we have a movie review website, where we publish reviews on the date that the movie is released. By default, Ghost will list our posts from the most recently published to the oldest.

![Movies like Joker and Parasite showin in chronological order](https://ghost.org/tutorials/content/images/2022/05/movies-default.png)
### Reversing the order

But let’s say we wanted to reverse the order and display the oldest movies first. You only need to add one line to your `routes.yaml` file. In the example below, we’ve created a custom route called `/movies/` that loads our posts using the `channel` controller. (For more on creating channels and collections, see our guide.) The `order` property takes two parameters: the field you want to order by and the order direction: `asc` for ascending and `desc` for descending.

```
routes:
  /movies/:
      controller: channel
      order: published_at asc

```

Save your changes and upload your changes to Ghost. Navigate to `/movies/` and refresh. All posts will now be listed in ascending chronological order, from oldest to newest.

![Movies show in reverse order, from oldest to newest](https://ghost.org/tutorials/content/images/2022/05/movies_reverse.png)
### Beyond `published_at`

What if we wanted to have a page on our site where movies would be listed alphabetically by their titles, rather than publication date. Again, it’s just one easy change to the `routes.yaml` file.

```
routes:
  /movies/:
      controller: channel
      order: title asc

```
![Movies in alphabetical order](https://ghost.org/tutorials/content/images/2022/05/movies_a-to-z.png)

Movies now appear in alphabetical order. If you have a review website with products and you want to create a page where those products are listed in alphabetical order, then using this technique is a quick, easy solution.

### Combine `order` with `filter`

Additionally, you can add the `filter` property to limit your results. To create page that only featured movies from the ‘80s, we could add the following `filter` that loads at `/movies/80s/`. (This works because the publication date matches the movie’s release date.)

```
routes:
  /movies/80s/:
    controller: channel
      order: title asc
      filter: published_at:>1979-12-31+published_at:<1990-01-01 
```
![Now it's movies from the 80s like Back to the Future and Die Hard](https://ghost.org/tutorials/content/images/2022/05/movies_80s.png)
### More than one order

One last neat option is the ability to define multiple orders. The most common use case is where you want to return featured posts first, followed by the remaining posts. In our case, we’ll imagine you have two reviews that we want to feature followed by the remaining ones. We’d update `routes.yaml` like this:

```
routes:
  /movies/:
  controller: channel
  order: featured desc, published_at desc

```
![Featured movies are at the top, movies sorted by release date follow](https://ghost.org/tutorials/content/images/2022/05/movies_featured.png)

Now, our featured reviews of *Joker* and *Ford v Ferrari* are displayed first with custom styling, followed by the remaining posts in chronological order.

Summary
-------

In this tutorial, we provided a glimpse of what you can do with the `order` property on custom routes. Whether it’s reversing the order of posts, changing the field that they’re sorted by, or building complex groups of posts – the possibilities are endless!

Have you used custom routes in an interesting way or looking for more examples? Come join us and the Ghost community [on our Forum](https://forum.ghost.org/?ref=ghost.org). It’s a great place to make connections and get inspired.

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









