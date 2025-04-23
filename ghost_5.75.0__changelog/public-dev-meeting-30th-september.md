


Public Dev Meeting 30th September







































![](https://ghost.org/changelog/content/images/2021/01/image-34.png)

Ghost 0.5.2 is out! We managed to turn it around in 6 weeks, which for us is pretty speedy, as well as cram in a heap of code base improvements along with the shiny new design and awesome new features. As always, I want to thank all the people who worked hard on making 0.5.2 happen :)

This week's meeting ended up being pretty long, as we reviewed the issues that we're looking to get closed in the near future as well as the long list of open PRs. During the meeting we also reviewed the [public roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) and renamed the columns to try to make it clearer that it reflects the progress of the project as opposed to being a clear plan of what will happen and when. As an open source project depending on contributions from volunteers it makes far more sense to focus on making it clear to developers what is ready to work on, and showing our users what features they're likely to see next.

### What's next?

At the moment, there are quite a few open or PR'd UI issues as an (expected) result of the design refresh. Therefore the next time we cut master as a release, it's likely to be mostly full of UI bug fixes.

As well as the features on the roadmap, there are a number of high priority internal issues that need people working on them. In order to ship new features, we need to implement [#3910 permissions migrations](https://github.com/TryGhost/Ghost/issues/3910?ref=ghost.org) - specifically so that we can add new permissions for new parts of the API. There are also a number of missing column migrations that are needed in order to properly look at [#4134 reviewing max lengths in the database schema](https://github.com/TryGhost/Ghost/issues/4134?ref=ghost.org).

We have had a couple of recent PRs looking to add new storage methods to Ghost, but the issue  
[#2852 More Filestorage Abstraction](https://github.com/TryGhost/Ghost/issues/2852?ref=ghost.org) doesn't seem to get much love despite being a prerequisite to making this work. Additionally we have had quite a lot of interest in [#827 Proposal: expose Ghost as reusable express middleware](https://github.com/TryGhost/Ghost/issues/827?ref=ghost.org), but the discussion on how this should work never quite reaches conclusion - despite us being 90% of the way there. If these issues are interesting to you, come get involved!

I'm also looking to push forward on updating the admin functional tests with [#3350 Create functional tests for MU](https://github.com/TryGhost/Ghost/issues/3350?ref=ghost.org) as we've seen a couple of regressions in the UI which could have been prevented with testing. If you're looking to get started with contributing to Ghost, submitting PRs to improve the tests is often a great first step - and a guaranteed merge ;)

Full details:
-------------

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20140930?ref=ghost.org#pm43627) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 7th October, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-10-07,270,6bj).

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





 





 
















 






