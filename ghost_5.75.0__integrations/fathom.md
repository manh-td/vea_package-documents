Official Ghost + Fathom Analytics Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Plausible](/images/logos/integrations/plausible_hubdd59c639a2e80e3d62ecbddcb793d1c_52957_50x0_resize_q100_h2_box_3.webp)Plausible](/integrations/plausible/)
* [![Google Analytics](/images/logos/integrations/google-analytics_hu4d123172e6791cf5e37b9720bc0d3de1_1524_50x0_resize_q100_h2_box_3.webp)Google Analytics](/integrations/google/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![ChartMogul](/images/logos/integrations/chartmogul_hu01c73d47915043033a3a07dcbb830fa7_3078_50x0_resize_q100_h2_box_3.webp)ChartMogul](/integrations/chartmogul/)
* [![Churnbuster](/images/logos/integrations/churnbuster_hudae337c0f674707d1840f4c514d865a7_15531_50x0_resize_q100_h2_box_3.webp)Churnbuster](/integrations/churnbuster/)
[Integrations](/integrations/)
/
[Analytics](/integrations/?tag=Analytics)

Want simple, privacy-focused analytics for your Ghost publication? Ghost integrates with Fathom Analytics using straightforward code injection.

[Fathom Analytics](https://usefathom.com) empowers people and businesses to take control of their data and privacy with simple, GDPR compliant website analytics for bloggers and businesses who care about privacy.

Grab the Fathom embed code
--------------------------

When you create a new site in your Fathom Analytics account, you’ll be given **HTML embed code**, which you can copy to your clipboard:

![](/images/integrations/fathom-embed_huc5daf92b83a729c64e5c9e278a0c3b29_87786_1038x0_resize_q100_h2_box_3.webp)

Use Ghost code injection
------------------------

In Ghost you can inject code across your entire site or on an individual post or page. Since Fathom Analytics needs to track analytics across your entire site, we’ll use the global code injection feature which can be found in the Ghost Admin settings menu.

![](/images/integrations/code-injection-footer_hu60aa3e6a295a12ce4e040df79eb67285_140173_2000x0_resize_q100_h2_box_3.webp)

Fathom Analytics requires the tracking code to be in `<header>` of each page on your site, so paste it into the **Site Header** and hit save.

Your site is now fully integrated with Fathom Analytics and you can now enjoy privacy-focused aggregate data for your website, to see your most popular pages and referrers.

Bypass ad-blockers (optional)
-----------------------------

This next step is optional, but recommended. Since Fathom Analytics is a privacy focused analytics tool, it’s possible to create a custom domain to bypass ad-blockers and improve your website analytics.

To do this, head to **Domains** in your Fathom Analytics account and enter your custom domain. You’ll be given some DNS records:

![](/images/integrations/dns-fathom_hu9bfd17c64b255f485c5fc427702a191b_78462_742x0_resize_q100_h2_box_3.webp)

Add these records to your DNS settings and then wait for everything to resolve, you can check the progress from the **Custom domains** page:

![](/images/integrations/custom-domain-fathom_hu8431173975e56573ae5dc5329368909d_64594_1014x0_resize_q100_h2_box_3.webp)

Once your custom domain is active, you’ll receive an email. The final step is to update the site-wide tracking code you pasted in to Ghost code injection.

Head to **Sites** and view the code for your domain, you’ll see it has now been updated to include your custom domain in the script:

![](/images/integrations/fathom-embed-custom_hub27422f9698c78afb7768a64e642cb63_98764_1040x0_resize_q100_h2_box_3.webp)

Replace your HTML Embed code in Ghost code injection, hit save, and you’re done.

Your site data is now fully integrated with Fathom Analytics using a custom domain, which means your data will be much more accurate. For more advice, check out the official [guide](https://usefathom.com/support/custom-domains) for custom domains, or contact the Fathom Analytics team for support!

Create goals (optional)
-----------------------

The last thing you may want to do is to create goals in your Fathom Analytics dashboard, which can be implemented into your HTML Embed code, or directly into your Ghost theme, to track anything that isn’t a normal page view.

For example, you could track the following things as goals:

* Button clicks on a form
* Success page after a purchase
* Clicks on specific links

This is especially useful if you’re using the Members feature in Ghost, and want to track the conversions of your visitors to free or paid members. To find out more about implementing goals, check out this [support guide](https://usefathom.com/support/goals).

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

