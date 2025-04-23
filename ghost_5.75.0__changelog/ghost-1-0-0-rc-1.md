


Ghost 1.0 RC1






































Today we're announcing the first release candidate of Ghost 1.0 - which is (hopefully) the *last* step toward a final release. You can [install this version via Ghost-CLI](https://ghost.org/docs/ghost-cli/?ref=ghost.org) for **production usage**. If you want to migrate your LTS (0.11) site to 1.0, check out the [migration guide](https://ghost.org/docs/update/?ref=ghost.org).

Meanwhile, here's what's changed since the last beta:

* **[fixed]** A bug where empty posts could be published
* **[fixed]** An edge case that would send Casper's infinite scroll into an infinite loop
* **[fixed]** Broken positioning on welcome tour elements
* **[fixed]** Minor visual bugs with SVG icons
* **[fixed]** Session sync issues with multiple tabs/refreshes
* **[fixed]** A regex issue with Ghost subdirectory URLs
* **[fixed]** Re-enabled custom robots.txt via themes
* **[improved]** Editor now focuses on the content area by default rather than the title
* **[improved]** Tag management performance for sites with many (hundreds) of tags

You can see the [full change log](https://gist.github.com/kirrg001/c19aefb9ff19346b81eaa3c2f5b422a0?ref=ghost.org) for the details of all changes included in this release.

Updated documentation
---------------------

[Documentation for Ghost 1.0](https://ghost.org/docs/?ref=ghost.org) is available and complete. If you spot any errors or have any trouble, please come and find us on [slack](https://forum.ghost.org/?ref=ghost.org).

Breaking changes for theme activations
--------------------------------------

In a [previous beta release post](https://ghost.org/changelog/1-0-0-beta/) we announced some upcoming breaking changes for themes. In Ghost 1.0 all themes are [scanned](https://github.com/TryGhost/gscan?ref=ghost.org) for compatibility when they're uploaded. If a fatal error is detected, the theme will not be activated.

Here's an overview of all fatal errors and their solutions:

* **[fatal]** Usage of `{{pageUrl}}`, please use `{{page_url}}`
* **[fatal]** Usage of `{{image}}`, please use `{{feature_image}}`, `{{cover_image}}` or `{{profile_image}}` (depending on context)
* **[fatal]** Usage of `{{author.image}}`, please use `{{author.profile_image}}`
* **[fatal]** Usage of `{{post.image}}`, please use `{post.feature_image}}`
* **[fatal]** Usage of `{{@blog.cover}}`, please use `{{@blog.cover_image}}`
* **[fatal]** Usage of `{{author.cover}}`, please use `{{author.cover_image}}`
* **[fatal]** Usage of `{{tag.image}}`, please use `{{tag.feature_image}}`
* **[fatal]** Usage of `{{post.author.image}}`, please use `{{post.author. feature_image}}`
* **[fatal]** Usage of `{{post.author.cover}}`, please use `{{post.author. cover_image}}`
* **[fatal]** Usage of `{{post.tags.[#].image}}`, please use `{{post.tags.[#].feature_image}}`
* **[fatal]** Usage of `{{tags.[#].image}}`, please use `{{tags.[#].feature_image}}`
* **[fatal]** A template file called index.hbs must be present
* **[fatal]** A template file called post.hbs must be present.
* **[fatal]** Any unknown handlebars helper

You can always test your theme in advance on [https://gscan.ghost.org](https://gscan.ghost.org/?ref=ghost.org). Furthermore, please read through the [theme change log](https://ghost.org/docs/themes/?ref=ghost.org) for more information.

Node v6
-------

Our officially recommended version of Node.js is now >= v6.9. Node v4 is still supported. [Full list of supported Node versions](https://ghost.org/docs/faq/node-versions/?ref=ghost.org).

Ghost-CLI 1.0
-------------

We've also released a new version of Ghost-CLI — 1.0.0-rc.1. You have to update to the newest version by running `npm install -g ghost-cli@latest`.

**Please ensure `ghost --version` shows `1.0.0-rc.2`.**

Please see [here](https://ghost.org/docs/install/?ref=ghost.org) for details on how to setup your server and install Ghost.

Credits
-------

Kevin Ansfield, Aileen Nowak, Patrick Kim, John O'Nolan, Hannah Wolfe, Fixer, Austin Burdine and Katharina Irrgang.


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





 





 
















 






