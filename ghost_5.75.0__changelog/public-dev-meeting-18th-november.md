


Public Dev Meeting 18th November







































![](https://ghost.org/changelog/content/images/2021/01/image-17.png)

Today's meeting was largely interrupted by issues with the release of Ghost 0.5.4. Unfortunately I wasn't able to give it my full attention, but here's a quick overview of what we discussed:

### Releasing Ghost 0.5.4 and 0.5.5

This week there was a big push to clean up more bugs and issues and release Ghost 0.5.4 as we wanted to get the memory leak fix out in the wild. Ghost 0.5.4 was released yesterday (18th Nov), but we quickly discovered there was a charset issue affecting MySQL blogs. As a result we took Ghost 0.5.4 down temporarily whilst we located the problem.

Further investigation has turned up a serious configuration issue between [knex](https://knexjs.org/?ref=ghost.org), the library we use to create SQL queries, and the `node-mysql` mysql driver module. To resolve this short term we have reverted `node-mysql` back to an earlier version and released Ghost 0.5.5. Long term we will need a more in-depth fix and there will be further details of this in due course.

### Focus for 0.6

During the meeting I shared the 'Road to 0.6' write-up that is going to be published here on the blog shortly. This was digested and discussed by those present, and it was agreed that this helps  to provide more focus and clarity around priority features that we want to ship to our users. We also believe our users will be happy to hear that so many big features, like post scheduling, are priority issues and will be shipping in the near future.

Full details:
-------------

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20141118?ref=ghost.org#pm54842) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 25th November, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-11-25,270,6bj).

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





 





 
















 






