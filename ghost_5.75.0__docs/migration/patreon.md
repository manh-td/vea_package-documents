Official guide: How to migrate from Patreon to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Migrate from Patreon and import your Patrons to Ghost with this guide

Overview
--------

Since Patreon manages your subscriptions on your behalf, there is no direct migration path to move your paid subscriptions from Patreon to other platforms.

The good news: Ghost makes it possible to import all of your existing patrons and give them access to premium content on a custom Ghost publication, or to sync your Patreon account with Ghost using an automation. [Learn more here](https://ghost.org/resources/patreon-vs-your-own-site/).

Migrating Patrons to Ghost
--------------------------

Ghost has an easy to use importer that allows you to migrate a list of members from any other tool, including Patreon.

This method is useful if you’re planning to turn signups in Patreon off and have all new members sign up via Ghost, but still need to give your existing Patrons access to your new Ghost Publication.

### Export your subscribers

To get started, export your current subscribers in CSV format from [this page](https://www.patreon.com/members) in your Patreon account.

### Import subscribers to Ghost

Under the Ghost Admin members settings, select the import option from the settings menu.

![import members](/images/docs/migration/import-members-1_huc3d26abd3bec140dac4d1e5fd61f2b53_17353_1000x0_resize_q100_h2_box_3.webp)

Upload your CSV file to Ghost, and map each of the fields contained in your export file to the corresponding fields in Ghost. The **email** field is required in order to create members in Ghost, while the other fields are optional.

If you’d like to give these members access to content with an acceess level of `paid-members only` but retain their subscriptions in Patreon, you can give them unlimited access by setting their `complimentary_plan` status to `true` — read more about [Member imports](/help/import-members/).

Once the import has completed, all your subscribers will be migrated to Ghost. There’s nothing else you need to do, members can now log into your site and receive email newsletters.

Running Ghost alongside Patreon
-------------------------------

It’s also possible to use Zapier or the Ghost API to keep your Patrons and Members in sync in both platforms. This is useful if you’re giving your audience on Patreon access to premium content on a custom Ghost site as an additional perk, or if you’re accepting signups on both platforms.

To find out how to connect Ghost with Patreon, check out our [integration](/integrations/patreon/).

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

