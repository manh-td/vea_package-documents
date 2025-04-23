


Ghost on the JAMstack – Future-proof Professional Publishing











































After some major updates to Ghost's public API and tooling, it's now possible to use Ghost as a completely decoupled headless CMS.

Ghost has always been architected into 3 distinct areas: A core Node.js API, an Ember.js Admin client, and a speedy Handlebars.js front-end theme layer. Until now those 3 areas have been fairly tightly coupled, so it hasn't been possible to use them separately.

![](https://ghost.org/changelog/content/images/2019/01/ghost-core-1.png)

The static-site revolution
--------------------------

The last few years have seen lots of progress around static site generators, front end frameworks, and API-centric infrastructure. There have [never been more options](https://www.staticgen.com/?ref=ghost.org), and the competition between them is generating some very cool products such as [Gatsby](https://www.gatsbyjs.org/?ref=ghost.org), [Hugo](https://gohugo.io/?ref=ghost.org), [Hexo](https://hexo.io/?ref=ghost.org), [Nuxt](https://nuxtjs.org/?ref=ghost.org) and [many more](https://www.staticgen.com/?ref=ghost.org).

The way these systems work is by pulling content either from a filesystem or API endpoint and running a build task to generate an entire site in *static* HTML. The end result = wildly fast websites which have no back end and can be deployed just about anywhere.

With the latest updates to Ghost, you can now replace the Ghost theme layer completely in favour of a front-end framework which builds your site statically from the Ghost API - effectively running Ghost as a Headless CMS.

![](https://ghost.org/changelog/content/images/2019/01/headless-ghost.png)

The headless-cms evolution
--------------------------

Most static site generators work by storing Markdown files locally in the code repository, and in practice this works really well for small sites! But, it gets messy quickly with any sort of scale, and there's no admin client or API. You need a code editor to write content, you need a properly configured GIT workflow to publish, and your content is limited to just your website. Fine for developers with smaller sites, but not so much for other use-cases!

This is where a headless CMS comes in.

Now you can run a Node.js back end service with a stable, production ready REST API as your content infrastructure with a beautiful matching admin client - and it's all completely free, open source, and MIT licensed. You use Ghost for authoring, and then build out your front-end to pull from the API in any way that you prefer.

* Developers get to use their preferred stack
* Writers get to use their preferred editor
* Performance is the maximum possible *(no back-end, it's just HTML!)*
* Security is the maximum possible *(seriously, it's just HTML!)*

Building sites in this way has become known as the [JAMstack](https://jamstack.org/?ref=ghost.org) - (as in **J**avaScript, **A**PIs, **M**arkup) -  and has been progressing rapidly for some time. When you start to look at the bigger picture of [the content mesh](https://www.gatsbyjs.org/blog/2018-10-04-journey-to-the-content-mesh/?ref=ghost.org), it really starts to feel like an inevitable future is upon us.

![](https://ghost.org/changelog/content/images/2019/01/ghost-jamstack.png)

No more platform-specific plugins and extensions. Just one front-end, and many APIs; all connected together and served as a single site or application.

So what's new?
--------------

There isn't one headline feature to announce here, but rather a collection of additions, improvements and changes to Ghost which unlock all kinds of new possibilities for what developers can build with the platform.

![](https://ghost.org/changelog/content/images/2019/01/ghostapi.png)

Ghost API updates
-----------------

Ghost has had a full JSON API since day 1, but last month we released a completely new version of it with support for key generation and webhooks.

###### 🚢 NEW: [Content API](https://ghost.org/docs/content-api/?ref=ghost.org)

The new content API is what delivers published content to the world. Access from any client to render your content on the web, app or any other embedded media. Access control is managed via API key, and includes a simple Mongo-like query language for powerful, advanced filtering.

###### 🚢 NEW: [Admin API](https://ghost.org/docs/admin-api/?ref=ghost.org)

While the Content API sends your content out, the Admin API gives you the flexibility to send content **in** to Ghost from mobile and desktop writing clients like [Ulysses](https://ghost.org/integrations/ulysses/?ref=ghost.org) or [iA writer](https://ghost.org/integrations/ia-writer/?ref=ghost.org), or to create your own custom apps and workflows.

###### 🚢 NEW: [Custom integrations](https://ghost.org/integrations/custom-integrations/?ref=ghost.org) + [webhooks](https://ghost.org/docs/webhooks/?ref=ghost.org)

New API clients can now be registered as custom integrations with dedicated API keys, along with their own outgoing webhooks to notify external services when an event takes place in Ghost.

###### 🚢 NEW: [JavaScript API library](https://ghost.org/docs/content-api/javascript/?ref=ghost.org) + [SDK](https://ghost.org/docs/content-api/javascript/?ref=ghost.org)

As well as an official JavaScript client library for the Ghost API, we've also started pulling out common front end helpers from our Ghost theme API layer (eg. a tags helper to return a list of linked tags) and turning them into a JavaScript SDK to work with other front-ends and frameworks.

```
const GhostContentAPI = require('@tryghost/content-api');
const GhostHelpers = require('@tryghost/helpers');

const api = new GhostContentAPI({
    host: 'https://demo.ghost.io',
    key: '22444f78447824223cefc48062',
    version: 'v2'
});

api.posts
    .browse({include: 'tags,authors'})
    .then((posts) => {
        posts.forEach((post) => {
            console.log(post.title, GhostHelpers.tags(post, {prefix: 'tagged in '}));
        });
    })
    .catch((err) => {
        console.error(err);
    });

```

Real example! Copy/paste to test for yourself

![](https://ghost.org/changelog/content/images/2019/01/gatbsy.png)

Official Gatsby.js Source Plugin + Starter
------------------------------------------

We started rebuilding our [Ghost Docs](https://ghost.org/docs/?ref=ghost.org) site at the end of last year we set out to use Ghost as a headless CMS, along with a front-end written in [Gatsby.js](https://gatsbyjs.org/?ref=ghost.org). We fell in love hard and fast, and have been building new things with Gatsby ever since. So we're thrilled to announce:

###### 🚢 NEW: [gatsby-source-ghost](https://github.com/tryghost/gatsby-source-ghost?ref=ghost.org) plugin

A straightforward Gatsby source plugin which wraps the Ghost API and makes it compatible with Gatsby and GraphQL, so it's quick and easy to load all your Ghost data into any Gatsby project.

###### 🚢NEW: Advanced [sitemap plugin](https://github.com/tryghost/gatsby-plugin-advanced-sitemap?ref=ghost.org) for Gatsby

We wanted to emulate the advanced sitemap structure that we use on all Ghost publications by default for Gatsby, so we created this SEO friendly open source plugin which is available for anyone to use!

###### 🚢 NEW: [gatsby-starter-ghost](https://github.com/tryghost/gatsby-starter-ghost?ref=ghost.org)

We've also created an official **Gatsby starter** repository, similar to our [starter theme](https://github.com/tryghost/starter?ref=ghost.org), pre-configured to get content from Ghost and output it in a clean, blog-style design. The fastest way to get up and running with Gatsby and Ghost is to fork this repository, and check out our [Gatsby docs](https://ghost.org/docs/jamstack/gatsby/?ref=ghost.org).

![](https://ghost.org/changelog/content/images/2019/01/gatsby-starter-ghost.jpg)

Demo: [gatsby.ghost.org](https://gatsby.ghost.org/?ref=ghost.org) — It's fast. Really, really fast.

![](https://ghost.org/changelog/content/images/2019/01/perf-1.png)![](https://ghost.org/changelog/content/images/2019/10/netlify.png)

Official Netlify Support
------------------------

Deploying all of this should be easy, and it is! Our Gatsby starter is fully set up to deploy to [Netlify](https://netlify.com/?ref=ghost.org), which is the same setup we use for Ghost Docs. On top of that, we've created:

###### 🚢 NEW: [Netlify integration for Ghost](https://ghost.org/integrations/netlify/?ref=ghost.org)

The official integration guide for Netlify explains how to set up outgoing webhooks in Ghost to trigger a site rebuild on Netlify. This means that any time you publish, update or remove any content in Ghost, the front end will automatically update.

![](https://ghost.org/changelog/content/images/2019/01/image-8.png)

Front-end frameworks
--------------------

Since the latest Ghost API updates mean you can bring your own front-end and build entirely custom publications, we've also added new documentation for some of the most popular static site generators around. Find out how to get started using Ghost as a Headless CMS with:

###### 🚢 [Eleventy](https://ghost.org/docs/jamstack/eleventy/?ref=ghost.org)

###### 🚢 [Next.js](https://ghost.org/docs/jamstack/next/?ref=ghost.org)

###### 🚢 [Gridsome](https://ghost.org/docs/jamstack/gridsome/?ref=ghost.org)

###### 🚢 [Nuxt.js](https://ghost.org/docs/jamstack/nuxt/?ref=ghost.org)

###### 🚢 [Hexo](https://ghost.org/docs/jamstack/hexo/?ref=ghost.org)

###### 🚢 [VuePress](https://ghost.org/docs/jamstack/vuepress/?ref=ghost.org)

---

Future-proof publishing
-----------------------

What we like most about these emerging development workflows is how they reduce vendor lock-in. Converging disparate technologies under a single front-end centralises otherwise decentralised services in a way which caters predominantly to the needs of the site owner, rather than the platform.

Making Ghost work as a headless CMS in this new paradigm feels like it's good for users, and good for the web as a whole. So we're really excited about it!

If you're still curious about the rise of the JAMstack, check out this excellent talk by Netlify co-founder Matt Biilmann:

We're really excited to be a part of the JAMstack movement and, as of today, Ghost is now the biggest open source headless CMS project in the wild:

![](https://ghost.org/changelog/content/images/2019/01/headless-cms.jpg)

[headlesscms.org](https://headlesscms.org/?ref=ghost.org) - Ranked by Github stars

---

********[Ghost(Pro)](https://ghost.org/pricing/?ref=ghost.org)******** users have already been updated and have access to everything mentioned here. Self hosted developers can use [Ghost-CLI](https://ghost.org/docs/ghost-cli/?ref=ghost.org) to get the latest features by running `$ ghost update` to install the [latest release](https://github.com/TryGhost/ghost/releases?ref=ghost.org).

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





 





 
















 






