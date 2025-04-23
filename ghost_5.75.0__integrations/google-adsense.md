Official Ghost + Google AdSense Integration
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
* [![Viral Loops](/images/logos/integrations/viral-loops_hub6ff46da9b9c6679630be7af5b33f005_12635_50x0_resize_q100_h2_box_3.webp)Viral Loops](/integrations/viral-loops/)
[Integrations](/integrations/)
/
[Marketing](/integrations/?tag=Marketing)

Introduce a new revenue stream to your Ghost publication with a direct Google AdSense integration that places ads on your site that are relevant to your audience

[Google AdSense](https://www.google.com/adsense/start/) is a popular advertising solution for publishers who want to add additional streams of revenue to their content. It is a free platform which unlocks the ability to place customisable advertisements across your site and get paid when ads are seen or clicked.

Getting started with AdSense involves injecting code into your Ghost site, either using the code injection tool in Ghost Admin, or for more fine-grained control, in your site’s theme layer or front-end. Here’s how to get started with Google AdSense!

Sign up for Google AdSense
--------------------------

Head to [AdSense](https://www.google.com/adsense/) and use a valid Google account to get signed up. Initially, you’ll have to enter some details such as a valid address so that you can get paid, your domain, and some personal details. Once you’re in, you will then be given a code snippet which you can use to get your first ads up and running.

### Account activation

If this is a brand new account, it can take 24 hours or more for it to be activated once you’ve completed the initial setup:

![](/images/integrations/Activating-your-account_huc80116887c786253f4bfb0d4cd2aad23_43881_1866x0_resize_q100_h2_box_3.webp)

You will need to wait for this to be done before you are able to customise your ads and build up your campaigns. Note that if you’re using **Ghost(Pro)** then you will need to have a custom domain in place to integrate with Google AdSense.

> Tip: Once your account is setup, try using [Google Ad Manager](https://admanager.google.com/home/) to manage your campaigns and keep track of how your ads are performing.

Grab the Auto ads code snippet
------------------------------

If you want to get things set up in the simplest form - you can use the Auto ads code snippet (which is provided at setup or can be found in your account):

![](/images/integrations/Connect-your-AdSense-account-1_hu6bcec712bb1ae09cbe22712d3b1fcfda_116090_1868x0_resize_q100_h2_box_3.webp)

This code is intended to be used across your site and should be placed between the `<head>` and `</head>` tags, which you can achieve in Ghost Admin via the site header code injection feature:

![](/images/integrations/Code-Injection_hua2612c8704298bf9729475fd66c3ac83_266598_2356x0_resize_q100_h2_box_3.webp)

You can also enter your code on specific pages or posts instead using code injection within the editor:

![](/images/integrations/Page-code-injection_huc7e1bbddce74644ea97713e2fe5ad9c5_66855_2000x0_resize_q100_h2_box_3.webp)

AdSense [Auto ads](https://support.google.com/adsense/answer/7477845?hl=en&ref_topic=28893) technology means that Google will determine the best placement for your ads and use the available inventory on your site to display them.

Display ads in specific areas of your site using Ad units
---------------------------------------------------------

The more likely outcome is that you would like full control over the placement of your AdSense ads. There are several ways to achieve this using [Ad units](https://support.google.com/adsense/answer/181950?hl=en&ref_topic=28893) in AdSense.

Ad units can be created in your AdSense account and unlike Auto ads, they are designed to be used on specific pages and placed within the `<body>` and `</body>` tags. Once you have created a new Ad unit, copy and paste the code:

![](/images/integrations/Ad-Units-ad-code_hu773679facb0a8fa81f273797a1ba8671_280995_1286x0_resize_q100_h2_box_3.webp)

If you want to display ads on a specific post or page where the content exists in Ghost Admin, it’s possible to use an HTML card within the editor to display ad blocks in-line with your content:

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

On the other hand, you can also insert your AdSense code into the appropriate template files within your theme. This is useful if you want to specify exactly where ads appear within your site’s content. Common places include at the top or bottom of the page, and in the sidebar.

![](/images/integrations/Choose-where-you-want-your-ads-to-appear_hud7b1bec48e310b0266b7e3709f3d5bd8_341547_2000x0_resize_q100_h2_box_3.webp)

Locate the template file where you want to insert ad unit code. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add code right after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost.

Alternatively, you can insert your Ad units code in any area within a [Handlebars theme](/docs/themes/) template file, or in a custom [front-end](/concepts/front-end/).

Implement your AdSense code
---------------------------

Whether you’re using Auto ads where Google AdSense decides where to display the ads, or Ad units where you determine where your ads appear, once you’ve implemented your code in any of the ways shown above, you’ll start to see the ads appearing within a couple of hours.

All ad customisation, such as determining which ads are shown or to apply other advanced features such as [Custom Search Ads](https://support.google.com/adsense/answer/1239255?hl=en&_ga=2.44881699.685131210.1551069478-1593523937.1533635312), can be done within the AdSense dashboard. Find out more about how to customise your ads using the [AdSense help resource](https://support.google.com/adsense/?hl=en#topic=1250102).

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

