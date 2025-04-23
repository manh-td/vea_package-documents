Ghost Handlebars Theme Helpers: recommendations
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{recommendations}}`

Description
-----------

Use the `{{recommendations}}` helper anywhere in a theme to output a list of recommended sites as configured in Ghost Admin.

Default template
----------------

Ghost uses the following [default template](https://github.com/TryGhost/Ghost/blob/e8fec418227085d1418f45b49e800c753c40fa83/ghost/core/core/frontend/helpers/tpl/recommendations.hbs) to render recommendations.

```
{{#if recommendations}}
    <ul class="recommendations">
        {{#each recommendations as |rec|}}
        <li class="recommendation">
            <a href="{{rec.url}}" data-recommendation="{{rec.id}}" target="_blank" rel="noopener">
                <div class="recommendation-favicon">
                    {{#if rec.favicon}}
                        <img src="{{rec.favicon}}" alt="{{rec.title}}" loading="lazy" onerror="this.style.display='none';">
                    {{/if}}
                </div>
                <h5 class="recommendation-title">{{rec.title}}</h5>
                <span class="recommendation-url">{{readable_url rec.url}}</span>
                <p class="recommendation-description">{{rec.description}}</p>
            </a>
        </li>
        {{/each}}
    </ul>
{{/if}}

```

The template loops over recommendations and outputs an HTML list item for each recommendation. Use the CSS class names to style the content.

Alternatively, override the default template altogether with a custom one by adding a file called `recommendations.hbs` to the theme’s `partials` folder.

When building a custom template, the `recommendation` object contains the following data:

* `id`: Recommendation ID used to track the number of clicks.
* `url`: The recommended site’s URL. Use the [`readable_url` helper](/docs/themes/helpers/readable_url) to make a more human-readable URL.
* `favicon`: The recommended site’s favicon, output as an image URL
* `featured_image`: The recommended site’s feature image, output as an image URL
* `title`: The recommended site’s title
* `description`: The recommended site’s description
* `created_at`: The date the recommendation was created
* `updated_at`: The date the recommendation was updated

Attributes
----------

Combine the `{{recommendations}}` helper with the attributes listed below to customize its behavior.

### Limit

Specify the maximum number of recommendations to display. The default is 5.

```
{{recommendations limit="10"}}
<!-- outputs 10 recommendations -->

```
### Order

Order recommendations based on any valid resource field (like `title`) in ascending (`asc`) or descending (`desc`) order. The default order is `created_at desc` (or newest recommendations on top).

```
{{recommendations order="title asc"}}
<!-- outputs recommendations by title in alphabetical order -->

```
### Page

When the total number of recommendations exceeds the number defined in `limit`, recommendations become paginated. Use the `page` attribute to access subsequent pages of recommendations.

```
{{recommendations limit="5" page="2"}}
<!-- outputs the second page of recommendations when total recommendations are greater than 5 -->

```
### Filter

Use logic-based queries to filter recommendations. For a guide to filtering syntax, see our [Content API docs](https://ghost.org/docs/content-api/#filtering).

```
{{recommendations filter="favicon:-null"}}
<!-- only output recommendations with a favicon >

```

Advanced options
----------------

### Only show recommendations when enabled

Use `@site.recommendations_enabled` to only show recommendations when they’ve been enabled in Ghost Admin. This is useful when adding additional markup that should only be shown when recommendations are enabled:

```
{{#match @site.recommendations_enabled}}
    <h2>Recommendations</h2>
    {{recommendations}}
{{/match}}

```
### Open the recommendations modal

When Portal is enabled on a Ghost site, recommendations are displayed at `site.com/#/portal/recommendations`. Let users open the recommendations modal by adding the `data-portal="recommendations"` attribute to a button.

```
{{recommendations limit="5"}}
<!-- outputs 5 recommendations -->
<button data-portal="recommendations">Show all recommendations</button>
<!-- open the recommendations portal when clicked -->

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

