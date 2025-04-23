


Merry Christmas: The Ghost Hosted Platform is Now Open






































*Today we are bringing you an announcement from Ghost HQ that has been cooking for rather a long time: The Ghost Hosted Platform is now available to absolutely everyone.*

Our hosted platform is a premium service which allows you to set up and run a Ghost blog in a matter of seconds. It's incredibly powerful, easy to use, and is probably the best way of running any Ghost blog online.

Most importantly - as a NonProfit Organisation - this platform will secure the future of Ghost. Every penny we make from our hosted platform is re-invested into improving the Ghost software for everyone in the world. So if you want to help Ghost grow and improve, give it a try, and consider hosting your blog directly with us.

*Benefits include an incredible infrastructure, awesome support, and a warm fuzzy feeling as a result of helping to improve online publishing for the entire world.*

The hosted platform is available for all users, **right now**, from your [Ghost.org Dashboard](https://my.ghost.org/?ref=ghost.org).

For those of you interested in a little more of the story behind how we put this giant piece of work together to get where we are now... read on

Building Hosted Ghost
---------------------

Shortly after our Kickstarter campaign completed, we embarked on a journey which was - by all measures - a pretty crazy one. Simultaneously to building the Ghost blogging platform itself, we set out to create a hosted service which would allow people to get a brand new blog up and running with the click of a button and scale to handle millions of visitors.

To add an extra bit of spice to the mix, much of the infrastructure which we've now created has never been done before with a piece of software built on Node.js.

We were incredibly fortunate that our wonderful friends over at [aTech Media](https://atechmedia.com/?ref=ghost.org) had not only decided to become Ghost launch partners during the Kickstarter campaign - but also wanted to help us build out this entire side of the project.

*By early August, the boxes started to arrive, and we started plugging everything in and setting things up.*

![Ghost servers arriving in boxes](https://s3.amazonaws.com/ksr/assets/001/177/871/ccadae4f0d690de1ce2e58dc4c2934ae_large.jpg?1381819346)

After a couple of months of rigorous development, pushing the Ghost project, the Ghost.org website and the brand new hosted platform ahead all at the same time - and in sync with each other (I can't begin to tell you how hard this is!) - we had our first working version.

### The First Users

In mid-October, as we [launched](https://ghost.org/changelog/public-launch/) the first version of Ghost to the public - we started adding the first people to our shiny new hosted platform. Initially all the blogs lived on a subdomain of ghost.org, but after a lot of consideration and logistical tomfoolery, we decided to move public-facing hosted blogs to a ghost.io subdomain. Github style.

At this point [Hannah](https://twitter.com/ErisDS?ref=ghost.org) was doing live demo (roulette) of the hosted platform [preview](https://ghost.org/changelog/hosted-platform-preview/) on stage at various Node.js events and showing off the ease-of-use which would soon be coming to deploying a Ghost instance to the web. Fortunately, it worked every time!

### Getting in The Kickstarter Backers

A month later, in late November, we were ready to put the platform through its paces with some more heavy usage. We started adding our Kickstarter backers at a rate of around ~1,000 per day, and asked them to set up and use the platform as rigorously as possible to try and help us iron out any hiccups in the system.

We found a few problems, but nothing major, and we continued to optimise the system to handle more concurrent requests to provision blogs at a faster rate.

### Building it Differently

You see, what we've built is pretty special. Unlike something like WordPress.com or Tumblr or Medium - where they have one giant web application with multi-tenancy - The Ghost hosted platform provisions truly independent installs of Ghost on-the-fly. Why is that important? Well I'm glad you asked!

When multiple blogs all live within one large application, the blogs are all inherently linked to each other. This means that for security reasons, you can't give users full control over what they do. It would be very easy for a single user to bring down the entire network with one wrong move. That's why with these platforms, you are never allowed to have custom plugins or functionality, and you're almost always heavily limited on what (if anything) you can do with themes.

This limitation kind of sucks, because as soon as you get serious about blogging, as soon as you start to look at it from a professional publishing point of view... you want, and often *need* full control of your website to do things which go beyond the defaults.

With the Ghost hosted platform, each blog is an independent install of the Ghost software. It's not connected to any other blogs. This means that we can allow you to run apps (plugins) or custom themes or do (almost) anything you want. This was a really critical point for us, because we didn't just want to create this platform as something "easy" - suited to beginners.

We wanted to make it easy **and** create the best possible infrastructure for running Ghost that's available on the web. Giving publishers and developers full control over their Ghost blog is the most important piece of that puzzle.

Rolling Out To The Public
-------------------------

There's nothing like real-users to test your infrastructure (and your assumptions). In December, a few weeks ago, we started rolling out full access to Ghost.org users in bulk. We added 10-20,000 users almost every day. It was exciting (read: terrifying) and you guys successfully managed to wake us up several times at 3am to restart servers and rewrite systems which couldn't handle the volume of requests which they were being made subject to.

Slowly, but surely, it stabilised. We found the bottlenecks, we changed some of the UI based on your feedback, and we improved everything we've been working so hard on to get to this point.

**Today, the hosted platform is available to everyone.**

(PS. and it works!)

*A huge thank you to Charlie, Adam, Jack, aTech Media, and everyone who helped make this tremendous milestone possible.*


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





 





 
















 






