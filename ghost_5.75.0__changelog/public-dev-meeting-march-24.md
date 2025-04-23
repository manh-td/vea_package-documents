


Public Dev Meeting March 24th











































A little over a week ago, the [ember-cli](https://github.com/TryGhost/Ghost/pull/4853?ref=ghost.org) switch and the [removal of codemirror](https://github.com/TryGhost/Ghost/pull/5031?ref=ghost.org) were merged into master. There were a lot of changes and many files touched in that merge, so this is great news! The removal of codemirror not only closed a number of small bug issues with the Ghost editor, but it also introduced a feature that has been asked for for quite a long time (and rightfully so), spellcheck!

Spellcheck is not currently part of the latest release, but it has been merged into master. This definitely needs be tested, so feel free to grab the latest master, take it for a spin, and open any issues you see with it.

There is currently an [open issue](https://github.com/TryGhost/Ghost/issues/5060?ref=ghost.org) about updates to the `{{excerpt}}` helper. This will allow for excerpts to be chosen by paragraph rather than relying on words or characters. This will also keep all text styling instead of smashing all the content into one paragraph. The excerpt helper will provide much greater control on how much, and what kind of content is shown on the home page. Definitely a big improvement on what is currently available, so if you're interested in helping us build this, let us know!

The ability to [define where images are stored](https://github.com/TryGhost/Ghost/issues/4600?ref=ghost.org) was also merged in this week. This is a huge win for those who host Ghost on services like Heroku, because, now images can be stored on services like Amazon S3 while Ghost itself runs on Heroku. Documentation on how to do this will be made available with the next release.

The [showdown extensions were removed](https://github.com/TryGhost/Ghost/pull/5048?ref=ghost.org) from Ghost and now live in Hannah's fork. This removed some code duplication and allows Ghost to use it as a dependency rather than native code. This also allows other people to use this module outside of Ghost, which in turn, may bring in more contributors and help keep it maintained.

[Frontend route customization](https://github.com/TryGhost/Ghost/issues/4519?ref=ghost.org) is also a large refactor that has been merged in. This will eventually allow for current routes like `/tag/` to be customized. This is needed for Ghost to be multi-language, but also a good feature for if someone wants to use `/category/` instead of `/tag/` or something similar.

The [previous/next post](https://github.com/TryGhost/Ghost/issues/4799?ref=ghost.org) and [query](https://github.com/TryGhost/Ghost/issues/4439?ref=ghost.org) helpers are currently being worked on and are much closer to being finalized. The previous/next post helpers will allow you to link to the next post in chronological order from a post page. The query helper, is going to allow you to query certain tags, posts, pages, and many other attributes making your ability to customize what posts or data that is shown much greater than what it is now.

As always, if you have any new ideas, or features you would like to see added to Ghost, check out our [wishlist page](https://forum.ghost.org/?ref=ghost.org) and either vote or create a new item.

Thanks for another awesome meeting! We are very excited about the current progress and the future of Ghost. :)

Full details:
-------------

The [full logs of the meeting](https://botbot.me/freenode/ghost/msg/34931481/?ref=ghost.org) in our IRC logs, which are looked after by the lovely folks at [botbot.me](https://botbot.me/freenode/ghost?ref=ghost.org).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 31st March, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-03-31,270,6bj).


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





 





 
















 






