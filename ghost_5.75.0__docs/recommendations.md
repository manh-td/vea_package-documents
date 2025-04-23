Recommendations – Ghost Developer Docs
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Overview
--------

With recommendations, publishers can share their favorite sites with their readers and, likewise, be recommended by other publications. See [the Changelog](https://ghost.org/changelog/recommendations/) for an overview of this feature.

![Recommendations in Ghost](/images/docs/recommendations_hu87dd64b769c4fd4ef600cc9c9bc971ce_570214_2000x0_resize_q100_h2_box_3.webp)

Under the hood, Ghost’s recommendations feature is built on the [Webmention open standard](https://www.w3.org/TR/webmention/), which means recommendations aren’t limited to any single platform — but extend to every site on the web!

Recommendations also make it possible for readers to subscribe to recommended publications with a single click. While this feature is currently exclusive to Ghost sites, we are eager to help other platforms in implementing this 1-click functionality. Contact us if you’re interested in building 1-click subscriptions for the open web!

The sections below provide a high-level technical summary of how recommendations work.

See your site’s recommendations
-------------------------------

* The recommendations modal is shown automatically whenever a new member subscribes to a Ghost publication.
* Visiting `https://yoursite.com/#/portal/recommendations` will open the recommendations modal. Use this URL as a link in the navigation menu to create a recommendation button.
* See additional methods for opening the recommendations modal in our [theme docs](/docs/themes/helpers/recommendations/).

How Ghost sends a recommendation
--------------------------------

When you make a recommendation, it shows on your website and in Portal at `yoursite.com/#/portal/recommendations`. Behind the scenes, Ghost performs the following steps:

1. Ghost checks to see if the recommended site has Webmentions enabled. While it’s possible to recommend any site, Ghost only notifies sites about your recommendation if they have a Webmention endpoint that can receive it.
2. Ghost adds the recommendation to your site’s `/.well-known/recommendations.json` file. Here’s an example of this file:

```
[
  {
    "url": "https://shesabeast.co/",
    "updated_at": "2023-09-22T14:09:32.000Z",
    "created_at": "2023-09-22T14:09:32.000Z"
  },
  {
    "url": "https://makerstations.io/",
    "updated_at": "2023-09-22T14:12:40.000Z",
    "created_at": "2023-09-22T14:12:34.000Z"
  }
]

```

3. Ghost notifies the recommended site via a Webmention. This takes the form of a POST request to the endpoint discovered in step 1 and contains a reference to your site’s `recommendations.json` file. Here’s an example of a request:

```
POST /webmentions/receive/ HTTP/1.1
Host: recommendedsite.com
Content-Type: application/x-www-form-urlencoded
source=https://mysite.com/.well-known/recommendations.json&
target=https://recommendedsite.com/
HTTP/1.1 202 Accepted

```

How Ghost receives a recommendation
-----------------------------------

Your site receives recommendations in the same way as described above but as the recipient.

1. Ghost automatically adds a `link` tag to your publication to inform other sites about your Webmention endpoint. That tag looks like this:

```
<link href="https://myghostsite.com/webmentions/receive/" rel="webmention">

```

2. Ghost listens for Webmentions on this endpoint. Once the incoming recommendation is verified, it’s added to Ghost Admin and you receive a notification.

Updates and removals
--------------------

If you update or remove a recommended site, Ghost sends an updated Webmention about the change. Likewise, your site will be automatically updated whenever it receives an incoming recommendation change.

Theme support
-------------

Theme developers can extend the recommendation feature by using the [`recommendations`](/docs/themes/helpers/recommendations/) and [`readable_url`](/docs/themes/helpers/readable_url/) helpers. See the documentation for these features to learn more.

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

