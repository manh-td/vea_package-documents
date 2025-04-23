Ghost Handlebars Theme Helpers: @config
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

The `@config` property provides access to global data properties, which are available anywhere in your theme.

Specifically `@config` will pass through the special theme config that is added in the theme’s `package.json` so that it can be used anywhere in handlebars.

At the moment, there is only one property which will be passed through, as all other [properties](https://ghost.org/docs/themes/structure/#additional-properties) are accessed with their own helpers.

* `{{@config.posts_per_page}}` – the number of posts per page

### Example Code

Standard usage:

```
<a href="{{page_url "next"}}">Show next {{@config.posts_per_page}} posts</a>

```

In the get helper limit field:

```
{{#get "posts" filter="featured:true" limit=@config.posts_per_page}}
  {{#foreach posts}}
      <h1>{{title}}</h1>
	{{/foreach}}
{{/get}}

```
### Providing config

Config values can be provided by adding a `config` block to package.json

```
{
  "name": "my-theme",
  "version": 1.0.0,
  "author": {
    "email": "my@address.here"
  }
  "config": {
  }
}

```

There are currently four properties supported:

* `config.posts_per_page` — the default number of posts per page is 5
* `config.image_sizes` — see the [assets](/docs/themes/assets/) guide for more details on responsive images
* `config.card_assets` — configure the [card CSS and JS](/docs/themes/content/#editor-cards) that Ghost automatically includes
* `config.custom` - add [custom settings](/docs/themes/custom-settings/) to your theme
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

