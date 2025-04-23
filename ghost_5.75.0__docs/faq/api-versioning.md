Ghost API Versioning
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Ghost ships with a mature set of APIs. Each API endpoint has a status, which indicates suitability for production use. Read more about Ghost’s [architecture](/docs/architecture/).

Stability Index
---------------

* **Stable** - forward compatible changes only
* **Experimental** - being actively worked on, may receive breaking changes
* **Deprecated** - scheduled for removal

Accept-Version Header
---------------------

`Accept-Version: v{major}.{minor}`

The ‘Accept-Version’ header allows clients to indicate the minimum version of Ghost they can operate with. It also allows Ghost to determine and communicate if any recent breaking changes are unsuitable for a given client.

When the `Accept-Version` header is received, Ghost will respond with a `Content-Version` header indicating the version of the Ghost install that is responding.

If the `Accept-Version` header is received and the request cannot be processed, Ghost sends an email to the site’s owner and administrators with the details of the problem, to make it easy to find and fix issues with outdated clients.

Ghost [major versions](/docs/faq/major-versions-lts/) ship every 8-12 months, meaning code you write against our API today will be stable for a minimum of 2 years.

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

