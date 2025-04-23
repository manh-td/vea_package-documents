Ghost Handlebars Theme Helpers: block & contentFor
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{{block "section"}}}` and `{{#contentFor "section"}} content {{/contentFor}}`

Description
-----------

`{{{block "block-name"}}}` is a helper for creating a placeholder within a custom handlebars template. Adding the helper along with a unique ID creates a slot within the template, which can be optionally filled when the template is inherited by another template file.

The `{{#contentFor "block-name"}}...{{/contentFor}}` helper is used to access and populate the block definitions within the template that’s being inherited. The inherited template is referenced with `{{!< template-name}}` at the top of the file. If the `contentFor` is not used then the block will be gracefully skipped.

### Example

```
<!-- default.hbs -->
<body>
    <!-- ... -->
    {{{block "scripts"}}}
</body>

```

---

```
<!-- page.hbs -->
{{!< default}}
{{#contentFor "scripts"}}
    <script>
        runPageScripts();
    </script>
{{/contentFor}}

```

`{{{body}}}` helper
-------------------

The `{{{body}}}` helper behaves in a similar fashion to a defined block helper, but doesn’t require a corresponding `contentFor` helper in the inheriting template file.

### `{{{body}}}` example

```
<!-- default.hbs -->
<div class="site-wrapper">
    {{{body}}}
    <!-- ... -->
</div>

```

---

```
<!-- post.hbs -->
{{!< default}}
<section class="post-full-content">
    <div class="post-content">
        {{content}}
    </div>
</section>

```

Inherited template files, files that contain `{{{block "block-name"}}}`, cannot be templates used directly by Ghost. `post.hbs`, `page.hbs` `index.hbs` can inherit other template files and used the `contentFor` helper but cannot contain block definitions. See our [theme structure documentation](/docs/themes/structure/#templates) for more information.

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

