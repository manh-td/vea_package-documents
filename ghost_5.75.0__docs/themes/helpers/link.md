Ghost Handlebars Theme Helpers: link
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{#link href="/about/"}}About{{/link}}`

### Description

`{{#link}}` is a block helper that creates links with dynamic classes. In its basic form it will create an anchor element that wraps around any kind of string, HTML or handlebars constructed HTML.

With additional options it can have an active `class` or `target` behaviour, or `onclick` JavaScript events. A `href` attribute must be included or an error will be thrown.

Simple example
--------------

```
{{#link href="/about/"}}..linked content here..{{/link}}
Will output:
<a href="/about/">..linked content here..</a>

```

All attributes associated with the `<a></a>` element can be used in `{{#link}}`. Check out the MDN documentation on [the anchor element for more information](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a).

Variables
---------

Handlebars variables can be used for attribute values as well as strings. Variables do not need be wrapped with quotations:

### Simple variables example

```
{{#link href=@site.url}}Home{{/link}}

```
### Advanced variables example

```
{{#foreach posts}}
  {{#link href=(url) class="post-link" activeClass="active"}}
    {{title}}
  {{/link}}
{{/foreach}}

```

Dynamic attributes
------------------

### `activeClass`

By default the active class outputted by `{{#link}}` will be `nav-current`, this is consistent with our [navigation helper](/docs/themes/helpers/navigation/). However it can be overwritten with the `activeClass` attribute:

### `activeClass` Example

```
{{#link href="/about/" activeClass="current"}}About{{/link}}
When on the "/about/" URL it will output:
<a href="/about/" class="current">About</a>

```

`activeClass` can also be given `false` value (`activeClass=false`), which will output an empty string. Effectively turning off the behaviour.

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

