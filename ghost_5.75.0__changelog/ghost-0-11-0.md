


Ghost 0.11.0







































[Ghost 0.11.0](https://github.com/TryGhost/Ghost/releases/tag/0.11.0?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This release contains mostly bug fixes, with an important data migration for blogs that didn't have their dates migrated correctly during the 0.9.0 upgrade.

Highlights
----------

* **[Fixed]** Typing a space in the search bar no longer completes the search 🔍
* **[Fixed]** Date migrations for sqlite3/postgres blogs that were running in UTC 🕓
* **[Fixed]** AMP and previews now work properly when running Ghost in a subdirectory.
* **[Fixed]** Scheduling now works when blogs are run in a subdirectory ⏰
* **[Fixed]** Internal tags no longer appear in meta data or RSS feeds.
* **[Fixed]** More fixes for theme uploads causing unsupported type errors when they shouldn't 🐛
* **[Fixed]** Uploading over the top of an active theme now correctly reloads the theme & clears the cache 💥
* **[Fixed]** Issue with `lodash` when Ghost installed as an npm module.
* **[Fixed]** Sitemaps were sometimes rendering without any content 🔦
* **[Changed]** Downgraded missing `{{asset}}` helpers in themes to a warning so they can still be used with caution.
* And other things...

You can see the [full change log](https://gist.github.com/ErisDS/a18159169077ec434e490479cae44135?ref=ghost.org) for the details of every change included in this release.

In Detail
---------

This is the penultimate release of Ghost that will work with Node.js v0.10. Please take some time in the next 2 weeks to upgrade. More information can be found in this [blog post](https://ghost.org/changelog/end-of-node-js-0-10/).

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.11.0 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.11.0](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

**Note:** Due to the dependency changes in the last releases, it may be necessary to remove the `node_modules` folder, clear the cache and do a fresh npm install i.e. run `rm -rf node_modules && npm cache clear && npm install --production`. This is also described in the [upgrade troubleshooting](https://ghost.org/docs/update/?ref=ghost.org#troubleshooting) guide.

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Katharina Irrgang, Austin Burdine, Aileen Nowak, Ryan McCarvill, David Wolfe, Sebastian Gierlinger and Kevin Ansfield.


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





 





 
















 






