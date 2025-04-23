


Ghost 0.11.1







































[Ghost 0.11.1](https://github.com/TryGhost/Ghost/releases/tag/0.11.1?ref=ghost.org) is now available on GitHub, npm and Ghost.org. This is maintenance release that includes an important fix to the date migration logic - self-hosters please see the upgrade notes below. This will be the final release of Ghost that supports Node.js v0.10.

Highlights
----------

* **[Fixed]** Theme refreshes on activation && override, so that Ghost(Pro) users don't get stuck in a cache-based-purgatory ♻️
* **[Fixed]** Logic around date migrations, which caused some people with SQLite3 to not get migrated yet ⏱
* **[Fixed]** Error when trying to delete a user that has posts 📚
* **[Fixed]** Messaging around account locking 🔐
* **[Improved]** Initial database creation now happens in a transaction 🎉

You can see the [full change log](https://gist.github.com/ErisDS/801d188a3e488bc164ee74c7342bcc1f?ref=ghost.org) for the details of every change included in this release.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.11.1 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.11.1](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

**Special Upgrade Notes:**

If you're on Ghost 0.9.0-0.11.0 and you're using SQLite3, your dates may not have been migrated properly. This release contains a special fix to try to resolve this problem. Therefore, when you run this upgrade, you should use `npm start --production` to start Ghost the first time, wait for the migration to finish, save the output somewhere safe, and then start Ghost using your normal method.

Currently, the recommended upgrade path is:

* If you're on 0.4.2-0.7.0, upgrade to 0.7.1
* If you're on 0.7.1+, upgrade to 0.11.1

The upgrade to 0.11.1 can take time, especially if you have a lot of data. Your blog will run in migration mode whilst the migration is running.

Once the date migrations are working, there will be no further database changes in the LTS version of Ghost.

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Katharina Irrgang, Kevin Ansfield, John O'Nolan, Cezary Kluczyński and Austin Burdine.


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





 





 
















 






