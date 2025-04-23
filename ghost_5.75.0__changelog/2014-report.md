


Lessons from Building an Open Source Product from $0 to $350,000/year











































Just a year ago we launched our **Ghost(Pro)** hosted platform to allow people to easily deploy and run Ghost blogs.

We’ve come a long way.

From the very beginning, during the [Kickstarter Campaign](https://www.kickstarter.com/projects/johnonolan/ghost-just-a-blogging-platform?ref=ghost.org), we put forward the idea of a hosted platform for an Open Source project as a means to make it both sustainable and profitable.

At that point it was really just a theory and a dream. No Open Source project had ever done anything quite like it before.

**Today, the Ghost Foundation turns over $350,000 and, even more significantly: is profitable.**

2014 was a pretty incredible year. It’s surreal to look back at just how far we’ve come. 2015 is set to be even bigger.

A Bigger Focus on Transparency
------------------------------

For the last year we’ve realised that a lot of things we’re passionate about are symptoms of something larger. Ghost is Open Source because we believe in free and open software which is available to everyone to use, hack and redistribute as they see fit. Ghost is not-for-profit because we believe in building an incredible company which is dedicated to its users, rather than creating wealth for its founders.

We’ve realised the larger umbrella that embodies all of these elements that ties them all together is quite simple: Transparency.

What we’re really excited about is building a company with integrity that’s completely open about what it does and why.

This year we’re going to place a much bigger focus on being even more aggressive about the number of things which we open up to the public. We’ve learned a lot from our friends over at [Buffer](https://bufferapp.com/?ref=ghost.org) and we’re going to be taking a leaf out of their book in several ways.

We’ve got tons of exciting things planned around this, and we’re starting out with a very simple one: Revenue reports.

Ghost 2014 Revenue Report
-------------------------

We’re going to try and do these every month from now on, but to start with here’s a roundup of how we did last year:

![](https://ghost.org/changelog/content/images/2021/01/image-90.png)

* **Unique visitors:** 3,284,749
* **Total downloads:** 504,949
* **Total users**: 257,307
* **Ghost(Pro) subscribers:** 3,675
* **Monthly recurring revenue (MRR**): $29,177
* **Annual recurring revenue (ARR**): $350,124
* **Average revenue per user:** $7.94
* **Churn rate:** 4.87%
* **Team size**: 6 people across 3 continents

The overwhelming majority of our internal focus last year was on getting MRR up to make us profitable. Ghost Foundation being profitable makes it a sustainable business that can keep on going without outside investment. We prioritised high-traction features and did a lot of work on our pricing to reach this point.

We could have hit profitability in June, had we kept the team smaller - but we expanded to 6 full time people in order to be able to keep shipping new features in line with demand, so we eventually hit this milestone in December.

MRR is currently growing at around 8% month on month, which is definitely something we’d like to improve - but the pressure in 2015 is much lower than it was last year. Which is great!

Lesson 1: Getting Pricing Right is Critical
-------------------------------------------

Launching one of the world’s first consumer Node.js apps was like diving into a black-hole when it came to setting up a hosted infrastructure. We had almost no idea how much it was going to cost, what the margins would be like, or where we should even begin with charging.

We started out with a base $5/month plan with a few higher options, all the way up to $80/month for the highest plan.

After spending a lot of time doing customer development, we worked on a new plan structure with new pricing. The base plan would now be $10/month and range all the way up to $250/month for business users.

![](https://ghost.org/changelog/content/images/2021/01/image-91.png)

Having run a 33 day A/B test on the new pricing prior to changing it, we found that the price change actually lead to an *increase* in conversion rate. So, 2x the revenue and more customers than before. Despite a little negative feedback when we [announced it](https://ghost.org/changelog/new-ghostpro-plans/) at the end of September, the data told us that the new pricing was clearly the right way to go.

Pricing is something that’s never “finished” - and we’re planning to do more experiments in 2015 to optimise this further. The goal is always to give as much value to customers as we can, while creating a healthy business.

The most important lesson we learned here was that **it’s really, really hard to build a viable business with $5/month plans**. We’ve seen several other “Ghost hosting” companies enter and subsequently exit the market with price ranges from $2.99 to $5.99 - which isn’t a big surprise. Increasing our average revenue per user has been an enormous weight off our shoulders, and given us a lot more room to work with.

If you’re interested in anything to do with product pricing: I really recommend running your own experiments to find out what works for you. It's very easy to get distracted by blog posts which sound sensible but turn out not to be.

Lesson 2: A Small Change at The Start of The Funnel Has a Massive Impact at The End
-----------------------------------------------------------------------------------

We refer to the “funnel” as the process of moving a customer through the various stages of the onboarding process. Usually it looks something like this:

* User signs up [10,000 people]
* User starts trial [4,000 people]
* User sets up product for first time [2,000 people]
* User becomes a subscriber [400 people]

At each stage of the funnel there’s a conversion rate which can be worked on as you try to nudge users toward completing your desired goal: eg. becoming a subscriber.

The interesting thing is that each step of the funnel impacts every step of the funnel below it (but not above). So, while it can be tempting to just work on the conversion rate of your end-of-trial page at the very end… it can actually have a far larger impact to just get a 1% increase in the number of people who are starting trials right at the start of the funnel.

![](https://ghost.org/changelog/content/images/2021/01/image-92.png)

We [figured out what caused](https://ghost.org/changelog/ghost-onboarding/) users to be 1,000% more likely to convert to paying customers. When we applied this learning, we were immediately able to see a 370% conversion rate increase further down the funnel. There was no way we could have gotten a 370% increase in conversions just by working on A/B testing to improve that one particular page. To improve one action, we had to look upstream first.

This was a super interesting lesson.

**A tangential lesson here, too:** Make sure your analytics actually work correctly. There’s nothing worse than finding out you implemented a piece of tracking very slightly wrong, and now your last 6 months of data is totally meaningless and can’t be used for any kind of segmentation or analysis. Sounds obvious - but we’ve found flaws in our tracking implementations over and over and over again. It’s way easier to screw up than you might imagine.

Lesson 3: If Something Feels Weird and Broken, it Probably is
-------------------------------------------------------------

For the first half of the year or so, we did a big-bang release of Ghost every few months. We named each version and made a big fuss about what version number it was. We included details of all the things that had been worked on since the last release, and provided instructions on how to update.

This is how almost every single Open Source project in the world works, but after a while, it started to feel pretty weird and broken.

Why, in 2014, would you only release software a few times a year? Why do people constantly have to update? How can developers ever learn from user behaviour or improve on their work, when there’s a 6 month gap between usage and iteration?

![](https://ghost.org/changelog/content/images/2021/01/image-93.png)

*In August [we announced](https://ghost.org/changelog/ghost-0-5/) Ghost 0.5, and noted that it would be the last release in this format*.

Since then, we’ve moved to an agile release process - shipping new things every 2-4 weeks. In the last 4 months of 2014 [we released](https://github.com/TryGhost/Ghost/releases?ref=ghost.org) 7 different versions of Ghost. In 2015 that number is only going to increase as we automate more of the process.

Best of all - we automatically push these updates out to all **Ghost(Pro)** customers in the background. This isn’t just a better experience all round for everyone, but it also added a significant extra feature/benefit to using our hosted platform which would drive more people to using it.

Looking back, it seems insane that we ever did releases any other way. If you’re doing something because “that’s the way it’s always been done” - it might be time to try something new.

So What’s Coming in 2015?
-------------------------

*Lots.*

![](https://ghost.org/changelog/content/images/2021/01/image-94.png)

The [Ghost Roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org) is pretty full right now, and we’re incredibly motivated to ship the things which are in high demand, especially:

* Editor improvements (Spellcheck!)
* Tag management
* Navigation menus
* Code injection
* Post scheduling

*A major focus for the rest of the year is going to be around Apps and the [Ghost Marketplace](https://ghost.org/marketplace/?ref=ghost.org).*

We’ve been talking about this for a long time, and haven’t made much progress because it’s such a major project. This year we’re hoping to finally make some serious progress on allowing other apps and services to integrate with Ghost, and vice versa.

We know there are multiple issues with the current marketplace (which is really just a placeholder showcase gallery), and that’s something we’re going to be looking to completely overhaul in 2015. The long term plan is to have it look and feel a lot more like an Apple App Store or Google Play Store type experience. Shopify have done a pretty great job with [their marketplace](https://themes.shopify.com/?ref=ghost.org), which should give some indication of things we’d like to do.

There’s also going to be an increased focus on content for this blog (we’re going to share lots more), as well as work towards making Ghost and Ghost.org much more friendly for translation into other languages.

If there’s anything you’d like to see us writing about, sharing, or doing - or if you have any questions about what else we did in 2014: Let us know in the comments.

*Thanks for being a part of this journey and making it all possible. Without you, we’d be absolutely nowhere.*

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





 





 
















 






