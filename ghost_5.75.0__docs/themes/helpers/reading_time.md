Ghost Handlebars Theme Helpers: reading\_time
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Usage: `{{reading_time}}`

### Description

`{{reading_time}}` renders the estimated reading time for a post.

The helper counts the words in the post and calculates an average reading time of 275 words per minute. For the first image present, 12s is added, for the second 11s is added, for the third 10, and so on. From the tenth image onwards every image adds 3s.

By *default* the helper will render a text like this:

* `x min read` for estimated reading time longer than one minute
* `1 min read` for estimated reading time shorter than or equal to one minute

You can override the default text.

### Example Code

```
{{#post}}
    {{reading_time}}
{{/post}}

```

Custom labelling
----------------

Singular minute and plural minutes labelling can be customised using the options `minute` and `minutes`, using `%` as the plural minutes value.

### Example

```
{{reading_time minute="Only a minute" minutes="Takes % minutes"}}

```

[See our full tutorial](/docs/tutorials/show-reading-time-progress/) on how to customise and build upon the `reading_time` Handlebars helper.

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

