Author Context: Ghost Themes - Documentation
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Use: `{{#is "author"}}{{/is}}` to detect this context

Authors in Ghost each get their own page which outputs a list of posts that were published by that author. You’re in the `author` context when viewing the page thats lists all posts written by that user, as well as subsequent pages of posts. The `author` context is only set on the list of posts, and not on the individual post itself.

Routes
------

The default URL for author pages is `/author/:slug/`. The `author` context is also set on subsequent pages of the post list, which live at `/author/:slug/page/:num/`. The `slug` part of the URL is based on the name of the author and can be configured in admin. To change the author URL structure, use [routing](/docs/themes/#routing).

Templates
---------

The default template for an author page is `index.hbs` or you can use an `author.hbs` file in your theme to customise the author pages.

To provide a custom template for a *specific* author, name the file using `author-:slug.hbs`, file with the `:slug` matching the user’s slug. For example, if you have an author ‘John’ with the url `/author/john/`, adding a template called `author-john.hbs` will cause that template to be used for John’s list of posts instead of `author.hbs`, or `index.hbs`.

These templates exist in a hierarchy. Ghost looks for a template which matches the slug (`author-:slug.hbs`) first, then looks for `author.hbs` and finally uses `index.hbs` if neither is available.

Data
----

When in the `author` context, a template gets access to 3 objects: the author object which matches the route, an array of post objects and a pagination object. As with all contexts, all of the `@site` global data is also available.

### Author object

When outputting the author attributes, use a block expression (`{{#author}}{{/author}}`) to drop into the author scope and access all of the attributes. See a full list of attributes below:

### Author object attributes

* **id** — incremental ID of the author
* **name** — name of the author
* **bio** — bio of the author
* **location** — author’s location
* **website** — author’s website
* **twitter** — the author’s twitter username
* **facebook** — the author’s facebook username
* **profile\_image** — the profile image associated with the author
* **cover\_image** — author’s cover image
* **url** - web address for the author’s page

### Post list

Each of the posts can be looped through using `{{#foreach posts}}{{/foreach}}`. The template code inside the block will be rendered for each post, and have access to all of the post object attributes.

### Pagination

The best way to output pagination is to use the pagination helper — the pagination object provided is the same everywhere.

Helpers
-------

The `{{#author}}{{/author}}` block expression is useful for accessing all of the author attributes. Once inside the author you can access the attributes and use helpers like `{{img_url}}` and `{{url}}` to output the author’s details.

Using `{{#foreach posts}}{{/foreach}}` is the best way to loop through your posts and output each one. If you’re using the Members feature, consider the [content visibility](/docs/themes/members/#content-visibility) of your posts.

If your theme does have a `tag.hbs` and `author.hbs` file all outputting similar post lists to `index.hbs` you may wish to use a partial to define your post list item, e.g. `{{> "loop"}}`.

```
<!-- author.hbs -->
<!-- Everything inside the #author tags pulls data from the author -->
{{#author}}
  <header>
  	{{#if profile_image}}
    	<img src="{{img_url profile_image}}" alt="{{name}}'s Picture" />
    {{/if}}
  </header>
  <section class="author-profile">
  	<h1 class="author-title">{{name}}</h1>
    {{#if bio}}<h2 class="author-bio">{{bio}}</h2>{{/if}}
    <div class="author-meta">
      {{plural ../pagination.total empty='No posts' singular='% post' plural='% posts'}}
     </div>
  </section>
{{/author}}
<main role="main">
    <!-- includes the post loop - partials/loop.hbs -->
    {{> "loop"}}
</main>
<!-- Previous/next page links - displayed on every page -->
{{pagination}}

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

