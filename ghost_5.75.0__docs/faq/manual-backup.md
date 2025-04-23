How to backup your self-hosted Ghost install - Ghost Developers
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Learn how to backup your self-hosted Ghost install

When performing manual updates it’s always recommended to make a full backup of your site first, so if anything goes wrong, you’ll still have all your data.

The fastest way to perform a backup is to use Ghost CLI to automatically generate a zip file containing all of your site data using the `ghost backup` command.

If you need to perform a manual backup of your data, the following guide walks you through all of the steps.

### Export content

Log into Ghost Admin, navigate to the **Labs** view, and click **Export** to download all content. This will be a `.json` file, with a name like `my-site.ghost.2020-09-30-14-15-49.json`.

![Screenshot of content export in Ghost Admin](/images/docs/faq/download-content_hua52806e65860e327ac2a06c0b285d95b_21881_1722x0_resize_q100_h2_box_3.webp)
### Download routes and redirects

Staying on the **Labs** page, click **Download current redirects** to get your redirects file. This will be called `redirects.yaml` or `redirects.json` depending on your Ghost version. If you’re using custom routes, click **Download current routes.yaml** to get your `routes.yaml` file.

![Screenshot of routing and redirects export in Ghost Admin](/images/docs/faq/download-routes-redirects_hub0b987ca0988930e4cb2d6cb22c57b87_19346_1738x0_resize_q100_h2_box_3.webp)
### Download themes

Navigate to the **Design** settings page, and navigate to the themes section to download your active theme, and any other themes you want to store. This will be a `.zip` file.

![Screenshot theme install and download page in Ghost Admin](/images/docs/faq/download-themes_hu358079c312968754f2a55fd07e1e0d75_497694_2332x0_resize_q100_h2_box_3.webp)
### Copy images, files and media

To download images and media, you’ll need shell access to your server. If you’re unable to gain shell access to your current web host, you may need to contact their support team.

When logged in to your server, `cd` to the `content` directory:
`cd /var/www/ghost/content`

Then, `zip` the `images` and other file storage directories with their contents
`zip -r content-files.zip images/ files/ media/`

Then, to move the zip files from your server onto your local machine.
`scp user@123.456.789.123:/var/www/ghost/content/content-files.zip ~/Desktop/content-files.zip`

### Export members

Export all members in one CSV file from the Members dashboard in Ghost Admin.

![Screenshot of member download in Ghost Admin](/images/docs/faq/export-members_hua4d8503095287f368fad3a048eba2785_16838_1018x0_resize_q100_h2_box_3.webp)

---

Restoring your data from a manual backup
----------------------------------------

The following steps explain how to restore data from a manual backup.

### Copy images, files and media

All images, files and media need to be copied over to your new install.

After doing that, run this command to fix permissions:
`sudo chown -R ghost:ghost content`

Once this is complete, restart Ghost:
`ghost restart`

### Import content

To begin the content migration, head to the **Labs** section of Ghost Admin and import the `ghost.json` backup which you exported earlier.

### Upload routes and redirects

From the Labs page, import the `routes.yaml` and `redirects.yaml` files that you previously downloaded for your backup data.

### Upload theme

Next, upload your theme in the **Design** settings page of Ghost Admin to get your site looking the same way it did before.

### Reconnect Stripe

*Skip this step if you’re not using Stripe for paid subscriptions.*

To import paid members, Ghost needs to be connected to Stripe in Live mode before you import your members.

Make sure to connect Ghost to **the same Stripe account** you were using on your old installation - learn more about how to connect a Stripe account in [this guide](/help/setup-members/#connect-a-stripe-account).

### Import members

With Stripe connected, you can now import your members CSV file. You’ll receive an email notification when the import process has completed.

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

