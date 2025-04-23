


Database Migrations







































As we add new functions and features to Ghost, there's always the chance we need to add to or modify the database schema. This needs to be done in such a way that it doesn't impact our users... each change needs to be applied to every single user's database without effort or requiring any complex upgrade steps. Our database migration system is how we manage this process.

How migrations work
-------------------

From a user's perspective, database migrations are automatic. The database gets modified with any necessary changes whenever Ghost is upgraded to a new version - so when a blog owner copies over a new set of files, the database upgrade automatically happens when you restart. It is very very quick and you probably won't even notice it happening.

What is happening in the code, is on startup Ghost checks to see what version of the database it should be running - this is controlled by the `databaseVersion` value in `core/server/data/default-settings.json`. It then looks to see what version the database says it is running by requesting `databaseVersion` from the settings table. If there is no database at all yet, Ghost creates one from the latest schema, and if the settings table version is older than the code base version, Ghost knows it needs to upgrade.

Once Ghost knows it needs to do an upgrade, it then goes off to figure out what needs to change. It does this by checking for differences between the actual database structure, and the schema defined in `core/server/data/schema.js`. If something is missing, Ghost adds it in... if there is something extra, Ghost removes it\*.

All of this is pretty fancy, thanks to [@sebgie](https://github.com/sebgie?ref=ghost.org).

Working on Ghost core
---------------------

If you are working on Ghost core, there are a couple of migration-related issues you might run into.

If you are switching between branches, for example between latest master and a slightly out of date feature branch, you may find yourself getting the following error message:

![Error: Your database is not compatible with this version of Ghost](https://i.imgur.com/G9meoiJ.png)

This is because whilst on master, your database got upgraded. When you switched back to an earlier version of the codebase, Ghost's start up checks determine that the database is newer than the code base and throws an error. We don't automatically downgrade because this could result in accidental data loss.

The easiest way to fix this error is to delete your database, and let Ghost create you a fresh one with the right version. In some circumstances, changing the version number in your settings table to match the codebase may work. We will be introducing a command line tool in future for working with migrations to make all this a bit easier.

Another consideration to make when working on Ghost core, is that you cannot and should not add or remove things from the database without careful consideration. If you determine that your feature can only be implemented with a schema change, then you should make your change to `schema.js`, and bump the databaseVersion number in `default-settings.json` at the same time. Please clearly mark any pull requests which require migrations.

\* *Note: at the time of writing, automatic database migrations only work for adding and removing entire tables. Adding and removing columns is coming soon, and making modifications to columns themselves will come later.*

**Update: 7th Jan 2016:** This article is now quite out of date. Since writing, we've added an environment variable that will force the migrations to re-run `FORCE_MIGRATION=true npm start` will get you out of a bind if you've got half a migration on your local copy.


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





 





 
















 






