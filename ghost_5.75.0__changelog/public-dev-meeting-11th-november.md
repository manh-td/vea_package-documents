


Public Dev Meeting 11th November







































![](https://ghost.org/changelog/content/images/2021/01/image-25.png)

This week I was away at [Full Frontal](https://ffconf.org/?ref=ghost.org) speaking about managing open source projects. As a result I've got a lot of inspiration on how to improve our processes and be more open, but I'm also looking for feedback from our community members via issue [#4396](https://github.com/TryGhost/Ghost/issues/4396?ref=ghost.org) - a discussion on improving our development process. Please get involved!

### Progress towards 0.6

Since the release of 0.5, we've been working on releasing user-facing features to try to reach more of a feature parity with other publishing systems. We've been steadily releasing every time we have a few more feaures to offer, but what hasn't been clear is what the full set of features we want to have before we call Ghost 0.6 is, and what happens after that.

To try to resolve this, we're going to have a 'Road to 0.6' writeup either as an issue or on the wiki. This will detail both the features we need to build and the underlying infrastructure projects we need to do to build them well, and be ready for the next set of features. During the meeting we discussed which features those present felt were most obviously missing.

Some of the candidates include: tag management, previous and next post links, post filtering, shareable preview, a navigation builder tool and a query helper to give theme developers access to the API.

This will all be written up and shared on the dev blog when it's ready, so watch this space :)

### Memory Leak and Maintenance Release

There have been several reports in the last week or two of a memory leak in Ghost 0.5.3. That memory leak has been confirmed as existing in 0.5.3 only, found, and fixed (big thanks to [@jaswilli](https://github.com/jaswilli?ref=ghost.org)). There's one more small bug we'd like to fix before cutting a maintenance release: [#4400](https://github.com/TryGhost/Ghost/issues/4400?ref=ghost.org) - autosave is causing some people to get 'Do you want to leave' nag warnings at the wrong times. 0.5.4 will likely land this week with several bug fixes and improvements.

**Update:** the memory leak fix is a single file patch, if you need it you can find it [here](https://github.com/TryGhost/Ghost/pull/4430/files?ref=ghost.org). The fix will be released in 0.5.4 on Monday 17th.

Full details:
-------------

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20141104?ref=ghost.org#pm53732) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 18th November, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-11-18,270,6bj).

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





 





 
















 






