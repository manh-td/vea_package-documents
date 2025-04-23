


Public Dev Meeting October 13th











































This week we held our public development meeting as a Google hangout on air, for the first time. If you'd like to watch it back, you can do so [on youtube](https://youtu.be/fMmbvGTV_mc?ref=ghost.org).

### Wait, why a hangout?

We're moving towards working on small, two-week blocks of work, or sprints, where the focus is narrow and well understood. The plan is to have a 'hangout' meeting at the start of each two-week block to determine what we intend to work on. Every other week we will have a text-based progress meeting in the #dev channel on Slack, as per usual. Both meetings are open for anyone to join, and will be summarised here on the dev blog.

Meeting Summary
---------------

The focus for the next two weeks is on shipping a first version of read-only public API access. There is significant concern about how to manage versioning and breaking changes in the API, especially around features that may not quite be ready at the end of the two weeks, for example counts like asking 'How many posts does this tag have?'.

Some reference material was suggested around API versioning: [Stripe (slides)](https://speakerdeck.com/amfeng/move-fast-dont-break-your-api?ref=ghost.org), [Stripe (video)](https://www.heavybit.com/library/video/2014-09-30-amber-feng?ref=ghost.org) and [Clearbit (article)](https://blog.clearbit.com/versioning-apis?ref=ghost.org).

To mitigate this in the very short time, our plan is to focus on some key use cases, and ship what we have at the end of the sprint behind a labs flag, so as to communicate that this version is very, very 'beta'. An example use case is: fetching 5 posts which have the same tags as the current post. At the end of this sprint, it should be possible to perform this query inside a theme via the get helper, or via ajax.

The key issues needed to wrap up public API access were, at the start of the meeting, outlined in the 'Public API' section of [issue #5503](https://github.com/TryGhost/Ghost/issues/5503?ref=ghost.org) and are now all located in the Public API v1 milestone. This includes a few issues we identified needed to be written during the meeting. The issues that we are confident we can complete have been assigned, the remainder include things we'd like to pick up if the other work is completed.

If you're a developer looking for ways to contribute to Ghost, please check out our fix wanted label on GitHub.

### Full details

If you'd like more details of what happened during the meeting, you can [watch it in full on youtube](https://youtu.be/fMmbvGTV_mc?ref=ghost.org).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #dev channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 20th October, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-10-20,270,6bj).


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





 





 
















 






