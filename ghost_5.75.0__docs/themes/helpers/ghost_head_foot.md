Ghost Handlebars Theme Helpers: ghost\_head/foot
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{ghost_head}}` and `{{ghost_foot}}`

### Description

These helpers output vital system information at the top and bottom of the document, and provide hooks to inject additional scripts and styles.

### ghost\_head

`{{ghost_head}}` – belongs just before the `</head>` tag in `default.hbs`, outputs the following:

* Meta description
* Structured data Schema.org microformats in JSON/LD - no need to clutter your theme markup!
* Structured data tags for Facebook Open Graph and Twitter Cards.
* RSS url paths to make your feeds easily discoverable by external readers.
* Scripts to enable the Ghost API
* Canonical link to equivalent `amp` post *(if enabled in integrations)*
* Anything added in the `Code Injection` section globally, or at a page-level

### ghost\_foot

`{{ghost_foot}}` – belongs just before the `</body>` tag in `default.hbs`, outputs the following:

* Anything added in the `Code Injection` section globally, or at a page-level
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

