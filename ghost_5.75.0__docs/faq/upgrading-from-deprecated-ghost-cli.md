Updating from a deprecated Ghost-CLI - Ghost Developers
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

When managing your self-hosted Ghost publication using the recommended `ghost-cli` tooling, you should update your CLI version. If you are using a deprecated version and need to update in order to update or manage your Ghost site, some extra steps may be required.

Use the following troubleshooting guide if you run into issues because you are using a deprecated version of the Ghost-CLI.

### Upgrading from <=1.1.3

Ghost-CLI 1.2.0 added a fix, and Ghost-CLI 1.3.0 added a migration to solve some ssl renewal problems with letsencrypt and nginx. After upgrading `ghost-cli` run `ghost migrate` manually.

### Upgrading Ghost installs that used Ghost-CLI <1.0.0

If you installed Ghost using a pre-1.0.0 version of Ghost-CLI (any version less than 1.0.0, including alphas, betas and release candidates), you’ll need to run some commands manually to update your Ghost installation to one compatible with version 1.0.0 of the CLI.

From 1.0.0 onwards, installs are be automatically migrated. Once you’ve run the steps below, edit the `.ghost-cli` file in your ghost instance folder and replace the version noted by “cli-version” with “1.0.0”.

### You installed your Ghost instance with CLI versions between v1.0.0-beta.6 and 1.0.0

To update your instance to one that is 1.0.0 compatible, backup your data, then run these commands from within your ghost instance folder:

1. `crontab -e`, then in the editor remove the line that has `ghost ssl-renew` on it
2. Then run: `rm -f ./system/files/*.conf`
3. If you previously `setup ssl` then run: `ghost setup nginx ssl`. If you setup Ghost without ssl run: `ghost setup nginx`

### You installed your Ghost instance with CLI versions older than v1.0.0-beta.6

You’ll need to reinstall your Ghost instance from scratch following the update guide for [Ghost 0.x versions](/docs/faq/update-0x/).

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

