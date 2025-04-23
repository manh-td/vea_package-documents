Hosting a Ghost publication - Fully-managed PaaS & self-hosted
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

A short guide to running Ghost in a production environment and setting up an independent publication to serve traffic at scale.

Ghost is open source software, and can be installed and maintained relatively easily on just about any VPS hosting provider. Additionally, we run an official PaaS for Ghost called [Ghost(Pro)](/pricing/), where you can have a fully managed instance set up in a couple of clicks. All revenue from Ghost(Pro) goes toward funding the future development of Ghost itself, so by using our official hosting you’ll also be funding developers to continue to improve the core product for you.

Ghost(Pro) vs Self-hosting
--------------------------

A common question we get from developers is whether they should use our official platform, or host the codebase on their own server independently. Deciding which option is best for you comes with some nuance, so below is a breakdown of the differences to help you decide what will fit your needs best.

|  | Ghost(Pro) | Self-Hosting |
| --- | --- | --- |
| 🎛 Product features | Identical | Identical |
| ⚙️ Base hosting cost | From **$9**/mo | From **$10**/mo |
| 🌍 Worldwide Fastly CDN | Included | From **$50**/mo |
| 💌 Email newsletter sending | Included | From **$35**/mo |
| 📦 Full site backups | Included | From **$5**/mo |
| 🖼️ Built-in image editor | Included | From **$12**/mo |
| 💵 Payment processing fees | 0% | 0% |
| 🖥 Install & setup | ✅ | Manual |
| 🔄 Weekly updates | ✅ | Manual |
| 🚧 Server maintenance & updates | ✅ | Manual |
| 🔒 SSL Certificate | ✅ | Manual |
| ⚠️ Threat & uptime management | ✅ | ❌ |
| 🥊 Enterprise-grade security | ✅ | ❌ |
| 🔀 Custom edge routing policies | ❌ | ✅ |
| 👩‍💻 Direct SSH & DB access | ❌ | ✅ |
| 🔨 Ability to modify core | ❌ | ✅ |
| 🚑 Ghost product support | Email | Forum |
| ❤️ Where your money goes | New features in Ghost | 3rd party companies |

### Which option is best for me?

**Self-hosting** is the best choice for teams who are comfortable managing servers, databases and Node.js apps who want full control over their environment. There’s more complexity involved, and you have to signup-for and pay for your own Mailgun account (email delivery) and CDN service (performance and scale) — but ultimately more flexibility around exactly how the software runs. For people sending lots of email newsletters, self-hosting generally works out to be more expensive compared to Ghost(Pro), but for people who aren’t using email functionality, it can work out to roughly the same price.

[See self-hosting guides & instructions →](/docs/install/)

**Ghost(Pro)** is the best choice for most people who are focused on using the Ghost software, and don’t want to spend time managing servers. Setting up a new Ghost site takes around 20 seconds, and after that all weekly updates, backups, security and performance are managed for you. If your site ever goes down, our team gets woken up while you sleep peacefully. In most cases Ghost(Pro) ends up being lower cost than self-hosting once you add up the cost of the different service providers.

[See Ghost(Pro) pricing & plans →](/pricing/)

**TLDR:** If you want the easiest, cheapest option: Ghost(Pro) is probably your best bet. If you have a technical team and you want maximum control and flexibility, you’ll get more out of self-hosting.

---

Self-hosting details & configuration
------------------------------------

Ghost has a [small team](/docs/product/), so we optimize the software for a single, narrow, well defined stack which is heavily tested. This is the same stack that we use on Ghost(Pro), so we can generally guarantee that it’s going to work well. Ghost *can* also run successfully with different operating systems, databases and web servers, but these are not officially supported or widely adopted, so your mileage may (will) vary.

Our officially supported and recommended stack is as follows:

* **Ubuntu 16.04**, **18.04**, **20.04** or **22.04**
* MySQL 8.0
* NGINX
* Systemd
* [Recommended Node version](/docs/faq/node-versions/) installed via NodeSource
* A server with at least 1GB memory
* A non-root user for running `ghost` commands

[See self-hosting guides & instructions →](/docs/install/)

---

### Server hardening

After setting up a fresh Ubuntu install in production, it’s worth considering the following steps to make your new environment extra secure and resilient:

* **Use SSL** - Ghost should be configured to run over HTTPS. Ghost admin must be run over HTTPS. You can choose to [load admin on a separate domain](/docs/hosting/#separate-admin-domain) for additional security
* **Secure MySQL** - We strongly recommend running `mysql_secure_installation` after successful setup to significantly improve the security of your database.
* **Set up a firewall** - Ubuntu 18.04, 20.04 and 22.04 servers can use the UFW firewall to make sure only connections to certain services are allowed. We recommend setting up UFW rules for `ssh`, `nginx`, `http`, and `https`. If you do use UFW, make sure you don’t use any other firewalls.
* **Disable SSH Root & password logins** - It’s a very good idea to disable SSH password based login and *only* connect to your server via proper SSH keys. It’s also a good idea to disable the root user.
* **Separate admin domain** - Configuring a separate [admin URL](https://ghost.org/docs/config/#admin-url) can help to guard against [privilege escalation](https://ghost.org/docs/security/#privilege-escalation-attacks) and reduces available attack vectors.

### Optimizing for scale

The correct way to scale Ghost is by adding a CDN and/or caching layer in front of your Ghost instance. **Clustering or sharding is not supported in any way.** Every day 2-5 of the top stories on Hacker News are published with Ghost, and to the best of our knowledge no Ghost site has ever fallen over as a result of a traffic spike. Minimal, sensible caching is more than enough.

### Staying up to date

Whenever running a public-facing production web server it’s **critically important** to keep all software up to date. If you don’t keep everything up to date, you place your site and your server at risk of numerous potential exploits and hacks.

If you can’t manage these things yourself, ensure that a systems administrator on your team is able to keep everything updated on your behalf.

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

