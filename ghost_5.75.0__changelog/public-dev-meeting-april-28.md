


Public Dev Meeting April 28











































Yesterday's meeting had really great attendance. I'm really enjoying having the meetings in slack with a broader section of our community joining in. Please come hang out in our [slack](https://forum.ghost.org/?ref=ghost.org) channel on Tuesdays around 5:30pm UK time, the more the merrier!

This week saw 2 releases of Ghost land just 5 hours apart. 0.6.1 was a bug clean up release for 0.6.0, and 0.6.2 fixed a major issue where the new previous and next posts links did a disappearing act in what was a truly beautiful bug. Big thanks to the people who reported the issue so quickly and enabled us to get it fixed in a timely fashion. We did also squeeze a few other small bits into 0.6.2, but nothing that should affect the majority of people.

Since 0.6.2 we've gotten a few other things merged into master as well:

* When an active theme has gone missing, the users will now be able to select a correct theme instead of Ghost being broken ([#5191](https://github.com/TryGhost/Ghost/issues/5191?ref=ghost.org)) (was a regression that was fixed)
* When accessing rss through ssl, send all assets like images over https as well ([#5189](https://github.com/TryGhost/Ghost/issues/5189?ref=ghost.org)) (regression as well)
* a small change for people who are playing with the very very limited app capabilities ([#5184](https://github.com/TryGhost/Ghost/issues/5184?ref=ghost.org))
* A few test optimisation PR's were merged in ([#5182](https://github.com/TryGhost/Ghost/issues/5182?ref=ghost.org), [#5176](https://github.com/TryGhost/Ghost/issues/5176?ref=ghost.org), [#5161](https://github.com/TryGhost/Ghost/issues/5161?ref=ghost.org))

The test improvements allow you to run `grunt test-all` to run just the tests without linting, as linting can be quite slow. Also `grunt coverage` now generates a lovely coverage report in `core/test/coverage` that we can use to improve test coverage in a couple of key areas, namely middleware, url generation, and the frontend controllers when they get [refactored](https://github.com/TryGhost/Ghost/issues/5192?ref=ghost.org).

Also this week, [@novaugust](https://github.com/novaugust?ref=ghost.org) and I met up and hacked on the preview feature. We've got a [PR](https://github.com/TryGhost/Ghost/pull/5158?ref=ghost.org) that's almost ready to merge with the exception of needing a few tests. [@acburdine](https://github.com/acburdine?ref=ghost.org) has also completed his work on [password protected blogs](https://github.com/TryGhost/Ghost/pull/5103?ref=ghost.org) and so it's looking like 0.6.3 will land within the next 2 weeks with at least one, if not both of these features.

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1430238659003433?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 5th May, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-05-05,270,6bj).


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





 





 
















 






