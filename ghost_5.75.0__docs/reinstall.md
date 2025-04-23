How to reinstall Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Learn how to update to the latest version of Ghost by creating a new install.

A full reinstall of Ghost is recommended for:

* Sites running Ghost `0.x`, `1.x`, `2.x`
* Sites using SQLite3 in production on any Ghost version

Switch user
-----------

Switch to the user you used to setup your Ghost install for running Ghost commands:

`sudo -i -u ghost-mgr`

Update Node
-----------

Run `node -v` to check your node version.

If less than 14, update node:

* `curl -fsSL [https://deb.nodesource.com/setup_14.x](https://deb.nodesource.com/setup_14.x) | sudo -E bash -`
* `sudo apt-get install -y nodejs`

Update Ghost CLI
----------------

Ghost-CLI is an npm module that can be updated using npm.

`sudo npm install -g ghost-cli@latest`

Update to the latest minor version
----------------------------------

Before updating to a new major version, you must update your site to the latest minor version.

First, perform a preliminary backup of your site: `ghost backup`

Then, update to the latest minor version using: `ghost update`. This command will inform you of a more specific command to run.

Make a full backup
------------------

When performing manual updates it’s a good idea to make frequent backups, so if anything goes wrong, you’ll still have all your data.

Once you’re running the latest minor version, make a full backup using the following command to generate a download of your site’s data:

`ghost backup`

This creates a backup zip file of everything you need, including:

* Your content in JSON format
* A full member CSV export
* All themes that have been installed including your current active theme
* Images, files, and media (video and audio)
* A copy of `routes.yaml` and `redirects.yaml` or `redirects.json`

Read more about how to [manually download your site data](/docs/faq/manual-backup).

Disconnect Stripe
-----------------

*Skip this step if your Ghost site is not connected to Stripe.*

If you have Ghost connected to a Stripe account in *Live mode,* it needs to be disconnected in order for you to be able to reconnect on your new installation.

![Screenshot of content export in Ghost Admin](/images/docs/install/stripe-connection_hub376459ffe40b4ad66b7082f6966fac4_293097_2290x0_resize_q100_h2_box_3.webp)

If you have paid members, or complimentary members with Stripe customer IDs, you need to delete these members from Ghost before disconnecting Stripe is possible.

![Screenshot of content export in Ghost Admin](/images/docs/install/filter-members_hu0f4d0735bb9ab23a49c8adf254de8a98_18345_2098x0_resize_q100_h2_box_3.webp)

Filter your members list by member status to get a full list of members with paid and complimentary subscriptions, or delete your full members list (which has already been backed up) from the Member dashboard in Ghost Admin.

> When deleting members with a Stripe subscription from Ghost, the subscriptions in Stripe are not affected, unless you explicitly opt to cancel them. Do not cancel the subscriptions.

When all members with subscriptions are removed from Ghost, you can successfully disconnect Stripe.

Once this is done, log into Stripe and delete any [webhooks](https://dashboard.stripe.com/webhooks) related to the old connection:

![Screenshot of content export in Ghost Admin](/images/docs/install/stripe-webhooks_hu7a110a240dae732aa17e84a1b4005ae4_43075_1878x0_resize_q100_h2_box_3.webp)

Install Ghost
-------------

Once all your data is backed up, it’s time to spin up a fresh install of Ghost to migrate your publication over to. Follow the detailed [install guides](/docs/install/) to create a new install of Ghost.

When your install is complete, follow the steps to setup your new site.

Import your backup data
-----------------------

Once you have installed and setup a new site, it’s time to migrate your data.

If you used `ghost backup` to generate a backup zip, these are the steps to restore your data. If you did a manual backup, refer to the [manual backup guide](/docs/faq/manual-backup).

1. Starting in your ghost folder, `unzip` the backup into the `content` folder:
   `sudo unzip /path/to/backup-from-[backup-name].zip -d content`
2. Make sure the files have the right permissions:
   `sudo chown -R ghost:ghost content`
3. Restart Ghost:
   `ghost restart`
4. Import your content:
   `ghost import content/data/content-from[backup-name].json` - *This requires your username and password, and can also be done on the labs page in Ghost Admin.*

Reconnect Stripe
----------------

*Skip this step if you’re not using Stripe for paid subscriptions.*

To import paid members, Ghost needs to be connected to Stripe in Live mode *before* you import your members.

Make sure to connect Ghost to **the same Stripe account** you were using on your old installation - learn more about how to connect a Stripe account [in this guide](/help/setup-members/#connect-a-stripe-account).

Import members
--------------

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

