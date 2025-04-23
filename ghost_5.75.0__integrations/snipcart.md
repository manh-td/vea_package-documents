Official Ghost + Snipcart Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Stripe](/images/logos/integrations/stripe.svg)Stripe](/integrations/stripe/)
* [![Shopify](/images/logos/integrations/shopify.svg)Shopify](/integrations/shopify/)
* [![Gumroad](/images/logos/integrations/gumroad_hu6bde769c9f344d2ffa2f93e996bedfac_8155_50x0_resize_q100_h2_box_3.webp)Gumroad](/integrations/gumroad/)
* [![X-Cart](/images/logos/integrations/x-cart_hu6401096c4b2553ff2ba250a4636b896f_18022_50x0_resize_q100_h2_box_3.webp)X-Cart](/integrations/x-cart/)
[Integrations](/integrations/)
/
[Ecommerce](/integrations/?tag=Ecommerce)

Build a fully customisable ecommerce solution into your Ghost publication with a Snipcart integration

[Snipcart](https://snipcart.com/?utm_source=ghost&utm_campaign=integration) is a shopping cart solution that allows you add an ecommerce store to your Ghost publication.

Using the code injection feature within Ghost, it’s entirely possible to integrate with Snipcart directly and start selling ecommerce products from your site.

Sign up for a Snipcart account
------------------------------

Snipcart offer two payment options: 2% fees on each purchase or fixed fees. Check out their [pricing](https://snipcart.com/pricing) page and sign up for your Snipcart account. Alternatively, you can try out the software for free in test mode.

Add the default stylesheet
--------------------------

In Ghost you can inject code across your entire site or on an individual post or page. Snipcart requires two piece of code to be implemented across your site so that you’re able to manually add products on posts or pages.

To do this, use the global code injection feature:

![](/images/integrations/Code-Injection_hua2612c8704298bf9729475fd66c3ac83_266598_2356x0_resize_q100_h2_box_3.webp)

The first code snippet is the Snipcart default stylesheet. Copy this code and paste it into the **Site Header** section:

```
<link rel="stylesheet" href="https://cdn.snipcart.com/themes/v3.2.1/default/snipcart.css" />

```

Add the Snipcart script with your API key
-----------------------------------------

Next, copy the Snipcart script below, and paste this into the **Site Footer** section.

```
<script async src="https://cdn.snipcart.com/themes/v3.2.1/default/snipcart.js"></script>
<div hidden id="snipcart" data-api-key="YOUR_PUBLIC_API_KEY"></div>

```

Replace `YOUR_PUBLIC_API_KEY` with the API key that can be found in your Snipcart dashboard under **Account** → **API key**.

Hit save and your site is fully integrated.

Add products to your Ghost publication
--------------------------------------

Any HTML element can become a Snipcart product, but the most common way to add products to posts or pages in Ghost is to add a buy button using HTML cards in the Ghost editor.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

Here’s an example of Snipcart button code with all of the required product attributes:

```
<button class="snipcart-add-item"
  data-item-id="starry-night"
  data-item-price="79.99"
  data-item-url="/paintings/starry-night"
  data-item-description="High-quality replica of The Starry Night by the Dutch post-impressionist painter Vincent van Gogh."
  data-item-image="/assets/images/starry-night.jpg"
  data-item-name="The Starry Night">
  Add to cart
</button>

```

Alternatively, you can place your Snipcart code directly into your [Theme](/docs/themes/) or custom [front-end](/docs/jamstack/) if you’re using Ghost as a Headless CMS.

When visitors click buy buttons on your site it will open up the Snipcart ecommerce experience without having to leave your website. Check out the [demo](https://demo.snipcart.com/) to see it in action.

It’s also possible to customise your products further with custom fields. For more information, check out the Snipcart [documentation](https://docs.snipcart.com/v3/setup/products).

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

