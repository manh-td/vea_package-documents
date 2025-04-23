Ghost Handlebars Theme Helpers: price
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{price plan}}`

### Description

The `{{price}}` helper formats monetary values from their smallest denomination to a human readable denomination with currency formatting. Example:

```
{{price plan}}

```

This will output `$5`.

The `{{price}}` helper accepts a number of optional attributes:

* `currency` - defaults to `plan.currency` when passed a `plan` object
* `locale` - defaults to `@site.locale`
* `numberFormat` - defaults to “short”, and can be either “short” ($5) or “long” ($5.00)
* `currencyFormat` - defaults to “symbol” and can be one of “symbol” ($5), “code” (EUR 5) or “name” (5 euros)

`{{price}}` can be used with static values as well, `{{price 4200}}` will output `42`.

The default behaviour of the `price` helper is the same as:

```
{{price plan.amount
  currency=plan.currency
  locale=@site.locale
  numberFormat="short"
  currencyFormat="symbol"
}}

```

Passing a `currency` without a price will output the symbol for that currency:

```
{{price currency="USD"}} <!-- Outputs: $ -->

```
### Example Code

Outputting prices for all tiers.

```
{{#get "tiers" include="monthly_price,yearly_price,benefits" limit="all" as |tiers|}}
    {{! Loop through our tiers collection }}
    {{#foreach tiers}}
        {{#if monthly_price}}
            <div>
                <a href="javascript:" data-portal="signup/{{id}}/monthly">Monthly – {{price monthly_price currency=currency}}</a>
            </div>
        {{/if}}
          {{#if yearly_price}}
            <div>
                <a href="javascript:" data-portal="signup/{{id}}/monthly">Monthly – {{price yearly_price currency=currency}}</a>
            </div>
        {{/if}}
    {{/foreach}}
{{/get}}

```

Outputting prices for a member’s subscriptions.

```
<!-- account.hbs -->
{{#foreach @member.subscriptions}}
  <div class="subscription">
    <label class="subscriber-detail-label">Your plan</label>
    <span class="subscriber-detail-content">{{price plan}}/{{plan.interval}}</span>
  </div>
{{/foreach}}

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

