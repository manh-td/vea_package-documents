


Ghost Desktop 1.0 & Alpha 7













































Welcome! This week for the first time, we are updating our community with a more detailed blog post instead of a meeting. This is very much a work in progress idea, so please let us know what you think in the comments 📢

### What's occurring?

If you haven't already heard, the Ghost Team are currently focusing our development efforts on an alpha development stream, which will eventually turn into Ghost v1.0. If you're interested to know more, we've got a [v1.0 alpha support guide](https://ghost.org/changelog/tag/alpha/) that we use to share important details of how to test and get involved.

This week
---------

**Ghost Desktop v1.0.0 was released**

The **Ghost Desktop App** reached v1.0 this week 🎉. Grab yourself a Mac, Windows or Linux build from [our website](https://ghost.org/?ref=ghost.org).

**We split Ghost & Ghost-Admin a little further**

We're slowly working on separating our two main repositories to make Ghost & Ghost-Admin more independent of each other. This week we moved to fetching configuration from an endpoint, instead of outputting it in the HTML file that boots Ember [#368](https://github.com/TryGhost/Ghost-Admin/pull/368?ref=ghost.org), [#7631](https://github.com/TryGhost/Ghost/pull/7631?ref=ghost.org).

**Updates to the new Ghost editor**

One of the most exciting features of Ghost v1.0 is the brand new mobiledoc editor. It lives over in [Ghost-Editor](https://github.com/TryGhost/Ghost-Editor?ref=ghost.org). This week's update included soft returns & code block support [#373](https://github.com/TryGhost/Ghost-Admin/pull/373?ref=ghost.org), [#7649](https://github.com/TryGhost/Ghost/pull/7649?ref=ghost.org).

**Knex Migrator got a little more stable**

[Knex-migrator](https://github.com/TryGhost/knex-migrator?ref=ghost.org) is our database migration tool. Over the last 3 years we've gained experience of initialising our database and running migrations in distributed software. This knowledge is now bundled in a public npm module, which everybody can use.

You can [read here](https://github.com/TryGhost/Ghost/issues/7489?ref=ghost.org#issuecomment-251698188) why we opted not to use knex's built-in migration system. This week, knex-migrator reached feature-completion, full details in the [readme](https://github.com/TryGhost/knex-migrator?ref=ghost.org#cli-usage). You'll need it globally installed if you want to contribute to Ghost 👻

**We also released Ghost [0.11.3](https://ghost.org/changelog/ghost-0-11-3) (LTS release)**

Over the last 2 weeks, Node.js has moved v6.9 into LTS and ended the maintenance period for Node.js v0.10. Ghost's ["lts" branch](https://github.com/TryGhost/Ghost/tree/lts?ref=ghost.org) has been updated inline with our [Node version support strategy](https://ghost.org/docs/faq/node-versions/?ref=ghost.org). Our latest LTS release also includes some minor bug fixes to scheduling and to Casper.

Releases
--------

* Ghost Desktop 1.0.0 🚀
* Ghost [0.11.3 LTS](https://github.com/TryGhost/Ghost/releases/tag/0.11.3?ref=ghost.org)
* Casper [1.3.4](https://github.com/TryGhost/Casper/releases/tag/1.3.4?ref=ghost.org)
* Ghost [1.0.0-alpha.7](https://github.com/TryGhost/Ghost/releases/tag/1.0.0-alpha.7?ref=ghost.org)
* Ghost CLI [1.0.0-alpha.6](https://github.com/TryGhost/Ghost-CLI/releases/tag/1.0.0-alpha.6?ref=ghost.org)
* Knex-migrator [0.1.2](https://github.com/TryGhost/knex-migrator/releases/tag/0.1.2?ref=ghost.org)

Follow us!
----------

Want to find out more about Ghost development? Subscribe to the [updates feed](https://ghost.org/changelog/tag/updates/rss) for to the [alpha feed](https://ghost.org/changelog/tag/alpha/rss) if you're more interested in how v1.0 is progressing. Alternatively, follow us on [twitter](https://twitter.com/TryGhost_dev?ref=ghost.org) 🐦 or sign up to get our weekly newsletter in your inbox 📬.


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





 





 
















 






