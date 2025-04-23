Context Overview: Ghost Themes - Documentation
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Each page in a Ghost theme belongs to a context, which determines which template is used, what data will be available and what content is output by the `{{body_class}}` helper.

A Ghost publication follows a structure that allows URLs or routes to be mapped to views which display specific data. This data could be a list of posts, a single post or an RSS feed. It is the route that determines what data is meant to be shown and what template is used to render it.

Rather than providing access to all data in all contexts, Ghost optimises what data is fetched using contexts to ensure publications are super fast!

### Using contexts

Contexts play a big part in the building blocks of a Ghost theme. Besides determining what data is available and what template to render, contexts also interact with [handlebars helpers](/docs/themes/helpers/), since the context also determines what dynamic data the helper outputs.

For example, the `{{meta_title}}` helper outputs different things based on the current context. If the context is `post` then the helper knows it can use `post.meta_title` and in a `tag` context it uses `tag.meta_title`.

To detect a context in your theme, use the `{{#is}}` helper. For example, in a partial template that is shared between many contexts, using `{{#is}}` passes it a context and only executes the contained block when it is in that context.

List of contexts
----------------

* [index](/docs/themes/contexts/index-context/)
* [page](/docs/themes/contexts/page/)
* [post](/docs/themes/contexts/post/)
* [author](/docs/themes/contexts/author/)
* [tag](/docs/themes/contexts/tag/)
* [error](/docs/themes/contexts/error/)
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

