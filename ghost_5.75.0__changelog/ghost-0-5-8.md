


Ghost 0.5.8







































[Ghost 0.5.8](https://github.com/TryGhost/Ghost/releases/tag/0.5.8?ref=ghost.org) is now available on GitHub, npm and Ghost.org. 0.5.8 is an incremental update to Ghost containing several new features as well as numerous bug fixes.

Highlights
----------

* **[New]** Tag Management UI
* **[New]** Labs options for WIP features
* **[New]** Importer handles images and markdown files
* **[New]** Socket permissions can be set from config
* **[Fixed]** Custom favicons not working correctly
* **[Fixed]** New posts added to bottom of list in admin
* **[Fixed]** Has helper tag matching bug
* **[Fixed]** Email sending issue when blog title has a comma
* **[Fixed]** Issues with fetching a Gravatar
* **[Fixed]** Various admin UI issues

You can see the [full change log](https://gist.github.com/ErisDS/ae2ee81553817561422c?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

The first iteration of tag management which arrives in 0.5.8 is just part of the big picture [vision for tags](https://github.com/TryGhost/Ghost/wiki/Tags-101?ref=ghost.org). This brings with it several updates to the API, and there are several more to come. We're making progress towards that all important v1.0 for the API.

Providing options for enabling work in progress features on the Labs page gives us a new way to ship features to users a little bit earlier than we usually would. This ties in with our faster releases to get more feedback from users as we build new stuff. It also gives us a safe place to try out features we aren't certain about shipping.

Updates to the importer in 0.5.8 provide a number of new opportunities for anyone building tools to migrate from other platforms to Ghost. The importer now takes a zip file which can contain either a Ghost JSON file or a set of markdown files, plus accompanying images. More information can be found in the [import format](https://github.com/TryGhost/Ghost/wiki/Import-format?ref=ghost.org) guide.

Theme API Changes
-----------------

There are no major theme API changes in Ghost 0.5.8, but there are a number of bug fixes and improvements to the existing set of helpers.

* The `{{has}}` helper was incorrectly matching partial tags.
* `{{image}}`, `{{meta_title}}` and `{{meta_description}}` have all been updated to use the properties which can be set in the tag management UI.
* `{{excerpt}}` helper now does a better job at handling footnotes
* `{{url}}` and `{{image}}` are no longer async meaning they'll work in conjunction with the `{{encode}}` helper.

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for more details.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.5.8 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.5.8](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org). If you've missed out a version or two, don't worry you can upgrade directly from any 0.5.x version straight to 0.5.8.

Enjoy!

Credits
-------

This release was lovingly crafted by Jason Williams, Hannah Wolfe, Paul Adam Davis, Robert Jackson, cobbspur, Felix Rieseberg, John O'Nolan, Eugene Kulabuhov, Jeremiah Hoyet, Delgermurun, Ilya Radchenko, Jason Friedrich, Daniel Tsui, Martin H. Normark, Matt Enlow and Mikael Brockman.


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





 





 
















 






