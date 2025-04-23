Official guide: How to migrate from Gumroad to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Migrate from Gumroad and import your customers to Ghost with this guide

Overview
--------

Since Gumroad manages your subscriptions on your behalf, there is no direct migration path to move your paid subscriptions from Gumroad to other platforms.

The good news: Ghost makes it possible to import all of your existing customer emails and give them access to premium content, or to sync your Gumroad with your Ghost site using an automation.

Export your customers
---------------------

To get started, export your current subscribers from Gumroad in CSV format.

![export members from gumroad](/images/docs/migration/gumroad-export_hu56c76fc0713e6fce5586b59ad57c30de_7136_1520x0_resize_q100_h2_box_3.webp)

Gumroad allows you to export all customers who have ever purchased from you within a specific date range, or to segment your export per product.

Import subscribers to Ghost
---------------------------

Under the Ghost Admin members settings, select the import option from the settings menu.

![import members](/images/docs/migration/import-members-1_huc3d26abd3bec140dac4d1e5fd61f2b53_17353_1000x0_resize_q100_h2_box_3.webp)

Upload your CSV file to Ghost, and map each of the fields contained in your export file to the corresponding fields in Ghost. The **email** field is required in order to create members in Ghost, while the other fields are optional.

It’s recommended to edit your data as required before uploading your CSV file to Ghost.

Once the import has completed, all your subscribers will be migrated to Ghost. There’s nothing else you need to do, members can now log into your site and receive email newsletters.

Running Ghost alongside Gumroad
-------------------------------

It’s also possible to use Zapier or the Ghost API to keep customers who have purchased from you on Gumroad in sync with a Ghost membership site. This is useful if you’re giving your existing customers on Gumroad access to premium content on a custom Ghost site as an additional perk, or if you’re accepting signups on both platforms.

To find out how to connect Ghost with Gumroad, check out our [integration](/integrations/gumroad/).

##### On this page

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

