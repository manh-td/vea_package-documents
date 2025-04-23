


Public Dev Meeting May 19th











































Since our last meeting, [Ghost 0.6.3](https://ghost.org/changelog/ghost-0-6-3/) was released! With this release comes two great new features, blog password protection and post previews. Post previews are definitely a nice feature to have and a very welcome addition to Ghost. Here is the full [change log](https://gist.github.com/ErisDS/934f74b8d7f0bf75217b?ref=ghost.org) for anyone interested in knowing exactly what has changed from 0.6.2 to 0.6.3 :).

There has been a little bit of a caching problem with the latest release and the password protection that some people may have experienced. Some maintenance fixes are being put into place that should fix the problem shortly.

There were a lot of little PR's this week to get everything ready for the release, but there were also a couple of others worth mentioning. As part of a larger [front-end refactor](https://github.com/TryGhost/Ghost/issues/5286?ref=ghost.org), a PR was merged to pull away each middleware function into its own file ([#5287](https://github.com/TryGhost/Ghost/pull/5287?ref=ghost.org)). All of the other functions need to be pulled out of the `middleware.js` file and moved into their own functions as well. If you are a beginner looking to get one of your first PR's merged into Ghost, this is a great place to start. Just take a look at the example PR above that has already been done and take a crack at one of the other functions :).

For anyone who develops on Ghost, some changes were made so that `grunt clean` will now wipe out all the `node_modules` and `bower_components`. This will help if your `grunt dev` breaks for any reason.

One other PR that we wanted to mention was an optimization to the password protection url ([#5278](https://github.com/TryGhost/Ghost/pull/5278?ref=ghost.org)). This PR just removed some of the bloat from the url to make it a cleaner and nicer experience.

One large change coming down the pipeline is a new admin interface, nicknamed Zelda ([#5273](https://github.com/TryGhost/Ghost/pull/5273?ref=ghost.org)). This new admin will allow Ghost to continue to grow and evolve without having to figure out where to place new features into the existing framework. There will be more details on this in the coming weeks, but feel free to checkout that PR and take it for a spin :).

![](https://ghost.org/changelog/content/images/2021/01/slack-imgs-com-1.png)

Thanks for hanging out, see you next week :D.

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1432053029001534?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 26th May, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-05-26,270,6bj).

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





 





 
















 






