


Time to Upgrade your CLI!






































We've released version [1.3.0](https://github.com/TryGhost/Ghost-CLI/releases/tag/1.3.0?ref=ghost.org) of Ghost-CLI — with some very important updates...

##### Please [upgrade](#howtoupgrade) as soon as you can!

Highlights
----------

* **[New]** SSL renewal fix & migration
* **[New]** Added Ghost compatibility check
* **[Improved]** CLI upgrade notifications
* **[Fixed]** Removed [knex-migrator](https://github.com/TryGhost/knex-migrator?ref=ghost.org) dependency

In Detail
---------

1.3.0 is an important release, for the following reasons:

* The SSL renewal issue will be automatically fixed when you run `ghost update` or if you run `ghost migrate`, see below for more info.
* Ghost-CLI now knows if it is out-of-date and prompts you to upgrade
* Removal of the [knex-migrator](https://github.com/TryGhost/knex-migrator?ref=ghost.org) dependency means less compatibility issues with nvm, sqlite, etc.

### SSL Renewal

A month ago we received a [report](https://github.com/TryGhost/Ghost-CLI/issues/495?ref=ghost.org) that SSL certificate renewal does complete successfully with <=1.1.3. Although the certificates were regenerated correctly, nginx was not restarted, meaning the new certificates were not picked up.

> If you're reading this and your blog is offline with the error `NET::ERR_CERT_DATE_INVALID`, run `sudo nginx -s reload` to fix the problem and then upgrade Ghost-CLI to ensure it doesn't happen before..

If your blog was created with the CLI <= 1.1.3 **please [upgrade](https://ghost.org/faq/upgrading-from-deprecated-ghost-cli/?ref=ghost.org) now to the latest version** and then run either `ghost migrate` or `ghost update`.

Our [CLI docs](https://ghost.org/docs/ghost-cli/?ref=ghost.org) have been updated. If you run into problems, please swing by our [community forum](https://forum.ghost.org/?ref=ghost.org) or raise a bug issue [here](https://github.com/TryGhost/Ghost-CLI/issues?ref=ghost.org).

### Removal of knex-migrator

If you used Ghost-CLI before and ran into difficulty managing node versions, using nvm, or with sqlite3 (even if you weren't using sqlite3), you should find that Ghost-CLI is now much easier to use.

How to Upgrade
--------------

For **npm** users, run:

`sudo npm i -g ghost-cli@latest`

Followed by

`ghost migrate`

For **yarn** users, run:

`sudo yarn global add ghost-cli@latest`

Followed by

`ghost migrate`

The full upgrade guide lives here: [https://ghost.org/faq/upgrading-from-deprecated-ghost-cli/](https://ghost.org/faq/upgrading-from-deprecated-ghost-cli/?ref=ghost.org)


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





 





 
















 






