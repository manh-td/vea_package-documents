Official Ghost + PayPal Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![ChartMogul](/images/logos/integrations/chartmogul_hu01c73d47915043033a3a07dcbb830fa7_3078_50x0_resize_q100_h2_box_3.webp)ChartMogul](/integrations/chartmogul/)
* [![Churnbuster](/images/logos/integrations/churnbuster_hudae337c0f674707d1840f4c514d865a7_15531_50x0_resize_q100_h2_box_3.webp)Churnbuster](/integrations/churnbuster/)
* [![Mailchimp](/images/logos/integrations/mailchimp_hucb75d06be88e6331905252c3cff4ebbc_32058_50x0_resize_q100_h2_box_3.webp)Mailchimp](/integrations/mailchimp/)
* [![FirstPromoter](/images/logos/integrations/firstpromoter_hu13330b4d32004712e337efa3113c94c8_6190_50x0_resize_q100_h2_box_3.webp)FirstPromoter](/integrations/firstpromoter/)
[Integrations](/integrations/)
/
[Members](/integrations/?tag=Members)

Embed payment buttons from PayPal directly into your content in Ghost and collect payments for your membership content

If you’re using PayPal as a payment gateway, then you may want to integrate PayPal directly with your Ghost site. It’s possible to embed PayPal buttons on any Ghost site, and you can add new PayPal customers as [Members](/help/members-introduction/) in Ghost, to give them direct access to premium membership content.

This guide explains how to create and embed PayPal buttons on a Ghost site using sensible HTML embeds, and how to automatically add new customers as members of your Ghost site.

Create a PayPal business account
--------------------------------

In order to create PayPal buttons, you’ll need an active [PayPal business account](https://www.paypal.com/bizsignup/#/checkAccount). You can either create one from scratch, or convert an existing personal PayPal account to a business account.

Create a PayPal button
----------------------

Navigate to the Seller Tools area of your PayPal dashboard and locate the [PayPal Buttons](https://www.paypal.com/us/smarthelp/article/how-do-i-add-a-paypal-payment-button-to-my-website-faq3629) option:

![PayPal business dashboard - seller tools](/images/integrations/Seller-Tools_hu25a26b096a4f30432e96748ed4f28607_295960_2226x0_resize_q100_h2_box_3.webp)

From here, you can decide whether to create a “Buy Now” button for one-off payments, or a “Subscribe” button for recurring subscriptions.

![Buy button options in PayPal for business](/images/integrations/Create-a-PayPal-button_hu6814c9b4f9605758252aee9a5883266d_207695_2000x0_resize_q100_h2_box_3.webp)

You can embed as many PayPal buttons as you like on your Ghost site, but it’s recommended to keep your pricing structure simple to avoid confusing potential customers. The most popular pricing configuration are two plans for monthly and yearly subscriptions.

In order to create this pricing structure, you’ll need to create two **[Subscribe](https://www.paypal.com/us/brc/article/setting-up-recurring-payments-for-business)** buttons in PayPal. The first step allows you to select a name, currency, amount and billing cycle for your Subscribe buttons:

![Creating a subscription buy button in PayPal](/images/integrations/Creating-a-button-1_hu49600b3b7aada8976e6fa36b3fe2b257_170329_1550x0_resize_q100_h2_box_3.webp)

**Tip:** In the advanced settings area, you can optionally redirect people to a custom URL on your site when checkout is complete (such as your site’s homepage, or a custom welcome page), or if someone leaves before completing payment.

![Creating a Buy Button with PayPal - Advanced Options](/images/integrations/Advanced-settings_hud8f35c35e960991c9c49734f2369eefc_123822_1534x0_resize_q100_h2_box_3.webp)

Use the button embed code
-------------------------

Once you’ve created your button(s), use the embed code provided to add the buttons to your website:

![Embed code for PayPal Buy Buttons](/images/integrations/Button-embed-code_hu545cb2b16b4ff03691cf1352130785e4_192045_1706x0_resize_q100_h2_box_3.webp)

You can use this code anywhere on your Ghost site, by creating an HTML card in the editor:

![Adding an HTML card in the Ghost editor](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

It’s also possible to use the PayPal embed code directly in Ghost theme files too, which is useful if you’re creating a custom `/subscribe/` page within your theme, for example.

Create a Zapier automation
--------------------------

Connect your PayPal account using a [Zapier](/integrations/zapier/) automation to give your customers automatic access to member only content on your site.

Zapier automatically creates new Members in Ghost each time someone makes a successful sale from your PayPal buttons:

![PayPal > Ghost Zapier Integration](/images/logos/integrations/zapier_hu76c04ccfd9407fb306e44c2572d39c65_1450_200x0_resize_q100_h2_box_3.webp)

This is useful if you’d prefer to use PayPal as a payment provider instead of [Stripe](/docs/members/subscriptions/), or if you want to create one-off payments as well as subscriptions.

Turn free member sign up off
----------------------------

The final step is to turn **Allow free member signup** off in your Members settings inside Ghost:

![Allow free member signup in Ghost](/images/integrations/Free-member-signup-option_hu4d4c24b02b278021147ebd6cee6a682b_17915_1372x0_resize_q100_h2_box_3.webp)

This means you can use the **[Members only](/help/protected-content/)** content access level to publish premium content, that only your paying Members who subscribed via PayPal will be able to access 🎉

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

