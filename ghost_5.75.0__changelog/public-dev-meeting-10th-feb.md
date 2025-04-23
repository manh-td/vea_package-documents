


Public Dev Meeting 10th Feb










































This week we switched over to Ember 1.10, so the Ghost admin now runs on HTMLbars rather than Handlebars.

It's been another relatively quiet week where I've been (unfortunately) internally focused. However, this week we've seen PRs land for both of the major remaining parts of navigation, and we're hoping to get them merged asap so that we can test the whole feature in the wild.

There were a few minor updates to the `{{navigation}}` helper discussed in the meeting, but these are expected to land very quickly.

Implementation of the [`{{#get}}` helper](https://github.com/TryGhost/Ghost/issues/4439?ref=ghost.org) is currently stuck due express-hbs's async helpers not working properly for block helpers. A fix is being worked on, as this is also blocking the [next and prev post](https://github.com/TryGhost/Ghost/issues/4799?ref=ghost.org) helpers.

Support for node v0.12 was briefly discussed during the meeting, we're still waiting for some of our dependencies to add support. Ghost itself should not need changes to support it, so once our dependencies are ready our next release will support it.

Full details:
-------------

The [full logs of the meeting](https://botbot.me/freenode/ghost/2015-02-10/?msg=31680044&page=2&ref=ghost.org) in our IRC logs, which are looked after by the lovely folks at [botbot.me](https://botbot.me/freenode/ghost?ref=ghost.org).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 17th February, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-02-17,270,6bj).


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





 





 
















 






