


Ghost 0.11.4







































[Ghost 0.11.4](https://github.com/TryGhost/Ghost/releases/tag/0.11.4?ref=ghost.org) is now available on GitHub, npm and Ghost.org. The main contents are the removal of Node v0.12 support and the new redirects feature.

Highlights
----------

* **[New]** ✨ Define redirects as JSON file
* **[New]** ✨ Make AMP optional
* **[Removed]** ⬇️ Node v0.12.x support - Node v0.12 is no longer maintained
* **[Fixed]** Import subscribers on database import
* **[Fixed]** Fix admin redirect, when using a subdirectory
* **[Security]** Expand subscriber email validation
* **[Security]** Escape sameAs for structured data
* **[Security]** Detect symlinks when uploading themes via the admin panel
* many dependency updates

You can see the [full change log](https://gist.github.com/kirrg001/ea5b2628d24b0ede677aacbc84f04ba8?ref=ghost.org) for the details of all changes included in this release.

In Detail
---------

Ghost no longer supports Node.js v0.12. It's is no longer maintained as of 31st December 2016. We will continue to recommend using Node v4 with Ghost for the time being - even that this version is not the version recommended for most users by [Node.js](https://nodejs.org/?ref=ghost.org), it's v6.

Our Node version support follows the [Node.js LTS strategy](https://github.com/nodejs/LTS?ref=ghost.org). Full details can always be found at: [https://ghost.org/docs/faq/node-versions/](https://ghost.org/docs/faq/node-versions/?ref=ghost.org).

Furthermore, this release contains two new features.

### Redirects

You can now add a redirects JSON file to your content folder to define your own HTTP redirects for your blog. We have written a [redirects support guide](https://ghost.org/docs/themes/routing/?ref=ghost.org#redirects) for it.

### AMP is now optional

You can enable or disable AMP in the admin panel under **Settings - General - AMP support**. If you disable amp, all amp requests will render a 404 page.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.11.4 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.11.4](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

Credits
-------

Kevin Ansfield, Aileen Nowak, John O'Nolan, Austin Burdine, 唐佳诚 , Vivek Kannan, Kenneth Ashley, John O'Mahoney, Hannah Wolfe and Katharina Irrgang


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





 





 
















 






