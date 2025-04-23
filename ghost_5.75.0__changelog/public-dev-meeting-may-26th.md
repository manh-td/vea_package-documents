


Public Dev Meeting May 26th











































Two big events took place in the last week. The first being the release of [0.6.4](https://ghost.org/changelog/ghost-0-6-4/). This release consisted mostly of bug fixes from the 0.6.3 release the week before.

A couple of notable bugs that were fixed were a problem where, on import, multiple owners could be created ([#5260](https://github.com/TryGhost/Ghost/pull/5260?ref=ghost.org)). That would leave people stuck because the system is only supposed to have one owner. Now, if an owner is already in the system, it will demote anyone else it believes to be an owner, down to an admin.

There was also a caching issue that was causing problems with the password protection as well as the post previews. That was solved in [#5302](https://github.com/TryGhost/Ghost/pull/5302?ref=ghost.org) and [#5292](https://github.com/TryGhost/Ghost/pull/5292?ref=ghost.org).

The other big ticket item from this week is that a new admin UI (nicknamed [Zelda](https://github.com/TryGhost/Ghost/pull/5273?ref=ghost.org)) was merged in! This new UI allows for the admin to be much more extensible and flexible for future features. Hannah has created a bunch of issues that need to be taken care of in regards to the new admin and put them into the [current backlog](https://github.com/TryGhost/Ghost/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22Current+Backlog%22&ref=ghost.org). This is definitely a place of need for anyone who is looking for a place to contribute. Hannah wrote a good post on why she is [so excited](https://hannah.wf/zelda/?ref=ghost.org) for the new admin :).

One large topic of discussion during the meeting was whether or not redirects should be added inside the admin when url's are changed to specific areas. The conclusion that was decided on, was to not add any redirects for now, and see if people complain. It would be good not have this bloat in the codebase, so we are taking a wait and see approach to see if anyone complains when it's not there.

### Need Help

* [Implementing search](https://github.com/TryGhost/Ghost/issues/5321?ref=ghost.org) - If you, or anyone you know, has any experience with search, that is an area that is up for [discussion](https://github.com/TryGhost/Ghost/issues/5321?ref=ghost.org). We are trying to figure out the best way to move forward in this respect, and would love some help figuring out the best way to do this.
* [Middleware Refactor](https://github.com/TryGhost/Ghost/issues/5286?ref=ghost.org) - A task list was added to the [middleware refactor issue](https://github.com/TryGhost/Ghost/issues/5286?ref=ghost.org) to help split apart that issue. If you are looking for a place to start contributing with Ghost, this issue may be a good one. One PR was already merged that can be used as guidance ([#5287](https://github.com/TryGhost/Ghost/pull/5287?ref=ghost.org))
* [Current Backlog](https://github.com/TryGhost/Ghost/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22Current+Backlog%22&ref=ghost.org) - As was stated above, these are all important issues to help with the new admin. If there are any other issues you find with "Zelda", feel free to comment on them on [#5314](https://github.com/TryGhost/Ghost/issues/5314?ref=ghost.org) as it is serving as the place to keep track of Zelda issues for now.

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1432657906000344?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 2nd June, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-06-02,270,6bj).


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





 





 
















 






