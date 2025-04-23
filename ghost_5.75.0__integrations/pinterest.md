Official Ghost + Pinterest Integration
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

Add Pin it buttons on images in your posts and make it easy for your visitors to pin your content on Pinterest

Give your readers a new way to engage with your content and share your work using these integrations for Pinterest.

Add the Pinterest save button
-----------------------------

Pinterest provide a simple `pinit.js` script which you can copy and paste into global code injection in Ghost, to automatically add a Pinterest save button to all images in your content.

Copy this script:

```
<script src="//assets.pinterest.com/js/pinit.js"
type="text/javascript" async defer
data-pin-hover="true"></script>

```

Paste it into the **Site header** section of code injection in Ghost Admin:

![](/images/integrations/code-injection-footer_hu60aa3e6a295a12ce4e040df79eb67285_140173_2000x0_resize_q100_h2_box_3.webp)

Hit save — now your visitors will now see a Pinterest save button on each image when hovering over it. For more information, check out the [Pinterest widget builder](https://developers.pinterest.com/tools/widget-builder/?).

Create a pinnable image with Pinterest attributes
-------------------------------------------------

Many creators and bloggers include a **pinnable image** with [Pinterest attributes](https://business.pinterest.com/en/blog/pin-it-button-technical-tune-up-5-tips-to-make-sharing-from-your-site-better) applied to the top or the bottom of a post. This allows visitors to use Pinterest browser extensions to pin your content along with a pre-defined description, URL and an optional alternative image size.

This integration method allows you to optimise your pinned images using a Markdown card in the editor. First, add a new Markdown card and add your pinnable image into the card:

![](/images/integrations/image-markdown-url_hu23e426fe408ef551dec22cc6fcc2c3e0_31508_1658x0_resize_q100_h2_box_3.webp)

Once the image is uploaded, grab the **Ghost.io URL** for your image and copy it to your clipboard. This URL can be used it to populate the following HTML code inside the same Markdown card:

```
    <img src="https://example.ghost.io/content/images/2020/08/example.jpg"
    data-pin-url="https://example.com"
    data-pin-media="https://example.ghost.io/content/images/2020/08/example.jpg"
    data-pin-description="Enter a description about your pinnable image here"/>

```

* `img-src` — paste the URL of your pinnable image here
* `data-pin-url` — enter the URL that you’d like the pinned image to link to (usually the post that you’re adding the image to)
* `data-pin-media` — optionally set a different pinned media version of an image (for example, a different image size or a vertical image instead of horizontal)
* `data-pin-description` — write your custom description that you’d like to be pinned with your image here

Once you’ve customised this code snippet, your Markdown card is ready to go:

![](/images/integrations/final-markdown_huc68b8d6f3e1d6325e594eca58cb196af_60840_1628x0_resize_q100_h2_box_3.webp)

Pin this
--------

Here’s an example of what the end result looks like. Use your Pinterest browser extension to share the below image and see it populate with the custom attributes we added using the method above.

![](/images/integrations/pinterest_hu1c29bcc04084fd235b138cfb3be567bf_518481_2000x0_resize_q100_h2_box.webp)

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

