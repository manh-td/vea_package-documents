Migrating to Ghost - Developer Troubleshooting
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

There are a number of ways in which an import file may trigger an **Error** or a **Warning** particularly if the JSON file was created by a third-party tool.

### Error

When Ghost detects an error, the import will be cancelled, no information is imported and there should be a suitable error message to help you debug the problem. This also means there may be multiple errors in your import file but you will only see a single error during the import process.

An Error or warning should contain a relevant message on why the import was not successful along with a the relevant JSON entry that caused the issue where applicable.

An example of an error would be a user that contains a null email field:

![Import Failed](/images/docs/migration/import-failed_huf428cfe26909636680c1789263b6e36a_21350_1317x0_resize_q100_h2_box_3.webp)
### Warning

The import may generate multiple warnings. These are issues that may want to know about but are not significant enough to prevent the data being imported. Examples of this include a duplicate user (either duplicated in your JSON file or matching an existing user) or a post linked to an unknown user.

![Import Warnings](/images/docs/migration/import-warnings_huabac39385072c3bd3050630215f15f1f_43188_1179x0_resize_q100_h2_box_3.webp)
##### On this page

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

