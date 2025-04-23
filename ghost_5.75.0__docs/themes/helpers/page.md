Ghost Handlebars Theme Helpers: @page
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

The `@page` object provides access to page properties, which are available anywhere in your theme.

* `@page.show_title_and_feature_image` - true (default) or false value from Ghost Editor

This toggle, only available for pages, lets users hide a page’s title and feature image to create pages that look radically different than posts (for example, full-width headers, CTAs, and landing pages).

This setting is only available when using the [new Beta editor](https://ghost.org/changelog/editor-beta/). However, since the `@page.show_title_and_feature_image` is always present and defaults to `true`, supporting this feature in your theme won’t break anything for anyone using the old editor.

Using the `@page` object is **not backward-compatible** with earlier versions of Ghost: once implemented the theme will only be compatible with Ghost 5.54.1 or later.

Example code
------------

```
{{#match @page.show_title_and_feature_image}}
...content...
{{/match}}

```

Styling tips when hiding the title and feature image
----------------------------------------------------

1. Whenever the page title and feature image are hidden, and the page content starts with a full-width card (such cards will have the class `.kg-width-full`), remove spacing between the top navigation and content (on pages only).
2. Whenever multiple full-width cards are stacked, remove spacing between them (on posts and pages).
3. Whenever content ends with a full-width card, remove spacing between the content and the footer (on pages only, posts often have additional content at the bottom such as comments, CTAs, related posts, etc.).

As a reminder, cards that have the ability to be set to full width are header cards, signup cards, image cards, and video cards. When an image or video has a caption, it will have the class `.kg-card-hascaption`, and maintaining spacing is desirable in this case.

The implementation of these changes will look different on every theme. Find examples of these recommended changes in Casper [here](https://github.com/TryGhost/Casper/commit/d9c9390e17c1df1322ebfec774886058a56a0891) (1 and 3) and [here](https://github.com/TryGhost/Casper/blob/a60e3e976a341df462ba948d395bc52c37faffa4/assets/css/screen.css#L1345-L1348) (2).

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

