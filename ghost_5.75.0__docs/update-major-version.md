Ghost Updates: How to update to the latest major version
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Learn how to update your self-hosted Ghost install to the latest major version.

Before updating to a new major version, you must update your site to the latest minor version, e.g if you are on 3.23.0 you need to be on 3.42.9 before updating to v5. You also need to make sure that your setup meets all the latest requirements. This guide will take you through everything step-by-step.

**Updates are recommended for sites that are:**

* Running Ghost version `3.0.0` or higher and are using MySQL in production
* Development sites using any database

> Make sure you can login to Ghost Admin before starting this process.

Switch user
-----------

Switch to the user you used to setup your Ghost install for running Ghost commands:

`sudo -i -u <user>`

Update Node
-----------

Run `node -v` to check your node version.

If less than 14, update node:

* `curl -fsSL [https://deb.nodesource.com/setup_14.x](https://deb.nodesource.com/setup_14.x) | sudo -E bash -`
* `sudo apt-get install -y nodejs`

Update Ghost CLI
----------------

Ghost-CLI is an npm module that can be updated using npm:
`sudo npm install -g ghost-cli@latest`

Update to the latest minor version
----------------------------------

Before updating to a new major version, you must update your site to the latest minor version.

First, perform a preliminary backup of your site: `ghost backup`

Then, update to the latest minor version:

* On Ghost 3.0 run `ghost update v3`
* On Ghost 4.0 run `ghost update v4`

If Ghost is not already running, run `ghost start`, then login to Ghost Admin and check this update has worked before continuing.

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

Read more about how to [manually download your site data](/docs/faq/manual-backup/).

Check MySQL version
-------------------

MySQL 8 is the only supported database in production. Use the following commands to check your database version:

`ghost config database.client`

This should output `sqlite3` or `mysql`. If it says mysql, run `mysql --version` to find the details of your mysql install.

If you’re already running MySQL 8, proceed to the next steps. Otherwise, [read more](/docs/faq/supported-databases/) about how to update or migrate your database if you’re using any other version.

Check for theme update requirements
-----------------------------------

To ensure your publication’s front-end doesn’t break, you may need to make some changes to your theme.

Ghost CLI will output a report with any theme incompatibility errors and recommendations, or you can upload your theme directly to the **[GScan](https://gscan.ghost.org/)** theme testing tool.

Update to the latest major version
----------------------------------

> Before updating to a new major version, review [breaking changes](/docs/changes/) that might affect you.

Once you’re running the latest minor version, it’s time to update to the latest major version.

Finally, you can now run the update command again to upgrade to the latest major version:

`ghost update`

---

Troubleshooting
---------------

The most common reason for an update failure is running out of memory, so make sure you have enough RAM or swap configured in advance.

Find your Ghost folder
----------------------

Run the `ghost ls` command anywhere on your server to find the details of your Ghost install.

### Download your backup

If you need to move your backup between machines, run the `scp` command on the machine you want to move the file *to:*

`scp user@123.456.789.123:/var/www/ghost/backup-from[...].zip ~/Desktop`

### Force update

If an update fails you can start by forcing a retry to attempt the upgrade a second time.

`ghost update --force`

### Rollback

If something goes wrong, you can always revert to the previous stable version of Ghost.

`ghost update --rollback`

If you’re still having trouble, start by searching the **[Ghost forum](https://forum.ghost.org/)** to see if your issue has come up before.

### Downgrade Node

If you need to downgrade Node, these are the steps:

```
sudo apt-get remove -y nodejs
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs

```
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

