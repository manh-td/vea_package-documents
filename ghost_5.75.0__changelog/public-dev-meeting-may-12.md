


Public Dev Meeting May 12











































This week was filled mostly with bug fixes and maintenance gearing up towards the release of 0.6.3. Hopefully this release will be coming next week or so and will have some great new features along with it.

Bug Fixes
---------

There was a bug found that would cause the auto save to change the post status from draft to published. A pull request was merged in ([#5244](https://github.com/TryGhost/Ghost/pull/5244?ref=ghost.org)) that makes it so auto save isn't able to change the status of the post, just save in its current state.

Also, there was an issue with the email validator that was fixed in [#5243](https://github.com/TryGhost/Ghost/pull/5243?ref=ghost.org).

Maintenance
-----------

A number of the dependencies for Ghost were updated ([#5225](https://github.com/TryGhost/Ghost/pull/5225?ref=ghost.org) and [#5226](https://github.com/TryGhost/Ghost/pull/5226?ref=ghost.org)), and some updates were made to ember ([#5222](https://github.com/TryGhost/Ghost/pull/5222?ref=ghost.org) and [#5221](https://github.com/TryGhost/Ghost/pull/5221?ref=ghost.org)) to keep it updated and get it ready for the new versions of ember that are coming shortly.

A new editor config file was added that makes it easier for contributors to keep all of the code styling the same ([#5244](https://github.com/TryGhost/Ghost/pull/5244?ref=ghost.org)).

And lastly, some updates were made to help reduce the payload of storing and using the password to protect the front end of the blog ([#5232](https://github.com/TryGhost/Ghost/pull/5232?ref=ghost.org)).

Coming Up
---------

Front end password protection is currently under the 'Labs' section in the Ghost admin. It will be moved into full production for the upcoming release.

As we are coming up on the next release, we could definitely use some help picking up any lingering bug issues, or having some QA testing done to make sure any new bugs are fixed. Thanks, and see you again next week :).

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1431448449000611?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 19th May, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-05-19,270,6bj).


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





 





 
















 






