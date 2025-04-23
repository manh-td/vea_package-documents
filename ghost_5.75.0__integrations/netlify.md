Official Ghost + Netlify Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Zapier](/images/logos/integrations/zapier_hu76c04ccfd9407fb306e44c2572d39c65_1450_50x0_resize_q100_h2_box_3.webp)Zapier](/integrations/zapier/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![GitHub](/images/logos/integrations/github.svg)GitHub](/integrations/github/)
* [![Raycast](/images/logos/integrations/raycast.svg)Raycast](/integrations/raycast/)
* [![Buffer](/images/logos/integrations/buffer_hu2190af463302b978f69c864b508a1040_12312_50x0_resize_q100_h2_box_3.webp)Buffer](/integrations/buffer/)
[Integrations](/integrations/)
/
[Automation](/integrations/?tag=Automation)

A guide to deploying your site with Netlify and using Ghost as a headless CMS for a modern JAMstack experience

If you’re using Netlify to deploy a static site built with Gatsby, Hugo, Jekyll or any other modern framework - then you’ll probably want to trigger rebuilds of your site any time that content is updated using webhooks.

Fortunately, this is easy to set up in just a few steps!

Add a new custom integration
----------------------------

Firstly, add a new custom integration within Ghost Admin

![](/images/integrations/Custom-integrations_hua5a772b7dd6c29477e8fb5550868d86f_309563_2526x0_resize_q100_h2_box_3.webp)

Add Netlify details
-------------------

Just for your own reference, add an integration title, description and icon. Tip: You can save the icon from the top of this page and use that!

![](/images/integrations/netlify-integration-name_hu12eb09c38646964e218d1415eb6398e7_41563_1318x0_resize_q100_h2_box_3.webp)

Add a new Netlify build webhook
-------------------------------

Head over to your Netlify **Build & deploy** settings, and add a new build hook. Name it `Ghost` or the name of your site, and copy the webhook URL.

![](/images/integrations/netlify-build-hooks_hu65b6034babfd33a3ce2a788849ca8a18_58284_1770x0_resize_q100_h2_box_3.webp)

Then, inside your Ghost integration, add a new webhook to be triggered on the **Site changed** event.

![](/images/integrations/netlify-webhook_hue0690946c05fed294863fa954509885e_113741_1572x0_resize_q100_h2_box_3.webp)

Finish creating the webhook, save your integration settings, and you’re all done! Now, whenever anything updates in Ghost - a webhook will be sent to Netlify to trigger a new build of your front end.

Do more with Zapier automation
------------------------------

It’s possible to connect Netlify to many more of your favourite tools and align all of your processes using Zapier. Here are a few ideas to get you started:

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

