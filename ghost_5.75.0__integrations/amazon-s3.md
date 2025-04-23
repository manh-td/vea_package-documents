Official Ghost + Amazon S3 Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Google Drive](/images/logos/integrations/google-drive_hu913f42107a23b424c040d16e6adfc3c2_11844_50x0_resize_q100_h2_box_3.webp)Google Drive](/integrations/google-drive/)
* [![Azure Storage](/images/logos/integrations/azure_hu42cc40de4f1b54c43e3e8229c0490bab_4957_50x0_resize_q100_h2_box_3.webp)Azure Storage](/integrations/azure-storage/)
* [![Google Cloud](/images/logos/integrations/google-cloud-storage_hue39ea26f91f3c3431542b099a688c192_7359_50x0_resize_q100_h2_box_3.webp)Google Cloud](/integrations/google-cloud-storage/)
* [![Backblaze](/images/logos/integrations/backblaze_hu6907e4e24ad4353924a32ef30dccedaf_12839_50x0_resize_q100_h2_box_3.webp)Backblaze](/integrations/backblaze/)
[Integrations](/integrations/)
/
[Storage](/integrations/?tag=Storage)

Integrate secure image storage into Ghost using Amazon S3 - deployed using a custom storage adapter

[Amazon S3](https://aws.amazon.com/s3/) is an object storage service for developers that offers secure, high-performance storage at scale. For Ghost sites with a high volume of image assets, it’s possible to override the default storage method and use Amazon S3 to store all images that are dropped into Ghost Admin.

There are a few ways to integrate Amazon S3 with Ghost.

Full Amazon S3 storage adapter
------------------------------

By default, Ghost stores any images uploaded to Ghost Admin locally to its filesystem, and delivers them via the same Ghost front-end service which delivers Ghost themes. It’s possible to replace this layer entirely using a custom storage adapter.

A custom storage adapter allows Ghost to upload and serve images directly to/from external services like Amazon S3. Here are some widely tested, open source storage adapters for Amazon S3 that have comprehensive setup guides:

* **[ghost-s3-compat](https://github.com/spanishdict/ghost-s3-compat)**
* **[ghost-storage-adapter-s3](https://github.com/colinmeinke/ghost-storage-adapter-s3)**

When using a storage adapter in Ghost, your images are uploaded directly to Amazon S3 and integrated into its media library, allowing you to use their service directly to manage your image assets.

Do more with Zapier automation
------------------------------

It’s also possible to connect Amazon S3 to more of your favourite tools with Zapier to make it more useful and powerful to your workflow.

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

