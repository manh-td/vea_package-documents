


Ghost 0.7.9







































[Ghost 0.7.9](https://github.com/TryGhost/Ghost/releases/tag/0.7.9?ref=ghost.org) is now available on GitHub, npm and Ghost.org. 0.7.9 contains lots of bug fixes, upgrades, improvements and tweaks that you mostly shouldn't notice 😊 and one breaking change for some people using the Public API Beta...

Highlights
----------

* **[Improved]** Static pages now have structured data, just like posts, so they will pass validation for twitter cards and other social media sharing tools.
* **[Improved]** Relaxed CORS handling, meaning less people should have issues logging in to their blog if their URL isn't configured exactly right.
* **[Improved]** Draft post slugs (urls) are updated when the title changes, so that you don't get weird half-titles in slugs anymore.
* **[Fixed]** Static files immediately result in a 404, because trying a filename with a trailing slash on the end is never going to result in a happier ending.
* **[Fixed]** Incorrect preview link & icon position in the editor making it easier to preview your post by clicking the word "preview" at the bottom of the editor.
* **[Fixed]** Requesting `url` as a field from the Posts API didn't return the correct response (Public API Beta).
* **[Changed]** Trusted domains now require their protocol be included. See below for details (Public API Beta).
* And much more...

You can see the [full change log](https://gist.github.com/ErisDS/558b0790afdd944d0547c3c26c8187ac?ref=ghost.org) for the details of every change included in this release.

In Detail
---------

We improved the Public API beta in this release.

### Public API Beta Changes

**Breaking Change**

If you've enabled the Public API Beta flag in labs and added a trusted domain to your database, there's a breaking change for you in this release. This change will not affect anyone else.

Trusted domains **must** now include the protocol. So where previously you may have added `ghost.org` as your trusted domain in the `client_trusted_domains` table, the domain will need to be updated to `https://ghost.org` once you upgrade to 0.7.9. If you need both http & https, then you will need two rows in the database.

If you are running on Ghost(Pro) this change should have already been made for you. Any problems, please contact [support@ghost.org](mailto:support@ghost.org) as usual 👻

**Other Changes**

It is now possible to request `url` as a field from the posts endpoint. E.g. `{{#get "posts" fields="title, url"}}` will now return the correct result. Previously `url` was not returned due to it being a computed property.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.7.9 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.7.9](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Kevin Ansfield, Jason Williams, Austin Burdine, David Balderston, Peter Szel, king6cong, quangtt, JT Turner, Jeff Jewiss, Jeremiah Hoyet, Joerg Henning, cobbspur and Aileen Nowak.


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





 





 
















 






