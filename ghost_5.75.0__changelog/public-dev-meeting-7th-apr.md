


Public Dev Meeting 7th Apr











































We begin with big news from team Ghost this week. As we announced on the [main blog](https://ghost.org/changelog/), we've launched a new [public revenue dashboard](https://ghost.org/about/?ref=ghost.org#metrics) as part of our big push towards being more transparent. Read the [April update post](https://ghost.org/changelog/april-2015-update/) for more details.

This week in Ghost land, we've seen a few interesting PRs land in master. Code injection got syntax highlighting & line numbers ([#5016](https://github.com/TryGhost/Ghost/pull/5106?ref=ghost.org)), and is now awaiting a last pass over the UI before having it's labs training wheels removed.

Ember was updated to 1.11.1 ([#5094](https://github.com/TryGhost/Ghost/pull/5094?ref=ghost.org)), which means we no longer need `{{bind-attr}}`, making the code significantly neater. There are a couple of gotchas to be aware of, which [novaugust](https://github.com/novaugust?ref=ghost.org) explained:

* the first is that `style` and `script` contexts are vulnerable to xss via `{{}}` - ember *does not* know how to escape in those contexts (unlike with html), so we need to take extra care here for a little while
* the second thing was whether you should wrap an attribute in quotes or not, ie `foo={{bar}}` vs `foo="{{bar}}"`. Essentially, wrapping in quotes forces `toString()`, whereas bar puts the raw type in, which is useful in html5 for things like `data-count=5` `disabled=false`.

More info about the changes in Ember 1.11 can be found on the [Ember blog](https://emberjs.com/blog/2015/03/27/ember-1-11-0-released.html?ref=ghost.org).

There have also been a number of PRs raised/merged, which fix bugs with and improve the output from our RSS feeds. This includes moving the full content to the proper `<content:encoded>` element, using `<description>` properly, using the `<media:content>` for cover images, changing the mime type, fixing some issues with bad URLs, and soon we hope to also be changing the RSS feeds so they aren't generated on every request, meaning ETAGs will work properly. Hopefully these changes will help to make our RSS feeds more useful.

During this week's meeting there was some discussion around the [Ghost-Vagrant](https://github.com/TryGhost/Ghost-Vagrant?ref=ghost.org) setup. This has been somewhat unloved for a time, and needs a little work. There is a renewed push from our community to improve it, which should help more people get involved developing for and with Ghost.

The next release of Ghost is scheduled to happen before the next meeting, and will be Ghost 0.6.0!

### A note on contributing

One of the best, and easiest ways to get involved contributing to Ghost, is to help us get PRs merged. If you have a few minutes spare, check out a pull request, take it for a spin and let us know what you found. Did it work OK or was there a problem?

Not only does this help us to merge changes faster, and keep Ghost moving forward, but tracking changes & how they affect Ghost is a fantastic way to get to know pieces of the codebase.

Check out [this little guide](https://ghost.org/docs/tutorials/test-pull-request/?ref=ghost.org) on how to setup your environment so that checking out a pull request is as easy as `pr 1234`, and then try one out!

Full details:
-------------

The [full logs of the meeting](https://botbot.me/freenode/ghost/msg/36043125/?ref=ghost.org) in our IRC logs, which are looked after by the lovely folks at [botbot.me](https://botbot.me/freenode/ghost?ref=ghost.org).

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 14th April, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-04-14,270,6bj).


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





 





 
















 






