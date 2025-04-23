


Ghost 0.5.2







































[Ghost 0.5.2](https://github.com/TryGhost/Ghost/releases/tag/0.5.2?ref=ghost.org) contains several new features as well as a refresh of the admin design, important bug fixes, updates to the theme API, JSON API and importantly breaking changes to the way Ghost is started if you use it as an npm module.

Highlights
----------

**[New]** Admin design refresh  

**[New]** About Ghost page  

**[New]** Post settings menu  

**[New]** Meta data screen in post settings menu  

**[New]** Post cover image option in post settings menu  

**[New]** Privacy config flags  

**[New]** Direct mail sends mail without config  

**[Improved]** Error handling when starting Ghost  

**[Fixed]** Request entity too large error  

**[Fixed]** 'Post NOT saved' dialog keeps appearing on Safari  

**[Fixed]** Author dropdown only shows 15 authors  

**[Fixed]** Switching between blog and admin can cause blog to lose styling  

**[Fixed]** UpdateCheck can prevent login  

**[Fixed]** Login conflicts with multiple Ghost installs

### Breaking Changes

**[Changed]** Ghost no longer starts automatically when [used as an npm module](https://github.com/TryGhost/Ghost/wiki/Using-Ghost-as-an-NPM-module?ref=ghost.org)  

**[Changed]** Keyboard shortcut for headings is now Ctrl/⌘ + H

In Detail
---------

### Configuration changes

Ghost now supports direct mail. This means you no longer *have* to specify mail config for Ghost to be able to send emails. Direct mail is not as reliable as a 3rd party mail service, and emails may end up in spam, but you at least have a chance at getting the forgotten password email ;)

Additionally, we've improved the from address configuration. `mail.fromaddress` has been deprecated in favour of `mail.from` and now accepts either just an email address or a from address in the form: `Custom name <mail@my-blog.com>`. The default if left unset is `Blog title <ghost@blog-url>`, for more information see the [mail guide](https://ghost.org/docs/config/?ref=ghost.org#mail) on ghost.org/docs/.

Along with our new [PRIVACY.md](https://github.com/TryGhost/Ghost/blob/master/PRIVACY.md?ref=ghost.org) file, we've also added a new set of `privacy` config options to allow you to disable any of the features listed. In line with this, the `updateCheck` option has been deprecated in favour of `privacy.useUpdateCheck`. You can see all the new config options in the [configuration guide](https://ghost.org/docs/config/?ref=ghost.org#privacy) on support.ghost.org.

For those of you keeping an eye on our JSON Data API, there's a shiny new configuration API endpoint which has been added to provide access to some of the configuration options. This was used to build the new about Ghost page which appears in settings.

### Theme API changes

Ghost 0.5.2 includes the following additions and changes to the Theme API:

**[New]** {{is}} helper  

**[New]** Custom tag templates  

**[New]** {{image}} for posts  

**[Changed]** {{body\_classes}} outputs different classes  

**[Changed]** {{ghost\_head}} outputs pre & next links  

**[Changed]** Meta title & description helpers

For full details of what has changed and details on how to use the new features, please see the [theme change log](https://ghost.org/docs/changes/?ref=ghost.org).

### Using Ghost as an npm module

If you've been using Ghost as an npm module, you'll need to update your custom code which requires `ghost` after upgrading to 0.5.2. You'll find instructions on how to this on the [wiki page](https://github.com/TryGhost/Ghost/wiki/Using-Ghost-as-an-NPM-module?ref=ghost.org). Please also note that as we have switched our promise library from [when](https://github.com/cujojs/when?ref=ghost.org) to [bluebird](https://github.com/petkaantonov/bluebird?ref=ghost.org) that you'll need to use `catch` for handling rejections rather than `otherwise`.

You can see the full [change log](https://gist.github.com/ErisDS/5c2708e5fdcdf705ea2c?ref=ghost.org) for the full details of every change included in this release.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.5.2 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.5.2](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

Credits
-------

This release was lovingly crafted by John O'Nolan, Paul Adam Davis, Fabian Becker, Hannah Wolfe, Jason Williams, Felix Rieseberg, Matt Enlow, Harry Wolff, Gabor Javorszky, Robert Jackson, Jilles Soeters, Nicola Mustone, Maurice Williams, David Blurton, Sebastian Gierlinger, Thai Phan, cobbspur, Andrej Mlinarević, hiroshi kobayashi, Ashish Dixit, Chris Pearce, Jake Wright, Jamie Knight, Jay Beavers, Josh Vanderwillik, Julien Gilli, Kirill Yakovenko, Mattias Cibien, Mo Valipour, Pedro Teixeira, Robert Rhoades and Sarah.


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





 





 
















 






