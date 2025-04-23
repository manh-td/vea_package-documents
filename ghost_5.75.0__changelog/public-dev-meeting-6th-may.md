


Public Dev Meeting 6th May







































Today we are officially switching over to focusing on [Ember](([https://github.com/TryGhost/Ghost/issues?milestone=17&state=open](https://github.com/TryGhost/Ghost/issues?milestone=17&state=open&ref=ghost.org)).

The [API Project](https://github.com/TryGhost/Ghost/issues?direction=desc&milestone=19&sort=created&state=open&ref=ghost.org) still has a number of issues outstanding. We're working on wrapping these up as quickly as we can. We've done quite a bit of refactoring, and a lot of what's left is mopping up, so it may take a few more days to get all the PRs in on top of one another.

While a few people carry on cleaning up and finishing off the last few bits of the API, it is time for us to switch our focus to Ember 100%. This will happen over the course of this week. The first task is to figure out what to do with the 4 open PRs, whether to merge them or hold them for now so that we can merge the ember branch into master.

There are a couple of big niggles with the Ember project at the moment, most notably, how we plan to access the API and deal with the data. We need to make sure that we have a clear plan for this. It's being discussed in [#2699](https://github.com/TryGhost/Ghost/issues/2699?ref=ghost.org) and the outcome of the discussion should be a clear plan / process documented on the [Ember wiki doc](https://github.com/TryGhost/Ghost/wiki/Ember-Admin-UI?ref=ghost.org).

The next steps will be to get the Ember admin UI up to enough of a standard that we can delete the old admin. In order to do this, we need to have ported the majority of the functionality including all the minute details of behaviour that may otherwise be lost. There are many open issues and we will continue to improve visibility on where we are as the week goes on.

#### Tips for working on Ember:

The issue list lives on the [Ember.js milestone](https://github.com/TryGhost/Ghost/issues?milestone=17&state=open&ref=ghost.org), and there is an [epic issue](https://github.com/TryGhost/Ghost/issues/2271?ref=ghost.org) which is a good place to start looking to get an idea of what this project involves. The majority of the issues currently open are blocks of functionality that need porting over from the old admin. Any issue which is directly to do with Ember, or 'Emberifying' something, is also marked with `[Ember.js]` at the start of the title, so that people only interested in Ember issues can filter GitHub notifications from Ghost.

Currently, the Ember.js version of the admin lives on the [ember](https://github.com/TryGhost/Ghost/tree/ember?ref=ghost.org) branch on GitHub, on which there are two versions of the admin. The old admin still lives in its usual place at `/ghost/` and the Ember.js version lives at `/ghost/ember/`. This week we will merge the ember branch into master, and delete it. At that point the two admins will still coexist, but on the main master branch. We hope to be able to remove the old admin and have only the new admin somewhere around the meeting after next (20th May).

Please keep an eye on the [Ember wiki doc](https://github.com/TryGhost/Ghost/wiki/Ember-Admin-UI?ref=ghost.org) as we will continue to update that with relevant / useful info as we think of it.

If you have any questions, are interested in picking up some work or otherwise getting involved, please swing by our #ghost channel on freenode. We'd love to help you get started contributing to the Ember project. There will be a video chat, probably on Thursday 15th of May for anyone looking for some guidance on getting started - more details next week.

### Full details:

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20140506?ref=ghost.org#pm43616) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 13th May, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-5-13,270,6bj).


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





 





 
















 






