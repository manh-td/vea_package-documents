Ghost Handlebars Theme Helpers: post\_class
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{post_class}}`

### Description

`{{post_class}}` outputs classes intended for your post container, useful for targeting posts with styles.

The classes are as follows:

* `post` - All posts automatically get a `post` class.
* `featured` - All posts marked as featured get the `featured` class.
* `page` - Any static page gets the `page` class.
* `tag-:slug` - For each tag associated with the post, the post get a tag in the format `tag-:slug`.

For example:

A post which is not featured or a page, but has the tags `photo` and `panoramic` would get `post tag-photo tag-panoramic` as post classes.

A featured post with a tag of `photo` would get `post tag-photo featured`.

A featured page with a tag of `photo` and `panoramic` would get `post tag-photo tag-panoramic featured page`.

Setting a post as featured or as a page can be done from the post settings menu.

### Example Code

```
<article class="{{post_class}}">
  {{content}}
</article>

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

