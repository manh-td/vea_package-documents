


Ghost 0.7.2







































[Ghost 0.7.2](https://github.com/TryGhost/Ghost/releases/tag/0.7.2?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This version includes improved tag management in the admin panel, some public API features (in Beta), and was brought to you from Singapore. Oh, and we now support Node v4.2 😉

Highlights
----------

* **[New]** `{{#get}}` Helper (Beta)
* **[New]** Public API access via Ajax in themes (Beta)
* **[New]** Support for Node v4.2
* **[New]** Drag & drop reordering for tags in post settings menu
* **[New]** `/edit/` quick URL for tags
* **[Improved]** tags now shown in admin search results
* **[Fixed]** Body parser limit increased to 1mb to support larger posts
* **[Fixed]** Page deletion not updating sitemap-page.xml
* **[Fixed]** Image and validation issues on tag management screen

You can see the [full change log](https://gist.github.com/ErisDS/3fb61372c29d5a176615?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

This release contains a lot of under-the-hood changes on both the client and the server. On the client side, we've gotten rid of our casper.js test suite in favour of using Ember acceptance tests and begun some serious refactoring to continue our efforts improving and extending the admin panel. Meanwhile on the server there has been refactoring work in the models, middleware, frontend controller & theme handling as well as significant new features added to the API ready for public access.

### Public API Access

The first phase of API access is now available as a Beta feature - meaning it lives behind a checkbox in labs. With this feature enabled, you get access to both the `{{#get}}` helper, and the ability to query the API via ajax from your theme.

For detailed information on the Public API Beta, please check out the [developer guide](https://ghost.org/docs/?ref=ghost.org).

### Theme API Changes

For those who've been waiting for the `{{#get}}` helper, this release is your first chance to start playing with it. For the time being, it is a Beta feature as we feel it's important to collect feedback before finalising how it works. Check out the full [get helper documentation](https://ghost.org/docs/themes/helpers/get/?ref=ghost.org).

Along side this, for the first time in 0.7.2 Ghost is providing a JavaScript function in the theme API in the form of `ghost.url.api()`. This function allows you to easily build URLs for ajax requests without having to pay attention to urls, protocols or client credentials. Check out the full [api url builder documentation](https://ghost.org/docs/content-api/javascript/?ref=ghost.org).

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for full details of what changed in Ghost 0.7.2. The theme documentation is frequently updated with more details and better examples. Please also use the suggest edits feature if you see something that is missing.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.7.2 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.7.2](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

**Note:** Having a correctly configured url in config.js is now a hard requirement. If you get the error **Access Denied from url** whilst trying to login, please see the [configuration documentation](https://ghost.org/docs/config/?ref=ghost.org#url).

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Kevin Ansfield, Austin Burdine, vdemedes, Sebastian Gierlinger, John O'Nolan, cobbspur, Delgermurun, Matthew Beale, Yann Verry, Leonard Camacho, Alex Cusack, Gabor Javorszky, Jakob Gillich, Adam Hess, Nazar Gargol, Oliver Schneider, Reinoud Kruithof and Stephan Bönnemann.


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





 





 
















 






