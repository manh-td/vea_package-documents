Ghost Handlebars Theme Helpers: pagination
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{pagination}}`

Description
-----------

`{{pagination}}` is a template driven helper which outputs HTML for ’newer posts’ and ‘older posts’ links if they are available and also says which page you are on.

You can override the HTML output by the pagination helper by placing a file called `pagination.hbs` inside of `content/themes/your-theme/partials`. Details of the default template are below.

The data used to output the `{{pagination}}` helper is generated based on the post list that is being output (index, tag posts, author posts etc) and always exists at the top level of the data structure.

Pagination Attributes
---------------------

* **page** - the current page number
* **prev** - the previous page number
* **next** - the next page number
* **pages** - the number of pages available
* **total** - the number of posts available
* **limit** - the number of posts per page

Default Template
----------------

The [default template](https://github.com/TryGhost/Ghost/blob/3d989eba2371235d41468f7699a08e46fc2b1e87/ghost/core/core/frontend/helpers/tpl/pagination.hbs) output by Ghost is shown below. You can override this by placing a file called `pagination.hbs` in the partials directory of your theme.

```
<nav class="pagination" role="navigation">
    {{#if prev}}
        <a class="newer-posts" href="{{page_url prev}}">&larr; Newer Posts</a>
    {{/if}}
    <span class="page-number">Page {{page}} of {{pages}}</span>
    {{#if next}}
        <a class="older-posts" href="{{page_url next}}">Older Posts &rarr;</a>
    {{/if}}
</nav>

```

Unique helpers within this context
----------------------------------

* `{{page_url}}` - accepts `prev`, `next` and `$number` to link to a particular page
* `{{page}}` - outputs the current page number
* `{{pages}}` - outputs the total number of pages
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

