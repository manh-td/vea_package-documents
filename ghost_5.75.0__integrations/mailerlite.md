Official Ghost + Mailerlite Integration
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
* [![ConvertKit](/images/logos/integrations/convertkit.svg)ConvertKit](/integrations/convertkit/)
* [![Drip](/images/logos/integrations/drip_hue74350adbe930e7f83945370c9f0969f_21161_50x0_resize_q100_h2_box_3.webp)Drip](/integrations/drip/)
* [![EmailOctopus](/images/logos/integrations/email-octopus_hu400ccf720817a03a4dc8ff7c2a14fdc4_2913_50x0_resize_q100_h2_box_3.webp)EmailOctopus](/integrations/emailoctopus/)
[Integrations](/integrations/)
/
[Email](/integrations/?tag=Email)

Integrate Ghost with Mailerlite to keep your members and email subscribers in sync and deliver email campaigns with ease

The most popular ways to integrate Mailerlite with Ghost are to sync your email list in Mailerlite with members in Ghost, or to embed custom email subscription or signup forms on your Ghost site.

Here’s how you can connect your Ghost publication to Mailerlite!

Import a CSV
------------

When using the members feature in Ghost, you might want to import an existing list of subscribers from your Mailerlite account to get things going. This is entirely possible using CSV exports and imports.

In your Mailerlite account, navigate to the Subscribers tab, and apply any filters necessary to locate the list of emails you’d like to import to Ghost members. Once you’re done, click **Export CSV**.

In Ghost, you can import a CSV file from the member dashboard, and the only required field is email. However, if you have additional information it’s recommended to add it now using the optional headings available. [Read more about formatting your CSV file](/help/import-members/).

Once your CSV adheres to Ghost’s import format, login to your site’s admin and click the settings icon in the members dashboard to import your file:

![](/images/integrations/import-members_hu9b731faacde4c189bfec36de74b029ce_92095_2424x0_resize_q100_h2_box_3.webp)

That’s it. All of your email subscribers have been imported as members of your Ghost site. You can now let your Mailerlite subscribers know that they can head to your website and enter their email address to access members-only content, or upgrade to a paid plan.

Sync Ghost members with MailerLite
----------------------------------

If you’re running a membership publication with Ghost, it’s possible to link this with your MailerLite account using Zapier to ensure everything stays in sync.

There’s a few common use case examples for this:

* Import new subscribers in Mailerlite as members on your Ghost site
* Send new members in Ghost to your Mailerlite email list
* Automate sending new members in Ghost automated campaigns from Mailerlite, like a welcome or onboarding series
  This saves tons of time manually updating members and email lists across your tools and ensures everything is fully in sync and secure.

Once this integration has been setup it’ll run in the background and make sure that your member lists are always up to date everywhere.

Embed an email subscription form
--------------------------------

If you’d like to use one of Mailerlite’s own subscriber forms directly, that works too! You can use absolutely any embedded forms or popup options provided by Mailerlite within Ghost.

![](/images/integrations/Mailerlite-forms-dashboard_hud5899f8c1e5d6451a0fb1e0a9f5d916e_112244_2000x0_resize_q100_h2_box_3.webp)

First you’ll need to create a new form in Mailerlite by choosing your form type, your email list and giving your form a name. Once your form has been created, Mailerlite allows you to change the design and settings, before giving you the embed code to add it to your Ghost site:

![](/images/integrations/mailerlite-embeds_hue12caad65c5816977f46a69d096037da_270858_2000x0_resize_q100_h2_box_3.webp)
### Add the form to a single post

If you just want to add the signup form to one particular post or page on your site - you can add a new HTML block within the Ghost editor and paste the embed code there. Hit publish. And you’re all set.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)
### Add the form to multiple pages of your site

On the other hand, if you’d like to add a newsletter signup form to multiple pages of your site - then you’ll need to add the embed code to your Ghost theme.

Locate the template file where you want to insert the signup form. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add the newsletter signup form after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost. The form’s now visible on every post!

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

