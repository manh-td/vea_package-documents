


New custom canonical URLs feature – Ghost Blog












































You can now implement custom canonical links directly in the Ghost editor for guest posts, multiple versions of the same page or when you need to curate a list of links to external sources

A canonical URL allows you to tell search engines what the preferred URL is for content that can be found on multiple URLs, or even multiple websites. It's a common technique used for SEO that is implemented with the `rel="canonical"` attribute in the `<head>` of any page on your site.

When you create new content on a Ghost publication, a self-referencing canonical URL that points towards your new post as the preferred version is automatically applied by default. Now we've introduced a new feature that allows you to override this completely and implement custom canonicalisation from within the editor.

Using custom canonicals in Ghost
--------------------------------

When authoring any post or page, you can access the custom canonical URL feature from within the meta data area of the post settings menu:

![](https://ghost.org/changelog/content/images/2019/03/Custom-canonical.png)

It's also possible to use the canonical URL feature via our APIs using the `"canonical_url":` field.

When to use the custom canonical feature
----------------------------------------

The primary reason to use a custom canonical is to ensure that the search engines know which page to index, rank and display in the results pages when there are several active versions of similar content on any domain.

Here's a handy in-depth [overview from Moz](https://moz.com/blog/rel-canonical?ref=ghost.org) about when and how to use canonicals. As a rule of thumb, when you're removing or moving content, a 301 redirect is required. When you're dealing with multiple versions, a rel="canonical" is required.

Here's some example use cases of a custom canonical:

### Guest posts

![](https://ghost.org/changelog/content/images/2019/03/Syndicating-Content.jpg)

One of the most common use cases of a custom canonical is when you'd like to publish guest content on your site that has already been posted by the author on another site.

It's now possible to syndicate an authors existing content (with permission, of course) and publish it on your Ghost site with a custom canonical that points to the original published version. All you need to do is add the full URL including `https://` to the new canonical URL field in post settings.

### Multiple versions of the same pages

![](https://ghost.org/changelog/content/images/2019/03/Multiple-Versions.jpg)

When you have multiple versions of content is identical, or near-identical, you’ll need to implement a custom canonical on each page that specifies the preferred version.

Examples of circumstances where you might have multiple versions include: Running A/B tests, multiple pages for tracking purposes, similar pages targeting slightly different audiences or multiple pages for paid advertising campaigns.

These are pages that you would like visitors to be able to access, without confusing the search engines and hindering your SEO.

### Curated lists to external sources

![](https://ghost.org/changelog/content/images/2019/03/What-we-re-reading.jpg)

If you’d like to build a curated list of links, you can use the canonical feature for this too. For example, you could create something similar to the **What We’re Reading** list on [NiemanLab](https://www.niemanlab.org/?ref=ghost.org):

![](https://ghost.org/changelog/content/images/2019/03/NiemanLab-curated-list-of-links.png)

*NiemanLab's curated list of top stories from external sources*

This can be created using the `{{get}}` helper to fetch content from Ghost, and the `{{canonical_url}}` instead of `{{url}}` to link to the original source.

```
{{#get "posts" filter="primary_tag:link"}}
    {{#foreach posts}}
        <div class="post">
            <a href="{{canonical_url}}">{{title}}</a>
            <p>{{excerpt}}</p>
        </div>
    {{/foreach}}
{{/get}}

```

Optimise your site with built-in SEO
------------------------------------

Ghost always implements automatic canonicals on *every* page of your site when you're not using the custom canonical URL feature. This ensures your SEO is clean and prevents any URLs with tracking parameters from being indexed.

As for the rest of your SEO optimisation, with Ghost much of it happens in the background without any extra effort, plugins or downloads. This includes detailed structured data ([Schema.org](https://schema.org/?ref=ghost.org)), automatically generated XML sitemaps, permalinks, AMP and semantic markup. Leaving you with more time to focus on nailing your custom meta data for Google, Facebook and Twitter 👩‍💻

---

****************Ghost(Pro)**************** users have already been updated and have access to custom canonicals. Self hosted developers can use [Ghost-CLI](https://ghost.org/docs/ghost-cli/?ref=ghost.org) to get this feature by running `$ ghost update` to install the [latest release](https://github.com/TryGhost/ghost/releases?ref=ghost.org).

### Get notified when we ship new features.






 
### You might also like...

Apr

08


![Custom content for every subscriber](/changelog/content/images/size/w750/2025/04/Ghost-Call-to-action-card.png)

Custom content for every subscriber
-----------------------------------

Calls to Action got an upgrade, now you can fine-tune the design and who sees them in more detail.
Apr 8, 2025


New





 
Apr

01


![Social web (beta)](/changelog/content/images/size/w750/2025/04/image--1-.png)

Social web (beta)
-----------------

Increase your reach by connecting your publication to the Fediverse
Apr 1, 2025


Beta





 





 
















 






