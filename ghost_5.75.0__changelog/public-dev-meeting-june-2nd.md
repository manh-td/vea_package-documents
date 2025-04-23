


Public Dev Meeting June 2nd











































Quick Summary
-------------

Our focus is still on Zelda, with some refactoring work ongoing on the server side to improve the codebase & get ready for things like channels, apps & better theme handling.

Progress Report
---------------

Non-Zelda:

* Server-side cleanup, ongoing work on [splitting out middleware](https://github.com/TryGhost/Ghost/issues/5286?ref=ghost.org) - thanks to @hex337 and @morficus for getting stuck in. There is plenty more to do in this issue, so feel free to grab one and use their PR's as an example of how to do it.
* @jaswilli has been working on optimizing & cleaning up Ember - [5340](https://github.com/TryGhost/Ghost/pull/5340?ref=ghost.org), [5348](https://github.com/TryGhost/Ghost/pull/5348?ref=ghost.org), [5351](https://github.com/TryGhost/Ghost/pull/5351?ref=ghost.org)

Zelda:

* New screens mocked up in HTML for [Apps](https://github.com/TryGhost/Ghost/pull/5333?ref=ghost.org) & [Themes](https://github.com/TryGhost/Ghost/pull/5362?ref=ghost.org). There will be issues for these once they're ready to code up in Ember.
* Lots of things are blocked by [inline validation](https://github.com/TryGhost/Ghost/issues/5336?ref=ghost.org). This is a high priority issue as it is the biggest blocker we have right now
* [User onboarding](https://github.com/TryGhost/Ghost/issues/5315?ref=ghost.org) (a new setup process) is in progress with an open PR for user invites. This is currently blocked by inline validation.

Priority Issues
---------------

* As stated above, by far and away the most important issue we need fixed is [inline validation](https://github.com/TryGhost/Ghost/issues/5336?ref=ghost.org), as that is a dependency for several other changes.
* All Zelda issues are a priority and have been moved to the [Zelda milestone](https://github.com/TryGhost/Ghost/issues?q=is%3Aopen+is%3Aissue+milestone%3AZelda&ref=ghost.org). Feel free to grab any open issues as these all need to be resolved before the next release can happen.
* Please keep picking up bits of the [middleware refactor](https://github.com/TryGhost/Ghost/issues/5286?ref=ghost.org), as that is super helpful.
* [Autocomplete search](https://github.com/TryGhost/Ghost/issues/5343?ref=ghost.org) is another issue that is a priority and has been assigned to @acburdine and @morficus to tag team.
* There are plenty of beginners issues right now, and a few more are going to be raised. If you are looking for a good way to start contributing, these issues are a great place to start getting involved.

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1433262749001105?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 9th June, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-06-09,270,6bj).


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





 





 
















 






