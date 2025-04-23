


Ghost 0.11.7







































[Ghost 0.11.7](https://github.com/TryGhost/Ghost/releases/tag/0.11.7?ref=ghost.org) is now available on GitHub, npm and Ghost.org. 0.11.7 contains a fix for a pretty awful custom template bug we shipped in 0.11.6.

We've been working on some gnarly issues with load times & timeouts to make Ghost LTS more stable. A key thing was changing how themes are loaded & ensuring we don't load more information than we need to. Unfortunately, we over did it a bit, and lost information used to render custom theme templates 😱. Sorry about that - it's all back now.

Highlights
----------

* **[Fixed]** Themes ignoring all templates except index.hbs and post.hbs

From 0.11.6:

* **[Improved]** Subscriber: sanitize email
* **[Improved]** Refactored packages, apps and more
* **[Fixed]** Old accesstokens are not cleaned up
* **[Fixed]** Fix cors middleware
* **[Fixed]** Fix incorrect icon on AMP app page
* **[Fixed]** Ensure config is update when deleting theme
* **[Fixed]** Fix version check error for minor versions >= 10

You can see the [full change log](https://gist.github.com/kirrg001/e2b440e47f0cf8ade3b6831ab7ca5386?ref=ghost.org) for the details of all changes included in this release.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.11.7 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.11.7](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

Credits
-------

Hannah Wolfe & Katharina Irrgang.

Special credit to Hannah for the awful bug 😝 & to Kate for helping to get a super fast fixup release out 💨.


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





 





 
















 






