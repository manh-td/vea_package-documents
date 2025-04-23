


Public Dev Meeting 15th Apr







































This week, we have shaken things up. For the past few weeks the focus of the team has been split between Ember, Apps and the API. We don't have a big enough team for so many big projects!

From now on, we want to switch our focus from big milestones to small (no more than 4 weeks), individual projects and getting everyone working together on one thing at a time. In this way, I believe we'll be able to focus our resources and deliver more.

The [Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org) has been overhauled, with us focusing on the [API project](https://github.com/TryGhost/Ghost/issues?milestone=19&state=open&ref=ghost.org) first, as it is a dependency for everything else. This will be followed by the [Ember.js](https://github.com/TryGhost/Ghost/issues?milestone=17&page=1&state=open&ref=ghost.org) project, and then [Multi-user](https://github.com/TryGhost/Ghost/issues?milestone=4&page=1&state=open&ref=ghost.org) so that we can deliver something big to our users. This is as much as we have planned at present, as time goes on we'll see if this approach works, and schedule in more projects based on what people are asking for, and what the dependencies are.

There is more detail on the [Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org) page, which is constantly updated with more information as and when the plan becomes clear.

#### Master is NOT stable

There was a lengthly discussion during the meeting about the use of the `master` branch.

> Noone should be running a live blog with data they care about on the `master` branch.

It is not a stable branch: this doesn't just mean there could be bugs, it means that you could get your data into a state from which it cannot be migrated, or you could end up unable to edit your blog. If you want to run Ghost from git, either use a [release tag](https://github.com/TryGhost/Ghost/tags?ref=ghost.org) or the [stable](https://github.com/TryGhost/Ghost/tree/stable?ref=ghost.org) branch.

In order to be absolutely clear about this, we're going to add a [warning message](https://github.com/TryGhost/Ghost/issues/2594?ref=ghost.org) to one of the `grunt` tasks, so that anyone trying to build Ghost from master is reminded not to use this for a live blog.

#### Core Developer Hangout

We're going to start running Google+ hangouts for core developers. The first one will be 6:30pm London time on Thursday 17th April. The hangout will be posted to IRC.

We'll aim to do these every 2 weeks or so, at different times to give different people the opportunity to join.

### Full details:

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20140415?ref=ghost.org#pm44304) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode (note that the UK has just moved onto Daylight Savings Time, so the meeting is an hour earlier than it was previously). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: Tuesday 22nd April, 5:30pm London time.


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





 





 
















 






