Official Ghost + Custom RSS Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Zapier](/images/logos/integrations/zapier_hu76c04ccfd9407fb306e44c2572d39c65_1450_50x0_resize_q100_h2_box_3.webp)Zapier](/integrations/zapier/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Netlify](/images/logos/integrations/netlify_hu1b4209e1158b533f7cea6d5e486e460d_36182_50x0_resize_q100_h2_box_3.webp)Netlify](/integrations/netlify/)
* [![GitHub](/images/logos/integrations/github.svg)GitHub](/integrations/github/)
* [![FirstPromoter](/images/logos/integrations/firstpromoter_hu13330b4d32004712e337efa3113c94c8_6190_50x0_resize_q100_h2_box_3.webp)FirstPromoter](/integrations/firstpromoter/)
[Integrations](/integrations/)
/
[Marketing](/integrations/?tag=Marketing)

Create custom RSS feeds for your publication using the flexible dynamic routing layer in Ghost and Handlebars templates

Adding `/rss/` to most URLs in Ghost produces an automatically generated `rss` feed, for example:

* **Main post index** - <https://demo.ghost.io/rss/>
* **Author archive** - <https://demo.ghost.io/author/lewis/rss/>
* **Tag archive** - <https://demo.ghost.io/tag/fiction/rss/>

Automatic `rss` feeds save time, and allow external applications to access an up-to-date feed of your content. However, when the default implementation of `rss` feeds in Ghost doesn’t suit your requirements, you can create custom feeds using the dynamic routing layer and a Handlebars template.

Here’s an example of how to create a custom `rss` feed for a specific route on a Ghost publication:

Add an `rss` route in `routes.yaml`:
------------------------------------

In order to create a custom `rss` feed you’ll need to add a new route, which is the URL where your feed will appear.

Download the latest version of the `routes.yaml` file from Ghost Admin and open it in any code editor:

![](/images/integrations/Download-routes_hud3b9157eddb0812a49b48bb078b78484_22187_1946x0_resize_q100_h2_box_3.webp)

Under routes add the URL where your new custom `rss` feed will exist, for example:

```
routes:
  /news/rss/:
    template: news/rss
    content_type: text/xml

```

Custom `rss` feeds need to be defined with the `content_type` property and mapped to a template as shown in the example above.

Create an new template
----------------------

The next step is to create a custom template in your theme. Following the example above, create a new template with the file name: `news/rss.hbs`. Here’s a code example of what a custom `rss` template can look like:

```
<rss xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:content="http://purl.org/rss/1.0/modules/content/" xmlns:atom="http://www.w3.org/2005/Atom" xmlns:media="http://search.yahoo.com/mrss/" version="2.0">
<channel>
<title><![CDATA[ {{@site.title}} ]]></title>
<description><![CDATA[ {{@site.description}} ]]></description>
<link>{{@site.url}}</link>
<image>
    <url>{{@site.url}}/favicon.png</url>
    <title>{{@site.title}}</title>
    <link>{{@site.url}}</link>
</image>
<lastBuildDate>{{date format="ddd, DD MMM YYYY HH:mm:ss ZZ"}}</lastBuildDate>
<atom:link href="{{@site.url}}" rel="self" type="application/rss+xml"/>
<ttl>60</ttl>
{{#get "posts" limit="all" include="authors,tags"}}
    {{#foreach posts}}
    <item>
        <title><![CDATA[ {{title}} ]]></title>
        <description><![CDATA[ {{excerpt}} ]]></description>
        <link>{{url absolute="true"}}</link>
        <guid isPermaLink="false">{{id}}</guid>
        <category><![CDATA[ {{primary_tag.name}} ]]></category>
        <dc:creator><![CDATA[ {{primary_author.name}} ]]></dc:creator>
        <pubDate>{{date format="ddd, DD MMM YYYY HH:mm:ss ZZ"}}</pubDate>
        <media:content url="{{feature_image}}" medium="image"/>
        <content:encoded><![CDATA[ {{content}} ]]></content:encoded>
    </item>
    {{/foreach}}
{{/get}}
</channel>
</rss>

```

You can copy and paste this exact implementation for your site, then go ahead and customise it to suit your needs!

Update your active theme and `routes.yaml`
------------------------------------------

Once you’ve saved your changes, upload your updated theme in Ghost Admin as a `.zip` file and upload your new `routes.yaml` file. That’s it, you’ve successfully created a custom RSS feed - you can test it out for yourself using the feed’s URL!

Advanced RSS feeds for podcasting
---------------------------------

If you’re looking for a more detailed examples specifically for generating an iTunes compatible podcast RSS feed, make sure you check out our [in-depth podcast feed tutorial](/tutorials/custom-rss-feed) for Ghost, which builds on the things covered here!

Do more with Zapier
-------------------

As always, you can power up your site even further using [Zapier](https://zapier.com). Check out some of these powerful RSS automations:

Launch your site
----------------

Last week, 5,069 brand new  
publications got started with Ghost.

Today, it's your turn.

[Start a free trial now →](https://account.ghost.org/signup/)Product

* [Creator platform](/)
* [Theme marketplace](/marketplace/)
* [Integrations](/integrations/)
* [Experts](/experts/)
* [Ghost for news](/news/)
Developers

* [How to install Ghost](/docs/install/)
* [Core concepts](/docs/)
* [Ghost hosting](/pricing/)
* [API documentation](/docs/content-api/)
* [Security overview](/docs/security/)
* [Source code](https://github.com/TryGhost/Ghost)
Resources

* [Ghost tutorials](/tutorials/)
* [Resources](/resources/)
* [Node.js CMS guide](https://nodecms.guide)
* [Open Subscription Platforms](https://opensubscriptionplatforms.com)
Comparisons

* [Ghost vs Substack](/vs/substack/)
* [Ghost vs WordPress](/vs/wordpress/)
* [Ghost vs Medium](/vs/medium/)
* [Ghost vs Memberful](/vs/memberful/)
* [Ghost vs Patreon](/vs/patreon/)
* [Ghost alternatives →](/alternatives/)
Support

* [Help center](/help/)
* [Community forum](https://forum.ghost.org/)
* [Status  
  Triangle
  
  
  
   99.9%](https://status.ghost.org/)
[![Non-Profit Foundation](/images/logos/indie.svg)](/about/)
[![Open Source](/images/logos/opensource.svg)](https://github.com/tryghost)
[![Carbon Neutral](/images/logos/carbonneutral.svg)](https://climate.stripe.com/6MNofu)

