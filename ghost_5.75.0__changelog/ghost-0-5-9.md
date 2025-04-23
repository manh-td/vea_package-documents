


Ghost 0.5.9







































[Ghost 0.5.9](https://github.com/TryGhost/Ghost/releases/tag/0.5.9?ref=ghost.org) is now available on GitHub, npm and Ghost.org. Ghost 0.5.9 is an incremental update to Ghost containing the new Navigation feature, several minor security fixes and many other improvements.

Ghost 0.5.9 is compatible with **Node v0.10.x** only, and does not add support for Node v0.12 or io.js, support for these is [coming soon](https://github.com/TryGhost/Ghost/pull/4955?ref=ghost.org).

Highlights
----------

* **[New]** Navigation builder
* **[New]** `{{navigation}}` helper
* **[New]** Image in RSS feed
* **[Fixed]** Incorrect user role shown on profile
* **[Fixed]** Re-authentication modal not accepting passwords
* **[Fixed]** Post published\_by can be overridden via the API
* **[Security]** Users can edit objects they don't have permissions for via the API
* **[Security]** XSS vulnerability when deleting tags
* **[Security]** XSS vulnerability when using URLs for blog & user images

You can see the [full change log](https://gist.github.com/ErisDS/6111e30e006ed34cf9f6?ref=ghost.org) for the full details of every change included in this release.

Security Fixes
--------------

Ghost 0.5.9 contains several minor fixes for security issues affecting authenticated users on multi-user blogs. This includes two potential XSS vulnerabilities in the admin UI and two privilege issues where the API allowed users to change data they should not be able to change. Thanks to Matteo Beccaro & Abdel Adim Oisif for discovering & responsibly reporting these issues.

Theme API Changes
-----------------

Ghost 0.5.9 delivers the long awaited navigation interface. This allows users to specify a set of URLs and labels they wish to have displayed as a menu in their theme. This is output using a new `{{navigation}}` helper. Theme developers are encouraged to update their themes to use the new `{{navigation}}` feature.

The `{{navigation}}` helper works in much the same way as the `{{pagination}}` helper - it outputs a block of HTML which can be customised by specifying a `navigation.hbs` partial template in the `partials` folder of your theme. The default template can be found [here](https://github.com/TryGhost/Ghost/blob/master/core/server/helpers/tpl/navigation.hbs?ref=ghost.org).

See the [theme API changelog](https://ghost.org/docs/changes/?ref=ghost.org), and particularly the [navigation helper](https://ghost.org/docs/themes/helpers/navigation/?ref=ghost.org) documentation for further information.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.5.9 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.5.9](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org). If you've missed out a version or two, don't worry you can upgrade directly from any 0.5.x version straight to 0.5.9.

Enjoy!

Credits
-------

This release was lovingly crafted by Jason Williams, Hannah Wolfe, Paul Adam Davis, Fabian Becker, Andrew Chilton, Matt Enlow, Marcos Ojeda, David Balderston, 1Pete, rmfx, Eugene Kulabuhov, Felix Rieseberg, Harry Hope, Ivan Votti, Jimmy Hsu, Josh Vanderwillik and Mark Stosberg.


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





 





 
















 






