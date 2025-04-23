


Ghost 0.5.6







































[Ghost 0.5.6](https://github.com/TryGhost/Ghost/releases/tag/0.5.6?ref=ghost.org) is now available on GitHub, npm and Ghost.org. 0.5.6 is an incremental improvement to Ghost, adding bug fixes and new features, including... Sitemaps!

Highlights
----------

* **[New]** Sitemaps
* **[New]** Footnotes & Highlight
* **[New]** Labs page
* **[Fixed]** Posts failing to save after an error
* **[Fixed]** Password reset and invitation links not working with mailgun
* **[Fixed]** Image helper not working correctly with subdirectories
* **[Fixed]** RSS feed warning in Chrome

You can see the [full change log](https://gist.github.com/ErisDS/1b97fe28930c19fd7c64?ref=ghost.org) for the full details of every change included in this release.

Labs Page & Hidden Features
---------------------------

The new labs page is intended as a way for us to showcase upcoming and experimental features to our users before they are officially ready for release. At the moment, it holds the import, export and other tools, which used to live at `/ghost/debug/`. These tools need an overhaul and will be worked on before finding a new home.

Soon we'll be adding options to this page so that users can enable in-development features which are normally only accessible via a config flag. For example, in 0.5.6 if you set `tagsUI: true` or `codeInjectionUI: true` in your config.js (just below `url:` a good spot) you'll be able to access the work-in-progress [tag management](https://github.com/TryGhost/Ghost/issues/4248?ref=ghost.org) and [code injection](https://github.com/TryGhost/Ghost/issues/1993?ref=ghost.org) features. The features are still being built, so use them at your own risk and if you do find any issues, please be sure to [report them](https://github.com/TryGhost/Ghost/blob/master/CONTRIBUTING.md?ref=ghost.org#bugs)!

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.5.6 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.5.6](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org). If you've missed out a version or two, don't worry you can upgrade directly from any 0.5.x version straight to 0.5.6.

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Paul Adam Davis, Jason Williams, Felix Rieseberg, Nazar Gargol, Jacob Gable, cobbspur, John O'Nolan, Sebastian Gierlinger, Stefan Baumgartner, sanddudu, Harry V. Kiselev, Harry Wolff, Hugo Jobling, Jaiden Mispy, Matt Enlow, Paul Davis and Robert Jackson.


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





 





 
















 






