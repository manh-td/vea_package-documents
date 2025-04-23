Configuration for using Cloudflare with Ghost self-hosted - Ghost Developers
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

If you’ve added Cloudflare to your self-hosted Ghost publication and find that Ghost Admin doesn’t load after updates you may run into some errors in the JavaScript console:

### Error

Open developer tools to check for errors in the JavaScript code:

`TypeError: n.item is not a function or Uncaught SyntaxError: Unexpected string`

### To fix

It is recommended that you add a page rule which turns off some RocketLoader, mirage2 and autominify for the path `/ghost*`, so these features don’t affect the Ghost admin panel.

![Using Cloudflare with Ghost](/images/docs/faq/cloudflare-ghost_hu3292e1ab34393a3f83860fc03720b502_39786_791x0_resize_q100_h2_box_3.webp)

This solution is for developers who are maintaining a self-hosted instance of Ghost. If you’re on Ghost(Pro) both nginx and CloudFlare are configured as standard and you don’t need to do anything.

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

