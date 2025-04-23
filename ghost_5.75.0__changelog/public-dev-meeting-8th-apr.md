


Public Dev Meeting 8th Apr







































Last week we set out three things as core focus points for the week:

* Tests - get these passing reliably again
* Ember.js - get both notifications and modals in place
* The API - get the issues for this sorted out

We've made some serious progress on improving the tests, most of the random failures are now resolved. There are still a few in the [pg build](https://github.com/TryGhost/Ghost/issues/2499?ref=ghost.org) which is going to be looked at this week.

Modals have landed in the [ember](https://github.com/TryGhost/Ghost/tree/ember?ref=ghost.org) branch, notifications are in a PR which is almost ready to merge. Elsewhere in ember-land there has been much progress and with modals and notifications many features can be built out. The main blocker now is having a full fake API for the ember branch to work against. This will be a core focus this week.

Progress with the API hasn't been quite so smooth. Last week we were in a position where a decision had been made on how to proceed, and we just needed to divide it up into a set of issues to get it into the pipeline. However, that was turned on its head by me having second thoughts about the [JSON-API](https://jsonapi.org/?ref=ghost.org) standard and [what it means for Ghost](https://github.com/TryGhost/Ghost/issues/2362?ref=ghost.org).

I feel very strongly that in our case, consistency between the different ways of consuming the API is more important than potential performance improvements that can be achieved by using linked objects instead of inline objects. During the meeting, this was the consensus - that we should continue to work towards supporting the JSON API standard, but keep our objects inline, and later on add an option for linked objects.

One result of the change towards following JSON API is that the `pagination` object which is currently created and given to themes will be renamed `meta`. This will not affect the pagination helper, but will affect any themes using the `pagination` object directly (I know of none, if you're doing this, please get in touch). `pagination` will be deprecated for 2 releases before it is removed.

In the world of Apps, much progress has been made in the last week, however the majority of that progress is living out on the [apps-perms](https://github.com/TryGhost/Ghost/tree/apps-perms?ref=ghost.org) branch. This branch contains all of the data models & new permissions code needed to deliver apps in a safe way. The next step is to create a set of test cases to verify that what we have is correct, and merge in this branch after next weeks meeting unless there are problems.

This week's focus points:

* Ember.js - ensure the mock API is complete with lots of data & start looking at how we might use models in future.
* API - get issues opened for migrating the format & ensuring consistency
* Apps - get everyone working towards their own example app & helping define the missing GDK APIs

The big focus for the core team this week is to get building the fundamentals of a series of apps. We want to use this to inspire tests and use cases for different apps, collaborate on a set of wiki pages around missing GDK Apis (routing, assets, etc) and to put together a series of issues to move these forward. Next weeks meeting will focus on how to deliver various parts of the GDK.

### Full details:

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20140408?ref=ghost.org#pm43551) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode (note that the UK has just moved onto Daylight Savings Time, so the meeting is an hour earlier than it was previously). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: Tuesday 15th April, 5:30pm London time.


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





 





 
















 






