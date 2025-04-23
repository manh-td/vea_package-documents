Root user permissions fix
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

A fix for root user permissions problems

Error
-----

`We discovered that you are using the DigitalOcean One-Click install. You need to create a user with regular account privileges and migrate your installation to this user.`

Solution
--------

When you installed Ghost with the [DigitalOcean One-Click install](https://www.digitalocean.com/products/one-click-apps/ghost/) you probably set up your Ghost installation as a `root` user. As of Ghost-CLI 1.5.0, running Ghost commands as `root` is disallowed. Therefore you will need to migrate your current installation to a new Linux user.

Run the following steps as `root` user to fix it:

Add a new user:

```
adduser <user>

```

Add user to sudo group:

```
usermod -aG sudo <user>

```

Now create a new instance file and move to new user location:

```
mkdir -p /home/<user>/.ghost/
chown <user>:<user> /home/<user>/.ghost
mv /root/.ghost/config /home/<user>/.ghost/config
chown <user>:<user> /home/<user>/.ghost/config

```

Next, change into your ghost installation directory (`/var/www/ghost/` is default in the DigitOcean One-Click installs) to change the ownership of your installation files:

```
cd /var/www/ghost

```

And then execute this command (might take a while):

```
find . -group root -user root -exec chown <user>:<user> {} \;

```

Last step, Login as new user:

```
su - <user>

```

You can check `ghost ls` now to see if your installation is still up and running.

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

