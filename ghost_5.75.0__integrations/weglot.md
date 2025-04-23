Official Ghost + Weglot Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Instagram](/images/logos/integrations/instagram_hua2b50eb6f034ade3c8b1b1bbd03165af_809353_50x0_resize_q100_h2_box_3.webp)Instagram](/integrations/instagram/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![YouTube](/images/logos/integrations/youtube_hud6a8b6adc63a1086de676a1c87304581_6257_50x0_resize_q100_h2_box_3.webp)YouTube](/integrations/youtube/)
* [![Twitter / X](/images/logos/integrations/twitter_hu844154aeedc321ce71128e37fdffff46_151721_50x0_resize_q100_h2_box_3.webp)Twitter / X](/integrations/twitter/)
* [![Senja](/images/logos/integrations/senja_hubcd17ef19d159794c0e0686efdaaa9ba_14692_50x0_resize_q100_h2_box_3.webp)Senja](/integrations/senja/)
[Integrations](/integrations/)
/
[Content](/integrations/?tag=Content)

Translate your Ghost site and go from local to global in minutes with Weglot.

[Weglot](https://weglot.com/) provides a powerful solution to make your Ghost website multilingual and manage your translations. It will detect all your website content and allow you to translate it in any language.

There are two ways to integrate your Ghost site with Weglot. The first is to configure your [custom domain](/help/using-custom-domains/) DNS settings and inject a JavaScript snippet across your site to display translated content on a dedicated subdomain like `es.yoursite.com`.

Alternatively, you can inject the JavaScript snippet on its own, to dynamically translate your posts and pages directly in the visitors browser. This guide will explain how to started with your translations!

Create a Weglot account
-----------------------

To get started, [create your account](https://dashboard.weglot.com/register):

![weglot signup page](https://lh6.googleusercontent.com/CdG2sRZEkSn74qqWXpe52Q7TR6KlhfevLZVubaNYX325l1hDV8ULGiFt9_48ljNwtQ0B5yyki96UvxO69vTBbBO7AMPey49IkbAdRDXHcbW9yjJYEarMSKggsQaxnQy4eXtO6adr)

On the next page, select “other in the technology list:

![weglot project creation page](https://lh6.googleusercontent.com/EtTnEz4MqRs_bxv46dupGbpesXcW_JUN_BCRACnEfGXhUWcBAu3S5OcFut3uDTmfBhlh241iXDbC7Jm9mwxXgunEmEKTyT-u_Tva8tPa5a6yTAhw2i-N4Fk3C1wK0-0JryJEgC5t)

Add your domain URL
-------------------

Add the custom domain URL for your Ghost site, and select the original language your content is written in, as well as which translated languages you’d like to implement:

![integrating weglot with ghost cms](https://lh6.googleusercontent.com/TOlpGFy98zytV-TzLsE_4NvKO3ZwJ_MEW4Ewgdx9ov1JLqM8A3MYf32q40AkpLTwm7uMf7cj3A5wfNLMGLI75Tnt951gyjRDMFVEqj5_ienU3m2AhnqGhFK6_bfrl1iN1duDATms)

If you’re not using a custom domain for your Ghost site, you can choose to only use the JavaScript integration. Leave your Domain URL blank, pick your languages and skip to step 4 of this guide! Don’t worry, you can always add a custom domain and change this later on.

Add CNAME entries to your DNS settings
--------------------------------------

Go to your DNS provider to add the two CNAME entries provided by Weglot:

![DNS entries for weglot + ghost integration](https://lh5.googleusercontent.com/Dl2uNhLB4OxzLLS7Vvuv1_012cUv9QVYrHDwpKBqBcscsk7N3TBP71z6Awevd9jSYvEE5gmIJDuEf_Sra9L7Lq6Tz31UyfsqgI8l6G45KVMef0xvQTfqCkUVxbDFNZ3PfYUFXKlo)

This will allow you to have a dedicated subdomain for each translated language such as `fr.yoursite.com` – this is a great solution for a fully optimised website in all languages.

Add the JavaScript snippet
--------------------------

Navigate to the Weglot Javascript code snippet and copy it:

![example of a weglot javascript snippet](https://lh3.googleusercontent.com/OKVhqn-CWxcJnVcOaizx0NomMs48AYyOW-JJNH5mAoOKoj8MGFAlmaHFUVJo5JEmzJZ0IwgEBv4aF7G6Sue1AB2ek5e0Uh0sM7-mJWaQyVBxInMuvOufkFYmIS6dc0nzEe3bbqQX)

Paste your snippet into Ghost admin > Settings > Code injection > Site header and save.

![site-wide code injection in Ghost](/images/integrations/Code-Injection_hua2612c8704298bf9729475fd66c3ac83_266598_2356x0_resize_q100_h2_box_3.webp)

If you don’t have a custom domain and skipped to this step from the beginning of this article, this step is all you’ll need. Your translated content will be created dynamically on the page without unique subdomain support.

Final steps
-----------

That’s it – your site is now multilingual! When you visit your Ghost publication, you’ll see the Weglot language switcher at the bottom right of your site. It’s possible to change this to suit your needs using custom styling.

> 💡Tip: If you’re using static pages within your Ghost theme and would like these to be translated, you’ll also need to include the Weglot script in your theme files.

Click on the translated language you selected and discover your translated blog!

Here’s a live [example demo:](https://www.weglot-translate-ghost.com/)

![](https://lh6.googleusercontent.com/CQqHBsIDuAYM_JhggvNNwfT_TCbTCjl1CCFejmnv2nnF0MSbC1tdsTltGDP20Mq9Vq9z1sNVwkBEKNd-eOyDU5_hUP63JhJ5-7rO1OmgbljZdOdzTM9Cmiyx_GExF_0pdTM1xWbd)

Your first round of automatic translation is provided by Weglot and saves you time managing translated content. It’s possible to edit your translations, or order professional translations from within the [Weglot dashboard](https://dashboard.weglot.com).

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

