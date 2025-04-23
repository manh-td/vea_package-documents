Official Ghost + Google Ad Manager Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![FirstPromoter](/images/logos/integrations/firstpromoter_hu13330b4d32004712e337efa3113c94c8_6190_50x0_resize_q100_h2_box_3.webp)FirstPromoter](/integrations/firstpromoter/)
* [![CookieYes](/images/logos/integrations/cookieyes_hu2a52b95f92072c1126fd208573722580_14497_50x0_resize_q100_h2_box_3.webp)CookieYes](/integrations/cookieyes/)
* [![Search Console](/images/logos/integrations/google-search-console.svg)Search Console](/integrations/google-search-console/)
* [![Google AdSense](/images/logos/integrations/gaslogo_hu0d3b27cbc6f7330e2e6bcbec3aae3479_3987_50x0_resize_q100_h2_box_3.webp)Google AdSense](/integrations/google-adsense/)
[Integrations](/integrations/)
/
[Marketing](/integrations/?tag=Marketing)

Place customisable ads across your Ghost publication with a Google Ad Manager integration

[Google Ad Manager](https://admanager.google.com/) can help you manage your advertising business and grow your revenue streams with user-driven tools that scale to the needs of your publication. It is an efficient, hosted ad serving platform that streamlines ad management on your site, giving you full control of your brand.

Here’s how to get started with Google Ad Manager and Ghost.

Sign up for Google Ad Manager
-----------------------------

In order to [sign up](https://admanager.google.com/) for Google Ad Manager, you will need to have an approved Google [AdSense](/integrations/google-adsense/) account.

![](/images/integrations/Sign-up-for-Google-Ad-Manager-1_hu30fce06688ee9bb9bdd2bb978b831c9a_40753_1701x0_resize_q100_h2_box_3.webp)

Create Ad Units
---------------

Next up, build your ads by [creating Ad Units](https://support.google.com/admanager/answer/177203?hl=en) in the Google Ad Manager dashboard. For further information about Ad Manager elements, read this [Google help doc](https://support.google.com/admanager/answer/6012282?hl=en&ref_topic=7519088) which explains how inventory and delivery works.

You can also [enable AdSense](https://support.google.com/admanager/answer/1670087?hl=en) for your Google Ad Manager network, or specific Ad Units. ‌

Inject generated code on your Ghost publication
-----------------------------------------------

Once you have completed the necessary configuration for your ads in the Google Ad Manager dashboard, [generate your ad tags](https://support.google.com/admanager/answer/177207?hl=en) to place on your site.

Google Ad Manager gives you full control over how you serve ads on your site. With Ghost, there are a few different ways to implement the generated code and unique ad tags.

Code injection
--------------

If you would like to place a snippet of code across your site, you can use the Code Injection feature. This will inject the code across all of your posts and pages in Ghost in the `<head>` or `<foot>`:

![](/images/integrations/Code-Injection_hua2612c8704298bf9729475fd66c3ac83_266598_2356x0_resize_q100_h2_box_3.webp)

To inject generated code for a specific ad slot, you can also use code injection on individual posts or pages from within the editor:

![](/images/integrations/Page-code-injection_huc7e1bbddce74644ea97713e2fe5ad9c5_66855_2000x0_resize_q100_h2_box_3.webp)

Or you could use an HTML card within the editor to place ad slots inline with your content:

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

Place ads in specific areas of your site
----------------------------------------

The more likely outcome is that you would like full control over the placement of your ads within your theme. Popular places to display ads include in the sidebar or at the top and bottom of a page.

It’s entirely possible to paste your ad slot generated code anywhere in the theme layer in Ghost, which makes it possible to build designated ad slots across all posts that fits in neatly with the design of your publication.

To do this, locate the template file where you want to insert your ad unit code.

One spot for this code is right after the content in the template file. In Ghost’s official themes, add slot code right after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

‌

Once you’re done, save your updated files and upload a fresh copy of your theme. This can be done from the design menu in Ghost Admin. Don’t forget to [restart](/docs/ghost-cli/#ghost-restart) Ghost if you’re self-hosting.

Install an ads.txt file
-----------------------

Using an ads.txt file is not a requirement but is advised in order to protect your brand and declare authorised sellers.

> [Authorized Digital Sellers, or ads.txt](https://iabtechlab.com/ads-txt/), is an initiative to improve transparency in programmatic advertising. Publishers can create their own ads.txt files to identify who is authorised to sell their inventory. The files are publicly available and crawlable by buyers, third-party vendors, and exchanges.

An ads.txt file can be [created via Google Ad Manager](https://support.google.com/admanager/answer/7544382) or manually, and must be uploaded to your root domain. To do this with Ghost, simply move your `ads.txt` file to your theme’s root directory, and then update the active theme on your site. This will ensure your file is available publicly.

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

