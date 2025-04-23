


Moving to Node.js v4 LTS






































As of this week, we've updated our recommended version of Node.js for Ghost to be **Node.js v4 LTS**.

We're doing this a little later than planned. However, after much testing we are now confident that Ghost on v4 runs smoothly and with a smaller initial memory footprint than it did previously. Every single blog on [Ghost(Pro)](https://ghost.org/pricing/?ref=ghost.org) now runs on Node.js v4 LTS and we had zero problems upgrading everyone 😅 🎉

### Why upgrade?

Having upgraded everyone on Ghost(Pro) blogs, we've found that the base memory footprint for a Ghost blog is now under 100mb ⚡️ (NB: Your mileage may vary based on theme, content, traffic, and environment)

The [Node.js LTS schedule](https://github.com/nodejs/LTS?ref=ghost.org) means the 0.10.x line will reach end of life on 1st October 2016. Ghost will be following this schedule, meaning the next upgrade released on or after October 1st will no longer support being run on 0.10.x. Support for Node.js 0.12.x will end in a similar fashion on the 31st December 2016.

If you self-host Ghost, you should plan to upgrade in the next 3 months. We recommend upgrading Node.js independently of upgrading Ghost to make any issues easier to debug.

### How to upgrade

Upgrading your Ghost install from an older version of Node.js to v4 is a 4 step process:

1. Backup!
2. Upgrade the Node.js version on your server
3. Run `npm install --production` inside the Ghost directory to ensure that the binary dependencies are recompiled for Node.js v4 LTS
4. Restart Ghost

If you're using a Digital Ocean droplet, you can learn how to upgrade Node.js on a one-click install of Ghost from this [excellent Q & A post](https://www.digitalocean.com/community/questions/how-to-upgrade-node-js-on-older-ghost-droplets?ref=ghost.org).

### More details

If you really want the meat and potatoes:

* Node.js [Official LTS Schedule](https://github.com/nodejs/LTS?ref=ghost.org)
* Ghost's [Supported Node Versions](https://ghost.org/docs/faq/node-versions/?ref=ghost.org)
* Details of the switch [on GitHub](https://github.com/TryGhost/Ghost/issues/7098?ref=ghost.org)


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





 





 
















 






