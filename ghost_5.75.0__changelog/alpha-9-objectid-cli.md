


Alpha 9, ObjectIDs & CLI installs









































This week we merged some big changes into Ghost, which meant it took a little extra time to get the alpha ready. There will not be an alpha next week, but there will be a blog post. Any thoughts or questions? Let us know in the comments 📢

### What's occurring?

As of this week, we're briefly switching the team's focus from the Ghost v1.0 alpha, to the internal tools that will support it. For the next 3-5 weeks, you'll notice less activity on the public repositories - the calm before the storm ☀️. We'll use this period to explain some of the changes we've made so far and how we're making Ghost better.

Heads up (again): there will be an v0.11 LTS release very soon! Therefore, if you'd like to get a bug fix into Ghost please submit it to the [lts](https://github.com/TryGhost/Ghost/tree/lts?ref=ghost.org) branch ASAP ⏳

This week
---------

##### Ghost CLI nearing feature completion

In the last week or so there have been some major updates to our new CLI tool [Ghost-CLI](https://github.com/TryGhost/Ghost-CLI?ref=ghost.org). These updates surround the recommended stack for production installs, with support for MySQL by default, systemd as the process manager and more handy messaging to guide the install process.

Ghost-CLI will be the recommended way to install Ghost once we reach v1.0. The CLI will have two major install-modes: `ghost install local` for quickly setting up a development or test install on your local machine and `ghost install` for installing and setting up Ghost on a production machine ready for prime time.

The recommended system stack for production installs will have the best chance of running Ghost successfully, and will be the stack which receives the most support from Ghost itself. It looks like this:

* Ubuntu 16.04 LTS (xenial) as the operating system
* Systemd (to manage the Ghost process)
* MySQL as the database engine
* Nginx as the webserver
* SSL (will be built into a future update)

The aim of `ghost install` is to get your entire system setup ready to run Ghost in production. With process management, a database, logging, SSL and so on. Using flags and plugin process managers, it will be possible to use Ghost CLI to install Ghost in a different way, but the recommended setup will always be a single simple command away.

##### ObjectId instead of auto increment

Until now, Ghost has used a combination of an auto increment `id` field and a `uuid` field using [RFC4122 v4 UUID](https://www.npmjs.com/package/uuid?ref=ghost.org#uuidv4options--buffer--offset) to identify all resources in our database. This week we replaced this with a single `id` field containing a globally unique identifier generated using [ObjectId](https://docs.mongodb.com/v3.2/reference/method/ObjectId/?ref=ghost.org). ObjectID comes from MongoDB and provides a globally unique identifier which is also sequential.

This means that each resource in Ghost will now have a single 24-character string identifier that is not only unique across a single Ghost install, but across all Ghost installs. This provides many benefits, including making it easier to replicate databases, providing us some interesting options for handling import/exports and much more. You can read more about the technical reasons for this change [here](https://github.com/TryGhost/Ghost/issues/7494?ref=ghost.org).

##### Further Ghost Editor improvements

This week has been on of consolidation for the editor project. We started on a code refactoring / cleanup process, began the process to make it more “ghost like”, completed the functionality of the “/" menu, and released a few small bug fixes around markdown and card handling. Nothing revolutionary but all part of our steady march onto 1.0! 🎖

##### Breaking change for storage adapters

We have added a new required method to the storage layer. It's a `read` method. The `read` method returns the bytes of a requested image path. If you would like to test alpha 9 and you are using a custom storage adapter, please note that you have to contact the publisher of your storage adapter to request an update.

Releases
--------

* Ghost [1.0.0-alpha.9](https://github.com/TryGhost/Ghost/releases/tag/1.0.0-alpha.9?ref=ghost.org)
* Ghost-Admin [1.0.0-alpha.9](https://github.com/TryGhost/Ghost-Admin/releases/tag/1.0.0-alpha.9?ref=ghost.org)
* Ghost-CLI [1.0.0-alpha.8](https://github.com/TryGhost/Ghost-CLI/releases/tag/1.0.0-alpha.8?ref=ghost.org)
* Ghost-Editor [0.1.5](https://github.com/TryGhost/Ghost-Editor/releases/tag/0.1.5?ref=ghost.org)

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





 





 
















 






