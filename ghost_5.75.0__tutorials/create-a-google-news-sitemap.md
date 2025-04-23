





Add your Ghost site to Google News









































---


Add your content to Google News by adding a [Google News sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/news-sitemap?ref=ghost.org) to your Ghost site. The sitemap lets Google News know all the important details about your published content.

This tutorial walks you through how to create a Google News sitemap by implementing a new route on your Ghost site and by creating a custom template that is fully optimized for the Google News aggregator.

Add a new route for your sitemap
--------------------------------

To make your sitemap accessible on the web, add a new route using Ghost's dynamic routing layer.

Download the most up-to-date version of your `routes.yaml` file from Ghost Admin. Go to **Settings** → **Labs** → **Download current routes.yaml**. Open the file in your [code editor](https://ghost.org/tutorials/open-a-theme-in-a-code-editor/) of choice.

![Ghost Admin, upload and download custom routing](https://ghost.org/tutorials/content/images/2022/10/CleanShot-2022-10-25-at-16.08.17.png)

Add the following route:

```
routes:
  /sitemap/:
    template: sitemap
    content_type: text/xml
```

This entry tells Ghost to create a route at `yoursite.com/sitemap/`, and on that route, to serve the `sitemap` template file and send an XML response (which is what Google News expects).

Your `routes.yaml` file should now look like the file below, plus any other changes you may have made to it.

```
routes:
  /sitemap/:
    template: sitemap
    content_type: text/xml

collections:
  /:
    permalink: /{slug}/
    template: index

taxonomies:
  tag: /tag/{slug}/
  author: /author/{slug}/
```

Save the file and upload it to Ghost Admin (**Settings** → **Labs** → **Upload routes YAML**).

Create a template for the Google News sitemap
---------------------------------------------

The next step is to create a Handlebars template in your theme. This requires a little bit of coding, but the example in this tutorial provides a fully functional starting point.

Create a new file in the root of your theme called `sitemap.hbs`.

### Add your posts

The code below tells Ghost to fetch your latest 1,000 posts created in the last two days and format the information for Google News. The template follows [the specifications for a Google News sitemap](https://www.google.com/schemas/sitemap-news/0.9/sitemap-news.xsd?ref=ghost.org) like including the title and publication date as well as indicating if the content is for members only.

```
<?xml version="1.0" encoding="UTF-8"?>
  <urlset
    xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
    xmlns:news="http://www.google.com/schemas/sitemap-news/0.9"
  >
    {{#get "posts" filter="published_at:>now-2d" limit="1000" include="tags"}}
      {{#foreach posts}}
        <url>
          <loc>{{url absolute="true"}}</loc>
          <news:news>
            <news:publication>
              <news:name>{{@site.title}}</news:name>
              <news:language>{{@site.locale}}</news:language>
            </news:publication>
            {{#has visibility="members"}}
            <news:access>Registration</news:access>
            {{/has}}
            {{#has visibility="paid"}}
            <news:access>Subscription</news:access>
            {{/has}}
            <news:publication_date>{{date published_at format="YYYY-MM-DDTHH:mm:ssZ"}}</news:publication_date>
            <news:title>{{title}}</news:title>
            <news:keywords>{{tags limit="5" autolink="false"}}</news:keywords>
          </news:news>
        </url>
      {{/foreach}}
    {{/get}}
  </urlset>
```

Copy and paste this code to the `sitemap.hbs` file or customize it to suit your needs. With customization, be aware that Google is stringent about attributes and formatting, so be sure [to include all required fields](https://developers.google.com/search/docs/crawling-indexing/sitemaps/news-sitemap?ref=ghost.org#news-specific-tag-definitions).

Update your theme
-----------------

Save the new template, zip up your theme, and [upload it to your Ghost site](https://ghost.org/tutorials/download-and-upload-a-theme/). Check to see if your Google News sitemap is active by visiting `yoursite.com/sitemap/`. (We added a sitemap to this Tutorials site as an example: <https://ghost.org/tutorials/sitemap/>. Note that if no tutorials have been published in the past two days, the sitemap will be empty.)

![Google News sitemap example](https://ghost.org/tutorials/content/images/2022/10/google-news.png)

Submit your Google News sitemap
-------------------------------

Google Search Console is essential for monitoring your search performance in Google. [See our guide on integrating it with Ghost](https://ghost.org/integrations/google-search-console/?ref=ghost.org). It's also the best way to let Google know about your new Google News sitemap.

In Google Search Console, go to Sitemaps and add your new URL to the **Add a new sitemap** box. Click **Submit**. The sitemap should be fetched immediately, but occasionally it can take some time for Google to crawl the URLs listed in it. A successful status indicates that Google has indexed all of your links submitted to Google News. That means your content is available to show up on Google News 📰

Customize how your publication shows up in Google News by configuring it through Google's [Publisher Center](https://publishercenter.google.com/?ref=ghost.org). Via the Publisher Center, you get advanced control over content and branding, monetization opportunities, and additional placement eligibility.

Summary
-------

In this tutorial, you used Ghost's routing system and theme layer to create a custom Google News sitemap 🙌

Creating the sitemap helps your content show up in Google News, but Google also provides several other options for customization, monetization, and improved placement. See [Google's guide](https://support.google.com/news/publisher-center/answer/9607025?hl=en&ref=ghost.org) to learn more.

Having trouble with this tutorial or seeing great success with your new Google News sitemap? Come share your experience in the [official Ghost Forum](https://forum.ghost.org/?ref=ghost.org), where developers, publishers, and content creators come together to discuss all things Ghost.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### How to debug your theme

8 min read](/tutorials/debug/)

[### Change the URL for tags and authors

1 min read](/tutorials/change-taxonomy-url/)

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









