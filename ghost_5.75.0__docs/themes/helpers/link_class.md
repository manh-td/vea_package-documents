Ghost Handlebars Theme Helpers: link\_class
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{link_class for="/about/"}}`

### Description

The `{{link_class}}` helper adds dynamic classes depending on the currently viewed page. If the page slug (e.g. `/about/`) matches the value given to the `for` attribute the helper will output a `nav-current` class. A `for` value must be provided.

Simple example
--------------

```
<li class="nav {{link_class for="/about/"}}">About</li>
When on the "/about/" URL it will output:
<li class="nav nav-current">About</li>
By default it will output:
<li class="nav ">About</li>

```
### `activeClass`

By default the active class outputted by `{{link_class}}` will be `nav-current`, this is consistent with our [navigation helper](/docs/themes/helpers/navigation/). However it can be overwritten with the `activeClass` attribute:

```
<li class="nav {{link_class for="/about/" activeClass="active"}}">About</li>
Will output:
<li class="nav active">About</li>

```

`activeClass` can also be given `false` value (`activeClass=false`), which will output an empty string. Effectively turning off the behaviour.

### `class`

Optionally `{{link_class}}` can have additional active classes. Using the `class` attribute will add whatever value has been provided when the link is the active URL, `nav-current` (the default active class value) will be added last:

```
<li class="nav {{link_class for="/about/" class="current-about"}}">About</li>
Will output:
<li class="nav current-about nav-current">About</li>

```

Parent URLs
-----------

Not only can `{{link_class}}` add active classes to current URLs, but it can also apply classes to parent URLs. If a user navigates to `/tags/toast/` then `{{link_class}}` can provide an active class to `/tags/` as well as `/tags/toast/`.

### Example

```
<li class="nav {{link_class for="/tags/"}}">Tags</li>
When on the "/tags/" URL it will output:
<li class="nav nav-current">Tags</li>
When on the "/tags/toast/" URL it will output:
<li class="nav nav-parent">Tags</li>

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

