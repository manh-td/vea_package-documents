


Public Dev Meeting 17th May











































Quick Summary
-------------

Tonnes of improvements & bug fixes landed this week ready for 0.8, which will be landing very soon. We're also planning to split off the Ghost admin client into it's own repo shortly after the release.

Progress Report
---------------

* General bug fixes - [#6808](https://github.com/TryGhost/Ghost/pull/6808?ref=ghost.org), [#6818](https://github.com/TryGhost/Ghost/pull/6818?ref=ghost.org), [#6821](https://github.com/TryGhost/Ghost/pull/6821?ref=ghost.org), [#6822](https://github.com/TryGhost/Ghost/pull/6822?ref=ghost.org), [#6830](https://github.com/TryGhost/Ghost/pull/6830?ref=ghost.org), [#6834](https://github.com/TryGhost/Ghost/pull/6834?ref=ghost.org)
* Dependency upgrades - [#6838](https://github.com/TryGhost/Ghost/pull/6838?ref=ghost.org)
* Structured data improvements - [#6823](https://github.com/TryGhost/Ghost/pull/6823?ref=ghost.org), [#6824](https://github.com/TryGhost/Ghost/pull/6824?ref=ghost.org)
* Subscribe functionality - [#6764](https://github.com/TryGhost/Ghost/pull/6764?ref=ghost.org), [#6809](https://github.com/TryGhost/Ghost/pull/6809?ref=ghost.org), [#6811](https://github.com/TryGhost/Ghost/pull/6811?ref=ghost.org), [#6814](https://github.com/TryGhost/Ghost/pull/6814?ref=ghost.org), [#6816](https://github.com/TryGhost/Ghost/pull/6816?ref=ghost.org), [#6817](https://github.com/TryGhost/Ghost/pull/6817?ref=ghost.org), [#6842](https://github.com/TryGhost/Ghost/pull/6842?ref=ghost.org)
* Test improvement - [#6703](https://github.com/TryGhost/Ghost/pull/6703?ref=ghost.org)
* Pre-populate setup values - [#6810](https://github.com/TryGhost/Ghost/pull/6810?ref=ghost.org)
* Remove select-all on click for PSM slug - [#6812](https://github.com/TryGhost/Ghost/pull/6812?ref=ghost.org)
* Update document title on blog title change - [#6839](https://github.com/TryGhost/Ghost/pull/6839?ref=ghost.org)
* Permissions improvements - [#6804](https://github.com/TryGhost/Ghost/pull/6804?ref=ghost.org)

Two further open PRs for the structured data [#6841](https://github.com/TryGhost/Ghost/pull/6841?ref=ghost.org), [#6847](https://github.com/TryGhost/Ghost/pull/6847?ref=ghost.org)

Discussion
----------

This week we talked about splitting the Ghost admin client into its own repository. The ember app that is hte admin client has its own needs in terms of testing, tooling and dependency management. Keeping it in the same repository as the Node.js app has started to create serious pain points particularly around the travis builds.

We feel we've reached the crossover point, where the cons of having the repos together are starting to outweigh the benefits. The current plan is to move the content of the `core/client` folder into a new repo, and include it back into Ghost using git submodules, in the same way that Casper is managed.

Not everyone is convinced this is a good plan. We've tried splitting out pieces of Ghost before and ended up reverting due to the difficulties of managing issues across multiple repos. In this case, we're planning to not have an issues list on the second repo, and to use submodules instead of package dependencies to try to mitigate the issues we saw previously.

This is an experiment, and only time will tell us whether splitting is the best option🔬.

The [full logs of the meeting](https://ghost.slack.com/archives/dev/p1462897862000906?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #dev channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 24th May, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2016-05-24,270,6bj).


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





 





 
















 






