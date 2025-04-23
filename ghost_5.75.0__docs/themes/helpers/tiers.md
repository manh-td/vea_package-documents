Ghost Handlebars Theme Helpers: tiers
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{tiers}}` / `{{tiers prefix=":" separator=" - " lastSeparator=", " suffix='options'}}`

### Description

`{{tiers}}` is a formatting helper for outputting tier names. It defaults to a comma-separated list with `and` as the last separator and `tier(s)` as the suffix. Customize the helper by using a custom prefix, separator, last separator, and/or suffix. Note that values are white-space sensitive.

### Example code

Use the tiers helper to output tier names in ascending order by price. The examples below use tier names of “bronze,” “silver,” and “gold.”

```
{{tiers}}
{{! output: "bronze, silver and gold tiers" }}

```
#### Custom prefix

Use a custom prefix to add text before tier names.

```
{{tiers prefix="Access with:"}}
{{! output: "Access with: bronze, silver and gold tiers" }}

```
#### Custom separator

Use a custom separator to change the text between tier names.

```
{{tiers separator=" | "}}
{{! output: "bronze | silver and gold tiers" }}

```
#### Custom last separator

With multiple tiers, customize the last separator.

```
{{tiers lastSeparator=" plus "}}
{{! output: "bronze, silver plus gold tiers" }}

```
#### Custom suffix

Change the term “tier” with a custom suffix.

```
{{tiers suffix="options"}}
{{! output: "bronze, silver and gold options" }}

```
#### HTML values

`separator`, `prefix` , `lastSeparator`, and `suffix` accept HTML values.

```
{{tiers separator=" &bull; "}}
{{! output: "bronze • silver and gold tiers }}

```

Fetching tiers with the `{{#get}}` helper
-----------------------------------------

`{{tiers}}` helps with *formatting* your tier names. To fetch tier data, use the `{{#get}}` helper.

```
{{! Get all tiers with monthly price, yearly price, and benefits data }}
{{#get "tiers" include="monthly_price,yearly_price,benefits" limit="all" as |tiers|}}
    {{! Loop through our tiers collection }}
    {{#foreach tiers}}
        {{name}}
        {{#if monthly_price}}
            <div>
                <a href="javascript:" data-portal="signup/{{id}}/monthly">Monthly – {{price monthly_price currency=currency}}</a>
            </div>
        {{/if}}
        {{#if benefits}}
            {{#foreach benefits as |benefit|}}
                {{benefit}}
            {{/foreach}}
        {{/if}}
    {{/foreach}}
{{/get}}

```

See our [{{#get}} helper docs](/docs/themes/helpers/get/) to learn more about using this helper with tiers.

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

