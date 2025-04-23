


Ghost 0.6.0











































[Ghost 0.6.0](https://github.com/TryGhost/Ghost/releases/tag/0.6.0?ref=ghost.org) is now available on GitHub, npm and Ghost.org. Ghost 0.6.0 represents numerous changes to the codebase as well as many new features, improvements and bug fixes. It's been a busy month!

Highlights
----------

* **[New]** Spellcheck in the editor
* **[New]** Mobile uploads in the editor
* **[New]** Next & previous post helpers
* **[New]** Code injection
* **[New]** Customisable image storage
* **[Improved]** RSS Feeds
* **[Improved]** Structured data
* **[Fixed]** Subdomains break in navigation
* **[Fixed]** Meta title & description helpers output wrong value for posts
* **[Fixed]** @blog globals missing from helper templates

You can see the [full change log](https://gist.github.com/ErisDS/0a60eccf8638941f8ce5?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

Since Ghost 0.5.10 there have been significant changes to how the Ghost admin panel is built, as we switched from using the now deprecated Ember App Kit in favour of the shiny new [Ember CLI](https://www.ember-cli.com/?ref=ghost.org). We also updated to using Ember 1.11, meaning we no longer need to use `{{bind-attr}}` in our Ember templates. These changes are huge, but they should only affect developers.

If you're building Ghost from the source code in the git repository, rather than using one of the release zips, you'll still need to follow the same steps. However, you may find you need to do the following after a pull and before `grunt init` to clear dead code from your existing repository:

* `rm -rf bower_components`
* `rm -rf node_modules`
* `rm -rf core/client`
* `git checkout -- core/client`

If you are on a Mac, and run into `EMFILE` errors when running `grunt dev`, please see details of the fix in the [grunt-contrib-watch README](https://github.com/gruntjs/grunt-contrib-watch?ref=ghost.org#how-do-i-fix-the-error-emfile-too-many-opened-files) and also further information [in this PR](https://github.com/gruntjs/grunt-contrib-watch/pull/398?ref=ghost.org).

### Custom Storage

It is now possible to replace the image storage layer in Ghost with a custom storage module. This will allow users without a persistent filesystem (e.g. Heroku) to send images elsewhere for safe keeping. Custom storage is currently a very beta feature, but we encourage you to try it out and give us some feedback on how we can improve.

Documentation on how to setup & create custom storage modules can be found on the [Ghost wiki](https://github.com/TryGhost/Ghost/wiki/Using-a-custom-storage-module?ref=ghost.org).

### Theme API Changes

Ghost 0.6.0 brings with it the long-awaited `{{#next_post}}` and `{{#prev_post}}` helpers. These new helpers are the first of their kind, as they make additional requests to the API to fetch next and previous post data only if they are included within a theme. This is a departure from the existing data in Ghost, which is all pre-fetched based on the [current page context](https://ghost.org/docs/themes/contexts/page/?ref=ghost.org).

The next & previous post helpers are block helpers, and inside their opening and closing tags all of the existing post helpers will work to output the details of the requested post. Full details and examples of how this works can be found in the [theme documentation](https://ghost.org/docs/themes/helpers/prev_next_post/?ref=ghost.org), and you can also see how this feature is used in the [latest version of Casper](https://github.com/TryGhost/Casper/commit/dd02a1225803f96ede1d6217179bf72f17a7cdcb?ref=ghost.org#diff-83352707fdf3b9057fe76c7a38bf9a03R80).

As well as this addition, the `@blog` globals have been made available in the helper templates `navigation.hbs` and `pagination.hbs`, fixing a bug with the RSS url in Casper if your blog runs on a subdirectory. Additionally, the `{{meta_title}}` and `{{meta_description}}` helpers have be overhauled and now work properly for posts as well as in the document head.

See the [theme API docs](https://ghost.org/docs/themes/?ref=ghost.org) for more details of what changed in Ghost 0.6.0. The theme documentation is frequently updated with more details and better examples. Please also use the suggest edits feature if you see something that is missing.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.6.0 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.6.0](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org). If you've missed out a version or two, don't worry you can upgrade directly from any 0.5.x version straight to 0.6.0.

**Please note:** there is a minor change in the upgrade process in 0.6.0, in that the `npm-shrinkwrap.json` also needs replacing. If your Ghost zip file is missing that file, you need to re-download the zip.

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Matt Enlow, Jason Williams, John O'Nolan, Paul Adam Davis, cobbspur, Felix Rieseberg, baogechen, JonathanKryza, Blaine Bublitz, Ian Lopshire, Austin Burdine, Katie Fenn, Markus Siemens and Pascal Borreli.


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





 





 
















 






