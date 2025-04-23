Using nvm with local and production Ghost installs
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

This guide explains how to use `nvm` with local and production Ghost installs.

### Production install

If `nvm` is installed locally in `/root` or `/home` then you’ll run into permission problems. Ghost requires a system wide installation. We recommend uninstalling nvm to avoid permission problems. A symlink from the local installation to `usr/bin/node` will not work.

Uninstall `nvm` using:

```
rm -rf $NVM_DIR ~/.npm ~/.bower
unset NVM_DIR;
which node;
rm -rf {path_to_node_version}

```

Open `~/.bash_profile or ~/.bashrc` and remove any `nvm` lines.

### Local installation

If you run into problems during a local install, it could be due to your installation of `nvm` (Node Version Manager).

Ensure `nvm` is installed correctly:

* Ensure that `nvm` is not installed in the root folder `/root/.nvm`. If nvm is installed in the root folder, uninstall nvm, and reinstall it using a non-root user.
* Set your `nvm` default version to the one you will use for Ghost before installing `ghost-cli`. If your default is different, you should switch to the correct version each time you start a new session and run any ghost commands.
* Ensure ghost-cli is installed in the correct environment. On a machine with nvm configured correctly, you should see:

```
which ghost -> /Users/[username]/.nvm/versions/node/[node version]/bin/ghost
npm root -g -> /Users/[username]/.nvm/versions/node/[node version]/lib/node_modules

```

If these paths aren’t in the same [node version], it means you’ve installed `ghost-cli` in a different environment than the active node environment. `ghost-cli` needs to be installed and run in the same environment.

**To resolve this choose one of the following:**

Run `npm install ghost-cli -g` in the current environment to get the right sqlite3 node module into the environment and go through `ghost setup` process again.

If you remember which nvm node environment you’ve installed `ghost-cli` under, run `nvm use <node version>`.

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

