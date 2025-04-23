


Public Dev Meeting 25th Feb







































Yesterday's meeting revolved heavily around our decision to use [Ember.js](https://emberjs.com/?ref=ghost.org) as our framework of choice for rebuilding the admin UI. If you'd like to read more about this decision, check out our [announcement post](https://ghost.org/changelog/hello-ember).

I would like to thank everyone who took the time to write one of the ~100 incredibly valuable and constructive comments on the [discussion thread](https://github.com/TryGhost/Ghost/issues/2144?ref=ghost.org) and particularly thank the people who took the time to write some demo code: [@hswolff](https://github.com/hswolff?ref=ghost.org) wrote an example of the post settings menu in [Angular](https://github.com/TryGhost/Ghost/pull/2211?ref=ghost.org), [@samccone](https://github.com/samccone?ref=ghost.org) and [@brian-mann](https://github.com/brian-mann?ref=ghost.org) demonstrated how much better our Backbone code could be with [Marionette](https://github.com/TryGhost/Ghost/pull/2253?ref=ghost.org), [@petehunt](https://github.com/petehunt?ref=ghost.org) showed how much easier it would be to build our settings page in [React](https://github.com/TryGhost/Ghost/pull/22590?ref=ghost.org) and [@manuelmitasch](https://github.com/manuelmitasch?ref=ghost.org) wrote an [ember demo](https://github.com/manuelmitasch/ghost-admin-ember-demo/?ref=ghost.org) of the Ghost admin UI that was also worked on by [@Globegitter](https://github.com/Globegitter?ref=ghost.org).

Over the next week or so, we'll start getting a branch ready to redevelop the admin in Ember. If you'd like to get up to speed with ember, you can try out the [CodeSchool](https://www.codeschool.com/?ref=ghost.org) course (drop an email to [corey@codeschool.com](mailto:corey@codeschool.com) if you need it adding to your account). We've got several core team members and developers from ember willing to help us out, but we also want to get as many Ghost contributors, new and old, involved in the code re-write as possible.

Right now, we're not 100% sure whether we're going to down tools on Apps to focus on this, or focus on shipping Apps first. The two projects will likely run side by side for a little while until we have a clearer idea of how much work is involved. We will update the roadmap & publish details of any changes to the plan as and when we are certain.

---

As well as the exciting news of the switch over to ember, we have a few other updates from today's meeting:

#### Introducing Ghost UI

This week we started a new GitHub repository called Ghost UI. We're going to split out the UI - that is SASS and interaction based JS into this repo in the form of a heavily Bootstrap-inspired user interface framework. Ghost UI will contain SASS and JS, which will be built out into a single `.css` and `.js` file that will then be included in Ghost via [bower](https://github.com/bower/bower?ref=ghost.org).

The Ghost UI repository will also contain extensive documentation for the framework, it's components and the parts that make them up. The intension is to make it easier for designers and frontend developers to get involved with and contribute to the Ghost project. We believe we're the first OSS project of our kind to structure our development this way, and we really hope it will help to encourage more frontend contributions.

#### Ghostalk

A few of our contributors have started a Ghost podcast! The first episode of 'Ghostalk' featuring [Fabian Becker](https://github.com/halfdan?ref=ghost.org), [Gabor Javorszky](https://github.com/javorszky?ref=ghost.org) and [Nick Pfisterer](https://github.com/nickpfisterer?ref=ghost.org) is available on [https://talk.ghost.io](https://talk.ghost.io/?ref=ghost.org), it covers all the latest goings on in the world of Ghost Development, and is far more digestible than IRC logs!

[![Ghostalk](https://puu.sh/7b3XN.jpg)](https://talk.ghost.io/?ref=ghost.org)

### Full details:

The full logs of the meeting are available from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next weeks meeting: Tuesday 4th March, 5:30pm London time.


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





 





 
















 






