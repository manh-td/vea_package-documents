How to update from v0.x to v1.x and beyond - Ghost Developers
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

If you’re running Ghost 0.x versions, your site must be updated to Ghost 1.0 before it can be successfully updated to Ghost 2.0 and beyond.

It’s recommended to update to the latest version of Ghost to keep your site and data secure, and gain access to the latest features in Ghost. For a successful upgrade, ensure that Ghost, Ghost CLI, and Node are all on compatible versions. Use our [Node Compatibility Matrix](https://ghost.org/docs/faq/node-versions/#node-compatibility-matrix) as a reference.

This is a major update with [breaking changes](/docs/changes/).

1. First, make a full backup
----------------------------

Whenever doing a manual update it’s a good idea to take a full backup of your site first. If anything goes wrong, you’ll still have all your data.

1. Start by exporting a JSON file backup of all your posts from the **Labs** area of Ghost Admin.
2. Then, make a copy of your entire `/content` directory as a backup for themes and images.

2. Update your theme
--------------------

Quite a few things have changed compared to the pre 1.0 version of Ghost, so you’ll need to make some changes to your theme. To see what changes need to be made, download a copy of your theme zip file, and upload it to [GScan](https://gscan.ghost.org).

GScan will provide a report on any new features in the Ghost theme API which are not being used, or any old ones you might be using which have been deprecated - so you can get everything fixed up.

3. Create a brand new Ghost install
-----------------------------------

There is no direct update path to the latest version of Ghost, so you’ll need to create a brand new install to migrate to.

Major versions of Ghost break compatibility to allow the platform to evolve. Creating a new install means you’ll have the latest version of the app while still being able to import your old content.

On Ghost(Pro) this takes a few clicks, or if you’re self-hosting you can follow our in-depth guides.

To install v1 run the command `ghost install --v1`

4. Migrate your content from old to new
---------------------------------------

Once the new install is set up, the only thing left to do is to import all of the content which was backed up at the start of this process.

### Import JSON

To begin the migration, head to the **Labs** section of Ghost Admin and import the `ghost.json` backup which you exported earlier. The importer will let you know if there are any issues.

### Copy images

Password tokens are not migrated, so all users will need to go through the password reset flow to unlock their accounts. If you have any trouble, start by searching the docs and the forum for help!

5. Update to the latest version
-------------------------------

Now that you’ve successfully updated from Ghost 0.x versions to 1.0, you can proceed to update to the latest version to access all [new features](/changelog/), and keep your site secure — follow this [guide](/docs/update/) to get started.

6. Upload theme
---------------

Finally, upload your updated theme to the **Design** section of Ghost Admin to get your site looking the same way it did before. Again, the theme uploader will tell you if there are any issues.

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

