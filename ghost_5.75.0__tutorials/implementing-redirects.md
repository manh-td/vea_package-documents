





Implementing redirects in Ghost









































---


Redirects forward one URL to another. They are commonly used when removing or moving content on your site, fixing broken links, or migrating content between different domains.

In Ghost, redirects are configured by adding rules to the `redirects.yaml` file. The basic process is to download this file from Ghost Admin, edit the file in a code editor, and then re-upload it to the admin interface.

This tutorial will walk you through:

* When not to use the `redirects.yaml` file 🙃
* Accessing the `redirects.yaml` file and its basic structure
* How to create your redirects with common examples for reference
* Implementing your new redirects
* Some tips for getting started with regular expressions

**When not to use redirects.yaml**
----------------------------------

Before we get started, make sure you are not trying to implement some common patterns where it is not necessary or advised to use the `redirects.yaml` file:

* Page rules for www or HTTP/HTTPS redirection should always be implemented with your DNS provider.
* Ghost automatically forces trailing slashes, so you do not need to write any page rules to accommodate for duplicate content caused by this.
* Use [dynamic routing](https://ghost.org/docs/tutorials/creating-content-collections/?ref=ghost.org) to change the URL structure of your publication, for example, to change `/tag/` to `/topic/`.

**Accessing the redirect file in Ghost**
----------------------------------------

If you're creating redirects for the first time, create a file called `redirects.yaml` in your code editor. Upload (and download) the `redirects.yaml` file from Ghost Admin (**Settings** → **Labs**).

![Ghost Admin page with Redirects area highlighted](https://ghost.org/tutorials/content/images/2024/04/redirects-in-admin.png)💡Older versions of Ghost used the JSON format for redirects. While these redirects will still work, it's recommended to use YAML when writing any new redirects. 
### **File structure**

`redirects.yaml` has two keys: `301` and `302`. Each key contains a list of redirects. The `301` key contains the permanent 301 redirects. The `302` key contains the temporary 302 redirects. A new Ghost publication has no redirects by default.

Entries to the redirects file follow this structure:

```
301:
  /permanent-redirect-from: /permanent-redirect-to
  /permanent-redirect-from-2: /permanent-redirect-to-2

302:
  /temporary-redirect-from: /temporary-redirect-to

```

Enter multiple entries on separate lines. Redirecting to external URLs is possible. It's also possible to use regular expressions.

**Creating redirects in `redirects.yaml`**
------------------------------------------

Create redirects by listing the source URL and the destination URL, separated by a colon.

The following examples demonstrate common use cases for redirects in Ghost.

### **⚡️ Redirect an old URL to a new one**

If you update or remove a URL, it's best practice to redirect it. This prevents broken links and your visitors from landing on error pages. It also informs search engines that a page has changed, which benefits your site's SEO.

For example, to redirect `domain.com/old-postname/` to `domain.com/new-postname/`, include the following in `redirects.yaml`:

```
301:
  /old-postname/: /new-postame/

```
### **⚡️ Redirect your post structure from an existing domain**

Redirects are a good option if you're migrating content from an existing site that uses a different post structure than Ghost uses.

Here are some common examples of restructuring a Ghost publication:

**Category to tag**

```
301:
  /category/category-slug/: /tag/tag-slug/
```

**Date to post name**

```
301:
  /blog/year/month/day/post-slug/: /post-slug/
```

**Search labels**

```
301:
  /search/label/: /tag/tag-name
```

With these redirects, someone following an old link will still end up in the right place because they'll be redirected to the new content.

### **⚡️ Fixing URL discrepancies**

As a site grows, content can be duplicated and URLs can change. Consolidate multiple versions of the same URL with redirects. In the example below, we redirect the old URLs `editing-a-post` and `editing-posts` to `editing`, the new one.

```
301:
  /editing-a-post: /editing
  /editing-posts: /editing
```

**Implementing redirects in Ghost**
-----------------------------------

Once you have created your redirects by editing your `redirects.yaml` file, upload it in Ghost Admin.

Once the file is in place, test your redirects by visiting any URL you redirected. Using the example above, visiting `/editing-posts` will take you to `/editing` in the browser.

**Using regular expressions**
-----------------------------

Use regular expressions (or regex) to write redirects with advanced pattern matching.

A common use case is migrating content from a platform with a different URL structure. For example, let's say posts used to live on `/blog/post-slug` but now in Ghost live at `/posts-slug`. While it's possible to write each redirect on a new line, we can use regular expressions to match all possibilities in one line.

```
301:
  /blog/post-1: /post-1
  /blog/post-2: /post-2
  /blog/post-3: /post-3
```



Individual redirects



```
301:
  ^\/blog\/([a-z0-9-]+)\/$: /$1
```



Redirect with regex



The regex matches what comes after `/blog/` like `post-1` and redirects to it (`$1` represents the match). With this in place, you can redirect all existing URLs without writing them out one by one.

As powerful as regex are, writing them is a bit of an art. The best resource to assist with designing regular expressions for a wide variety of use cases is [regex101](https://regex101.com/?ref=ghost.org). Use this tool to test out your redirect regular expressions. Not only does this tool show if you're pattern works, but it'll also explain how it works. (Be sure to choose ECMAScript/JavaScript as the flavor.)

Common Redirects
----------------

When migrating from other platforms to Ghost, it's common to need redirects that cover a lot of older URLs. We can use regular expressions, we can create redirects that redirect any URL that matches the pattern provided.

### WordPress

Convert `/category/slug/` URLs to `/tag/slug/`

```
301:
    ^\/category\/(.*): /tag/$1
```

Convert `/yyyy/mm/dd/slug/` to `/slug/`

```
301:
    ^\/[0-9]{4}\/[0-9]{2}\/[0-9]{2}\/(.*): /$1
```

Convert `/yyyy/mm/slug/` to `/slug/`

```
301:
    ^\/[0-9]{4}\/[0-9]{2}\/(.*): /$1
```
### Squarespace

Convert `/category/slug/` URLs to `/tag/slug/`

```
301:
    ^\/category\/(.*): /tag/$1
```

Convert `/blog/slug/` to `/slug/`

```
301:
    ^\/blog\/(\S+): /$1
```
### Substack

If you had a custom domain on Substack, you will need to handle the `/p/` from backlinks. This removes that but does not affect preview links from Ghost, which also start with `/p/`.

```
301:
    \/p\/(?![0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12})(.*): /$1
    ^\/subscribe\/?$: /#/portal/subscribe
```
### Medium

If you had a custom domain on Medium, you'll need to remove the ID appended to the post slug.

```
301:
    ^\/(?!p\/)(.*)(-[0-9a-f]{10,12}): /$1
```

Remove redirects
----------------

To remove redirects that aren't working as expected, upload an empty `redirects.yaml` file like in the example below.

```
301:

302:
```

This will remove all existing redirects on your site.

**Summary**
-----------

That’s it. You have discovered the recommended process for implementing redirects in Ghost:

1. Create a `redirects.yaml` file or download it from Ghost Admin
2. Edit the file to add new redirection rules
3. Upload the file in Ghost Admin

This process can be repeated as often as required. All of your redirects will always be stored in one accessible place and are always managed and owned by you.

Have questions about more complex redirects or want to show off some crazy regex you wrote? Come on over [to our Forum](https://forum.ghost.org/?ref=ghost.org) and have a chat.

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









