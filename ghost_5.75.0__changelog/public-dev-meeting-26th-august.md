


Public Dev Meeting 26th August







































![](https://ghost.org/changelog/content/images/2021/01/image.png)

We've had a couple of interesting developments in the codebase this week. Firstly, [@jaswilli](https://github.com/jaswilli?ref=ghost.org) did an epic [PR](https://github.com/TryGhost/Ghost/pull/3826?ref=ghost.org) to switch our promise library from [when](https://github.com/cujojs/when?ref=ghost.org) to [Bluebird](https://github.com/petkaantonov/bluebird?ref=ghost.org), which we hope will bring improvements to both performance, and reliability. Secondly, [@JoshWillik](https://github.com/JoshWillik?ref=ghost.org) has refactored the [Ghost startup](https://github.com/TryGhost/Ghost/pull/3815?ref=ghost.org), such that  requiring Ghost no longer results in the express server starting. This moves us much closer to being useful as a package to include in other software and to exposing Ghost as [express middleware](https://github.com/TryGhost/Ghost/pull/827?ref=ghost.org).

#### 0.5.1 Maintenance release

Out on the [next](https://github.com/TryGhost/Ghost/tree/next?ref=ghost.org) branch, all the critical bugs have been fixed, ready to ship as 0.5.1. This morning (since the meeting) the 0.5.1 release has been cut and pushed to [GitHub](https://github.com/TryGhost/Ghost/releases?ref=ghost.org), [npm](https://www.npmjs.org/package/ghost?ref=ghost.org) and the [stable branch](https://github.com/TryGhost/Ghost/tree/stable?ref=ghost.org).

#### Triaging the backlog

Over the past couple of weeks, there's been an effort to triage and close as many old issues as possible and cleanup our backlog. Moving forward we want to be leaner and cleaner with what issues are open. Issues which are bugs and features or technical improvements we actively want to work on will live in the 0.5.x backlog. Bugs should be a priority, if they are true bugs we don't want them hanging around for longer than 1 release if possible.

Any longer term issues which are not actively ready to work on will live in the future backlog, this list will stay minimal and mostly be old issues with lots of history. Feature requests that aren't likely to be worked on in the near future will be closed in favour of a card on the [public roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). The aim is to make it much, much clearer what issues are ready to be worked on and make the backlog much easier to digest and become familiar with.

#### Core Team

We've been talking for a while now about having a concept of a 'Core Team': a group of contributors who lead development and help us to regularly ship high quality code. I have published an overview of the [Core Team](https://github.com/TryGhost/Ghost/wiki/Core-Team?ref=ghost.org) on the wiki which covers what it means and what makes someone likely to be considered for the role. In next week's meeting we'll announce who the first members will be.

#### End of Ghost-UI

Back in [March](https://ghost.org/changelog/no-more-ruby-dependency/) we moved all of Ghost's SASS over to the Ghost-UI repository so that we no longer had a ruby dependency in the main Ghost repo. We hoped to turn the code into a Bootstrap-esque framework with reusable generic components.

Unfortunately this hasn't worked out. Managing issues across the two repositories is an administrative nightmare, and the switch to Ember means there's not really a good way to build components in a separate repo. This week we'll be switching Ghost-UI to use [libsass](https://github.com/sass/libsass?ref=ghost.org) to remove the ruby dependeny, and then move the SASS back to the Ghost repo.

#### Towards 0.5.2

In order to ship another feature release, we need to clean up after the GUI 2.0 design refresh (see  
[#3810](https://github.com/TryGhost/Ghost/issues/3810?ref=ghost.org)), which in turn depends on us moving Ghost-UI back to the Ghost repo. Once this is done we hope to bash out a couple of the features which are made possible by the new Post Settings Menu design. We'll release 0.5.2 as soon as the bugs are fixed and we have a couple of worthy features ready to go.

### Full details:

The full logs of the meeting are available from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 2nd September, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-9-2,270,6bj).

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





 





 
















 






