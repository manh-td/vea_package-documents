


Comments for Ghost










































Today we're introducing native commenting in Ghost, so you can invite your members to participate in community discussions directly on your publication.

After [Search](https://ghost.org/changelog/search/), this was one of our most requested features of-all-time, so as well as giving you a first look at the feature, we've included a longer behind the scenes section at the end of this post about how (and why!) this was made.

0:00/

Any Ghost publication with comments enabled displays a commenting area at the bottom of each post, where members are prompted to start or join the conversation by subscribing or signing in.

![](https://ghost.org/changelog/content/images/2022/08/start-conversation-1.png)

Members who are creating their first comment will be asked to fill out their name and expertise, to add more context and depth to each contribution.

![Add expertise to Ghost comment profile](https://ghost.org/changelog/content/images/2023/02/CleanShot-2023-02-08-at-16.36.01.png)

Members can reply to comments, like comments, and edit or delete their own comments. To help increase engagement, there are also built-in email notifications every time someone replies to a members comment, which can be toggled on or off from the member profile page in Portal 🔥

Authors also receive email notifications when conversations are happening on posts they have published.

![](https://ghost.org/changelog/content/images/2022/08/comments-in-ghost-1.png)

---

### Community moderation

We built Ghost Comments with features to help you keep your community healthy.

* **On-page moderations tools** — Staff users with the owner or administrator role can moderate comments right from the comment thread.
* **Comment reporting** — Site owners are emailed when any comment is reported by another member.
* **Member-only comments** — Comments can only be created by logged-in members, which helps protect you from spam and negativity.

Before introducing comments on your publication, it's a good idea to put together some community guidelines for your members. We've put together a short guide and template that you can steal and modify:

[Community guidelines — fostering valuable contributionsLaunching a community around your creative work? Get a head start with this adaptable Community Guidelines template & promote valuable contributions.![](https://ghost.org/resources/content/images/size/w256h256/2021/10/ghost-orb-pink-transparent-01-1.png)Ghost NewsletterKym Ellis![](https://images.unsplash.com/photo-1577563908411-5077b6dc7624?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDF8fGRpc2N1c3Npb258ZW58MHx8fHwxNjYwMTY1NDUx&ixlib=rb-1.2.1&q=80&w=2000)](https://ghost.org/resources/community-guidelines-template/?ref=ghost.org)

---

### Get started with comments

💬[**Ghost(Pro)**](https://ghost.org/pricing/?ref=ghost.org) users can log in and start enjoying all of this right away! If you're a developer, self-hosting Ghost, you'll need to [upgrade](https://ghost.org/docs/update/?ref=ghost.org) to the latest version to get access to everything that's new.

Comments are already integrated into all official themes (you'll need to [update](https://ghost.org/help/update-official-theme/?ref=ghost.org) to the latest version of your theme). Then, all you need to do is [turn commenting on](https://ghost.org/help/commenting?ref=ghost.org) from the `Settings → Membership` page in Ghost Admin.  
  
If you're using a premium or custom theme, comments can be added to the `post.hbs` template using the new `{{comments}}` Handlebars helper — read more in the [theme docs](https://ghost.org/docs/themes/helpers/comments/?ref=ghost.org).

Read more about free trial signup strategies:

[How to grow a creator business with free trial signupsFind out how to approach a free trial acquisition model for your independent publishing business, including how to implement a free trial.![](https://ghost.org/resources/content/images/size/w256h256/2021/10/ghost-orb-pink-transparent-01-1.png)Ghost NewsletterKym Ellis![](https://images.unsplash.com/photo-1541701494587-cb58502866ab?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDl8fGFic3RyYWN0fGVufDB8fHx8MTY2MTM1NjM0NQ&ixlib=rb-1.2.1&q=80&w=2000)](https://ghost.org/resources/free-trials-for-publishers/?ref=ghost.org)

---

Behind the scenes: Building comments
------------------------------------

For those of you that have been using Ghost for a while, and can remember all the way back to 2012, [the very first blog post about Ghost](https://john.onolan.org/ghost/?ref=ghost.org) touted "no comments!" as a key product decision. Even in the years since then, we've been pretty consistent about saying "no" when people requested it.

So, what changed? Two big things.

**First** — As Ghost has evolved over the last few years to handle memberships, premium subscriptions and email newsletters, *community* has become a much more important aspects of what creators and publishers are looking for in a platform.

Today, there are a huge number of Ghost sites popping up around all sorts of different niches, but one thing they all have in common is communities of highly engaged audiences with similar interests. This is a very different perspective to the traditional "random stranger on the internet comments on blog post" model of the past.

**Second** — The biggest problem with building comments, historically, has been automated spam. It was the #1 reason that comments was excluded from the original idea of Ghost, because forms on the internet fundamentally get abused by spammers and it takes a Goliath amount of time and energy to (largely unsuccessfully) prevent it. There are entire companies devoted to trying to prevent comment spam.

Fortunately, we're now able to get around this problem entirely thanks to member authentication that already exists in Ghost. The feature is not exposed publicly to strangers (and bots) on the internet, it can only be used by registered, verified members of a Ghost site.

Based on these two things we changed our mind about the idea of building comments, and decided to take a swing at building something beautiful and minimal for all Ghost publishers.

The first versions of both Search and Comments were built in the space of 5 days by two product teams when we all got together for a team retreat last month (our first since 2019). But... that's not quite the whole story.

It actually took us many (many) cycles of building APIs, UI components, membership authentication, and email subscriptions to get all the pieces in place that *allowed* us to take only 5 days at the end to put together these two features.

10 years to overnight success and all that.

As with Search, we're very aware of the fact that a simple/minimal approach we've taken with Comments won't be enough for every type of publisher — so we've built it with extensibility in mind.

The new `{{comments}}` helper provides an ideal hook for external integrations to embed their own code, and we're working towards making it possible to completely replace Ghost comments with powerful 3rd party systems like [Cove](https://cove.chat/?ref=ghost.org) or [Discourse](https://www.discourse.org/?ref=ghost.org).

---

For now, though, we're looking forward to seeing how you use comments within all your respective communities! More updates on the way. 💬

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





 





 
















 






