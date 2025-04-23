


Milestone 0.4 Complete








































It has been a long slog, there have been **374** commits (not including merges) since we released 0.3.3 almost 3 months ago, but the milestone is closed and [0.4](https://github.com/TryGhost/Ghost/releases/tag/0.4.0?ref=ghost.org) is finally here!

### Ghost 0.4 - Aton - is here!

Opening Ghost up to public contributions has been fantastic. The hard work, careful consideration and wide-ranging skill set of our community members has really driven 0.4 to be the first fully grown-up version of Ghost. It's been an amazing transformation to watch.

### Thank you

I would like to say a personal thank you to each and every one of the people who contributed to 0.4. Without you, Ghost would not be the platform it is today. I hope to see more PRs from you all soon :)

I would also like to call out just a few people for their extraordinary contributions:

* [**Fabian Becker**](https://github.com/halfdan?ref=ghost.org) - for his incredible number of contributions, which included delivering static pages and subdirectory support, among much, much more
* [**Harry Wolff**](https://github.com/hswolff?ref=ghost.org) - for grabbing Ghost by the proverbials and delivering hard core refactoring work in a carefully considered and managable way
* [**Sebastian Gierlinger**](https://github.com/sebgie?ref=ghost.org) - for re-building our database migrations in such epic style
* [**Jacob Gable**](https://github.com/jgable?ref=ghost.org) - for his continuous and unwavering dedication to the app platform.

### Come join us

Want to see your name on the next release? Come get stuck in with us on [GitHub](https://github.com/TryGhost/Ghost?ref=ghost.org). The official kick-off for 0.5 will happen during the public dev meeting on Tuesday 14th January at 17:30 UTC in the #ghost IRC channel on Freenode. Details of what we have planned for 0.5 are currently being updated on the [roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org).

Release Notes:
--------------

This version has focused heavily on refactoring Ghost, with a large number of non-user facing changes. These release notes detail only the features, fixes and changes that we consider will be of interest to most Ghost users. For those who are interested, the [full changelog](https://gist.github.com/ErisDS/8397171?ref=ghost.org) is available as a gist.

### New Features

* static pages
* unsaved changes notification
* featured posts
* sexy new loading bar
* quick edit post URL
* date based permalink support.
* subdirectory support
* gravatar for user images
* SSL support
* welcome email on blog creation
* available update notifications
* tag helper has suffix and prefix property
* new encode helper

### Noteworthy Changes

* notifications are now bottom left
* switch to busboy for uploads
* switch to server side sessions
* more secure password reset process
* sort by publish date on content screen
* time supported in published date
* support for SVG images when uploading
* swapped nodejs-bcrypt for bcryptjs

### Important bug fixes

* duplicate content on content screen
* content disappears after publishing
* issues with partials and theme switching
* email address is not case sensitive on signin
* reversed post order on import
* unicode characters in post slugs are converted to ascii
* unpublished posts are not accessible
* no negative posts per page
* content & excerpt helpers work with unicode characters
* punctuation in titles not properly respected
* preview pane in editor no longer editable

These are just a few highlights. The 0.4 release contains almost 100 minor bug fixes, including numerous fixes to styling, the markdown editor, admin interface behaviour, security, rss feeds and the Casper theme.

Ghost has also been refactored significantly, meaning the codebase is considerably improved. Some key areas of refactor work occurred around config loading and management, storage and retrieval of paths and URLs, the removal of the ghost.js file, cleanup work around the API and a complete re-write of the database migrations system.

Finally, there has also been significant advances in the test suite, including running tests against sqlite, mysql and pg, improvements to unit, functional and integration tests and the ability to generate a coverage report. This improved test suite makes it easier for us to move faster and deliver more features with confidence in the future.

Notes on key features
---------------------

A few of our new features are worthy of further explanation.

### Static pages

You can now toggle any post to be a "page" from within your post settings menu on the editor or content screen. This will remove it from your post feed. About / Contact / Terms galore!

### Unsaved changes notifications

We'll now give you a heads up when you're about to lose unsaved changes. So you can, you know, save.

### Featured posts

Clicking the star on the content screen will mark a post as featured. Featured posts get an extra class so they can be styled differently.

### Sexy new loading bar.

Always know when Ghost is doing something, a little blue bar crawls across the screen to let you know!

### Quick edit post URL

You can now slap /edit/ on the end of any post URL and, boom, you're editing it.

### Date based permalink support.

Available from the general settings menu, you can now get Ghost to output URLs in the format: `/:year/:month/:day/:slug/` rather than just `/:slug/`.

### Subdirectory support

You can now configure your URL in `config.js` to contain a subdirectory, such as `https://my-ghost-blog.com/blog/`.

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Fabian Becker, Sebastian Gierlinger, John O'Nolan, Harry Wolff, Jacob Gable, William Dibbern, Jakob Gillich, Matthew Harrison-Jones, Michael Bradshaw, Zach Schneider, cobbspur, jamesbloomer, Dane Springmeyer, Sebastian Gräßl, Zach Geis, buddhamagnet, Benjamin Chodoroff, Daniel Hanson, Gabor Javorszky, Mark Berger, Matt DuVall, Patrick Garman, Seb Gotvitch, Tim Griesser, Tony Gaskell, b1nd, germanrcuriel, remixz, sjama, Ben Gladwell, Declan cook, Derek Myers, Devin Doolin, Enrique Chavez, Harry Walter, Henning Sprang, Jacob Kaplan-Moss, Jacques Marneweck, Jeff Escalante, Jonathan Johnson, Jono Warren, Jorge Niedbalski, Karl Mikkelsen, Karolis Dzeja, Kumar Abhinav, Lev Gimelfarb, Lucas, Luke Arduini, Manuel Gellfart, Matheus Azzi, Matt Florence, Matt Hughes, Matthew DuVall, Michael Nason, Micheil Smith, Nick Donohue, Nick Pfisterer, Nick Schonning, Pascal Borreli, Paul, Paul Adam Davis, Peter deHaan, Ryan Powell, Ryan Seys, Sean Hellwig, Simone D'Amico, StevenMcD, Talon, Thomas Faurbye Nielsen, Tim Mansfield, Tom Gillett, Vineet Sinha, WangSai, Will Glynn, William Golden, Zlatan Vasović, abe33, ali, andy matthews, danschumann, enahs, jtw, moritz haarmann, nason, nicovalencia, omeid and rektide.

**Thank you all!**


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





 





 
















 






