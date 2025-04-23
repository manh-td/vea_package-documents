


Dropping Support for PostgreSQL







































Adding a [long-term support strategy](https://ghost.org/changelog/lts) for Ghost v0.11, and focusing on an all new, backwards-incompatible Ghost v1.0 has given us an exciting opportunity to fix some our biggest development pain points.

PostgreSQL support was added organically by several contributors who showed up in the early days, raised bugs, fixed bugs, got a build added to travis, and did QA to ensure that Postgres worked. At a certain point, it seemed natural to say we supported it.

Since then, it has become one of our biggest difficulties when developing new features, second only to our permissions system.

There was a comment in the early thread [advocating support](https://github.com/TryGhost/Ghost/issues/1333?ref=ghost.org#issuecomment-27621908) about how having "official support" earlier would prevent Postgres being a second-class citizen. The logic was sound, but in practice this hasn't been true.

The Ghost team use Sqlite3 for development, and Ghost(Pro) uses MySQL - meaning we're running tens of thousands of blogs on MySQL all day every day. Bugs and opportunities for improvement in those two databases are found and handled quickly. We are able to **guarantee** first-class support for MySQL in a way we have never been able to for Postgres.

Over time we've reached a point where we no longer have any active core team members or regular contributors that use Postgres in production. No one using Postgres is contributing to code or to QA. We miss things because we aren't using it. Bugs get raised by the community, but they don't get fixed.

Postgres is a particular challenge because it is quite different to MySQL and SQLite. Code that automatically works for MySQL & SQLite often needs special modifications for Postgres, meaning it is time consuming and hard to maintain. Knex's abstractions just aren't doing the job well enough.

Without active community support, Postgres has always been, and always will be a second-class citizen. For that reason, we are dropping official Postgres support from Ghost core.

Moving forward
--------------

From Ghost 1.0 we're going to be officially throwing our weight behind MySQL. Although SQLite will still be available for development (and particularly useful for developing themes and apps), we'll be recommending MySQL for production Ghost installs. We'll be actively optimising, improving and tweaking bits of the data model to make sure that MySQL works as well as it possibly can.

By narrowing our focus on just one database, we'll be able to provide a much better, more optimised and efficient Ghost ⚡️.

We're also streamlining our development efforts, so we can spend our time on building the tools our users need to build awesome online publications. Supporting lots of databases was a nice idea in principle, however in practice being a jack of all databases makes us a master of none.

None of this precludes us from ever supporting Postgres again in future, if demand and contributions warrant it. For now, we believe this is what's best for the project.


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





 





 
















 






