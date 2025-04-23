


Native search










































We've just introduced native Search in Ghost to give your readers fast and intuitive access to find content anywhere across your publication. First, a quick overview of how this new feature works. After that, a few more details about how (and why) we built and released this feature, for those amongst you who have been around for a while and asking us to create it!

---

Ghost Search works out-of-the-box with *any* theme, and allows your readers to search across all published posts, tags and authors.

0:00/

Adding Search to a Ghost site is easy, and can be done in two ways:

1. Add a `#/search` link to your site navigation in Ghost Admin, and you'll have a clickable navigation link that opens the search interface.  
   Read more in our [help docs](https://ghost.org/help/search?ref=ghost.org).
2. Add a `data-ghost-search` attribute to any element in your theme (a 🔎 icon, perhaps?), and you'll have a clickable button to open the search interface.  
   Read more in our [developer docs](https://ghost.org/docs/themes/search?ref=ghost.org).

Once added, people visiting your site will easily be able to find what they're looking for with a single click — or even open the search UI directly by using the `Ctrl/Cmd` + `K` keyboard shortcut!

All [official Ghost themes](https://ghost.org/themes/?category=official&ref=ghost.org) have been updated to support Search. All **[Ghost(Pro)](https://ghost.org/pricing/?ref=ghost.org)** sites already have access to Search, and self-hosted users can [update](https://ghost.org/docs/update/?ref=ghost.org) to the latest version using Ghost-CLI.

---

Behind the scenes: Why did it take so long to build Search?
-----------------------------------------------------------

A Search function has been our most requested feature of-all-time, over [on the Ghost forum](https://forum.ghost.org/c/ideas/5?ref=ghost.org). Everyone has been asking for it, for nearly 10 years. So, why didn't we do it sooner? For developers and technical users, here's a bit of history.

Search is one of those features where if it works well, it's fantastic, but if it works poorly — it's worse than having no search feature at all. Anyone who has used the search function in older open source content management systems will remember all too well how often you would search for an exact post title and get hundreds of results back... except for the post you were searching for.

There are entire companies with *thousands* of developers dedicated to doing search well, like [Google](https://google.com/?ref=ghost.org), [DuckDuckGo](https://duckduckgo.com/?ref=ghost.org), and [Algolia](https://algolia.com/?ref=ghost.org) — so for a long time, with a product team of (until very recently) only *4* product engineers, we didn't feel we could deliver search to a high enough standard to be useful. We also didn't like the idea of every single theme having to implement a custom, inconsistent UI for search results - which is a poor experience on lots of other platforms.

The last thing we want to do is ship something half baked that people have been asking for, only to be overwhelmed with complaints about how bad it is.

A few things have changed in the last couple of years.

First, we built a [Content API](https://ghost.org/docs/content-api/?ref=ghost.org) for Ghost which makes it easy to interact programmatically with a site's full content archive.

After that, we added [custom integrations](https://ghost.org/integrations/?ref=ghost.org), so 3rd party services could generate their own API keys to work with Ghost content and settings.

Then, we figured out how to build embedded UI components for the front-end of Ghost, which could sit cleanly alongside any theme - eg. our [Members Portal](https://ghost.org/changelog/portal/).

Eventually, all that was missing was a link to connect these different concepts together. The Ghost front-end is rendered server-side, and didn't have its own Content API key to be able to talk to the Ghost back-end. A handful of clever, well-implemented [3rd party search plugins](https://github.com/jamwise/ghostHunter?ref=ghost.org) for Ghost had popped up — but they all had the same limitation: The site owner would have to go and manually generate an API key, then edit their theme files manually, and paste in the key to get Search working. Not the best experience.

This all changed in [Ghost 5.0](https://ghost.org/changelog/5/) — as we added a default Content API key, included automatically and by default in every Ghost front-end.

Finally, the whole Ghost team got together last week for the first time in 3 years(!) for a retreat in sunny Spain, and we set out to build a simple, high-quality search function that would work across any Ghost site. That's what we're launching today.

![](https://ghost.org/changelog/content/images/2022/07/DSCF2803.jpg)

It still comes with a few limitations, though. The search feature indexes post titles, excerpts, authors and tags - but it does not search across post content, and it can only index 10,000 posts to make sure the performance is blazing-fast. These limitations are where the difficulty of implementing a search feature goes from "*relatively easy*" to "*oh shit*".

Our plan for the next iteration of Search is to make it extensible, so the UI remains largely the same - but it will be possible to completely replace the back-end search functionality and index with something more technically sophisticated (like [Algolia](https://algolia.com/?ref=ghost.org)) for large/hungry publishers who need even more power.

For the vast majority of publishers and creators, though, the native Search implementation launched today will be everything they need.

---

**A very special thanks to Ghost team member: Sodo.**  
In 2020 [we acquired](https://ghost.org/changelog/iveel/) a very popular Ghost theme company called IVEEL, whose founder—Sodo—joined the team and immediately took over the care, maintenance and development of all our official Ghost themes. Sodo had written his own custom search feature in all IVEEL's themes before joining Ghost, and it was that code that formed the basis (and now the core) of the official Search feature in Ghost.

---

Thanks for your patience while we worked hard to get this right! And, of course... Search was not the only highly-requested feature that we worked on during our team retreat.

Stay tuned!

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





 





 
















 






