Official Ghost + Google Analytics Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Plausible](/images/logos/integrations/plausible_hubdd59c639a2e80e3d62ecbddcb793d1c_52957_50x0_resize_q100_h2_box_3.webp)Plausible](/integrations/plausible/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![ChartMogul](/images/logos/integrations/chartmogul_hu01c73d47915043033a3a07dcbb830fa7_3078_50x0_resize_q100_h2_box_3.webp)ChartMogul](/integrations/chartmogul/)
* [![Churnbuster](/images/logos/integrations/churnbuster_hudae337c0f674707d1840f4c514d865a7_15531_50x0_resize_q100_h2_box_3.webp)Churnbuster](/integrations/churnbuster/)
* [![Search Console](/images/logos/integrations/google-search-console.svg)Search Console](/integrations/google-search-console/)
[Integrations](/integrations/)
/
[Analytics](/integrations/?tag=Analytics)

Want deep analytics for your Ghost publication? Ghost integrates with Google Analytics using simple code injection.

Get in-depth site metrics and gain a deeper understanding of your readers with a seamless integration for site-wide tracking. Google Analytics is the most widely used platforms for analysing site data in Ghost, and it only takes a few minutes to setup!

Set up a new Google Analytics property
--------------------------------------

When you set up a new [Google Analytics](https://analytics.google.com) account, follow the prompts to create a new property for your Ghost site.

If you’re already using Analytics, navigate to the admin area from the cog button in the bottom left corner, and click the blue `Create Property` button.

![](/images/integrations/ga-create-property_hu8492aa4797f22262f3953193091199f8_65753_1035x0_resize_q100_h2_box_3.webp)

Next, add a data stream and choose `Web`.

![](/images/integrations/ga-choose-a-platform_hu4319d5ff4a4e9c05cba253c9f6e69f4d_75070_1920x0_resize_q100_h2_box.webp)

Enter the URL for your website (like demo.ghost.io) and a stream name (like “My Ghost Site”). Choose the options you want to enable and click `Create stream`.

![](/images/integrations/ga-add-a-data-stream_hu4319d5ff4a4e9c05cba253c9f6e69f4d_82054_1920x0_resize_q100_h2_box.webp)

Get the tracking code
---------------------

Once your stream is active, you’ll see an option to add a global site tag.

![](/images/integrations/ga-copy-code_hu4319d5ff4a4e9c05cba253c9f6e69f4d_115142_1920x0_resize_q100_h2_box.webp)

Copy the provided code snippet to your clipboard.

Use Ghost Code Injection
------------------------

In Ghost, you can inject code across your entire site or on an individual post or page. Since Google Analytics needs to track user behavior across your entire site, we’ll use the global code injection feature, which can be found in the Ghost Admin `Settings` menu.

![](/images/integrations/ga-code-injection_hu4319d5ff4a4e9c05cba253c9f6e69f4d_101249_1920x0_resize_q100_h2_box.webp)

Google Analytics requires the tracking code to be added to `<head>` of each page on your site, so paste the copied code into the **Header** section and hit **Save**.

Confirm Google Analytics is working
-----------------------------------

Your site is now fully integrated with Google Analytics. In Google Analytics, go to **Reports** in sidebar, click on **Realtime**, and refresh your site. Your activity on the dashboard confirms that Google Analytics is working on our site!

![](/images/integrations/ga-dashboard_hu4319d5ff4a4e9c05cba253c9f6e69f4d_119938_1920x0_resize_q100_h2_box.webp)

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

