How to install Ghost on Digital Ocean - Official guide
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

A full guide for installing, configuring and running Ghost on a Digital Ocean Droplet VPS, for use in production environments.

Overview
--------

Digital Ocean the official hosting partner of the Ghost open source project, and our favourite provider! Our teams have worked together to make installing Ghost on Digital Ocean VPS droplets as easy as possible for developers, with officially supported 1-click marketplace apps.

Prerequisites
-------------

For this install there are three things which you need to have ready up-front:

1. A DigitalOcean account ([This signup link](https://m.do.co/c/9ff29836d717) will give you $100 free credit)
2. Your SSH key added to the account. [Follow these instructions](https://www.digitalocean.com/docs/droplets/how-to/add-ssh-keys/to-account/)
3. A domain name to point at your new site (Mandatory for SSL configuration during install)

---

Setting up the marketplace app
------------------------------

Head over to [the official Ghost app in the Digital Ocean marketplace](https://marketplace.digitalocean.com/apps/ghost), and click on the “Create Ghost Droplet” button.

![Select a size](/images/docs/install/digitalocean-1_huf7cfbbf5bf09b89b2ece9aa193086014_364320_2648x0_resize_q100_h2_box_3.webp)

For most Ghost installs, the $5 base option is sufficient to run the app. If you’re running a high traffic site or one with lots of members, then you may want to choose an option with more resources.

![Select a size](/images/docs/install/digitalocean-2_hu99e10db7fda0845d639fea0ea6962c3c_57813_2170x0_resize_q100_h2_box_3.webp)

The rest of the options for the Droplet can be selected based on what you prefer. Make sure you only create **one** Droplet, Ghost runs on a single process and cannot be sharded across multiple machines.

When you’re done, click the “Create Droplet” button at the bottom of the screen.

Server Setup
------------

Once the Droplet has been created you will have an IP address to log into. Open your terminal and login to your new server as the root user, with SSH:

```
# Login via SSH
ssh root@your_server_ip

```

At the first login Ghost-CLI will automatically perform an update check for all available packages, and make sure that the environment is ready for use. When finished, you’ll see a prompt to let you know what’s next:

```
Ghost will prompt you for two details:
1. Your domain
 - Add an A Record -> xxx.xxx.xxx.xxx & ensure the DNS has fully propagated
 - Or alternatively enter http://xxx.xxx.xxx.xxx
2. Your email address (only used for SSL)
Press enter when you're ready to get started!

```

Configuring your domain
-----------------------

It’s best to set up your domain and DNS at this point so that SSL certificates can be automatically provisioned during the install process. Create an **A-Record** from your domain, pointing at your server’s IP address, then press `Enter` in terminal when you’re ready.

Setting up Ghost
----------------

Ghost-CLI will now install and configure Ghost for you, and along the way it will prompt you with some questions about how you’d like things to be set up:

##### Blog URL

Enter the exact URL (the domain you pointed at your droplet’s IP address) that your publication will use, and include the protocol for HTTP or HTTPS. For example, `https://example.com`. If you use HTTPS, Ghost-CLI will offer to set up SSL for you.

Your new site
-------------

Once the install is finished you’ll be able to access your new site on `https://yourdomain.com` and `https://yourdomain.com/ghost` to access Ghost Admin ✨

**That’s it! You’re done.**

---

#### Future maintenance

Once Ghost is properly set up it’s important to keep it properly maintained and up to date. Fortunately, this is relatively easy to do using Ghost-CLI. Run `ghost help` for a list of available commands, or explore the full [Ghost-CLI documentation](/docs/ghost-cli/).

---

#### What to do if the install fails

If an install goes horribly wrong, use `ghost uninstall` to remove it and try again. This is preferable to deleting the folder to ensure no artifacts are left behind.

If an install is interrupted or the connection lost, use `ghost setup` to restart the configuration process. If the install succeeds, but starting Ghost fails, you can try starting ghost manually with `ghost start`.

For troubleshooting and errors, use the site search and [FAQ section](/docs/faq/) to find information about common error messages.

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

