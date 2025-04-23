Official Ghost + Placid Integration
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
* [![Twitter / X](/images/logos/integrations/twitter_hu844154aeedc321ce71128e37fdffff46_151721_50x0_resize_q100_h2_box_3.webp)Twitter / X](/integrations/twitter/)
* [![Buffer](/images/logos/integrations/buffer_hu2190af463302b978f69c864b508a1040_12312_50x0_resize_q100_h2_box_3.webp)Buffer](/integrations/buffer/)
* [![Imgur](/images/logos/integrations/imgur_huf9be42a5da9d192330acb6d6dee2dbd2_5740_50x0_resize_q100_h2_box_3.webp)Imgur](/integrations/imgur/)
[Integrations](/integrations/)
/
[Social](/integrations/?tag=Social)

Instantly make your content more shareable with automatic social images.

[Placid](https://placid.app) generates Facebook and Twitter card images for your publication from custom templates. Design your share images once, and let Placid automatically deliver them for all your posts and pages.

---

Create a Ghost project in Placid
--------------------------------

After signing up for Placid, create a new Ghost project.

![](/images/integrations/New-project-placid_hu2e36fd9e048d9bc15fd4417dba767407_72774_1308x0_resize_q100_h2_box_3.webp)

Create a template for your images
---------------------------------

**Add a new template** in the templates tab of your Placid project to design custom templates for your social card images with a drag and drop editor, or choose from the preset designs.

![](https://lh6.googleusercontent.com/c8R31gbPdLOgbGVna6rrqqysSjAbedu3qVx02RDW7dLAgscgZplXJRuUtL_pQom6aTzubseGLUdgISMYJ2I8QwTf9sPZl971AJtYNtZJLnEidHJMzieSVxZxHHj1-fsrnwp3b0tC)

Design your template to fit your publication’s brand. It’s best to give meaningful layer names, and uncheck the option **Element is dynamic** in the layer settings if a layer won’t contain dynamic content.

![](https://lh4.googleusercontent.com/ovC59B-IVc-3wJXtal8qucysWiBeijqTiIR6EW6CqJiBq6GsW-rkURkoK6K1Slgr_APlQkrwGxfxjO4Q0Ssew6rhs49hZ3-vVZI88wNb5LB9YCi4kVBJIBCYfjcmk4d7gSpsiyIJ)

Connect your publication
------------------------

To connect your Ghost publication to Placid, create a custom integration in Ghost first. Go to **Settings > Integrations** and add a custom integration. Name it Placid, or another name of your choice.

Within the integration, you will see an Admin API Key and an API URL. Copy them into the Placid project settings.

![](https://lh6.googleusercontent.com/kWRAAk3g8j4N3thjihrhfyXuZsxrXQ70Aslo-9jv3OG4Pmb9tTDP5Hs5fFZTvb0wupmgI6nnvC2omAYy7FFnoI-O5qmfB_pYIErAYx2v-DjSfs-PWi_8U8WnZU5_kTIHj4cEJQSr)

Add webhooks
------------

If you want Placid to create images whenever you create or edit content, you need to add two webhooks to your new integration in Ghost.

Copy the **Ghost** **Webhook URL** from your Placid project settings:

![](/images/integrations/webhooks_hu82c8ae62fa5cf5d370237ee7df9fa89b_28184_745x0_resize_q100_h2_box_3.webp)

Paste this into the **Target URL** field of both webhooks, and set the event to **Post updated** on one, and **Page updated** on the other.

![](https://lh5.googleusercontent.com/q9zWU2VFwCDg6yzKMF82hXLIHvd1Vpz9UJKre_xYF29oxB2jXs-DzGSEG-Dvm3658aakVU3S8bWpNra5uoOlN3phJ5C-_1u14_5OnIAS6LaJsOfCtISxSWJV_d6z77XJ4dhmrTTe)

Create an automation action
---------------------------

With Placid actions, you can set up image automations.

**Add a new action** in the **Actions tab** of your Placid project, give it a title and choose the interval in which it should be repeated – the Continuous (Webhook) setting is recommended, but you can choose to only run it manually as well.

Select the content type you want to create images for: Ghost posts or pages. (Create two separate actions if you want images for both!)

Then you can select the template you want to use and map the content of your Ghost publication to your template’s elements.

![](https://lh4.googleusercontent.com/WGtfksoKHcQ5MqPA2tVUN_6GByK1dOKdUitdSQsYeCsx4RqcDNayjH3kS5p9dyywJ5b1OrAc9Ryfyye5fo8Mu2J3GR1Nl1naYLpeT97eam4lhWeLMKiY2s4uUFxCUY1YsN3bMc4D)

Run your automation
-------------------

After creating your action, run it manually for the first time to generate images for all your existing content.

Placid won’t overwrite any custom social card images you have previously set, and will only send images to empty fields. In case you want to replace all your old images, or have redesigned your template and want to regenerate your images choose the option **run & overwrite**.

To preview how your posts and pages look when they are shared, you can view the Twitter and Facebook card settings in Ghost. Placid also offers a [browser extension](https://socialsharepreview.com/browser-extensions) that quickly shows you the social card previews while you browse.

You’re now all set up and no longer have to worry about social sharing images 🙌

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

