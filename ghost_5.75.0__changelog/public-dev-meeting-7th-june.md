


Public Dev Meeting 7th June











































Quick Summary
-------------

Release of 0.9.0 Beta 1. The back end and front end for timezones has been merged in.

Progress Report
---------------

* Force UTC timezone at server level - [#6877](https://github.com/TryGhost/Ghost/pull/6877?ref=ghost.org), [#6917](https://github.com/TryGhost/Ghost/pull/6917?ref=ghost.org), [#6921](https://github.com/TryGhost/Ghost/pull/6921?ref=ghost.org)
* Add timezone front end to the admin - [#29](https://github.com/TryGhost/Ghost-Admin/pull/29?ref=ghost.org)
* Add version header to api calls - [#38](https://github.com/TryGhost/Ghost-Admin/pull/38?ref=ghost.org), [#39](https://github.com/TryGhost/Ghost-Admin/pull/39?ref=ghost.org)
* Improvement to the CSV subscriber import feature - [#6923](https://github.com/TryGhost/Ghost/pull/6923?ref=ghost.org)
* Bug fixes - [#6920](https://github.com/TryGhost/Ghost/pull/6920?ref=ghost.org)
* General improvements - [#6889](https://github.com/TryGhost/Ghost/pull/6889?ref=ghost.org), [#6915](https://github.com/TryGhost/Ghost/pull/6915?ref=ghost.org)
* Dependency updates - [#6927](https://github.com/TryGhost/Ghost/pull/6927?ref=ghost.org), [#35](https://github.com/TryGhost/Ghost-Admin/pull/35?ref=ghost.org), [#33](https://github.com/TryGhost/Ghost-Admin/pull/33?ref=ghost.org), [#42](https://github.com/TryGhost/Ghost-Admin/pull/42?ref=ghost.org), [#43](https://github.com/TryGhost/Ghost-Admin/pull/43?ref=ghost.org), [#16](https://github.com/TryGhost/Ghost-Admin/pull/16?ref=ghost.org), [#6934](https://github.com/TryGhost/Ghost/pull/6934?ref=ghost.org)

Discussion
----------

* Continued progress on the validations refactor - [#46](https://github.com/TryGhost/Ghost-Admin/pull/46?ref=ghost.org)
* Would love some testing on the early [0.9.0 beta release](https://github.com/TryGhost/Ghost/issues/6933?ref=ghost.org)
  + You **must do a backup** before installing this because Ghost will perform a migration of every single date in your database
  + That allows all the dates and times to be utc which can then be converted based on the date the user choses
* Some more work needed to make things better for the repository split
* Working on post scheduling is next now that timezones has been added
* Ghost 0.9.0 will not including emailing subscribers. Once the scheduling stuff is nailed down, then that will come.

The [full logs of the meeting](https://ghost.slack.com/archives/dev/p1465317064000058?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #dev channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 14th June, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2016-06-14,270,6bj).


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





 





 
















 






