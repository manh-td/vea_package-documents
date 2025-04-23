


Ghost 0.7.5







































[Ghost 0.7.5](https://github.com/TryGhost/Ghost/releases/tag/0.7.5?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This contains a number of bug fixes, and some further improvements to the `{{tags}}` and `{{#foreach}}` helpers.

Highlights
----------

* **[New]** `from` and `to` attributes added to `{{tags}}` and `{{#foreach}}`
* **[Fixed]** Admin panel slow/unresponsive when navigating or searching with large numbers of posts
* **[Fixed]** Private blogging correctly disables author/tag rss feeds
* **[Fixed]** Login in Safari's private browsing mode
* **[Fixed]** Generation of http vs https urls for meta data
* **[Fixed]** Sitemaps missing tag images

You can see the [full change log](https://gist.github.com/ErisDS/e34949f5eb92344448d6?ref=ghost.org) for the full details of every change included in this release.

Theme API Changes
-----------------

In 0.7.5, the `{{tags}}` and `{{#foreach}}` helpers both got two new attributes: `from` and `to`. These allow you to output a specific set of data, either from the standard lists of posts and tags that are provided to templates by Ghost, or more powerfully, in conjunction with using the `{{#get}}` helper to fetch more data.

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for full details of what changed in Ghost 0.7.5. The theme documentation is frequently updated with more details and better examples. Please also use the suggest edits feature if you see something that is missing.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.7.5 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.7.5](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

**Note:** Having a correctly configured url in config.js is a hard requirement since 0.7.2. If you get the error **Access Denied from url** whilst trying to login, please see the [configuration documentation](https://ghost.org/docs/config/?ref=ghost.org#url).

Enjoy!

Credits
-------

This release was lovingly crafted by Kevin Ansfield, Hannah Wolfe, John O'Nolan, JT Turner, Sean Hussey, Aileen Nowak, Szu Yaung, Austin Burdine, Fabian Becker and Jacob Gable.


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





 





 
















 






