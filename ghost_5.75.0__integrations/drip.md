Official Ghost + Drip Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Mailchimp](/images/logos/integrations/mailchimp_hucb75d06be88e6331905252c3cff4ebbc_32058_50x0_resize_q100_h2_box_3.webp)Mailchimp](/integrations/mailchimp/)
* [![FirstPromoter](/images/logos/integrations/firstpromoter_hu13330b4d32004712e337efa3113c94c8_6190_50x0_resize_q100_h2_box_3.webp)FirstPromoter](/integrations/firstpromoter/)
* [![CookieYes](/images/logos/integrations/cookieyes_hu2a52b95f92072c1126fd208573722580_14497_50x0_resize_q100_h2_box_3.webp)CookieYes](/integrations/cookieyes/)
* [![ConvertKit](/images/logos/integrations/convertkit.svg)ConvertKit](/integrations/convertkit/)
[Integrations](/integrations/)
/
[Email](/integrations/?tag=Email)

Give your email campaigns a boost and integrate Ghost with Drip – sync subscribers and deliver email campaigns efficiently

The most popular ways to integrate Drip with Ghost are to sync your email subscribers, embedding custom email subscription or signup forms and creating an RSS driven newsletter.

Let’s take a look at a few of the different ways you can use Ghost with Drip to automate and improve your email campaigns:

Sync Ghost members with Drip
----------------------------

When collecting reader email addresses using the built-in [members feature](/help/members-introduction/) in Ghost, it’s possible to sync these email addresses with your Drip account using [Zapier](https://zapier.com/). This ensures members in Ghost are always pushed to Drip or vice versa and keeps everything in sync, saving you the time of doing manual updates.

Once this integration has been setup it’ll run in the background and make sure that your lists are always up to date everywhere.

Embed Drip email subscription forms
-----------------------------------

If you prefer to use Drip’s own subscriber forms directly, it’s possible to use any of the form builders, widgets or other embed options within Ghost. They can all be enabled or embedded efficiently using code injection or HTML cards in the editor.

First you’ll need to create a new **signup form** in your Drip account:

![](/images/integrations/Create-a-signup-form-in-Drip_hu0d7dec2db147384c0efbd3f27c0e755e_277227_1908x0_resize_q100_h2_box_3.webp)

Each form you create has a unique reference name and can be configured individually, with the option to use the embed code to inject raw un-styled forms in HTML, or the widget popup forms across your site.

---

### Embed an HTML form on a single post

To use HTML embedded forms, locate the embed code from within the form editor in your Drip account:

![](/images/integrations/Drip-embed-form-code_hu92632a923f7016f501ace261df471893_125706_1922x0_resize_q100_h2_box_3.webp)

To add the signup form to a particular post or page on your site, add a new HTML block within the Ghost editor and paste the embed code there.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

Once you hit publish, an un-styled (but functional) form will appear on your post or page. To add your own styling to this form, edit the CSS in your theme files and update your theme in Ghost Admin.

---

### Embed an HTML form across multiple pages

On the other hand, if you’d like to add a newsletter signup form to multiple pages of your site - then you’ll need to add the embed code to your Ghost theme.

Locate the template file where you want to insert the signup form. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add the newsletter signup form after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost. The form’s now visible on every post!

---

### Use the widget form on multiple pages of your site

If you’d like to use the Drip widget forms on various parts of your site, go to your account settings in Drip and copy and paste the Javascript snippet in the site setup menu:

![](/images/integrations/Drip-site-code-snippet_hub8b44da41739d99bedafc81f75115b78_165124_1744x0_resize_q100_h2_box_3.webp)

This snippet can be pasted into the site-wide code injection in Ghost Admin if you’d like to implement the widget across your site. Additionally, Drip allows you to specify which URLs the widget will appear on in the form editor for more fine-grained control.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

Setup an RSS to Email campaign
------------------------------

It’s also possible to use the Drip [RSS-to-Email](https://help.drip.com/hc/en-us/articles/115003731671-RSS-to-Email) feature to generate automated newsletters of your latest content on Ghost, directly to your subscribers!

Once you’ve activated the feature, wire up the RSS feed which you’d like to use to populate your newsletter content. Don’t forget: You can add `/rss/` to most URLs in Ghost to get a custom RSS feed. Here are some demo examples:

* **Main post index** - <https://demo.ghost.io/rss/>
* **Author archive** - <https://demo.ghost.io/author/lewis/rss/>
* **Tag archive** - <https://demo.ghost.io/tag/fiction/rss/>

Do more with Zapier automation
------------------------------

Connect Drip to many more of your favourite tools and align all of your processes using Zapier. Get started with lots of commonly used Zaps already pre-built, or if you can’t find what you’re looking for you can build your own:

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

