


Public Dev Meeting 23rd September







































![](https://ghost.org/changelog/content/images/2021/01/image-35.png)

As of the meeting, we had all the intended features on [the roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) for this release sat ready and waiting to go. There are 7 major features in this release, which is a lot more than we expected to be packing for 0.5.2. All that's left now is to clean up the remaining bugs and blocker issues and we can push this out to the world.

Over the past few weeks, we've made a lot of progress not just on features, but also on cleaning up our backlog of issues on GitHub - even with the ongoing release-bug-finding madness, our issue count sits in the 160s, whereas two months ago that was well over 300. That's not just because we've been closing invalid issues, but because we've struck a great balance between working on issues from the backlog and developing new features. We're building new things and improving the code base and it's all very exciting.

The last week has seen a lot of outstanding UI bugs closed, as well as many more found and raised. We've also crammed in some refactoring and cleanup work to try to make the server side clearer and easier to work with as well as improve the Ghost start up sequence with much better error handling. We hope this will reduce some common difficulties with installing and upgrading by making them much easier to solve.

### When do we release?

We're getting asked a lot of questions around when the code base is considered ready for release, when a release is done, and how to know it has been done or find the code in advance.

The first step in being ready for a release is that all the code we want in the release is merged into the codebase. The [public roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) lists the status of all the user-facing features that are intended to be in the release. Any issue or pull request that needs to be fixed or merged before the release is marked with the blocker label on GitHub.

As soon as everything is merged, you'll see a Release Candidate appear on the [GitHub releases](https://github.com/TryGhost/Ghost/releases?ref=ghost.org) page. These are orange 'pre-releases', and are essentially the release minus any serious bugs that get found. The RC is created for testing purposes, it gives everyone a stable point to work from to check everything is a-ok.

Once we're happy that the RC is ok, or if there are bugs once they are resolved, the release will then happen at the next opportunity. At the moment, the process is pretty manual, long winded and done by me so it's always started in the morning UK time, this will change in future as we work on automating the release process.

If you're looking to see if the release has happened yet, the first place the release will appear will be on the [GitHub releases](https://github.com/TryGhost/Ghost/releases?ref=ghost.org) page, followed by npm, the stable branch and Ghost.org. Meanwhile, Ghost(Pro) blogs are upgraded in the background.

### After 0.5.2

With 0.5.2 nearly ready for release, it's time to start looking at what will make it into the next feature release. The roadmap is fully loaded, continuing the split focus between improving the admin panel to provide more features like [auto save](https://trello.com/c/egFgiq01/31-post-auto-save?ref=ghost.org) and the [filter menu](https://trello.com/c/7GUDsl3J/48-post-filter-menu?ref=ghost.org) and adding enhancements to the theme API such as [adding open graph tags](https://trello.com/c/ZfTHFqcy/43-open-graph-tags-by-default?ref=ghost.org) and other structured data by default.

If there's a feature you'd like to help us build, come visit us in IRC and we'll give you a hand getting started!

Full details:
-------------

The full logs of the meeting are available from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 30th September, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-9-30,270,6bj).

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





 





 
















 






