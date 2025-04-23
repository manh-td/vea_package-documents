


Ghost 0.6.3







































[Ghost 0.6.3](https://github.com/TryGhost/Ghost/releases/tag/0.6.3?ref=ghost.org) is now available on GitHub, npm and Ghost.org. 0.6.3 includes some bug fixes and a couple of nice new features, including post previews :)

Highlights
----------

* **[New]** Post previews
* **[New]** Password protected blogs
* **[New]** Custom author templates
* **[Improved]** Session length is now 7 days
* **[Fixed]** Word count in editor not counting non-latin chars
* **[Fixed]** Secure URLs in RSS when accessed via HTTPS
* **[Fixed]** Autosave causing post to be published
* **[Fixed]** Admin app errors when active theme missing

You can see the [full change log](https://gist.github.com/ErisDS/934f74b8d7f0bf75217b?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

In recent weeks, we've started to focus on refactoring the code which renders blog pages. This part of the codebase has been left unloved whilst we focused on the admin UI, and it's time to give it some much needed attention. The ongoing work is the first step towards making [Channels](https://github.com/TryGhost/Ghost/wiki/Channels-101?ref=ghost.org) a possibility.

By unifying the code that renders the index, tag and author 'channels' which exist in Ghost, we are reducing duplication as well as ensuring they all work consistently. As a result of this work, Ghost 0.6.3 adds the ability to specify a custom template for each author, as can already be done with tags.

### Theme API Changes

There are two major additions to the theme API in Ghost 0.6.3.

The first is the addition of the custom author templates. Meaning that you can now add, for example, a `author-hannah.hbs` template to your theme and this will be used to render the author page if the author's slug matches `hannah`. This can be used to create individual author pages.

Secondly, Ghost 0.6.3 adds the new password protected blogs feature, which allows you to hide your blog behind a shared password - very useful whilst your blog is under construction etc. When this page is enabled, all visitors to your blog get sent to `/private/` and shown a password form.

The new private page is treated as its own [context](https://ghost.org/docs/themes/contexts/?ref=ghost.org). It can be customised by including a `private.hbs` template in your theme. `{{#is 'private'}}` will be true, and the `{{body_class}}` helper will output `private-template`. Full details can be found in the [theme documentation](https://ghost.org/docs/themes/?ref=ghost.org).

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for more details of what changed in Ghost 0.6.3. The theme documentation is frequently updated with more details and better examples. Please also use the suggest edits feature if you see something that is missing.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.6.3 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.6.3](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org). If you've missed out a version or two, don't worry you can upgrade directly from any 0.5.x version straight to 0.6.3.

Enjoy!

Credits
-------

This release was lovingly crafted by Jason Williams, Hannah Wolfe, Austin Burdine, John O'Nolan, Paul Adam Davis, Robert Jackson, Matt Enlow, Sebastian Gierlinger, Wilhansen Li, Adrian Estrada, lmoe, Alex Kleissner, Artyom Fedenko, David Balderston, Fabian Miiro and Harry Hope.


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





 





 
















 






