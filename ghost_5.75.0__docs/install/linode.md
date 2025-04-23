How to install & setup Ghost on Linode
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

A full guide for installing, configuring and running Ghost on your Linode server, for use in production.

Overview
--------

This the official guide for hosting Ghost on Linode. If you’re comfortable installing, maintaining and updating your own software, this is the place for you. By the end of this guide you’ll have a fully configured Ghost install running in production using MySQL.

This install is **not** suitable for [local use](/docs/install/local/) or [contributing](/docs/install/source/) to core.

Prerequisites
-------------

The officially recommended production installation requires the following stack:

* A [configured](https://www.linode.com/docs/guides/getting-started/) and [secured](https://www.linode.com/docs/guides/securing-your-server/) Linode server
* A server with at least 1GB memory

---

Server Setup
------------

This part of the guide will ensure all prerequisites are met for installing the Ghost-CLI.

### Setup the server

Follow the [official “Getting Started with Linode” guide](https://www.linode.com/docs/guides/getting-started/) to setup your server. You must choose the **Ubuntu image** when creating your server. As you’re creating a new server you should prefer Ubuntu version 22.04 LTS. However you can use Ubuntu 20.04, 18.04 or 16.04 if you want.

> Note: Using the user name `ghost` causes conflicts with the Ghost-CLI, so it’s important to use an alternative name.

### Secure your server

Follow the [official “How to Secure Your Server” Linode guide](https://www.linode.com/docs/guides/securing-your-server/) to secure your server.

### Install Ghost on Ubuntu

Now that you have a secure server with Ubuntu, follow the [Ubuntu](/docs/install/ubuntu/) instructions to install Ghost.

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

