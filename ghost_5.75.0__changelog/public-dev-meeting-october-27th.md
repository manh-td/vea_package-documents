


Public Dev Meeting October 27th











































This week we held our public development meeting as a Google hangout on air for the second time. If you'd like to watch it back, you can do so [on youtube](https://youtu.be/hFZ-_iCbs0I?ref=ghost.org).

Meeting Summary
---------------

This was our first meeting after attempting to work in a 2 week sprint. There was an overwhelming consensus that the two weeks went by incredibly quickly, that we didn't get as much done as we thought we would, and that we are going to need to do this a few times to get into the rhythm of it. It does feel good to have a clear focus for the two week period though.

For the next two weeks, the focus is going to be on finishing up the few outstanding pieces of public API work so we can do an initial release of the new features behind a labs flag. Once that's done, the remaining time in the sprint will be used to do some maintenance tasks that have become much-needed. This includes putting together a clear plan for doing ember acceptance tests, and refactoring several pieces of the frontend and API code that are getting in the way of other work.

As there will be a release mid-sprint, we'll also be able to pick up any bug fixes or improvements, which result from feedback on the next version of Ghost.

A couple of things that were brought up during the meeting:

#### Node 4.2 support

We intend to add support for Node 4.2 (LTS) once we've achieved confidence that our dependencies all work correctly and that there are no memory issues with Ghost on Node 4.2. Although people are keen for us to switch, it is hard to build a value proposition for this as Ghost doesn't make use of any new features. There may be a minor performance boost, but the garbage collection behaviour is lazier, so overall there's no real benefit to using it.

There is also an issue as newer versions of npm use up significantly more memory whilst doing `npm install`. This means users on small VPSs will likely need to configure their virtual memory correctly to be able to install Ghost.

#### API helper

There has been significant [discussion](https://github.com/TryGhost/Ghost/issues/5942?ref=ghost.org) on the best approach for adding an API helper to Ghost themes, so that theme authors can quickly and easily make ajax requests to the API. During the meeting we discussed adding config via meta tags, and doing a quick implementation of a helper included via `{{ghost_foot}}` if the labs flag is checked and the `ghost-frontend` client is active.

With Public API access, an api/ajax helper, and the `{{#get}}` helper all available behind a labs flag, we should be able to provide an initial release very soon. This should allow theme developers to start testing out these new pieces of functionality and provide some feedback, and permit us to make backwards incompatible changes before releasing without the labs flag.

### Full details

If you'd like more details of what happened during the meeting, you can [on youtube](https://youtu.be/hFZ-_iCbs0I?ref=ghost.org).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #dev channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 3rd November, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-11-03,270,6bj).


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





 





 
















 






