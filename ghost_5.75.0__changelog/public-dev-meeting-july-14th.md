


Public Dev Meeting July 14th











































Quick Summary
-------------

More work done on the initial blog setup and continued progress towards 0.7.

Progress Report
---------------

Non-Zelda:

* The tests that were constantly failing have been fixed - [#5541](https://github.com/TryGhost/Ghost/pull/5541?ref=ghost.org)
* io.js has been removed from the build matrix - [#5547](https://github.com/TryGhost/Ghost/pull/5547?ref=ghost.org)
* Owners are now only editable by themselves [#5539](https://github.com/TryGhost/Ghost/pull/5539?ref=ghost.org)
* New rss item filter has been added - [#5538](https://github.com/TryGhost/Ghost/pull/5538?ref=ghost.org)

Zelda:

* Fixed invited users not being able to sign up bug - [#5534](https://github.com/TryGhost/Ghost/pull/5534?ref=ghost.org)
* New image upload component/gravatar image pull as a part of the initial setup - [#5355](https://github.com/TryGhost/Ghost/pull/5355?ref=ghost.org), [#5531](https://github.com/TryGhost/Ghost/pull/5531?ref=ghost.org)

Priority Issues
---------------

* Pagination with offset instead of page - [#5093](https://github.com/TryGhost/Ghost/issues/5093?ref=ghost.org)
* No more staticPages parameter and better pages support - [#5151](https://github.com/TryGhost/Ghost/issues/5151?ref=ghost.org)

> Both of the issues above are needed for the get helper and to move the public API forward

* Everything in the [Zelda milestone](https://github.com/TryGhost/Ghost/issues?q=is%3Aopen+is%3Aissue+milestone%3AZelda&ref=ghost.org) is considered a blocker for the next release - [#5314](https://github.com/TryGhost/Ghost/issues/5314?ref=ghost.org)
* The [middleware refactor issue](https://github.com/TryGhost/Ghost/issues/5286?ref=ghost.org) has a full list of all the middleware that needs to be split. - [#5286](https://github.com/TryGhost/Ghost/issues/5286?ref=ghost.org)

Discussion
----------

* An update was pushed to [#5516](https://github.com/TryGhost/Ghost/pull/5516?ref=ghost.org) that sanitizes any API options that are not recognized or, if the option is valid, it checks for known datatypes and returns an error if they are incorrect. This is based on the spec laid out in [#2758](https://github.com/TryGhost/Ghost/issues/2758?ref=ghost.org)
* Ghost is hiring! - [https://ghost.org/careers/](https://ghost.org/careers/?ref=ghost.org)

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1436891546007214?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 21st July, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-07-21,270,6bj).


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





 





 
















 






