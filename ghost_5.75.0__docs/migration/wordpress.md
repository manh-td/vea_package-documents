Official guide: How to migrate from WordPress to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Migrate from WordPress and import your content to Ghost with this guide

If you're a Ghost(Pro) customer, our team may be able to help you migrate your content and subscribers. Learn more about our [Concierge service](/concierge/).

Self-service Migration
----------------------

Most publishers can do this right now using our [WordPress migrator](https://ghost.org/help/importing-from-wordpress/).

![Image showing WordPress importer in Settings > Advanced > Import/Export](/images/docs/migration/wordpress/ghost-import_hu962a01aa25518bdd09da163d2805bfcd_160396_2164x0_resize_q100_h2_box_3.webp)
### Supported Content

What is supported:

* XML files up to 100mb
* Up to 2,500 posts
* Some shortcodes, such as `[caption]`, `[audio]`, `[code]`, along with most `[vc_]` & `[et_]` based shortcodes from page builder plugins.

What’s not supported:

* Custom post types
* Most uncommon shortcodes
* Plugins that alter access to content

Complex Migrations
------------------

For more complex migrations, those comfortable with the command line can use our CLI tools.

First, install the CLI. Then build and run your command. All options for this tool can be found on [GitHub](https://github.com/TryGhost/migrate/tree/main/packages/mg-wp-xml).

```
# Install
npm install --global @tryghost/migrate
# Migrate posts only, add a 'News' tag, retain the existing /yyyy/mm/dd/slug permalink structure
migrate wp-xml --pathToFile ./file.xml --pages false --addTag News --datedPermalinks '/yyyy/mm/dd/'

```

Troubleshooting
===============

If you’re having trouble exporting an XML file, or have lot of content, try the [API-based tools](https://github.com/TryGhost/migrate/tree/main/packages/mg-wp-api) which can successfully handle migrations with tens of thousands of posts.

Authors who were migrated will most likely need to reset their passwords, which can be done when logging into Ghost.

---

Summary
-------

Congratulations on your migration to Ghost 🙌. All that’s left to do is check over your content to ensure the migration has worked as expected. We also have a guide on [how to implement redirects](/tutorials/implementing-redirects/#common-redirects) to make your transition smoother.

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

