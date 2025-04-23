Using Ghost as a headless CMS with JAMstack
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

How to use Ghost as a headless CMS with popular static site generators

Ghost ships with a default front-end theme layer built with Handlebars, but based on its flexible [architecture](/docs/architecture/) it also be used as a headless CMS with third party front-end frameworks. We have setup guides for most of the most popular frameworks and how to use Ghost with them.

[![Next.js](/images/docs/jamstack/nextjs-logo.svg)](/docs/jamstack/next/)
[![Gatsby.js](/images/docs/jamstack/gatsby-logo.svg)](/docs/jamstack/gatsby/)
[![Hexo](/images/docs/jamstack/hexo-logo.svg)](/docs/jamstack/hexo/)
[![Nuxt.js](/images/docs/jamstack/nuxtjs-logo_hu9cae5061ed1f69c9d83af67ed2b31db3_33854_921x0_resize_q100_h2_box_3.webp)](/docs/jamstack/nuxt/)
[![VuePress](/images/docs/jamstack/vuepress-logo_hu682ba1d96ca023ceb24ae8867fa88f58_8588_1031x0_resize_q100_h2_box_3.webp)](/docs/jamstack/vuepress/)
[![Gridsome](/images/docs/jamstack/gridsome-logo.svg)](/docs/jamstack/gridsome/)
[![Eleventy](/images/docs/jamstack/eleventy-logo.svg)](/docs/jamstack/eleventy/)
[![Custom](/images/docs/jamstack/custom.svg)](/docs/jamstack/custom/)

Tips for using Ghost headless
-----------------------------

Something to keep in mind is that Ghost’s default front-end is not just a theme layer, but also contains a large subset of functionality that is commonly required by most publishers, including:

* Tag archives, routes and templates
* Author archives, routes and templates
* Generated sitemap.xml for SEO
* Intelligent output and fallbacks for SEO meta data
* Automatic Open Graph structured data
* Automatic support for Twitter Cards
* Automatic Google AMP routes and templates
* Custom routes and automatic pagination
* Front-end code injection from admin

When using a statically generated front-end, all of this functionality must be re-implemented. Getting a list of posts from the API is usually the easy part, while taking care of the long tail of extra features is the bulk of the work needed to make this work well.

### Memberships

Ghost’s membership functionality is **not** compatible with headless setups. To use features like our Stripe integration for paid subscriptions, content gating, comments, analytics, offers, complimentary plans, trials, and more — Ghost must be used with its frontend layer.

### Working with images

The Ghost API returns content HTML including image tags with absolute URLs, pointing at the origin of the Ghost install. This is intentional, because Ghost itself is designed (primarily) to be source of truth for serving optimised assets, and may also be installed in a subdirectory.

When using a static front-end, you can either treat the Ghost install as a CDN origin for uploaded assets, or you can write additional logic in your front-end build to download embedded images locally, and rewrite the returned HTML to point to the local references instead.

### Disabling Ghost’s default front-end

When using a headless front-end with Ghost, you’ll want to disable Ghost’s default front-end to prevent duplicate content issues where search engines would see the same content on two different domains. The easiest way to do this is to enable ‘Private Site Mode’ under `Settings > General` - which will put a password on your Ghost install’s front-end, disable all SEO features, and serve a `noindex` meta tag.

You can also use dynamic redirects, locally or at a DNS level, to forward traffic automatically from the Ghost front-end to your new headless front-end - but this is a more fragile setup. If you use Ghost’s built-in newsletter functionality, unsubscribe links in emails will point to the Ghost origin - and these URLs will break if redirected. Preview URLs and other dynamically generated paths may also behave unexpectedly when blanket redirects are used.

Usually ‘Private Site Mode’ is the better option.

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

