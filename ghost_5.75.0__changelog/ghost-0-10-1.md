


Ghost 0.10.1







































[Ghost 0.10.1](https://github.com/TryGhost/Ghost/releases/tag/0.10.1?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This is a bug fix release, which resolves some gnarly issues with 0.10.0.

Highlights
----------

* **[Fixed]** Uploads & imports on Windows - sorry about that 😳
* **[Fixed]** Memory Leak ☔️ - downgrading bookshelf & knex solves this, we're still looking for the exact culprit
* **[Fixed]** AMP pages with missing images now fallback gracefully
* **[Fixed]** AMP doesn't like old-school HTML attributes such as `border`
* **[Fixed]** Migrations from <0.7 to 0.10.1 will no longer throw an error
* **[Fixed]** Cannot find module... config.example error when starting Ghost after upgrading
* **[Fixed]** Multiple upgrade notifications - one is enough 😜
* And a few other bits & pieces...

You can see the [full change log](https://gist.github.com/ErisDS/78dffbfd3101ac4fa27e9d16a547d2e8?ref=ghost.org) for the details of every change included in this release.

In Detail
---------

The most important changes in this release are dependency updates for bug fixes, and dependency downgrades to try to resolve the memory issue. See the note in the How to Upgrade section about reinstalling npm modules.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.10.1 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.10.1](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

**Note:** Due to the dependency changes in this release, it may be necessary to remove the `node_modules` folder, clear the cache and do a fresh npm install i.e. run `rm -rf node_modules && npm cache clear && npm install --production`. This is also described in the [upgrade troubleshooting](https://ghost.org/docs/update/?ref=ghost.org#troubleshooting) guide.

Credits
-------

This release was lovingly crafted by Austin Burdine, Aileen Nowak, Hannah Wolfe, Katharina Irrgang and Kevin Ansfield.


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





 





 
















 






