


Public Dev Meeting April 21











































Last week, our Slack team was made available to the public, and it has been a great success! There are more people in the Slack channels now than there ever were in our IRC. This has definitely been a great win for the Ghost community. If you have not signed up for our Slack channel, John created a [blog post last week](https://ghost.org/changelog/ghost-slack/) with more details on why we switched, and how to access the channel.

Two more features were also announced on the blog. The first being [code injection](https://ghost.org/changelog/code-injection/) and the other being the [prev and next post helper](https://ghost.org/changelog/previous-next-post-links/). Both of these features were highly sought after and have received a great response from the community. Code injection is going to make it much easier for everyone to get code into their blog without having to make any edits to the theme. This can be used for something as simple as adding google analytics, or it can be used to add whole javascript libraries. Definitely a great addition to Ghost.

Most of the PR's over the last week were minor bug fixes:

* [#5143](https://github.com/TryGhost/Ghost/pull/5143?ref=ghost.org) - Fixes a problem where authors were unable to access their profiles in the Ghost admin
* [#5149](https://github.com/TryGhost/Ghost/pull/5149?ref=ghost.org) - Fixes an error being thrown from `{{ghost_head}}` on custom 404 pages
* [#5140](https://github.com/TryGhost/Ghost/pull/5140?ref=ghost.org) - Fixes the publish button not updating to say "post" or "page" depending on the context
* [#5159](https://github.com/TryGhost/Ghost/pull/5159?ref=ghost.org) - Fixes author.email property being incorrectly available in certain contexts
* Casper ([#159](https://github.com/TryGhost/Casper/pull/195?ref=ghost.org), [#157](https://github.com/TryGhost/Casper/pull/197?ref=ghost.org)) - Fixes a footer bug and icon font caching problems.

[Novaugust](https://github.com/novaugust?ref=ghost.org) has created a proof of concept PR in regards to creating post previews ([#5158](https://github.com/TryGhost/Ghost/pull/5158?ref=ghost.org)). This is available for anyone (including beginners) to pick up and continue on with. This is a good opportunity for someone to become familiar with the Ghost codebase and get a great feature in at the same time.

Lastly, escaping markdown has been a bit of problem for a long time. Hannah has been working to fix these problems once and for all. If you get a chance, take her PR for a spin and try to see if you can break it ([#5167](https://github.com/TryGhost/Ghost/pull/5167?ref=ghost.org)).

Full details:
-------------

The [full logs of the meeting](https://ghost.slack.com/archives/ghost/p1429633857001995?ref=ghost.org) can be found in our Slack logs.

What is this?
-------------

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on Ghost's [slack](https://forum.ghost.org/?ref=ghost.org). In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 28st April, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2015-04-28,270,6bj).


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





 





 
















 






