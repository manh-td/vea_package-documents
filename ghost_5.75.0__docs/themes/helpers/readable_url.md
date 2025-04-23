Ghost Handlebars Theme Helpers: readable\_url
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{readable_url URL}}`

Description
-----------

The `readable_url` helper outputs a human-readable URL by stripping out its protocol, www, query paramters, and hash fragments. It doesn’t strip out any subdomains or pathnames. This helper pairs well with the [`recommendations` helper](/docs/themes/helpers/recommendations) to output more readable URLs.

See the examples below to understand the helper’s expected output:

```
{{readable_url "https://google.com"}}
<!-- removes the "https://" protocol. Outputs: "google.com" -->
{{readable_url "www.google.com"}}
<!-- removes "www". Outputs: "google.com" -->
{{readable_url "https://google.com?foo=bar&dog=love"}} 
<!-- removes query parameters. Outputs: "google.com" -->
{{readable_url "https://google.com#section-1"}}
<!-- removes hash fragments. Outputs: "google.com" -->
{{readable_url "https://ghost.org/about"}}
<!-- pathnames are not removed. Outputs: "ghost.org/about" -->
{{readable_url "https://account.ghost.org"}}
<!-- subdomains are not removed. Outputs: "account.ghost.org" -->

```
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

