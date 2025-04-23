Ghost Handlebars Theme Helpers: body\_class
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{body_class}}`

### Description

`{{body_class}}` – outputs dynamic CSS classes intended for the `<body>` tag in your `default.hbs` or other layout file, and is useful for targeting specific pages (or contexts) with styles.

The `{{body_class}}` helper outputs different classes on different pages, depending on what context the page belongs to. For example the home page will get the class `.home-template`, but a single post page would get `.post-template`.

Ghost provides a series of both static and dynamic `body_class` classes:

#### Static classes

* `home-template` – The class applied when the template is used for the home page
* `post-template` – The class applied to all posts
* `page-template` – The class applied to all pages
* `tag-template` – The class applied to all tag index pages
* `author-template` – The class applied to all author pages
* `private-template` – The class applied to all page types when password protected access is activated

#### Dynamic classes

* `page-{slug}` – A class of `page-` plus the page slug added to all pages
* `tag-{slug}` – A class of `tag-` plus the tag page slug added to all tag index pages
* `author-{slug}` – A class of `author-` plus the author page slug added to all author pages

### Examples

```
<!-- default.hbs -->
<html>
    <head>...</head>
    <body class="{{body_class}}">
    ...
    {{{body}}}
    ...
    </body>
</html>

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

