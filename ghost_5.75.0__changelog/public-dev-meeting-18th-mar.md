


Public Dev Meeting 18th Mar







































There were two main points on the agenda for this week's meeting:

* Shipping 0.4.2
* Ember.js rewrite

0.4.2
-----

We are about to release master as 0.4.2. The deadline for PRs was Monday, and now we are in the process of merging, testing, cleaning up and getting a release candidate ready. 0.4.2 has some awesome features, including tag pages, and will be the first version of Ghost published to npm.

There are a couple of issues which still have some work outstanding. [#2312](https://github.com/TryGhost/Ghost/issues/2312?ref=ghost.org) I have not yet PR'd as the fix is pretty ugly and it seems more appropriate at this stage to run a temporary showdown fork. [#2148](https://github.com/TryGhost/Ghost/issues/2148?ref=ghost.org) needs a little cleanup work, and [#2149](https://github.com/TryGhost/Ghost/issues/2149?ref=ghost.org) is still open as there is potential for futher improvements. All of this should be sorted out over the next day or so and the 0.4.2 RC should land on Thursday 20th, final release should be Tuesday 25th.

Ember.js rewrite
----------------

This week, @hswolff made significant headway with scaffolding the app - all the screens now exist in some form. There are [~20 new issues](https://github.com/TryGhost/Ghost/issues?milestone=17&page=1&state=open&ref=ghost.org) that have been opened and are mostly ready to start on.

For anyone who is unfamiliar with the Ember rewrite, it lives on the [ember](https://github.com/TryGhost/Ghost/tree/ember?ref=ghost.org) branch. This branch has the old admin located in it's usual place at `/ghost/` and the new ember admin located at `/ghost/ember/` so that anyone joining in but new to Ghost development can reference the old admin. When switching to the ember branch, we recommend running `grunt clean && grunt init && grunt dev` to get up and running (we should probably make a shorthand for this).

There are a couple of blockers to work on the Ember rewrite, the biggest of which being the discussion around the divide between what should live in Ember and what should live in Ghost-UI - Ghost's bootstrap-like frontend framework. I've raised issue [#2446](https://github.com/TryGhost/Ghost/issues/2446?ref=ghost.org) to continue this discussion, and welcome all to get involved.

Aside from this, there is also some work needed to get fixtures sorted out ([#2415](https://github.com/TryGhost/Ghost/issues/2415?ref=ghost.org)), which in part depends upon the work we are doing to redesign the API following the [JSON API](https://jsonapi.org/?ref=ghost.org) standard as closely as possible. The API redesign & refactor is also pivotal to delivering Apps, so we are looking to get more people involved with this - if you like APIs come give us a hand :)

### Full details:

The full logs of the meeting are available from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next weeks meeting: Tuesday 25th March, 5:30pm London time.


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





 





 
















 






