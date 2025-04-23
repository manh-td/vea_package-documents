


The New Ghost Admin API: Build advanced publishing workflows












































Ghost has always had a REST API at its very core, but for the first few years while we were fleshing out basic features there wasn't a whole lot you could do with it. Now, all your favourite apps work with Ghost!

At the beginning of this year we announced a brand new, public [Content API](https://ghost.org/docs/content-api/?ref=ghost.org) making it possible to easily pull any content ***out*** of Ghost. This also made it possible, for the first time, to use Ghost as a fully [headless CMS](https://ghost.org/changelog/jamstack/).

Today we're excited to be able to share our new [Admin API](https://ghost.org/docs/admin-api/?ref=ghost.org), which does just the opposite: It creates total flexibility around how you get content ***in*** to Ghost.

Now you can use mobile and desktop writing clients, or create your own custom Ghost Admin integrated into your own apps/workflow. It's the final piece of the puzzle to complete the architecture we've been working towards for a few years now, which involves making this little green dot less lonely:

![](https://ghost.org/changelog/content/images/2019/05/ghost-architecture.png)

All of these different pieces come together to create a robust publishing experience – but because they're decoupled, there's room for customisation to suit any modern development and workflow requirements.

Sounds great, so what does all that mean in practice?

Brand new integrations
----------------------

Firstly, we're thrilled to be launching the new Ghost Admin API with 4 wonderful partners who we've been working with for the last few months:

![](https://ghost.org/changelog/content/images/2019/05/ghost-admin-apps--1-.png)
### 🚢 [NEW: Ulysses Integration](https://ghost.org/integrations/ulysses/?ref=ghost.org)

One of the most requested integrations we've ever had! Ulysses is an extremely powerful and widely loved desktop editor for Mac, now with full Ghost integration so you can send draft posts directly to Ghost.

### 🚢 [NEW: iA Writer Integration](https://ghost.org/integrations/ia-writer/?ref=ghost.org)

The original Ghost editor was partially based on iA Writer's gorgeous minimal design, and as of iA Writer 5.2 you can now also send posts directly to Ghost from both MacOS and iOS. The iA Writer team helped us refine and improve the Admin API while it was in development, so a big thanks to them.

### 🚢 [NEW: Write.as Integration](https://ghost.org/integrations/write-as/?ref=ghost.org)

After being unceremoniously [kicked-off](https://write.as/blog/ending-our-medium-integration?ref=ghost.org) the Medium API for no reason at all a few months ago, we reached out to the Write.as team to offer them an open alternative. We're thrilled to be able to share a great new integration here which can never be shut down or restricted.

### 🚢 [NEW: Zapier v2 Integration](https://ghost.org/integrations/zapier/?ref=ghost.org)

Of course we couldn't add a new API without a major update to our Zapier integration - which hits V2 today - and opens up Admin API access to over 1,000 other apps and services all over the web. You can now send content into Ghost from almost anywhere!

> *Note: If you're already using Ghost<>Zapier, you'll need to remove and re-connect your Ghost site in order to use the new version of the app.*

---

Developer details
-----------------

Technically speaking, there are several different aspects to this update which come together to make all these new things possible.

![](https://ghost.org/changelog/content/images/2019/01/ghostapi.png)
### 🚢 [NEW: Admin API](https://ghost.org/docs/admin-api/?ref=ghost.org)

The latest updates provides secure role-based permissions, predictable resource URLs, standard HTTP verbs, response codes and authentication. It enables full control for creating, editing or deleting publication data. Ghost Admin uses the Admin API – which means you can do everything Ghost Admin can do, and more. Unlike several other platforms, our Admin API isn't a bolt-on afterthought; it's a first class citizen at the heart of the core platform.

### 🚢 [NEW: JavaScript Client Library](https://ghost.org/docs/admin-api/javascript/?ref=ghost.org)

We've also shipped an API client for JavaScript designed for use with integrations that use private API keys, to simplify authentication and make it easier to read and write data. This supports publishing workflows such as sending content from an desktop editor, automating social media sharing or syncing data to and from email campaigns.

```
const api = new GhostAdminAPI({
  url: 'https://localhost:2368',
  key: 'YOUR_ADMIN_API_KEY',
  version: 'v2'
});

api.posts.add({
    title: 'My first draft API post',
    mobiledoc: '{\"version\":\"0.3.1\",\"atoms\":[],\"cards\":[],\"markups\":[],\"sections\":[[1,\"p\",[[0,[],0,\"My post content. Work in progress...\"]]]]}'
});
```

Working example!

We're continuously adding new tools to our [integrations library](https://ghost.org/integrations/?ref=ghost.org), including deep integrations that are supported by our Admin API.

---

****************[Ghost(Pro)](https://ghost.org/pricing/?ref=ghost.org)**************** users have already been updated and have access to everything mentioned here. Self hosted developers can use [Ghost-CLI](https://ghost.org/docs/ghost-cli/?ref=ghost.org) to get the latest features by running `$ ghost update` to install the [latest release](https://github.com/TryGhost/ghost/releases?ref=ghost.org).

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





 





 
















 






