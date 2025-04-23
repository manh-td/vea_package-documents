Ghost Handlebars Theme Helpers: if
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{#if featured}}{{/if}}`

The `{{#if}}` block helper comes built in with Handlebars.

### Description

`{{#if}}` allows for testing very simple conditionals, and executing different template blocks depending on the outcome.

The conditionals that can be tested are very simple, essentially only checking for ’truthiness’. The evaluation rules are explained in the section below.

Like all block helpers, `{{#if}}` supports adding an `{{else}}` block or using `^` instead of `#` for negation - this means that the `{{#if}}` and `{{else}}` blocks are reversed if you use `{{^if}}` and {{else}} instead. In addition, it is possible to do `{{else if ...}}`, to chain together multiple options like a switch statement.

#### Evaluation rules

The if helper takes a single value, and evaluates whether it is true or false. Any passed in value which is equivalent to `false`, `0`, `undefined`, `null`, `""` (an empty string) or `[]` (an empty array) is considered false, and any other value is considered true.

* Any boolean value, like the featured flag on a post, will evaluate to true or false as you expect.
* Any string value will be true, as long as it is not null or empty
* All numerical values, with the exception of `0` evaluate to true, 0 is the same as false
* Any property which doesn’t exist or is not set will always evaluate false
* Empty arrays or objects will be false

### Example code

When in the scope of a post, `featured` is a boolean flag. The following code example will evaluate to true only if the post is marked as featured.

```
{{#post}}
  {{#if featured}}
   ...do something if the post is featured...
  {{/if}}
{{/post}}

```

You can also use this to test if any property is set. Strings, like image URLs will evaluate to true as long as one is present, and will be null (false) otherwise:

```
{{#post}}
  {{#if feature_image}}
     <img src="{{img_url feature_image}}" />
  {{else}}
		 <img src="{{asset "img/default-img.jpg"}}" />
  {{/if}}
{{else}}
<p>No posts to display!</p>
{{/post}}

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

