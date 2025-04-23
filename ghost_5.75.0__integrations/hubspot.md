Official Ghost + Hubspot Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![FirstPromoter](/images/logos/integrations/firstpromoter_hu13330b4d32004712e337efa3113c94c8_6190_50x0_resize_q100_h2_box_3.webp)FirstPromoter](/integrations/firstpromoter/)
* [![CookieYes](/images/logos/integrations/cookieyes_hu2a52b95f92072c1126fd208573722580_14497_50x0_resize_q100_h2_box_3.webp)CookieYes](/integrations/cookieyes/)
* [![Search Console](/images/logos/integrations/google-search-console.svg)Search Console](/integrations/google-search-console/)
* [![Google AdSense](/images/logos/integrations/gaslogo_hu0d3b27cbc6f7330e2e6bcbec3aae3479_3987_50x0_resize_q100_h2_box_3.webp)Google AdSense](/integrations/google-adsense/)
[Integrations](/integrations/)
/
[Marketing](/integrations/?tag=Marketing)

Integrate Ghost with Hubspot for more efficient email campaigns - keep your subscribers in sync and automate RSS to email

If you’re using the Hubspot marketing software to run your email campaigns, ensure your Ghost publication is fully integrated and all of your subscribers are in sync.

Here are some popular ways you can use Ghost and Hubspot together:

Sync Ghost subscribers to Hubspot
---------------------------------

Ghost comes with a built-in [subscribers feature](/help/members-introduction/) that allows you to collect reader email addresses and it’s entirely possible to link this with your Hubspot account using Zapier. This will ensure subscribers in Ghost are always pushed into Hubspot or vice versa, saving you from the task of manual updates.

Once your integration has been setup it’ll run in the background and make sure that your subscriber lists are always up to date.

Embed custom subscription forms
-------------------------------

If you prefer to use subscriber [forms](https://knowledge.hubspot.com/articles/kcs_article/forms/create-forms) from Hubspot directly - you can use their form builder tool to create a form and embed this in Ghost using HTML cards or directly in your site’s theme files.

First you’ll need to create a new **signup form** from your Hubspot account list and customise it as necessary:

![](/images/integrations/Create-a-form-in-Hubspot_hu5407c16ed7b3e81a86bf6a30cea6ec79_130971_1308x0_resize_q100_h2_box_3.webp)

Once you have personalised the design and behaviour for your form, use the embed code to integrate the form with your Ghost site:

![](/images/integrations/Embed-a-form-Hubspot_huf4fba40843fe78ff90ff6c20b7d8e1f2_272047_1182x0_resize_q100_h2_box_3.webp)

---

### Add the form to a single post

If you just want to add the signup form to one particular post or page on your site - you can add a new HTML block within the Ghost editor and paste the HTML embed code there. Hit publish. And you’re all set.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

---

### Add the form to multiple pages of your site

If you’d like to add a newsletter signup form to multiple pages of your site, then you’ll need to add the embed code to your Ghost theme.

Locate the template file where you want to insert the signup form. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add the newsletter signup form after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost. The form’s now visible on every post!

Setup an automated RSS email campaign
-------------------------------------

It’s also possible to use RSS feeds to setup automatically generated campaigns of the latest content on Ghost, directly to your subscribers!

In Hubspot your subscribers are able to manage their own subscriptions and decide which emails to receive, so you’ll need to [create a custom property](https://knowledge.hubspot.com/articles/kcs_article/cos-blog/set-up-an-rss-to-email-blog-subscription-for-an-external-blog) and an active subscription form tied to an email list specifically for your RSS email campaign.

Once this is complete, you can build a new email using a URL to automate the population of your content from Ghost. Don’t forget: You can add `/rss/` to most URLs in Ghost to get a custom RSS feed. Here are some demo examples:

* **Main post index** - <https://demo.ghost.io/rss/>
* **Author archive** - <https://demo.ghost.io/author/lewis/rss/>
* **Tag archive** - <https://demo.ghost.io/tag/fiction/rss/>

Once you’ve customised your email in the editor, you can schedule the email as a one-off or a recurring newsletter of your latest content.

Do more with Zapier automation
------------------------------

Connect Hubspot to more of your favourite tools and align all of your processes. Zapier has lots more commonly used automations already pre-built - or you can build your own.

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

