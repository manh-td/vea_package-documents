


Ghost 0.9.0







































[Ghost 0.9.0](https://github.com/TryGhost/Ghost/releases/tag/0.9.0?ref=ghost.org) is now available on GitHub, npm and Ghost.org. Ghost 0.9.0 contains the long-awaited scheduled posts feature among other new features and bug fixes.

Highlights
----------

* **[New]** Scheduled posts - tell Ghost to publish your post sometime in the future 🕑
* **[New]** Configurable blog timezone - super important for making scheduled posts work the way you expect.
* **[New]** Internal tags (Beta) - use tags for managing content without them appearing in your theme
* **[Improved]** Install & upgrade process by removing dependency on `semver` which regularly broke npm
* **[Improved]** Better error handling for visitors and admin users whilst performing upgrades
* **[Fixed]** "Access Denied" errors when uploading images
* **[Fixed]** Editing a post via the API without providing a tags list would delete the post's tags 😱
* **[Fixed]** Problems running in nested sub-directories, e.g. `mysite.com/my/blog`
* **[Fixed]** Session handling on intermittent connections - it should now be easier to stay logged in
* **[Changed]** Referrer policy changed from `origin` to `origin-when-cross-origin` to improve in-site analytics
* **[Changed]** [Node v4 is now the recommended node version](https://ghost.org/changelog/node-4/) for running Ghost 🎉
* And much more...

You can see the [full change log](https://gist.github.com/kevinansfield/ac440cd1433f33df0bc358b786608812?ref=ghost.org) for the details of every change included in this release.

In Detail
---------

A major change for developers since 0.8 is that the ember admin client has been split into [it's own repository](https://github.com/TryGhost/Ghost-Admin?ref=ghost.org). We're using git submodules as per the Casper dependency so after pulling down the core Ghost repo, run `grunt init` to update the submodules (you only need to do this once). If you want to make changes to the client you can then `cd core/client` where you can treat it as a normal git repository - it will be set up with `origin` pointing to [Ghost-Admin](https://github.com/TryGhost/Ghost-Admin?ref=ghost.org) by default so you'll want to rename that or add your own fork remote. Swing by [our slack channel](https://forum.ghost.org/?ref=ghost.org) if you need any help getting set up.

### New Timezone Feature

It's now possible to set the timezone of your blog - this should finally fix the "I posted at 3AM this morning but my post says says it was published yesterday" issues that arose from Ghost using the server's timezone which does not always match the blog owner's timezone.

In order to support customisable timezones and post scheduling this release contains a migration that will update all datetimes stored in the database to UTC. If your server timezone is already set to UTC there should be no change.

**Upgrade notice:** If you have a lot of data in your blog then the timezone migration may take a while, during this time visitors to your blog will see a "503 Under Maintenance" error and the admin panel will not be accessible. Keep an eye on your Ghost console logs to ensure that the migration completes successfully.

After upgrading please check and update the timezone setting in the General Settings screen - we use a best-guess method to set this during the migration process to avoid unexpected time changes but it may not match what you want.

### Scheduling

The default scheduler uses an internal system to keep track of time. This should work for most cases, however those on infrastructure that isn't always running (e.g. Heroku) will need to use an external service for scheduling. This can be achieved by adding a custom scheduling adapter to Ghost & passing the scheduling requests to another service.

The Ghost wiki contains documentation for [how to create your own scheduling adapter](https://github.com/TryGhost/Ghost/wiki/Using-a-custom-scheduling-module?ref=ghost.org).

### Theme API Changes

* Addition of `{{@blog.timezone}}`

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for full details of what changed in Ghost 0.9.0. The theme documentation is frequently updated with more details and better examples. Please also use the **suggest edits** feature if you find something is missing or out of date.

### Public API Changes

A couple of key bug fixes have been incorporated into 0.9.0:

* Querying the Post API and reducing the data returned by using `fields=title,url` will no longer return `undefined`
* When using the `filter` parameter it's now possible to filter by slugs starting with numbers without needing to escape them, e.g. `filter=slug:5-minutes-to-midnight`

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.9.0 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.9.0](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

Credits
-------

This release was lovingly crafted by Kevin Ansfield, Katharina Irrgang, Austin Burdine, Hannah Wolfe, Aileen Nowak, Lukas Strassel, Vijay Kandy, cobbspur, Joris Berthelot, zhenkyle, Gergely Nemeth, Ethan Garofolo, starcwl, and Felix Rieseberg.


### Get notified when we ship new features.






 
### You might also like...

Apr

08


![Custom content for every subscriber](/changelog/content/images/size/w750/2025/04/Ghost-Call-to-action-card.png)

Custom content for every subscriber
-----------------------------------

Calls to Action got an upgrade, now you can fine-tune the design and who sees them in more detail.
Apr 8, 2025


New





 
Apr

01


![Social web (beta)](/changelog/content/images/size/w750/2025/04/image--1-.png)

Social web (beta)
-----------------

Increase your reach by connecting your publication to the Fediverse
Apr 1, 2025


Beta





 





 
















 






