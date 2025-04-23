


Ghost 0.7.4







































[Ghost 0.7.4](https://github.com/TryGhost/Ghost/releases/tag/0.7.4?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This contains a handful of bug fixes for things which weren't quite right in 0.7.3, particularly relating to the new Public API features.

Highlights
----------

* **[Fixed]** Tag pages for tags starting with numbers
* **[Fixed]** Helpers still causing aSyNcId errors when used inside the `{{#get}}` helper
* **[Fixed]** `ghost.url.api()` utility issue with multiple requests
* **[Fixed]** authentication error on resubmitting setup/two
* **[Fixed]** broken `@last` when using `{{#foreach}}` with `limit`
* **[Fixed]** Duplicate URL input field in image uploader

Also note, in 0.7.3 the ability to use custom post templates was added, but not documented. This is being documented in 0.7.4.

You can see the [full change log](https://gist.github.com/ErisDS/8d05c9cea3a62c0ea6bf?ref=ghost.org) for the full details of every change included in this release.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.7.4 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.7.4](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

**Note:** Having a correctly configured url in config.js is a hard requirement since 0.7.2. If you get the error **Access Denied from url** whilst trying to login, please see the [configuration documentation](https://ghost.org/docs/config/?ref=ghost.org#url).

Enjoy!

Credits
-------

This release was lovingly crafted by Fabian Becker, Hannah Wolfe, Austin Burdine, Kevin P. Kucharczyk and Matt Enlow.


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





 





 
















 






