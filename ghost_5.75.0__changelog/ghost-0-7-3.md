


Ghost 0.7.3







































[Ghost 0.7.3](https://github.com/TryGhost/Ghost/releases/tag/0.7.3?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This is a maintenance release containing many bug fixes and improvements since 0.7.2.

Highlights
----------

* **[New]** permalinks & posts\_per\_page now available in themes via `@blog`
* **[New]** `/shared/ghost-url.js` script for accessing the API from external sites
* **[Changed]** Now returns 404 for nonexistent pages in pagination & RSS
* **[Fixed]** shortcut keys not working in the editor
* **[Fixed]** sub-dir being added to navigation urls
* **[Fixed]** caret jumping around in published date input
* **[Fixed]** checkbox labels being cut off on mobile
* **[Fixed]** pagination not working inside the `{{#get}}` helper
* **[Fixed]** issue with some theme helpers causing aSyNcId errors

You can see the [full change log](https://gist.github.com/ErisDS/56d590730df3a9d7c5e7?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

Since 0.7.2 there have been numerous refactors both in the Ember admin client and on the server side. Ember & Ember-Data are now at v2.2.0, Ember-cli is at 1.13.13 and ES6 features have been rolled out across the Ember codebase. Meanwhile on the server side, the frontend controller continues to be worked on to move towards [dynamic channels](https://github.com/TryGhost/Ghost/wiki/Channels-101?ref=ghost.org).

One significant change to how Ghost works, is that visiting large page numbers which don't exist now always 404, rather than redirecting back to the last available page. This affects both standard pages and the RSS feed. This was changed as redirecting with a 302 error cannot be cached, and is also considered a 'soft-404' crawl error by Google.

### Public API Beta Changes

The biggest change to the Public API tools is that the `ghost.url.api()` utility has been reworked so that it can easily be included and used on an external website. For example, we include it on [https://ghost.org](https://ghost.org/?ref=ghost.org) so that we can fetch posts from /changelog/.

For detailed information on the Public API Beta, please check out the [developer guide](https://ghost.org/docs/?ref=ghost.org).

### Theme API Changes

The theme API has had a few updates in 0.7.3, including a couple of bug fixes and additions. Most notably, the issue that users were encountering when trying to use certain helpers like `{{post_class}}` inside the `{{#get}}` helper and seeing **aSyNcId** being output on their page has been resolved for most cases.

In addition, the `{{tags}}` and `{{#foreach}}` helpers both got a brand new `limit` attribute and the `permalinks` and `post_per_page` settings are now both available to themes via the `@blog` global data attribute. **Update:** it is also now possible to specify custom post templates, much like you can for pages, tags & authors already.

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for full details of what changed in Ghost 0.7.3. The theme documentation is frequently updated with more details and better examples. Please also use the suggest edits feature if you see something that is missing.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.7.3 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.7.3](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

**Note:** Having a correctly configured url in config.js is a hard requirement since 0.7.2. If you get the error **Access Denied from url** whilst trying to login, please see the [configuration documentation](https://ghost.org/docs/config/?ref=ghost.org#url).

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Kevin Ansfield, Austin Burdine, Sebastian Gierlinger, Brandon Hops, Gary Cao, Syaiful Bahri, cobbspur, vdemedes, Eric Schultz, John Cruikshank, Kevin P. Kucharczyk, Matthew Beale and StevenMcD.


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





 





 
















 






