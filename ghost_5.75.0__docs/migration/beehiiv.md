Official guide: How to migrate from beehiiv to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Migrate from BeeHiiv and import your content to Ghost with this guide

If you're a Ghost(Pro) customer, our team may be able to help you migrate your content and subscribers. Learn more about our [Concierge service](/concierge/).

Exporting your subscribers
--------------------------

To get started, [download your full subscriber list](https://support.beehiiv.com/hc/en-us/articles/12234988536215-How-to-export-subscribers) (**Export Subscribers (Full)**) from BeeHiiv.

![start export](/images/docs/migration/beehiiv-subscriber-exports_huae1d966f695844077fd5c2e1914a81b1_25651_2148x0_resize_q100_h2_box_3.webp)
![download export](/images/docs/migration/beehiiv-subscriber-download_huff7cd490bded2324dbd2f44e962cade4_16919_2148x0_resize_q100_h2_box_3.webp)

Import subscribers to Ghost
---------------------------

If all of your subscribers are free, you can import this into Ghost directly.

![import members](/images/docs/migration/import-members-1_huc3d26abd3bec140dac4d1e5fd61f2b53_17353_1000x0_resize_q100_h2_box_3.webp)

If you have paid subscribers, you need to relate Stripe Customer IDs with your subscribers emails.

![import members](/images/docs/migration/import-members-2_hu4666f031efd860d74fa4f40b2a587fd0_130604_1000x0_resize_q100_h2_box_3.webp)

If you cannot connect your Ghost site to the same Stripe account you used with BeeHiiv, you may need to migrate customer data, products, prices, coupons to a new Stripe account, and then recreate the subscriptions before importing into your Ghost site. The [Ghost Concierge](/concierge/) team can help with this.

Migrating Content
-----------------

Developers can migrate content from BeeHiiv to Ghost using our [migration CLI tools](https://github.com/TryGhost/migrate/tree/main/packages/mg-beehiiv).

You will first need to [export your posts](https://support.beehiiv.com/hc/en-us/articles/12258595483543-How-to-export-your-post-content) from BeeHiiv. This will be a CSV file which includes all post content, titles, dates, etc.

![export posts](/images/docs/migration/beehiiv-content-export_hu692b89da164ad0d3b6abc7f18ee87332_11063_2148x0_resize_q100_h2_box_3.webp)
![download posts](/images/docs/migration/beehiiv-content-download_hu2bc2e7c63f879a9affdf18f111de440a_16136_2148x0_resize_q100_h2_box_3.webp)

First, make sure the CLI is installed.

```
# Install CLI
npm install --global @tryghost/migrate
# Verify it's installed
migrate

```

To run a basic migration with the default commands:

```
# Basic migration
migrate beehiiv --posts /path/to/posts.csv --url https://example.com

```

There are [more options](https://github.com/TryGhost/migrate/tree/main/packages/mg-beehiiv#usage), such as the ability define a default author name and choose where `/subscribe` links go to.

Once the CLI task has finished, it creates a new ZIP file which you can [import into Ghost](https://ghost.org/help/imports/).

### Using custom domains

If you’re using a custom domain on BeeHiiv, you’ll need to implement redirects in Ghost to prevent broken links.

BeeHiiv uses `/p/` as part of the public post URL, where as Ghost uses it in the URL for post previews. This means the redirect regular expression is quite complex, but necessary so that post previews in Ghost function correctly.

```
# redirects.yaml
301:
  ^\/p\/(?![0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12})(.*): /$1
  ^\/polls\/[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}(.*): /
  ^\/t\/(.*): /tag/$1
302:

```

This means that if a visitor or crawler goes to `https://mysite.com/p/awesome-post`, they will automatically be redirected to `https://mysite.com/awesome-post`.

---

Summary
-------

Congratulations on your migration to Ghost 🙌. All that’s left to do is check over your content to ensure the migration has worked as expected. We also have a guide on [how to implement redirects](/docs/tutorials/implementing-redirects/) to make your transition smoother.

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

