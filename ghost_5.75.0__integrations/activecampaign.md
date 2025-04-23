Official Ghost + ActiveCampaign Integration
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

Integrate Ghost with ActiveCampaign to sync your subscribers and embed custom subscription forms to grow your email list.

Whether you’re using ActiveCampaign to send one-off email campaigns to your readers, or running fully automated email marketing funnels - ensure your Ghost publication is fully integrated and your subscribers are in sync.

Here are some different ways you can use Ghost and ActiveCampaign together:

Sync Ghost members to ActiveCampaign
------------------------------------

If you’re collecting your visitors email addresses using the built-in [members feature](/help/members-introduction/) in Ghost, it’s possible to link this with your ActiveCampaign account using Zapier to ensure members in Ghost are always pushed into ActiveCampaign, or vice versa.

This saves lots of time updating email lists, and ensures your list is fully synchronised between the two different systems.

Once this integration has been setup it’ll run in the background and make sure that your members and subscriber lists are always up to date.

---

Embed an email subscription form
--------------------------------

If you’d rather use ActiveCampaign’s own forms directly, that’s fine too! You can use *any* form, bar, box or modal code provided by ActiveCampaign within Ghost.

First you’ll need to create a new **signup form** for your ActiveCampaign list. select the options you’d like to use, and copy the code provided. You can use either the `Simple Embed` or the `Full Embed` - they both do the same thing, but the Full Embed allows you to customise the code if you want to.

![](/images/integrations/activecampaign-form_hu570a07bf5ec095d9447e28a32b55f7a5_128254_1420x0_resize_q100_h2_box_3.webp)

---

### Add the form to a single post

If you just want to add the signup form to one particular post or page on your site - you can add a new HTML block within the Ghost editor and paste the embed code there. Hit publish. And you’re all set.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

---

### Add the form to multiple pages of your site

On the other hand, if you’d like to add a newsletter signup form to multiple pages of your site - then you’ll need to add the embed code to your Ghost theme.

Locate the template file where you want to insert the signup form. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add the newsletter signup form after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost. The form’s now visible on every post!

---

Setup an RSS to Email campaign
------------------------------

It’s also possible to use the ActiveCampaign [RSS-to-Email](https://help.activecampaign.com/hc/en-us/articles/206641310-RSS-and-email-marketing) feature to generate automated newsletters of your latest content on Ghost, directly to your subscribers! To do this, create a new **RSS Triggered** campaign:

![](/images/integrations/activecampaign-rss-triggered_hu3e571c8254ca43e8b16f87dab0dbf867_99572_1842x0_resize_q100_h2_box_3.webp)

Once you’ve selected the list options you’d like to use and you reach the design stage, insert an **RSS Feed** block into your newsletter template:

![](/images/integrations/activecampaign-rss-feed_hu4bb6ff5dc22ef76bc01c3feb0ba65d80_18709_1016x0_resize_q100_h2_box_3.webp)

Then select the RSS feed you’d like to use in your newsletter. Don’t forget: You can add `/rss/` to most URLs in Ghost to get a custom RSS feed. Here are some demo examples:

* **Main post index** - <https://demo.ghost.io/rss/>
* **Author archive** - <https://demo.ghost.io/author/lewis/rss/>
* **Tag archive** - <https://demo.ghost.io/tag/fiction/rss/>

![](/images/integrations/activecampaign-feed-builder_hu75d08296bb844f1599e4fe4822494df2_80672_1290x0_resize_q100_h2_box_3.webp)

Once everything is configured you’ll see your RSS feed appearing within your newsletter template. From here you can finish up your design, and set the schedule for how often you’d like your campaign to check the RSS feed for new items and send to your subscribers.

![](/images/integrations/activecampaign-weekly-newsletter_hub99fd748726a5cdf9937b0e4402e5788_105564_1416x0_resize_q100_h2_box_3.webp)

---

Do more with Zapier automation
------------------------------

You can connect ActiveCampaign to more of your favourite tools using Zapier, with lots of commonly used Zaps already pre-built. Here are some examples!

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

