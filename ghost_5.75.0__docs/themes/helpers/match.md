Ghost Handlebars Theme Helpers: match
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{#match @custom.color_scheme "=" "Dark"}} class="dark-mode"{{/match}}`

### Description

`{{#match}}` allows for simple comparisons, and executing different template blocks depending on the outcome.

Like all block helpers, `{{#match}}` supports adding an `{{else}}` block or using `^` instead of `#` for negation - this means that the `{{#match}}` and `{{else}}` blocks are reversed if you use `{{^match}}` and `{{else}}` instead. In addition, it is possible to do `{{else match ...}}`, to chain together multiple options like a switch statement.

### Operators

#### Equality

`match` supports comparing values for equality, which is the default behaviour:

```
{{#match @custom.color_scheme "=" "Dark"}}...{{else}}...{{/match}}
{{!-- Can be shortened to: --}}
{{#match @custom.color_scheme "Dark"}}...{{else}}...{{/match}}

```

The equality test can also be negated:

```
{{#match @custom.color_scheme "!=" "Dark"}}...{{else}}...{{/match}}

```
#### Numeric comparisons

The match handler supports >, <, >= and <= operators for numeric comparisons.

```
{{#match posts.length ">" 1}}...{{else}}...{{/match}}

```
#### Evaluation rules

Values passed to `match` are tested according to their *value* as well as their *type*. For example:

```
{{!-- Returns true/false --}}
{{#match feature_image true}}...{{else}}...{{/match}}
{{!-- Always returns false --}}
{{#match feature_image 'true'}}...{{else}}...{{/match}}

```

`match` can also be used to test boolean values similar to `if`:

```
{{!-- Default behaviour is to test if a value is truthy --}}
{{#match featured}}...{{else}}...{{/match}}

```
### Example code

The `match` helper is extremely useful when combined with [Custom settings](/docs/themes/custom-settings/) using `@custom`:

```
{{!-- Adds the 'font-alt' class when the Typography setting is set to 'Elegant serif' --}}
<body class="{{body_class}} {{#match @custom.typography "Elegant serif"}}font-alt{{/match}}">

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

