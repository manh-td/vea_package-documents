Official Ghost + Facebook Integration
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
[Social](/integrations/?tag=Social)

Ghost works with Facebook automatically in multiple ways to ensure that your content is fully optimised for the world’s largest social network

Integrated structured data
--------------------------

Ghost contains integrated global settings and user settings to associate your site, users, and individual posts with specific [Facebook](https://facebook.com) users and pages via automatic [Open Graph](http://ogp.me/) meta tags. This allows for rich data to appear whenever people share links to your site, as well as association with your official accounts.

---

Custom Facebook cards
---------------------

Fine-grained control over the structured data for each post is also available via the post settings menu of every post and page within Ghost, so you can always determine exactly what gets shared.

![](/images/integrations/facebook-custom-card_hu6dba4eb5215d8b28692b69153bcefe1b_629586_1588x0_resize_q100_h2_box_3.webp)

---

Embed posts in your content
---------------------------

All content from Facebook works with Ghost automatically via our OEmbed integration. All you have to do is paste a URL!

### Copy the URL of the status

Grab the URL of the status you’d like to embed into your post or page

![](/images/integrations/facebook-url_hu92b09222cf89b8fe479b34a9ea5f18e2_130474_1586x0_resize_q100_h2_box_3.webp)
### Paste it into the Ghost editor

When you paste it into the Ghost editor it’ll be automatically transformed into a rich embed of the status you selected

![](/images/integrations/card-render_hu2c78047432353a9629cd84520e241107_6034_1694x0_resize_q100_h2_box_3.webp)
### Publish your post

That’s all there is to it! Ghost interacts with Facebook via their [OEmbed](https://oembed.com/) API in order to retrieve all the correct settings automatically and serve your status in the best way possible.

---

Use Facebook comments with Ghost
--------------------------------

If you have an active Facebook community, then you may also want to use Facebook comments for your Ghost posts and pages to keep the conversation all in one place. You can do this using the official [Facebook Comments](https://developers.facebook.com/docs/plugins/comments/) plugin.

### Copy the Facebook comments code

Click on the `Get Code` button on the [Facebook Comments](https://developers.facebook.com/docs/plugins/comments/) plugin settings page, and select the Facebook Page you would like to associate with your site comments. We recommend disabling the `Collect Analytics` feature.

![](/images/integrations/facebook-comments-code_hub4cf02c43391be450d2cba3acc35479b_121167_1496x0_resize_q100_h2_box_3.webp)

Next, copy the provided code in **Step 2** and add it to Footer section of Ghost’s **Code Injection** settings area.

![](/images/integrations/code-injection-footer_hu60aa3e6a295a12ce4e040df79eb67285_140173_2000x0_resize_q100_h2_box_3.webp)
### Paste the final comment code into post.hbs

A good spot for this code is right after the content in the template file.

![](/images/integrations/theme-replace-comments-helper_hu0c29dd7fb66b77e2f53cbfd3a1b64bea_249652_2058x0_resize_q100_h2_box_3.webp)

Replace the the comments helper with your code

Replace the `comments` helper code with the following (instead of the code provided by Facebook in **Step 3**):

```
<div class="fb-comments" data-href="{{url absolute="true"}}" data-numposts="10"></div>

```

Then save the file, upload a fresh copy of your theme, and restart Ghost. Comments should now be loading on your site.

---

Do more with Zapier
-------------------

As always, you can power up your site even further using [Zapier](https://zapier.com). If you’re already using Facebook, you might also like some of these complimentary automations:

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

