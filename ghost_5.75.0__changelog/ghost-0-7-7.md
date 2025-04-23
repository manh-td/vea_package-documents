


Ghost 0.7.7







































[Ghost 0.7.7](https://github.com/TryGhost/Ghost/releases/tag/0.7.7?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This includes several bug fixes, UI tweaks and performance improvements as well as dependency updates, refactors and better test coverage.

**Update:** We've spotted a pretty nasty bug in 0.7.7 with saving tags. 0.7.8 will be along shortly...

Highlights
----------

* **[Fixed]** Node v4 LTS support handles 4.3 and all future v4 LTS versions 🚀
* **[Fixed]** Settings cache cleared on import, so your blog will now look correct without needing a restart
* **[Fixed]** Various issues with navigation - the UI behaves better, and you'll no longer get ignored by `{{current}}` if you forget a trailing slash.
* **[Fixed]** API serving invalid status codes, which was a potential source of crashes 💥
* **[New]** The delete all content button now creates a backup file first... just in case 😉
* And much more...

You can see the [full change log](https://gist.github.com/ErisDS/7d19d20b6495a621a8e8?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

For the developers out there, you may have noticed that the Ghost codebase is evolving and iterating at a very fast rate at the moment.

The Ember admin client operates almost a separate project now, and will likely move to its own repository sometime in the not-too-distant future. In Ember-land there is constant iteration and improvement, leveraging new features from Ember.js, improving our use of dependencies as well as significant work on including quality and coverage of the acceptance tests.

The serverside code in Ghost also needs a lot of love and attention. We're pushing hard to refactor it to make it more flexible (the channels refactor) as well as pushing it towards being a more "traditional" (if you can even use that word for such a new thing) Node project. This also includes a push towards improving the quality of our unit tests.

We're always looking for new contributors to help us with this work, as well as help us keep the balance between working on the codebase and shipping new features. If you'd like to get involved, come and chat to us in the #dev channel on [slack](https://forum.ghost.org/?ref=ghost.org) 👫.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.7.7 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.7.7](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

**Note:** Having a correctly configured url in config.js is a hard requirement since 0.7.2. If you get the error **Access Denied from url** whilst trying to login, please see the [configuration documentation](https://ghost.org/docs/config/?ref=ghost.org#url).

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Kevin Ansfield, Austin Burdine, Jason Williams, Fabian Becker, Kevin P. Kucharczyk, Cameron Viner, cobbspur, JT Turner, Matt Enlow, Naoya Kanai and Gabor Javorszky.


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





 





 
















 






