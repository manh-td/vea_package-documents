


Public Dev Meeting 1st Apr







































The past week has been pretty quiet, with the small exception of the release of 0.4.2 of course!

As always, I am incredibly grateful to every single person who contributed:

> Fabian Becker, John O'Nolan, Harry Wolff, Sebastian Gierlinger, Gabor Javorszky, Jacob Gable, Johan Stenehall, Kyle Nunery, mattse, Brad Dougherty, Jakob Gillich, Jonathan Johnson, Michael Bradshaw, Paul Adam Davis, Sam Saccone, Shashank Mehta, Aia Patag, Andy, Clinton Ryan, Dan Schnau, Dane Springmeyer, Daniel Niccoli, Declan Cook, Garrett Murphey, Jason Williams, John-David Dalton, Kenny Meyer, Lucas Churchill, Manuel Mitasch, Mark Stacey, Rob Graeber, Sean Hellwig, Xie JinBin, Zach Geis, balduv, cobbspur, nicksahler, polygonix, redwallhp

Releases are always time consuming, and putting our code in front of so many people inevitably turns up the odd issue or two. With the release of 0.4.2 we have encountered a problem with some themes which were not setup to correctly handle tag linking. This was not considered as a potentially breaking change by us, and so we spent some time discussing how we should manage this in future.

With Ghost being pre 1.0 and pretty fast-moving, there is a certain amount of expectation that things will break. However, we do believe we can improve the visibility and communication around potential breakage by allowing themes to determine which version of Ghost it should work with. This way we can do all sorts of interesting things around upgrading and informing users.

This week, we have 3 core points of focus:

* Tests - get these passing reliably again
* Ember.js - get both notifications and modals in place
* The API - get the issues for this sorted out

We're hoping to churn out some more issues tagged [beginner](https://github.com/TryGhost/Ghost/issues?direction=desc&labels=beginner&milestone=&page=1&sort=updated&state=open&ref=ghost.org) over the next week to try to help more people get involved.

Also this week I added a new branch to Ghost's GitHub. The [stable](https://github.com/TryGhost/Ghost/tree/stable?ref=ghost.org) branch is intended to contain the latest release of Ghost for anyone installing or buidling packages from git, so that it is easier to keep up to date. I'm interested to hear from anyone who might use this as to whether it would be useful to commit the built assets on this branch?

Don't forget that there is now a podcast about Ghost. Check out recent episodes of [Ghostalk](https://talk.ghost.io/?ref=ghost.org) for some particularly interesting insights from [Kezz Bracey](https://talk.ghost.io/4/?ref=ghost.org) of [Polygonix](https://www.polygonix.com/?ref=ghost.org) themes, Andy Boutte and David Balderston from [allaboutghost.com](https://allaboutghost.com/?ref=ghost.org) and this week [Julian Lam](https://talk.ghost.io/6/?ref=ghost.org) of [NodeBB](https://nodebb.org/?ref=ghost.org) :)

### Full details:

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20140401?ref=ghost.org#pm44023) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode (note that the UK has just moved onto Daylight Savings Time, so the meeting is an hour earlier than it was previously). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: Tuesday 8th April, 5:30pm London time.


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





 





 
















 






