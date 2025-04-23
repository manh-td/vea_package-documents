


Ghost 0.10.0







































[Ghost 0.10.0](https://github.com/TryGhost/Ghost/releases/tag/0.10.0?ref=ghost.org) is now available on GitHub, npm and Ghost.org. It includes support for Google AMP (Accelerated Mobile Pages), as well as theme uploads within Ghost, and many fixes/improvements.

Highlights
----------

* **[New]** AMP (Accelerated Mobile Pages) - deliver optimised content for mobile users
* **[New]** Theme upload, download & delete - theme management is now part of Ghost
* **[Improved]** Ghost now uses a native system font stack in place of Google Fonts for a faster and more delightful experience.
* **[Improved]** Deleting a user now clearly highlights any post content that will be deleted
* **[Improved]** Default referrer policy has changed to `no-referrer-when-downgrade` - works now in Safari
* **[Improved]** Cross Browser Support - The editor now works in IE Edge
* **[Fixed]** Date helper now generates correct published date based on blog timezone
* **[Fixed]** Internal tags are not shown in sitemap-tags.xml anymore
* **[Fixed]** Security Issue: Open redirect
* **[Changed]** Storage adapters now require save, delete, serve, exists methods (Breaking Change)
* And much more...

You can see the [full change log](https://gist.github.com/kirrg001/85a49c37bbcdb24914bb11c08b7f09b6?ref=ghost.org) for the details of every change included in this release.

In Detail
---------

This release contains two new features which require attention if you are a theme developer or use a custom storage adapter.

### Storage Adapter Changes

**Breaking Changes**

If you have installed a custom storage adapter, you might not able to start your blog anymore, because with `0.10.0` we require a function set for custom storage adapters (save, exists, delete and serve). We've contacted all publishers to create a new version to support the changes.

The breaking changes to the Storage Adapter API are explained in detail on the [wiki page](https://github.com/TryGhost/Ghost/wiki/Using-a-custom-storage-module?ref=ghost.org). Swing by [our slack channel](https://forum.ghost.org/?ref=ghost.org) if you have any questions!

### Theme API Changes

AMP now works out of the box with a default template, which can also be overridden by themes. For full details of how to customise this feature, see the [AMP theme documentation](https://ghost.org/integrations/google-amp/?ref=ghost.org). Also watch this space for a custom AMP theme tutorial coming very soon!

Theme uploads are now handled inside of Ghost. If you upload a broken theme, we will tell you and provide a very detailed validation error output - this is done with the help of [gscan](https://github.com/TryGhost/gscan?ref=ghost.org). Theme developers can test out their themes by uploading them and viewing the report on [https://gscan.ghost.org](https://gscan.ghost.org/?ref=ghost.org).

See the [theme API docs](https://ghost.org/docs/themes/?ref=ghost.org) for full details of what changed in Ghost 0.10.0. The theme documentation is frequently updated with more details and better examples. Please also use the **suggest edits** feature if you find something is missing or out of date.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.10.0 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.10.0](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

Credits
-------

This release was lovingly crafted by Aileen Nowak, Austin Burdine, Kevin Ansfield, Hannah Wolfe, Katharina Irrgang, David Balderston, John O'Nolan, Jesse Dijkstra, Misha Wakerman and Tim Walling.


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





 





 
















 






