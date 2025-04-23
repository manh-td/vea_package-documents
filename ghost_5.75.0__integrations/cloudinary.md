Official Ghost + Cloudinary Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Zapier](/images/logos/integrations/zapier_hu76c04ccfd9407fb306e44c2572d39c65_1450_50x0_resize_q100_h2_box_3.webp)Zapier](/integrations/zapier/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Netlify](/images/logos/integrations/netlify_hu1b4209e1158b533f7cea6d5e486e460d_36182_50x0_resize_q100_h2_box_3.webp)Netlify](/integrations/netlify/)
* [![GitHub](/images/logos/integrations/github.svg)GitHub](/integrations/github/)
* [![Raycast](/images/logos/integrations/raycast.svg)Raycast](/integrations/raycast/)
[Integrations](/integrations/)
/
[Utility](/integrations/?tag=Utility)

Deliver automatically optimised images using Cloudinary and Ghost in tandem, either on-the-fly or with full media library

[Cloudinary](https://cloudinary.com) is a full-stack media optimisation platform which automates processing and optimisation of images and video to help deliver them efficiently to your readers. Cloudinary is a paid service, however it does come with a free tier which is more than sufficient for most people.

There are a couple of ways to integrate it with Ghost.

Automatic optimisation with fetch
---------------------------------

Ghost has [automatic responsive image sizes](/docs/themes/assets/) built in by default, allowing you to output images at different sizes depending on the needs of your theme. If you prefer to use an externally hosted media solution, though, Cloudinary can do the same thing via API.

Cloudinary’s [Fetch remote images](https://cloudinary.com/documentation/fetch_remote_images) service is a simple way to deliver externally optimised images. For example, if you have 2000px cover images on all your posts, but on your homepage you want to display 200px thumbnails which are properly resized and optimised, then Cloudinary can take care of that part for you automatically just by prefixing your feature images with a special URL.

### Edit your theme files

First, you’ll need to sign up for a Cloudinary account and then edit your Ghost theme files with updated image URLs. In this example, we’ll look at the partial file used for all post archives in Ghost’s default theme, [Casper](https://github.com/tryghost/casper).

On [line 4](https://github.com/TryGhost/Casper/blob/main/partials/post-card.hbs#L4) of `/partials/post-card.hbs` we can see the code used to output the post’s feature image in post lists. This piece of code is used on the home page, tag archives, and author archives - so any changes made here will update everywhere.

```
{{#if feature_image}}
    <a class="post-card-image-link" href="{{url}}">
    <div class="post-card-image" style="background-image: url({{feature_image}})"></div>
    </a>
{{/if}}

```

To have Cloudinary resize this image automatically to a more appropriate size, all you have to do is replace the `{{feature_image}}` helper with your Cloudinary URL + an absolute image path. For example: `https://res.cloudinary.com/YOURUSERNAME/image/fetch/w_600,h_400,c_fit/{{img_url feature_image absolute="true"}}`

Cloudinary will automatically resize the image to fit within a 600x400px box, maintaining the original aspect ratio, and return the image as normal. You can customise how you want the image to be modified based on your own needs, using Cloudinary’s [image transformation features](https://cloudinary.com/documentation/image_transformations).

The final code in your theme should look like:

```
{{#if feature_image}}
    <a class="post-card-image-link" href="{{url}}">
    <div class="post-card-image" style="background-image: url(https://res.cloudinary.com/YOURUSERNAME/image/fetch/w_600,h_400,c_fit/{{img_url feature_image absolute="true"}})"></div>
    </a>
{{/if}}

```

Don’t forget to replace `YOURUSERNAME` with your Cloudinary username. Once you’ve saved and uploaded your theme, your images will be automatically delivered by Cloudinary’s CDN and resized on the fly.

Full Cloudinary storage adapter
-------------------------------

By default, Ghost stores any images uploaded to Ghost Admin locally to its filesystem, and delivers them via the same Ghost front-end service which delivers Ghost themes. However, it’s also possible to replace this layer entirely using a custom storage adapter, to upload and serve images directly to/from external services.

Using a storage adapter, images are uploaded directly to Cloudinary and integrated into its media library, unlocking a larger quantity of advanced image manipulation features which can be useful for people with image-heavy sites who need a lot of processing – or people who want a detailed media management user interface to manage their library of assets.

**[Ghost-Storage-Cloudinary](https://github.com/eexit/ghost-storage-cloudinary)** is a heavily tested open source storage adapter which contains detailed instructions about how to configure it.

Do more with Zapier automation
------------------------------

It’s also possible to connect Cloudinary to more of your favourite tools with Zapier to make it more useful and powerful to your workflow.

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

