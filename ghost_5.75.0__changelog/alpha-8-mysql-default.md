


Ghost Alpha 8 with MySQL as the default









































Welcome to this weeks update! Apologies for the tardiness this week, good news is we now have a tool for collecting information from across our repositories, so we should be on time (Wednesday) next week. This is very much a work in progress idea, so please let us know what you think in the comments 📢

### What's occurring?

We're still working away on our [Ghost v1.0 alpha](https://ghost.org/changelog/tag/alpha/) and the related projects. It's been a slightly quieter week as much of our effort has been on getting the new Ghost Auth service polished up.

Heads up: there will be an v0.11 LTS release within the next 2 weeks! Therefore, if you'd like to get a bug fix into Ghost please submit it to the [lts](https://github.com/TryGhost/Ghost/tree/lts?ref=ghost.org) branch ASAP ⏳

This week
---------

#### We made MySQL a default dependency, and made SQLite3 optional

Here at Ghost HQ we ♥️ SQLite3. For most one-user blogs, it's really all you need. However, although it removes the need for database credentials, the binary dependency has always made Ghost's install process a little troublesome. With Ghost v1.0 we intend to make the install process much, much easier.

As of Ghost v1.0, we'll be making MySQL the (overridable) default for production installs AND introducing [Ghost-CLI](https://github.com/TryGhost/Ghost-CLI?ref=ghost.org) as the One True Way™ to install Ghost.

The CLI tool will offer `ghost install` as a wrapper around `npm install`, doing its best to make the install process go smoothly, and providing smart error messages if things go really wrong. To aid in all this we've moved `sqlite3` to be an optional dependency and made `mysql` a normal, required dependency. This means that `npm install` will not fail if installing SQLite3 fails.

With the CLI you'll be able to run `ghost install local` to get a quick, SQLite3-based install for playing around on your local machine (handy for developing themes). The intention is that Ghost-CLI will first of all help to ensure that your environment is correct for installing Ghost with SQLite3 and in the worst case handle SQLite3 install failures by prompting with a fallback to MySQL.

We'll be writing more about the CLI tool over the coming weeks.

#### We replaced our brute force protection logic

Ghost's spam prevention middleware has needed an upgrade for a little while. This week we removed our custom code in favour of [express-brute](https://github.com/AdamPflug/express-brute?ref=ghost.org). This gives us more options for controlling how accounts are locked so it is now based on the much more desirable IP + email address combination, instead of the old email-address only.

This also moves account locking logic and state out of the user model. Recently, we also moved the concept of a user invite to be their own model instead of a state in the user model. With these two big changes, the concept of user state has been significantly simplified 🎉

#### Upgrades to the new GhostAuth service

We're working away behind the scenes to get the GhostAuth service ready to go. Ghost & passport-ghost both got several updates this week to handle changes in that service. If you're testing out the alpha, we're continuing to reset the GhostAuth service database regularly and therefore you will need to create a fresh database. This can be done by running `knex migrator reset && knex migratior init`.

#### Improvements to the new Ghost editor

We're still iterating hard on the [new mobiledoc editor](https://github.com/TryGhost/Ghost-Editor?ref=ghost.org). This week's update included the removal of markdown within Ghost [#379](https://github.com/TryGhost/Ghost-Admin/pull/379?ref=ghost.org).

Releases
--------

* Ghost [1.0.0-alpha.8](https://github.com/TryGhost/Ghost/releases/tag/1.0.0-alpha.8?ref=ghost.org)
* Knex-migrator [0.2.0](https://github.com/TryGhost/knex-migrator/releases/tag/0.2.0?ref=ghost.org)
* passport-ghost [1.3.0](https://github.com/TryGhost/passport-ghost/releases/tag/1.3.0?ref=ghost.org)
* Ignition [2.0.0](https://github.com/TryGhost/Ignition/releases/tag/2.0.0?ref=ghost.org)

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





 





 
















 






