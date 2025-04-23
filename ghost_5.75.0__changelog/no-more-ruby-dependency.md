


No more ruby dependency!!







































It is with **MUCH** excitement that I write this post to declare that building Ghost no longer depends on ruby.

![](https://ghost.org/changelog/content/images/2021/01/dog.gif)

That's right, you no longer have to have *both* node AND ruby on your development box to build or deploy Ghost. No more Gem files, no more bundler, no more bourbon. We don't have to wait for [Travis](https://travis-ci.org/TryGhost/Ghost?ref=ghost.org) to do ruby things, [Gemnasium](https://gemnasium.com/TryGhost/Ghost?ref=ghost.org) is no longer utterly confused and using tools like [Werker](https://wercker.com/?ref=ghost.org) is now straight forward. The PR removed so much complexity, you might even want to [look at it](https://github.com/TryGhost/Ghost/pull/2369/files?ref=ghost.org), you know, in awe and stuff.

### Why were you using ruby anyway?

Ghost's admin UI is written with Sass, and the ruby Sass compiler is the default. We tried to switch to [node-sass](https://github.com/andrew/node-sass?ref=ghost.org) (we really did), but the [libsass](https://github.com/hcatlin/libsass?ref=ghost.org) C library it uses to compile is unfortunately missing too many features which we require. Therefore we were stuck with requiring ruby.

### So how did you get rid of it?

![](https://ghost.org/changelog/content/images/2021/01/image-41.png)

Ghost has now split out the Sass for its admin UI into a frontend framework over at Ghost-UI. Much the same as Twitter Bootstrap, that repository generates a set of CSS files, fonts, and soon JS files that allow you to easily create simple UI components like buttons and tabs in the Ghost UI style. The framework is also open source, and if you're a frontend dev wanting to contribute to Ghost - it's the place to be (but you *will* still need ruby).

This week we made another important change to the Ghost infrastructure - we added [Bower](https://bower.io/?ref=ghost.org) to manage our frontend dependencies. This means that we can pull in the Ghost-UI files using bower and a grunt task to put the files in the right place. It also means that the Ghost codebase has significantly reduced in size this week which we hope will help make it easier for new developers to navigate.

If you're a frontend dev looking to work on Ghost-UI alongside Ghost, and wondering how to make it possible to work with them both without having to publish to Bower, I highly recommend having a read of Thomas Parisot's [Bower link](https://oncletom.io/2013/live-development-bower-component/?ref=ghost.org) tutorial. For everyone who just wants to work on Ghost core, or build Ghost from source, this is an important step forward. Excite!

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





 





 
















 






