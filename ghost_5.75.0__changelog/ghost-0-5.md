


Ghost 0.5 - MSR1







































Today we are releasing Ghost 0.5 - a massive technical progression and an exciting step forward for the Ghost blogging platform.

![](https://ghost.org/changelog/content/images/2021/01/05-team.jpg)

This release represents a total of **616 commits** across **471 issues** from **61 incredible contributors** all over the world.

*CodeName: MSR1* - this is the second release named for one of our 3 [Kickstarter backers](https://www.kickstarter.com/projects/johnonolan/ghost-just-a-blogging-platform/?ref=ghost.org) who pledged £1,000 to making Ghost a reality last year. A big thank you goes out to the [MSR Group](https://www.linkedin.com/in/topsec1?ref=ghost.org) for their support on this release.

What's in The Box
-----------------

By far the biggest release we've ever done, Ghost 0.5 is absolutely packed with new things. Here are the highlights:

Multi-User Support
------------------

![](https://ghost.org/changelog/content/images/2021/01/image-115.png)

This post, you may have noticed, is the first on the Ghost.org blog which is not written by [John](https://ghost.org/resources/author/john/?ref=ghost.org). Our flagship feature for this release is that **Ghost now has support for multiple Authors, Editors and Administrators.** Company, community and collaborative blogs are now all possible.

Public JSON API
---------------

Ghost is the first and only Open Source publishing platform to build a public JSON API. We're incredibly excited about the immense possibilities which this opens up for the future.

What does that mean, exactly? Just like Twitter and Pinterest have an API which developers can build apps on top of, Ghost has this power as well. This means that iOS, Android, Desktop and even Web Apps can now all be built on top of any Ghost blog.

Because Ghost is a self-consuming JSON API, every single feature which is in Ghost is available to 3rd party developers. Not just a subset; Everything.

In the very near future we'll be opening up authentication for the API via OAuth, In the meantime we'll be publishing documentation so that developers can start to get to grips with what's available.

Completely New Ember.js Admin
-----------------------------

The Ghost admin area may look generally the same, but under the hood it is a brand new beast. In February of this year we [made the decision](https://ghost.org/changelog/hello-ember/) to convert the Ghost web app (the admin app which consumes the JSON API) to use [Ember.js](https://emberjs.com/?ref=ghost.org).

What does that mean? Ghost is now a fully-featured client-side JavaScript application. Everything you do in the browser happens in real time. We're now able to start building user-interface components which look and feel like what you might expect from a desktop (or mobile) operating system.

A Bedrock for The Future
------------------------

![](https://ghost.org/changelog/content/images/2021/01/image-116.png)

These 3 flagship features cement the future of Ghost. We've spent a long time laying the foundations for a solid, stable application which can grow and scale effectively. Multi-user support has opened up an enormous amount of new use-cases for Ghost as a piece of software. The JSON API has infinitely expanded the possibilities for Ghost as a development platform. The Ember.js Admin is going to allow us to ship new features and functionality fast. Really fast.

A Whole 2nd Box of Things
-------------------------

As well as those three giants, there's practically a whole second box full of improvements and features which we're shipping today:

![](https://ghost.org/changelog/content/images/2021/01/image-117.png)

* **Casper 1.0** - Our default theme has had massive update with beautiful new user profile pages, full-bleed homepage cover images, restructured navigation, improved mobile styles, and a massive improvement to typography contributed by [Jake Giltsoff](https://twitter.com/designbyjake?ref=ghost.org) from Typekit.
* **Privacy.md** - Ghost is leading the way with a new Open Source initiative called [Privacy.md](https://github.com/TryGhost/Ghost/blob/master/PRIVACY.md?ref=ghost.org). We now ship a text file with a plain English description of every feature within the software which might affect user Privacy.
* **New Install Screen** - A refined UI when installing a new Ghost blog.
* **OAuth Support** - for extensible, secure authentication with less hassle.
* **Theme API improvements** - New helpers, functionality, and tools for theme developers. [More here](https://ghost.org/changelog/themes-multi-user-ready/).
* **Auto-GZip** - Theme assets are now automatically GZipped in production environments. This makes your blog load faster.
* **Improved Keyboard Shortcuts** - New navigational shortcuts and international (non-English) keyboard support.
* **Mobile Improvements** - Better support on touch based devices.
* **HTML Emails** - All system emails now sent in a beautiful HTML email template (with plaintext fallback).
* **Hundreds of bugfixes** and minor improvements
* [Much, much more](https://gist.github.com/ErisDS/b7aa1a6e954f415cbb5b?ref=ghost.org)

![](https://ghost.org/changelog/content/images/2021/01/image-118.png)

How to Upgrade
--------------

Gotcha! **Ghost(Pro)** subscribers have already been upgraded to 0.5. Enjoy it, and thank you so much for your support!

For people running Ghost on their own servers, you will need to [download Ghost 0.5](https://ghost.org/docs/install/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org). If you're using the default Casper theme without modifications, be sure to drop in a [fresh copy](https://github.com/TryGhost/Casper/releases?ref=ghost.org) of that - too!

A New Release Cycle
-------------------

After a lot of consideration, we believe we've made significant error in how we do our releases. Until now we've blindly followed how other Open Source projects do software releases: 2-3 releases a year with fixed milestones and feature-sets. Each time a release comes around, it's a big event and everyone has to upgrade (like right now).

If you look at it objectively: this model is good for precisely nobody. Developers have to wait 3-6 months to see how users respond to their work, and then iterate on it another 3-6 months after that. For users who have to upgrade, the release cycle is always either too long or too short. Both are understandably frustrating.

All of this is also a pretty archaic way of working, for web based software development in 2014.

**So we're going to change it up.**

Ghost is about experimenting and doing things differently. It's about building the best possible product for writers and publishers. To do that, we need to build fast, ship fast, and learn fast.

Starting today, we're moving to a more agile release process. **Every 2-4 weeks we're going to ship new features, improvements and bug-fixes to Ghost.** There won't be any more big-bang events like this one. There will be smaller, more frequent announcements that we've released new features, fixes and improvements.

These releases will be rolled out automatically to all **Ghost(Pro)** users as and when they happen. No input required. We'll let you know when there's cool new stuff on your blog - and you concentrate on using it. Then, 2-4 weeks later we'll ship the next round of improvements based on your feedback.

For self hosted users, you can update any time you like. We'll also push update notifications 4x a year, or whenever there is a critical security update.

*Want to know what's coming up next? Check out our new [feature roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) and follow along with progress as it happens.*

Credits
-------

This release was lovingly crafted by...

Hannah Wolfe, Jason Williams, Sebastian Gierlinger, Matt Enlow, Fabian Becker, Paul Adam Davis, David Arvelo, Jacob Gable, Maurice Williams, Harry Wolff, Andy Boutte, David Balderston, Robert Jackson, Felix Rieseberg, John O'Nolan, Gabor Javorszky, Steve Layton, Manuel Mitasch, Peter Szel, Lucas Holmquist, Ian Mitchell, Kevin Ansfield, Connor Tumbleson, Alan Richards, jomahoney, lennerd, Jason Sturges, Taras Mankovski, Martijn Swaagman, Marco Otte-Witte, Josh Kalderimis, Aia Patag, surgesoft, Andrew Schwartzmeyer, Brian White, David Blurton, Dmitry Mazuro, Erik Bryn, Glen E. Ivey, Hendrik Schaeidt, Jake Wright, Jarrett Cruger, Jarrod Mosen, Jesse Tane, Joel Fischer, Jordan Sexton, Justin Yek, Lev Gimelfarb, Luke Shiels, Nicola Mustone, Paul Connolley, Renyu Liu, Szél Péter, Tim Griesser, Waleed Ali, William Dibbern, Zach Schneider, cobbspur, fabfou, joeldrapper and sessa.

**Thank you all!**

Ghost 0.5 is available [right now](https://ghost.org/docs/install/?ref=ghost.org) on Ghost.org. **Ghost(Pro)** subscribers have already been upgraded and can simply log in to check out the new features.

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





 





 
















 






