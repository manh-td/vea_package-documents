


Public Dev Meeting 2nd September







































![](https://ghost.org/changelog/content/images/2021/01/pulse11.png)

Much of the progress this week has been around the merge of the Ghost-UI repo back into Ghost. The merge has been completed, along with the history, and transfer of all open issues. There has also been more refactoring work completed, and we've unstuck ourselves from being able to update our dependency on downsize, meaning that we can make progress on more advanced excerpts.

### Core Team

In this week's meeting we have announced that we are kicking off our new [Core Team](https://github.com/TryGhost/Ghost/wiki/Core-Team?ref=ghost.org) with two people: [Matt Enlow (@novaugust)](https://github.com/novaugust?ref=ghost.org) and [Jason Williams (@jaswilli)](https://github.com/jaswilli?ref=ghost.org). A big thank you to them for agreeing to take on these roles. Our hope is that this will allow us to ship a lot more awesome stuff, much quicker.

In addition [@pauladamdavis](https://github.com/pauladamdavis?ref=ghost.org) will also be getting commit rights on the [Ghost](https://github.com/TryGhost/Ghost?ref=ghost.org) repository, so that he can continue his work on the UI now that it is all in one repo.

### New Workflow

Since releasing 0.5, we've made a lot of changes to our workflow so that we can avoid doing such large releases, and instead release little and often. This switch towards a more agile workflow has included a number of changes, some of which require a little more explanation.

**The Roadmap**

We have a [new public roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) in Trello, which is much easier to keep up-to-date. As issues progress they move from left to right, starting off in the 'backlog column' - which is a big unsorted todo list and eventually landing in the right most 'recently released' column. They also have coloured labels to indicate their status. You can [find out more](https://trello.com/c/0e0L0alW/65-how-does-this-roadmap-work-click-here-to-find-out?ref=ghost.org) by visiting [the roadmap](https://trello.com/c/0e0L0alW/65-how-does-this-roadmap-work-click-here-to-find-out?ref=ghost.org).

The roadmap only lists new features, and is intended to be user-facing. Bugs and technical improvements remain only on GitHub. Once a feature hits one of the middle two columns, it will have a spec and a related issue in GitHub which is marked with the [feature](https://github.com/TryGhost/Ghost/labels/feature?ref=ghost.org) tag.

**GitHub Milestones**

Related to the roadmap, there are then two milestones in GitHub. The current, or 0.5.x Backlog which contains all the issues that are ready to be worked on (includes any features from the middle two columns of the roadmap) and the Future backlog, which much like the backlog on the roadmap, contains things which we know about but which we aren't ready to do just yet.

**Releases and Versioning**

The aim is to keep doing rolling releases, every time we feel like we've completed a couple of features that warrant shipping. The hope is to release every 2-4 weeks, bumping the minor version number (so 0.5.2, 0.5.3, etc). Some larger features, like Apps, or a new Editor would be worked on behind a config flag until they are ready. Turning off the config flag for a large feature is the kind of thing we might do a major version bump for (i.e 0.6).

The overall aim is to be more flexible about what is available to be worked on rather than sticking to projects and hopefully ship features to our users much faster as a result.

### Towards 0.5.2

In order to get ready to do another release, we need to get the admin UI back up to scratch. This means getting the sub items from [#3810](https://github.com/TryGhost/Ghost/issues/3810?ref=ghost.org) polished off and at least the first part of the [new post settings menu](https://github.com/TryGhost/Ghost/issues/3936?ref=ghost.org). Progress on these had been hindered by the Ghost/Ghost-UI split and merger, but are ready to be worked on now

Full details:
-------------

The full logs of the meeting are available from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 9th September, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-9-9,270,6bj).

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





 





 
















 






