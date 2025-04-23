


Public Dev Meeting 19th August







































![](https://ghost.org/changelog/content/images/2021/01/image-3.png)

Following such a large release, we've had a somewhat quieter week mostly focused on cleaning up old GitHub issues and fixing bugs. There have been ~5 major issues reported with 0.5 which are either fixed or being fixed, and the `next` branch will be released as 0.5.1 with just these fixes in a week or so.

Meanwhile, master has had a makeover, with the new 'GUI2' design refresh being merged in this week. The refreshed design focuses mostly around navigation and settings, giving us more freedom to build out future features. There are still some Ember bits and pieces which need wiring up for the new design, these are detailed in [#3810](https://github.com/TryGhost/Ghost/issues/3810?ref=ghost.org).

![](https://ghost.org/changelog/content/images/2021/01/image-4.png)

Priorities for Ghost development are now:

1. Fix the remaining 0.5 bugs marked next ready for a maintenance release
2. Resolve [issues](https://github.com/TryGhost/Ghost/issues/3810?ref=ghost.org) with the new design so that we are ready to do a feature release again
3. Get new features that are on the [roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) ready to ship
4. Resolve as many of the bugs in the 0.5.x backlog as possible

With the new release cycle, development will continue this way. With the [public roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) determining which features will ship next, and the current backlog being kept full of other issues that we want to make progress with. Each month, we'll release a new version, perhaps with some in-progress features disabled by default. When major features land or feature sets are completed this will result in a minor version bump (i.e. to 0.6), but otherwise we'll keep incrementing 0.5 as and when we feel we have something worth releasing :)

#### Note on the npm package

Due to an inconsistency between grunt and npm's handling of file globbing, the original 0.5 npm package was missing the HTML email templates. Therefore the npm package is currently at `0.5.1-1`, slightly ahead of everything else.

### Full details:

The full logs of the meeting are available from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 26th August, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-8-26,270,6bj).

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





 





 
















 






