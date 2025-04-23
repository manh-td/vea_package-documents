How to migrate data from Ghost to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Migrate from a self-hosted instance to Ghost(Pro) with this guide

If you're a Ghost(Pro) customer, our team may be able to help you migrate your content and subscribers. Learn more about our [Concierge service](/concierge/).

This guide will walk you through the process of migrating from a self-hosted Ghost instance on your own server to Ghost(Pro).

Prerequisites
-------------

If your self-hosted site is running an older major version of Ghost, you may need to update. Check the latest [version of Ghost on GitHub](https://github.com/TryGhost/Ghost/releases), and follow this [upgrade guide](/docs/update/).

Back up your data
-----------------

The first step towards moving from your own self-hosted Ghost instance to Ghost(Pro) is to retrieve all of your data from your server to your local machine. It’s best to do this first, to ensure you have a backup in place.

> The commands in this guide assume you followed our [Ubuntu guide](/docs/install/ubuntu/) to set up your own instance. If you used another method, you’ll need to adapt the paths in the commands to suit.

### Exporting content

Log into Ghost Admin for your self-hosted in production and navigate to the **Labs** view, and click **Export** to download your content. This will be `.json` file, with a name like `my-site.ghost.2020-09-30-14-15-49.json`.

![content import export](/images/docs/migration/self-hosted/ghost-content-import-export_hu272562aa500e83b9baeec6c17282ce1a_25089_1628x0_resize_q100_h2_box_3.webp)
### Routes and redirects

Staying on the **Labs** page, click **Download current redirects** to get your redirects file. This will be called `redirects.yaml` (or `redirects.json` depending on your Ghost version). If you’re using custom routes, click **Download current routes.yaml** to get your `routes.yaml` file.

![routes redirects](/images/docs/migration/self-hosted/ghost-route-redirects_hu954a63ee77a86db320db7d009e6fb2e9_29801_1628x0_resize_q100_h2_box_3.webp)
### Themes

Navigate to the **Design** view, and click the **Download** button next to the Active label export your current theme. This will be a `.zip` file. Optionally, if you have other themes that you’d like to save, download them and back them up.

![themes settings](/images/docs/migration/self-hosted/ghost-themes-settings_hu3b859fed207678d52a22902f80176aaf_12909_1628x0_resize_q100_h2_box_3.webp)
### Images

To download your images, you’ll need shell access to your server. If you’re unable to gain shell access to your current web host, you may need to contact their support team and ask for a zip of your images directory.

Once you’re logged in to your server, `cd` to the `content` directory:

```
cd /var/www/ghost/content

```

And then `zip` the `images` directory with all its contents:

```
zip -r images.zip images/*

```

Ensure your `images` folder only contains images. Any other file types may cause import errors.

Now we need to get that zip file from your server onto your local machine:

```
scp user@123.456.789.123:/var/www/ghost/content/images.zip ~/Desktop/images.zip

```

The folder structure should look like this, with `images` being the only top-level folder once unzipped:

![images in finder](/images/docs/migration/self-hosted/images-in-finder_huf248f9006ca4711e6e56a11852458172_99427_1260x0_resize_q100_h2_box.webp)

Uploading to Ghost(Pro)
-----------------------

Once you’ve retrieved all of these exports, you can upload them to Ghost(Pro) in the same order.

### Content

Log into your new Ghost(Pro) site, and head to the **Labs** view. Next to the **Import content** header, select your content `.json` file and click **Import**.

![user import successful](/images/docs/migration/self-hosted/ghost-import-successful_huade8b63d13532484da2176e269d2dc02_38287_1628x0_resize_q100_h2_box_3.webp)
### Routes and Redirects

Staying on the **Labs** view, click **Upload redirects JSON**, then select your `redirects.json` file to upload it. Then click **Upload routes YAML**, select your `routes.yaml` file to upload that.

### Themes

Head over to the **Design** view, and click **Upload a theme**, select your theme `.zip` file, and activate it.

![activate theme](/images/docs/migration/self-hosted/ghost-theme-upload_huf4a027a768e71e6bd93af4733d14943e_23711_1226x0_resize_q100_h2_box_3.webp)
### Images

The final step is to upload your images. The best way to approach this depends on how big your `images.zip` file is. A large file will take longer to upload and process.

If your file is less than 500mb, you can upload this zip in the same way you uploaded your content JSON file. If the file is larger, it’s recommended to split it into multiple smaller files, whilst retaining the folder structure.

If you have a large image directory or encounter any errors, contact support so we can help upload your images.

---

Summary
-------

Congratulations on moving to Ghost(Pro). All that’s left to do is check over your content to ensure everything works as expected.

By hosting your site with us, you directly fund future product development of Ghost itself and allow us to make the product better for everyone 💘

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

