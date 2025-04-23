Official Ghost + Google AMP Integration
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
[Marketing](/integrations/?tag=Marketing)

Ghost comes with a built-in integration for Google AMP which transforms all of the content on your site into a lightning-fast AMP version ⚡

The open source AMP project is led by Google, and provides a way for publishers to generate lightweight versions of their content for a faster and smoother user experience.

In Ghost, the AMP integration utilises the AMP framework inside a single Handlebars template: `amp.hbs`. This template transforms each post on your site into an AMP version which can be accessed by adding `/amp` to the end of any URL.

Ghost has a beautiful default AMP template which displays all of your content, images, galleries, code and bookmark cards for mobile devices.

![](/images/integrations/Group-1_hua6166be9797ff492a1e9a4f4e0ad4b5f_1272031_2000x0_resize_q100_h2_box_3.webp)

Here's an [AMP page demo](https://demo.ghost.io/welcome/amp/)

Enabling AMP in Ghost
---------------------

The AMP integration in Ghost is enabled by default, but if you prefer not to use the feature then you can turn it off in the settings within Ghost Admin. When enabled, all posts on your publication will automatically have an AMP page, with a canonical link to ensure the page is correctly identified by the search engines and no duplicate content issues are found.

AMP Analytics
-------------

If you’d like to track your AMP performance in Google Analytics, you can integrate AMP Analytics in a few simple steps, by entering your Google Analytics Tracking ID in your integrations settings:

![](/images/integrations/AMP-analytics_hu107118c92961b1282c287d2b2d8adec9_112394_1850x0_resize_q100_h2_box_3.webp)

Hit save and you’ll have successfully installed AMP Analytics 🎉

Customise the template with your own styles
-------------------------------------------

AMP in Ghost can be styled to suit your brand and theme too! Since the Ghost theme layer is entirely customisable, that means you can also customise the way your AMP pages are rendered by including a custom `amp.hbs` template file in your theme.

To access any post rendered using the `amp.hbs` template on your site, add `/amp/` to the end of any post URL on your publication. The parent post also has a canonical link to it’s AMP equivalent.

### Template

The amp context always uses the `amp.hbs` template. Ghost will look for this template within your theme files and use this by default.

The template structure is as follows:

```
.
├── /assets
|   └── /css
|       ├── screen.css
|   ├── /fonts
|   ├── /images
|   ├── /js
├── default.hbs
├── index.hbs [required]
└── post.hbs [required]
└── amp.hbs [optional]
└── package.json [required]

```

Check out the [default template](https://github.com/TryGhost/Ghost/blob/3d989eba2371235d41468f7699a08e46fc2b1e87/ghost/core/core/frontend/apps/amp/lib/views/amp.hbs) in full.

### Data

The `amp` [context](/docs/themes/contexts/) provides access to the post object which matches the route. As with all contexts in Ghost, all of the `@blog` global data is also available.

When outputting the post, you can use a block expression (`{{#post}}{{/post}}`) to drop into the post scope and access all of the attributes. See a full list of [attributes](/docs/themes/contexts/post/#post-object-attributes/).

### AMP features

AMP consists of three different parts:

* AMP HTML
* AMP JS
* Google AMP Cache

AMP has many restrictions for optimal performance. For example, JavaScript can only be used in certain circumstances, CSS must be in the correct tags inside of the `<head>` section, and AMP HTML must be used instead of common HTML.

If you are making adjustments to your `amp.hbs` file, follow the documentation provided on the official [AMP docs](https://www.ampproject.org/) site.

Edited `amp.hbs` templates can be updated in your theme by uploading a .zip of your updated theme in Ghost admin.

### Debugging AMP

Since AMP has strict restrictions, it’s important to ensure that your code passes AMP validation. The quickest way to do this is to add `#development=1` to the AMP URL, and check for validation errors in your browser console.

### Helpers

Because the `amp` context is using the `post` data, you can use almost every [post helper](/docs/themes/contexts/post/#helpers) inside of the `{{#post}}{{/post}}` block expression. In addition to this, there are three helpers especially for `amp` which are described below.

#### `{{amp_ghost_head}}`

This helper belongs just before the `</head>` tag in `amp.hbs` and outputs structured data in JSON/LD, Facebook Open Graph and Twitter cards, as well as an RSS URL path. It is a simplified version of `{{ghost_head}}` for AMP.

#### `{{amp_components}}`

This helper can exist just before the `</head>` tag in `amp.hbs` and can output the necessary javascript if your content contains a `.gif`, an `<iframe>` or an `<audio>` tag.

#### `{{amp_content}}`

This helper transforms post content into valid AMP HTML.

* `<img>` transforms to `<amp-img>`
* `.gif` transforms to `<amp-anim>`
* `<iframe>` transforms to `<amp-iframe>`
* `<audio>` transforms to `<amp-audio>`

#### `{{amp_style}}`

This helper belongs just before the `</style>` tag in `amp.hbs` and outputs the `--ghost-accent-color` variable to be used elsewhere in the AMP template styles. This allows themes to use the user-selected accent colour in a custom AMP template.

#### `{{img_url}}` helper

There are special requirements for using the `{{img_url}}` helper. It must be wrapped in an `<amp-img>` tag and must provide a `width` and `height` property. This only works for post images.

Validate your template in the console
-------------------------------------

There is an effective way to validate your AMP pages as you go directly in the console by adding `#development=1` to any AMP URL.

This is a useful way to ensure any customisations you make to your AMP template are valid and your AMP content is rendering correctly.

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

