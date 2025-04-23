Ghost Docs
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Learn how to update your self-hosted Ghost install to the latest version

Our team [release](https://github.com/TryGhost/Ghost/releases) updates to the open source software every week, and you can find out whether new updates are available any time by running `ghost check-update`.

If you’re already running the latest major version (`5.x`) - update using Ghost CLI with two commands:

1. Run `ghost backup` to generate a full backup of your site data
2. Then, run `ghost update` ✨

Updating to the latest major version
------------------------------------

If you’re not yet on the latest major version, there are two recommended methods for updating your Ghost install, depending on what version you’re currently on, and what type of database you’re using in production. Below is a full breakdown of the the recommended update paths.

**[Updates](/docs/update-major-version/) are recommended for sites that are:**

* Running Ghost version `3.0.0` or higher and are using MySQL in production
* Development sites using any database

**[A full reinstall](/docs/reinstall/) of Ghost is recommended for sites that are:**

* Running on a Ghost version less than `3.0.0`
* Using SQLite3 in production on any Ghost version

| Ghost Version | Database | Update method |
| --- | --- | --- |
| 0.x | Any | [Reinstall](/docs/reinstall/) |
| 1.x | Any | [Reinstall](/docs/reinstall/) |
| 2.x | Any | [Reinstall](/docs/reinstall/) |
| 3.x | SQLite | [Reinstall](/docs/reinstall/) |
| 3.x | MySQL | [Update](/docs/update-major-version/) |
| 4.x | SQLite | [Reinstall](/docs/reinstall/) |
| 4.x | MySQL | [Update](/docs/update-major-version/) |

*If you’re using MariaDB it is recommended to migrate to MySQL 8 - read more about [supported databases](/docs/faq/supported-databases/).*

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

