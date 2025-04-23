


Eleventy and Ghost: Use your favourite static site generator!












































We’ve expanded our roster of headless starter repositories – now you can build a completely custom front-end for a Ghost site with Eleventy.

Earlier this year [we shared what's possible with Ghost when used as a flexible headless CMS](https://ghost.org/changelog/jamstack/). One of those possibilities being the option to deliver [content via our API to a Gatsby site](https://ghost.org/docs/jamstack/gatsby/?ref=ghost.org). The end result: A robust and familiar space to create, organise and store your content, with a blazing fast static site on the front-end.

We're now extending our documentation to show what's possible with the Content API and [Eleventy](https://11ty.io/?ref=ghost.org), a popular static site generator in the JAMstack space.

![The 11ty logo](https://ghost.org/changelog/content/images/2019/08/eleventy-starter-banner.png)

What is Eleventy?
-----------------

Eleventy, or 11ty for those of you in a hurry, is a static site generator that was designed to be the JavaScript alternative to [Jekyll](https://jekyllrb.com/?ref=ghost.org). Without going into too much depth; [Eleventy](https://www.11ty.io/docs/?ref=ghost.org) is designed to be a flexible and easy tool to take an assortment of files and turn them into a [static website](https://www.11ty.io/docs/resources/?ref=ghost.org#static-sites). Those files could be [Markdown](https://daringfireball.net/projects/markdown/?ref=ghost.org), HTML, [Nunjucks](https://mozilla.github.io/nunjucks/?ref=ghost.org), [Handlebars](https://handlebarsjs.com/?ref=ghost.org) or even straight up JavaScript!

Eleventy works [without configuration](https://www.11ty.io/docs/resources/?ref=ghost.org#zero-config) – meaning it's accessible to newcomers but not overly opinionated on file structure and settings.

### How does this flexible static site generator fit in with Ghost?

I'm glad you asked that question: Under the hood of Eleventy is a [clever data pipeline](https://www.11ty.io/docs/data/?ref=ghost.org) that is accessible from any template file within an Eleventy project. It's possible to feed any type of data into it, including content coming from the Ghost content API.

![Diagram showing Ghost data being fed into Eleventy and subsequently Eleventy being deployed to various hosting platforms](https://ghost.org/changelog/content/images/2019/08/eleventy-starter-diagram.png)

Posts, pages, tags, authors, global site data; you name it. Eleventy is built on top of [Node.js](https://nodejs.org/en/?ref=ghost.org) (great choice if you ask us) which means it works really well with [our open source JavaScript libraries](https://ghost.org/docs/content-api/?ref=ghost.org).

So what's new?
--------------

We're excited to share what's possible with the Ghost API – hopefully these resources inspire and help you to create unique websites using Ghost as a headless CMS.

### 🚢 NEW: [Eleventy Starter Ghost](https://github.com/TryGhost/eleventy-starter-ghost/?ref=ghost.org)

We've created an official **Eleventy starter** repository, similar to our Gatsby starter, that's all setup to consume content from Ghost and build out a simple flat-file website with a clean blog-style design. The best way to use [this starter is to fork it](https://github.com/TryGhost/eleventy-starter-ghost/?ref=ghost.org). Want to see it in action? Check out this [live demo we've created](https://eleventy.ghost.org/?ref=ghost.org).

![Screenshot of Eleventy & Ghost demo site](https://ghost.org/changelog/content/images/2019/08/61880744-5b138980-aeed-11e9-9d8e-07c0b3c03cc5.png)

*Demo: [eleventy.ghost.org](https://eleventy.ghost.org/?ref=ghost.org)*

### 🚢 NEW: [Eleventy & Ghost Documentation](https://ghost.org/docs/jamstack/eleventy/?ref=ghost.org)

To coincide with this starter we've also created documentation on how to use this starter as well as ways you can use the [Content API Client Library](https://ghost.org/docs/content-api/?ref=ghost.org) to expose specific parts of your content to Eleventy.

💠 Works great with Netlify
--------------------------

This combination of Ghost and Eleventy works great when deploying to [Netlify](https://www.netlify.com/?ref=ghost.org). With the power of webhooks we can automatically let Netlify know when a change is made in Ghost and trigger a deploy causing Eleventy to rebuild the website with the new content. Check out our [Netlify Integration page](https://ghost.org/integrations/netlify/?ref=ghost.org) for more information.

What the future holds
---------------------

From a personal perspective I'm very excited about the possibilities that exist with [headless CMSs](https://headlesscms.org/?ref=ghost.org), APIs and static site generators – AKA the [JAMstack](https://jamstack.org/?ref=ghost.org). Ghost is a battle-tested headless solution for businesses who need the power and flexibility of a modern CMS to build and run successful digital publications ✨

For those of you that don't know me; my name is Dave and I recently joined the team as Developer Advocate. I've been a fan of the JAMstack for many years, creating open source projects and contributing to the community along the way. Feel free to [get in touch with me via Twitter](https://twitter.com/daviddarnes?ref=ghost.org), or [hop onto the Ghost Forum](https://forum.ghost.org/?ref=ghost.org) to share what you're making with Ghost!

---

Put the new Eleventy starter and Ghost through their paces with a free, no strings attached [**Ghost(Pro)**](https://ghost.org/pricing/?ref=ghost.org) trial – or get started with a [self-hosted](https://ghost.org/docs/install/ubuntu/?ref=ghost.org) install.

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





 





 
















 






