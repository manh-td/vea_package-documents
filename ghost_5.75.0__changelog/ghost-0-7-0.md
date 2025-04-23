


Ghost 0.7.0











































[Ghost 0.7.0](https://github.com/TryGhost/Ghost/releases/tag/0.7.0?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This version largely comprises a rework of the admin UI, including a redesign and significant changes to the underlying functionality. 0.7.0 also lays much ground work for API features which are coming soon.

Highlights
----------

* **[New]** New admin interface design
* **[New]** Admin search for posts & users
* **[New]** On-boarding flow (for new blogs)
* **[Improved]** jQuery not included in `{{ghost_foot}}`
* **[Improved]** Tags respect the order they are added to a post
* **[Improved]** `{{foreach}}` helper upgraded
* **[Fixed]** `{{tags}}` & `{{author}}` not working in next/prev post helpers
* **[Fixed]** Various RSS url issues
* **[Fixed]** Upgrade path for very old blogs

You can see the [full change log](https://gist.github.com/ErisDS/314914b570c4233eea8c?ref=ghost.org) for the full details of every change included in this release.

In Detail
---------

The majority of the 585 changes made to Ghost since the last release revolve around the total overhaul of the admin interface. As well as changing the design, we've switched from using Sass for the CSS, to using Myth. Myth uses a different approach to other preprocessors - instead of writing an abstraction, you write pure spec-compliant CSS & Myth will polyfill features that aren't fully supported yet.

There have also been significant changes to the underlying API & workings of Ghost. If you're already hacking on top of the unofficial JSON API you'll find we've made some improvements, particularly around validation & error handling. It will continue to evolve rapidly as we iterate towards our first official, public & documented version of the API with OAuth support.

### Theme API Changes

The theme API has had a number of updates in this release. Most significantly, jQuery is **no longer** included by Ghost via the `{{ghost_foot}}` helper. A full explanation of this change can be found in the [no more jQuery](https://ghost.org/changelog/no-more-jquery/) post we published several months ago. In short if you have an existing Ghost blog you are unaffected, if you are a theme developer, you need to update your themes accordingly.

The `{{next_post}}` & `{{prev_post}}` helpers have been fixed to allow you to output `{{author}}` and `{{tags}}`. The `{{foreach}}` helper has been upgraded to support block params the same as the native `{{each}}` helper, and also now has a `@number` variable. Finally, we've improved `{{tags}}` so that it will now respect the order that tags are added to a post. These changes will all be useful in conjunction with the `{{#get}}` helper we're working on for a near-future release\*.

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for more details of what changed in Ghost 0.7.0. The theme documentation is frequently updated with more details and better examples. Please also use the suggest edits feature if you see something that is missing.

\* If you're waiting for the `{{#get}}` helper, you can help us to get it ready by testing it & providing feedback. Details are [here](https://github.com/TryGhost/Ghost/pull/5608?ref=ghost.org), please also drop by the #themes channel in [slack](https://forum.ghost.org/?ref=ghost.org) to ask any questions about this :)

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.7.0 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.7.0](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org). If you've missed out a version or two, don't worry you can upgrade directly from any version as far back as 0.4.2 :)

Enjoy!

Credits
-------

This release was lovingly crafted by John O'Nolan, Hannah Wolfe, Kevin Ansfield, cobbspur, Austin Burdine, Jason Williams, Fabian Becker, Sebastian Gierlinger, John O'Mahoney, Matt Enlow, Alex Kleissner, Joe Wegner, Kowsheek Mahmood, Rem Zolotykh, Robert Jackson, Maurice Williams, Łukasz Kliś, Michael Auer, Nazar Gargol, Rafael Corrêa Gomes, hwdsl2, Roy van Kaathoven, Samuel Goodwin, BlueHatbRit, Sem, Augustus Yuan, Joe Cannatti, David Balderston, hoxoa, Clay Diffrient and Chris Maddox.


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





 





 
















 






