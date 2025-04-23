


Ghost 0.5.7







































[Ghost 0.5.7](https://github.com/TryGhost/Ghost/releases/tag/0.5.7?ref=ghost.org) is now available on GitHub, npm and Ghost.org. 0.5.7 is an incremental update to Ghost containing lots of bug fixes and small UI improvements.

Highlights
----------

* **[New]** Login via editor modal if session expires
* **[New]** View post link in notification when publishing/updating a post
* **[Fixed]** Clearer user deletion warning
* **[Fixed]** Change password form allows for updating password of other user
* **[Fixed]** Sitemap handling of draft posts and images
* **[Fixed]** Invite user token verification failing

You can see the [full change log](https://gist.github.com/ErisDS/6c4408b2f6b253b8315b?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

Behind the scenes tag management is getting closer to being ready to ship, with just a few more pieces left to output the number of posts each tag has, and to add some user-facing & theme features. You can check the progress of the new UI by adding `tagsUI:true` to your config.js file.

Improvements to ember-simple-auth and subsequent work on Ghost means that we now have much better session handling. If a session ends whilst you're writing a post, Ghost will now prompt you to log in again.

Additionally we've made some changes to the Post API so that it returns the pre-calculated URL for a post. This allows us to more easily place links in the editor so that you can view a post and will also mean that 3rd party apps won't need to duplicate the code to figure out the URL from the permalink setting. In the future we may roll this to users and tags as well.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.5.7 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.5.7](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org). If you've missed out a version or two, don't worry you can upgrade directly from any 0.5.x version straight to 0.5.7.

Enjoy!

Credits
-------

This release was lovingly crafted by Jason Williams, Hannah Wolfe, cobbspur, Paul Adam Davis, Matt Enlow, Sebastian Gierlinger, Nazar Gargol, Paul Davis, Richard King, Vikhyat Korrapati, David Balderston, zethraeus, Felix Rieseberg, Ihab Khattab, Jacob Gable, Katie Fenn and Marco Otte-Witte.


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





 





 
















 






