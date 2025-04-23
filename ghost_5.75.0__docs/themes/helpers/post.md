Ghost Handlebars Theme Helpers: post
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{#post}}{{/post}}` or `{{#foreach posts}}{{/foreach}}`

Description
-----------

When on a single post template such as `post.hbs` or `page.hbs`, outputting the details of your posts can be done with a block expression.

The block expression `{{#post}}{{/post}}` isn’t strictly a ‘helper’. You can do this with any object in a template to access the nested attributes e.g. you can also use `{{#primary_author}}{{/primary_author}}` inside of the post block to get to the primary author’s name and other attributes.

When inside a post list such as `index.hbs` or `tag.hbs` where there is more than one post, it is common to use the `{{#foreach post}}{{/foreach}}` to iterate through the list.

When inside a `{{#foreach posts}}{{/foreach}}` or `{{#post}}{{/post}}` block (i.e. when inside the post scope), theme authors have access to all of the properties and helpers detailed on this page.

Post Attributes
---------------

The full list of post attributes and more information about outputting posts can be found in the post context documentation.

Static pages
------------

When outputting a static page, you can use the same `{{#post}}{{/post}}` block expression, and all the same helpers you can use for a post.

Featured posts
--------------

Featured posts get an extra class so that they can be styled differently. They are not moved to the top of the post list or displayed separately to the normal post list.

Use `{{#if featured}}{{/if}}` to test if the current post is featured.

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

