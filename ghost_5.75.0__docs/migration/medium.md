Official guide: How to migrate from Medium to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Migrate from Medium and import your content to Ghost with this guide

Self-service Migration
----------------------

Most publishers can do this right now using our [Medium migrator](https://ghost.org/help/importing-from-medium/).

![Image showing Medium importer in Settings > Advanced > Import/Export](/images/docs/migration/wordpress/ghost-import_hu962a01aa25518bdd09da163d2805bfcd_160396_2164x0_resize_q100_h2_box_3.webp)
### Using custom domains

If you’re using a custom domain on Medium, you’ll need to implement redirects in Ghost to prevent broken links.

Medium appends a small random ID to each post, which is removed in the migration step above. The regular expression below removes that random ID, but does not affect preview links.

```
# redirects.yaml
301:
    ^\/(?!p\/?)(.*)(-[0-9a-f]{10,12}): /$1
302:

```

This means that if a visitor or crawler goes to `https://mysite.com/awesome-post-a1b2c3d4e5f6`, they will automatically be redirected to `https://mysite.com/awesome-post`.

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

