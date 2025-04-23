Official Ghost + ConvertKit Integration
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
* [![Drip](/images/logos/integrations/drip_hue74350adbe930e7f83945370c9f0969f_21161_50x0_resize_q100_h2_box_3.webp)Drip](/integrations/drip/)
* [![Mailerlite](/images/logos/integrations/mailerlite_hu2e914ea6740c50d99f1e8f58dff5ffd6_5009_50x0_resize_q100_h2_box_3.webp)Mailerlite](/integrations/mailerlite/)
* [![EmailOctopus](/images/logos/integrations/email-octopus_hu400ccf720817a03a4dc8ff7c2a14fdc4_2913_50x0_resize_q100_h2_box_3.webp)EmailOctopus](/integrations/emailoctopus/)
[Integrations](/integrations/)
/
[Email](/integrations/?tag=Email)

Integrate Ghost with ConvertKit to sync your subscribers and make sending your email campaigns more efficient

Whether you’re using ConvertKit to send one-off email campaigns to your readers, or running fully automated email marketing funnels - ensure your Ghost publication is fully integrated and your subscribers are in sync.

Here are some different ways you can use Ghost and ConvertKit together:

Import a CSV
------------

When using the [members feature](/features/) in Ghost, you might want to import an existing list of subscribers from your ConvertKit account to get things going. This is entirely possible using CSV exports and imports.

In your ConvertKit account, navigate to the Subscribers tab, and apply any filters necessary to locate the list of emails you’d like to import to Ghost members. Once you’re done, click **Bulk Actions** and **Export**.

In Ghost, you can import a CSV file from the member dashboard, and the only required field is `email`. However, if you have additional information it’s recommended to add it now using the optional headings available. Read more about [formatting your CSV file here](/help/import-members/#importing-a-csv).

Once your CSV adheres to Ghost’s import format, login to your site’s admin and click the settings icon in the members dashboard to import your file:

![](/images/integrations/import-members_hu9b731faacde4c189bfec36de74b029ce_92095_2424x0_resize_q100_h2_box_3.webp)

That’s it. All of your email subscribers have been imported as members of your Ghost site. You can now let your ConvertKit subscribers know that they can head to your website and enter their email address to access members-only content, or upgrade to a paid plan.

Sync Ghost members to ConvertKit
--------------------------------

If you’re running a membership publication with Ghost, it’s possible to link this with your ConvertKit account using Zapier to ensure everything stays in sync.

There’s a few common use case examples for this:

* Automatically import new ConvertKit subscribers in Ghost
* Send new members from Ghost to your ConvertKit account automatically
* Send new members in Ghost automated campaigns from ConvertKit, like a welcome or onboarding series

This saves tons of time manually updating members and email lists across your tools and ensures everything is fully in sync and secure.

Once your integration has been setup it’ll run in the background so you don’t have to worry about it again!

---

Embed custom subscription forms
-------------------------------

If you prefer to use ConvertKit’s own subscriber [forms](https://help.convertkit.com/article/244-creating-forms) directly - you can use any of the form builders, modals or other embed options provided by ConvertKit within Ghost. Once you create a new form in your ConvertKit account, you can integrate it with your Ghost site using code injection, using HTML cards or directly in your site’s theme files.

First you’ll need to create a new **signup form** from your ConvertKit account list and choose the type of form you’d like to embed:

![](/images/integrations/Create-a-form-in-convertkit_hud6ad26811e49707fd213675b45e0a3ae_52053_1640x0_resize_q100_h2_box_3.webp)

Once you have personalised the design and behaviour for your form, use the embed code to integrate the form with your Ghost site:

![](/images/integrations/HTML-embed-form-convertkit-1_hue160e08755b6ea0cb2e3dd6c47f8c164_396350_1338x0_resize_q100_h2_box_3.webp)

---

### Add the form to a single post

If you just want to add the signup form to one particular post or page on your site - you can add a new HTML block within the Ghost editor and paste the HTML embed code there. Hit publish. And you’re all set.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

---

### Add the form to multiple pages of your site

On the other hand, if you’d like to add a newsletter signup form to multiple pages of your site - then you’ll need to add the embed code to your Ghost theme.

Locate the template file where you want to insert the signup form. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add the newsletter signup form after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost. The form’s now visible on every post!

It’s also possible to use the **JavaScript embed snippet** using the site-wide code injection feature in Ghost. This is especially useful if you’re using the modal or slide in formats that ConvertKit offer, if you’d like the form to appear on every page.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

---

Setup an automated RSS email campaign
-------------------------------------

It’s also possible to use RSS feeds to setup automatically generated campaigns of the latest content on Ghost, directly to your subscribers!

Don’t forget: You can add `/rss/` to most URLs in Ghost to get a custom RSS feed. Here are some demo examples:

* **Main post index** - <https://demo.ghost.io/rss/>
* **Author archive** - <https://demo.ghost.io/author/lewis/rss/>
* **Tag archive** - <https://demo.ghost.io/tag/fiction/rss/>

![](/images/integrations/Automated-RSS-email-campaign-convertkit_hu007a53f1b9cba07c5df542dd10a0584f_365033_2000x0_resize_q100_h2_box_3.webp)

Once you’ve added your feed, you can follow the steps in ConvertKit to define how your campaigns will look, who they will be sent to and when they should be sent!

---

Do more with Zapier automation
------------------------------

Connect Drip to more of your favourite tools and align all of your processes. Zapier has lots more commonly used automations already pre-built - or you can build your own.

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

