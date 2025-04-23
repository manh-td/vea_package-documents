


Public Dev Meeting 29th July







































![](https://ghost.org/changelog/content/images/2021/01/image-7.png)

For the past 3 weeks, despite impressive progress, we've hovered at the ~40 open issue mark in the Multi-User backlog This week we're at less than 30 issues, and looking good to half that in the next 24-48 hours. With this in mind, we are aiming to ship the first RC for 0.5 on Thursday.

The largest part of what is left is [cleaning up](https://github.com/TryGhost/Ghost/issues/3086?ref=ghost.org) bits of the UI so that less privileged users don't see controls and resources that they aren't able to interact with. The API has a full suite of permissions controlling who can do what, but the admin UI needs to be updated to reflect some of that. Determining the best approach for some of this was a large part of today's meeting.

There is also a large amount of testing, both in terms of writing tests to ensure coverage, and physically testing out the code that needs to happen before we can be sure the code is ready to release. If you have some free time, please do check out master and take it for a test run!

At present, we don't have any contributors who are championing an effort to bring postgres support into line with our SQLite and MySQL support. As a result of this postgres support is falling behind rather than catching up. Currently the [build fails](https://travis-ci.org/TryGhost/Ghost?ref=ghost.org), and it's quite likely that 0.5 won't work with postgres unless someone gives it some attention.

It usually takes 8-10 days to get from a first RC to a release, and we'll set a firm date for the release of MU in next week's meeting.

### Full details:

The full logs of the meeting are available from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 5th August, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-8-5,270,6bj).

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





 





 
















 






