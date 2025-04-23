


Ghost August update: $500k annual revenue, doubled cashflow, new UI











































It's been a while since we last did a proper update on revenue and progress at Ghost. Last week we passed the $500,000 mark, and I thought it was about time to do a progress review.

**Here's an update on our numbers since [the April report](https://ghost.org/changelog/april-2015-update/)**

* **Monthly recurring revenue (MRR**): $41,714 (+22%)
* **Annual recurring revenue (ARR**): $500,569 (+22%)
* **Ghost(Pro) subscribers:** 4,139 (+10%)
* **Average revenue per user:** $9.10 (+15%)
* **Churn rate:** 6% (-19%)
* **Total downloads:** 755,574 (+35%)
* **Total users**: 363,051 (+26%)
* **Team size**: 7 people across 4 continents

All of our numbers are pretty healthy at the moment. Growth is slower than we'd like, but we are now into our 8th straight month of profitability. As a result, we're in really great shape financially, and we've started growing the team again more aggressively.

We added two new people ([Belle Beth Cooper](https://ghost.org/changelog/belle-beth-cooper/) & [Kevin Ansfield](https://ghost.org/changelog/kevin-ansfield/)) in the last month, and we're [still looking for several more](https://careers.ghost.org/?ref=ghost.org)—especially Node.js developers.

Fixing our two biggest mistakes
-------------------------------

We made two enormous mistakes at the beginning of Ghost's life which have crippled us for a very long time. We've finally gotten out from under them, and I think it's worth talking about.

### Doing Stripe Properly

**The first mistake** was to implement Stripe as a payment processor, while building a custom plan system and billing management. In short, this backed us into a tight, uncomfortable corner filled with edge-case stumbling blocks. Want to integrate with other Stripe apps (like [Baremetrics](https://ghost.org/about/?ref=ghost.org#metrics))? No dice. Want to offer annual billing and a referral program? Spend 3 months rewriting everything. Repeat.

This was an unmitigated disaster. At the start of this year, we spent 2 months rewriting our entire billing system to use the Stripe Plans API. In April, as a result, we were able to offer Annual Billing for the first time. Here's the impact it had on cashflow by the end of May:

![](https://ghost.org/changelog/content/images/2021/01/ghost-growth-1.png)

Ghost Cashflow

Annual customers pay 20% less, but they pay in advance, which provides additional revenue which can be used on acquiring new customers, who pay in advance, which provides additional revenue which can be used on acquiring new customers, and so on. About 50% of new customers select annual plans, so it works out to approximately **-10% Monthly Recurring Revenue in return for +100% monthly net revenue**.

Annual billing has single-handedly transformed Ghost as a business more than anything else we've ever done. **We should have done this much sooner. And we would have, if we hadn't implemented Stripe the wrong way to begin with.**

*Aside: Using the Stripe Plans API is **still** far from perfect. For all the love the Stripe API gets, there are still a boatload of edge cases to handle which catch us out regularly. Knowing what we know now, if we were going to start over with a small, bootstrapped team, we would use [Recurly](https://recurly.com/?ref=ghost.org) to manage our billing with Stripe. It's expensive, but (as we now know) probably worth it.*

### Moving to DigitalOcean

**Problem number two** was that we built the first version of **Ghost(Pro)** on our own dedicated infrastructure, which was a bit too clever for its own good, and that came back to bite us.

**The good:** We got everything setup in a couple of months to work at a scale where we could (relatively) flawlessly host tens of thousands of blogs on just 3 application servers.

**The bad:** After 18 months our hardware was about to become obsolete. Scaling our systems had a ~60 day lead time and long-term contract requirements. We'd written the service in such a way that we were unable to ship some of the most [requested features](https://forum.ghost.org/c/Ideas/?ref=ghost.org) in Ghost itself (eg. Scheduled posts).

In short: It performed really well for us for the first year, but we could see that in another 12 months we were going to be pretty screwed.

![](https://ghost.org/changelog/content/images/2021/01/digitalocean-1.png)

DigitalOcean

It took about 3 months of organising, planning and implementing—but a few weeks ago we complete our full infrastructure migration to [DigitalOcean](https://ghost.org/changelog/digitalocean/).

These two areas comprised a sum total of a good 6 months of tiring, thankless behind-the-scenes work which was done almost entirely by [Sebastian](https://github.com/sebgie?ref=ghost.org)—who is an absolute hero.

We're now in a place where we're finally unblocked from some of our biggest hurdles to building things for Ghost. It feels good.

What else
---------

At the end of September we're doing our second **team retreat** and flying everyone over to where I live, in Egypt. And if you're wondering – as most people do – *"omgwtf why do you live in Egypt?"*—[click here](https://images.google.com/search?tbm=isch&q=El+Gouna+Egypt&ref=ghost.org).

Proportionally to existing-user-base, Ghost was one of the **fastest growing platforms in the world** in July, [growing by a full 17%](https://blog.builtwith.com/2015/07/06/entire-internet-cms-usage-january-july-2015/?ref=ghost.org) compared to June. We're hoping to see this grow even further soon as *BuiltWith* expands tracking to subdomains, which is where most people install Ghost.

Perhaps most excitingly of all, we're about to launch Ghost's **first major user interface update**. More on that later, but here's a sneak preview:

![](https://ghost.org/changelog/content/images/2021/01/ghostnew.png)

Ghost 0.7

A small favour
--------------

Honestly, the biggest thing that helps us both as a business and as an open source community is helping more people find out about Ghost. We'd be tremendously grateful for your help in sharing our progress!

Here’s a simple copy/paste status, to make it super easy:

> The non-profit with $500,000 ARR and counting. How @TryGhost doubled cashflow and is about to launch a new design: /changelog/august-2015-update/

or use 1-click links for *Ultimate Efficiency* TM: [Tweet this](https://twitter.com/share?text=The+non-profit+with+%24500%2C000+ARR+and+counting.+How+%40TryGhost+doubled+cashflow+and+is+about+to+launch+a+new+design%3A&url=https%3A%2F%2Fghost.org%2Fchangelog%2Faugust-2015-update%2F&ref=ghost.org) or [Buffer it](https://bufferapp.com/add/?url=https%3A%2F%2Fghost.org%2Fchangelog%2Faugust-2015-update%2F&text=The+non-profit+with+%24500%2C000+ARR+and+counting.+How+%40TryGhost+doubled+cashflow+and+is+about+to+launch+a+new+design%3A&ref=ghost.org)

**We'll be hanging out in the comments if you have any questions or thoughts!**


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





 





 
















 






