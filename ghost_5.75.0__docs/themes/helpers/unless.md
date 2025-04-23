Ghost Handlebars Theme Helpers: unless
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{#unless featured}}{{/unless}}`

The `{{#unless}}` block helper comes built in with Handlebars.

### Description

`{{#unless}}` is essentially the opposite of `{{#if}}`. If you want to test a negative conditional only, i.e. if you only need the `{{else}}` part of an `{{#if}}` statement, then `{{#unless}}` is what you need.

It works exactly the same as `{{#if}}` and supports both `{{else}}` and `^` negation if you want to get really confusing!

Unless also uses the exact same conditional evaluation rules as `{{#if}}`.

### Example code

Basic unless example, will execute the template between its start and end tags only if `featured` evaluates to false.

```
{{#unless featured}}
  ...do something...
{{/unless}}

```

If you want, you can also include an else block, although in the majority of cases, if you need an else, then using `{{#if}}` is more readable:

```
<!-- This is identical to if, but with the blocks reversed -->
{{#unless featured}}
  ...do thing 1...
{{else}}
  ...do thing 2...
{{/unless}}

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

