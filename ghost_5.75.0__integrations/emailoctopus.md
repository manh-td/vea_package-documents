Official Ghost + EmailOctopus Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![ChartMogul](/images/logos/integrations/chartmogul_hu01c73d47915043033a3a07dcbb830fa7_3078_50x0_resize_q100_h2_box_3.webp)ChartMogul](/integrations/chartmogul/)
* [![Churnbuster](/images/logos/integrations/churnbuster_hudae337c0f674707d1840f4c514d865a7_15531_50x0_resize_q100_h2_box_3.webp)Churnbuster](/integrations/churnbuster/)
* [![Mailchimp](/images/logos/integrations/mailchimp_hucb75d06be88e6331905252c3cff4ebbc_32058_50x0_resize_q100_h2_box_3.webp)Mailchimp](/integrations/mailchimp/)
* [![FirstPromoter](/images/logos/integrations/firstpromoter_hu13330b4d32004712e337efa3113c94c8_6190_50x0_resize_q100_h2_box_3.webp)FirstPromoter](/integrations/firstpromoter/)
[Integrations](/integrations/)
/
[Email](/integrations/?tag=Email)

Integrate Ghost with EmailOctopus to send campaigns to your members, and keep your email subscribers in sync

Whether you’re using EmailOctopus to send one-off email campaigns to your readers, or running fully automated email marketing funnels - ensure your Ghost publication is fully integrated and your subscribers are in sync.

Here are some of the most popular ways to use Ghost and EmailOctopus together.

Import a CSV
------------

When using the [members feature](/features/) in Ghost, you might want to import an existing list of subscribers from EmailOctopus to kick off your membership website with an existing audience. This is entirely possible using CSV exports and imports.

In your EmailOctopus account, navigate to the list of emails you’d like to import to Ghost members. Once you’re done, click **Export**.

![](/images/integrations/export-list-emailoctopus_hu679d08d645159f1958a26c0bc4bac0d3_59939_2218x0_resize_q100_h2_box.webp)

In Ghost, you can import a CSV file from the member dashboard. The only required field is `email`. However, if you have additional information it’s recommended to add it now using the optional headings available. Read more about [formatting your CSV file here](/help/import-members/#importing-a-csv).

Once your CSV adheres to Ghost’s import format, login to your site’s admin and click the settings icon in the members dashboard to import your file:

![](/images/integrations/import-members_hu9b731faacde4c189bfec36de74b029ce_92095_2424x0_resize_q100_h2_box_3.webp)

That’s it. All of your email subscribers have been imported as members of your Ghost site. You can now let your EmailOctopus subscribers know that they can head to your website and enter their email address to access members-only content, or upgrade to a paid plan.

Sync Ghost members to EmailOctopus
----------------------------------

If you’re running a membership publication with Ghost, it’s possible to link this with your EmailOctopus account using Zapier to ensure everything stays in sync.

Here’s some of the most common automations:

* Automatically import new members in Ghost in EmailOctopus
* Unsubscribe deleted Ghost members from an EmailOctopus list
* Send your Ghost members automated campaigns from such as a welcome or onboarding series

This saves tons of time manually updating lists or sending individual campaigns!

Once your integration has been setup it’ll run in the background so you don’t have to worry about it again!

---

Embed custom subscription forms
-------------------------------

If you prefer to use EmailOctopus subscriber forms directly - you can do that too. It’s as easy as creating a form in EmailOctopus, and pasting the code provided on your site.

First you’ll need to navigate to the correct list in your EmailOctopus account and create a new **form**, using the `Embedded` option:

![](/images/integrations/create-a-form-emailoctopus_hu2d3810ba6566ebaf7cb55e3b9f97bf77_43430_1648x0_resize_q100_h2_box.webp)

Use the EmailOctopus settings to build your form to suit your needs:

![](/images/integrations/email-octopus-form-settings_hu7599231a8319606483035fe2d1539168_86970_1914x0_resize_q100_h2_box.webp)

Then grab the embed code:

![](/images/integrations/email-octopus-form-code_hu853c6ad78c7d8f91b5458e6f184b8fef_248424_2076x0_resize_q100_h2_box.webp)

---

### Add the form to a single post

If you just want to add the signup form to one particular post or page on your site - you can add a new HTML block within the Ghost editor and paste the HTML embed code there. Hit publish. And you’re all set.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

---

### Add the form to multiple pages of your site

If you’d like to add a newsletter signup form to multiple pages of your site - then you’ll need to add the embed code to your Ghost theme.

Locate the template file where you want to insert the signup form. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add the newsletter signup form after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost. The form’s now visible on every post!

---

Next steps
----------

That’s it! You’ve discovered all of the most popular ways to connect your Ghost publication with EmailOctopus. These powerful integrations will help you to keep everything in sync across tools, as well as provide a better experience for your readers and members!

It’s possible to connect EmailOctopus to many more of your favourite tools and align all of your processes using Zapier. There’s lots of popular templates ready to use, or you can create your own:

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

