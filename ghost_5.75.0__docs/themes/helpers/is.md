Ghost Handlebars Theme Helpers: is
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{#is "contexts"}}`

### Description

The `{{#is}}` helper allows you to check the context of the current route, i.e. is this the home page, or a post, or a tag listing page. This is useful when using shared partials or layouts, to output slightly different context in different places on your theme.

### Usage

The `is` helper takes a single parameter of a comma-separated list containing the contexts to check for. Similar to the `has` helper, the comma behaves as an `or` statement, with `and` being achieved by nesting helpers.

```
{{#is "post, page"}}
   ... content to render if the current route represents a post or a page ...
{{/is}}

```

As with all block helpers, it is possible to use an else statement:

```
{{#is "home"}}
  ... output something special for the home page ...
{{else}}
  ... output something different on all other pages ...
{{/is}}

```

If you only want the reverse, or negation, you can use the `^` character:

```
{{^is "paged"}}
 ...if this is *not* a 2nd, 3rd etc page of a list...
{{/is}}

```
### Contexts

The following contexts are supported:

* **home** - true only on the home page
* **index** - true for the main post listing, including the home page
* **post** - true for any individual post page, where the post is not a static page
* **page** - true for any static page
* **tag** - true for any page of the tag list
* **author** - true for any page of the author list
* **paged** - true if this is page 2, page 3 of a list, but not on the first page
* **private** - true if this is the private page shown for password protected sites
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

