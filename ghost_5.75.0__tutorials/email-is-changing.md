





💌 Build with Ghost: Email is changing in a big way









































---


Welcome to #13. In this month's issue:

* How new email requirements affect Ghost
* Portfolio inspiration, CSS tricks, and Copilot cheat codes
* Casey Newtown's *Platformer* moves to Ghost

🏋️****Pro tip:****In a recent Forum thread, users and staff shared their favorite features in Ghost like snippets, sidebar views, and more. [See how you can use these features in your workflow.](https://forum.ghost.org/t/community-question-of-the-week-5-whats-your-fave-feature/44339/?ref=ghost.org)

New email requirements affect Ghost
-----------------------------------

Email has been around since the 1970s, but a lot has changed since the days of disco 🪩

In February 2024, [Google](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/?ref=ghost.org) and [Yahoo](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam?ref=ghost.org) are introducing new requirements that make email more secure and less spammy. These requirements fall under three categories:

1. Authentication: Reliably know the source of your email
2. Unsubscription: Stop getting unwanted emails easily
3. Spam: Higher thresholds mean less spam in your inbox

We encourage you to check out the links above to learn more about these requirements, but we're going to focus here on what they mean for Ghost. ([A version of this info is also available on our official Forum.](https://forum.ghost.org/t/new-email-requirements-in-2024-what-you-need-to-know/44572?ref=ghost.org))

💡Ghost(Pro) has already implemented changes to comply with these requirements. See our [help docs](https://ghost.org/help/custom-sending-domains/?ref=ghost.org) or reach out to support to learn more.
### Who's affected by these requirements?

By and large, these new requirements apply to Ghost publications that send newsletters to **at least 5,000 recipients per day**. If your publication falls under this threshold, these requirements don’t apply to you.

### What do Ghost sites need to do?

The good news is that many Ghost sites are likely already compliant and don’t need to do anything 🙂

* **Update Ghost to the**[**latest version**](https://github.com/TryGhost/Ghost/releases?ref=ghost.org)**.** In recent releases, we’ve updated Ghost to comply with these new requirements, including the ability for members to easily unsubscribe and better support for custom-sending domains.
* Configure **DMARC records** for email domains and confirm SPF and DKIM records are configured correctly. These records are set via your DNS, not via Ghost.

### Will this affect my deliverability?

Google and Yahoo’s new requirements are significant. These changes are being gradually rolled out and may initially encounter some speed bumps. With that in mind, **we expect to see volatility in deliverability rates across the entire email industry for the next few months**.

In the long run, though, this will be a big win for reputable newsletters with less cluttered inboxes, a better experience for readers, and more security for senders.

### Where can I learn more?

* Our [mail config docs](https://ghost.org/docs/config?ref=ghost.org#mail) have been updated to better explain how sending email addresses work in Ghost.
* Understand DMARC better with [dmarcian’s guide](https://dmarcian.com/why-dmarc/?ref=ghost.org).
* [Google’s full list of requirements](https://support.google.com/a/answer/81126?ref=ghost.org).
* [Yahoo’s full list of requirements](https://senders.yahooinc.com/best-practices/?ref=ghost.org).

These new requirements promise a better email experience that’s more secure and less spammy 💌

However, dealing with these requirements is complex. Visit the [Ghost Forum](https://forum.ghost.org/?ref=ghost.org) with questions or if you're seeking additional guidance.

Ideas and tools 🛠️
------------------

* Modern CSS is incredible, and these [5 CSS snippets](https://web.dev/articles/5-css-snippets-every-front-end-developer-should-know-in-2024?ref=ghost.org) have the power to change how you style your next theme.
* Building a portfolio? Check out [60 of the best designs from 2023](https://muz.li/blog/60-most-creative-portfolio-websites-of-2023?ref=ghost.org).
* GitHub shares [10 unexpected ways to use Copilot](https://github.blog/2024-01-22-10-unexpected-ways-to-use-github-copilot/?ref=ghost.org), the AI code assistant.
* We've mentioned it before but the `dialog` element makes creating modals a breeze. Check out this [guide to using the element](https://www.nickyt.co/blog/the-native-browser-dialog-element-1nhn/?ref=ghost.org).
* The default styling for tables leaves a lot to be desired. [Make your tables look beautiful with this guide by Mads Stoumann](https://dev.to/madsstoumann/a-guide-to-styling-tables-28d2?ref=ghost.org).

Platformer, now on Ghost
------------------------

Casey Newton's [*Platformer*](https://www.platformer.news/?ref=ghost.org)recently migrated from Substack to Ghost. [Read about why they made the switch](https://www.platformer.news/why-platformer-is-leaving-substack/?ref=ghost.org).

![Platformer homepage, showing stories on Facebook, Meta AI, Apple Vision, and more](https://ghost.org/tutorials/content/images/2024/02/platformer.png)

Platformer publishes on social networks and their relationship with the world. They take on questions about the political, social, and technological impacts of these platforms.

If you ever wondered whether "[the Taylor Swift deepfakes are a warning](https://www.platformer.news/taylor-swift-deepfake-nudes-x/?ref=ghost.org)," whether "[platforms killed Pitchfork](https://www.platformer.news/why-pitchfork-died/?ref=ghost.org)," or whether "[Facebook helps predators find each other](https://www.platformer.news/how-facebook-helps-predators-find/?ref=ghost.org)," then you, like 140,000 others, will likely find the Platformer fascinating.

![Platformer article on Taylor Swift deepfakes](https://ghost.org/tutorials/content/images/2024/02/swifty.png)

---

Sites featured in the Build with Ghost newsletter are discovered through our creator network, [Ghost Explore](https://ghost.org/explore/?ref=ghost.org). It’s a way for creators and readers alike to discover their favorite new publications. Anyone running a Ghost site can add themselves to Explore to be featured throughout the wider Ghost ecosystem. If you’d like to be featured in this newsletter, add your site to Explore and reply to this email.

[![](https://ghost.org/tutorials/content/images/2023/04/image-1.png)](https://ghost.org/explore/?ref=ghost.org)

Thanks for building with us.
============================

Have an idea for a Ghost tutorial? Reply to this email and let us know ❤️

Looking for other creators and developers working with Ghost? Join the [official Ghost Forum](https://forum.ghost.org/?ref=ghost.org), where we talk about all things Ghost!

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### ✅ Remind me to change this title

5 min read](/tutorials/tk/)

[### 🎁 Build with Ghost: Wrapped 2023

2 min read](/tutorials/build-with-ghost-wrapped-2023/)

[### 📝 Build with Ghost: Documentation incoming

4 min read](/tutorials/build-with-ghost-documentation-incoming/)

[### ➕ Build with Ghost: Recommendations for the open web

5 min read](/tutorials/we-recommend-this-newsletter/)

[### ⦿ Build with Ghost: Meet our new official theme

6 min read](/tutorials/build-with-ghost-meet-our-new-official-theme/)

[### 👩‍🎨 Build with Ghost: The art of the post template

5 min read](/tutorials/post-time/)

[### 🥯 Build with Ghost: A partial guide to everything

5 min read](/tutorials/partial-guide/)

[### 🧠 Build with Ghost: Do you know these essential concepts?

4 min read](/tutorials/3-things/)

[### 🏗️ Build with Ghost: First steps for creating a custom theme

5 min read](/tutorials/build-with-ghost-the-first-for-creating-a-custom-theme/)

[### 💻 Build with Ghost: Themes made easy

5 min read](/tutorials/themes-made-easy/)

[### 📖 4 ways to build a read-next section in Ghost

4 min read](/tutorials/how-to-build-a-read-more-section/)

[### 🐛 How to debug your Ghost theme once and for all

3 min read](/tutorials/how-to-debug-your-ghost-theme/)

[### 🏎️ Build Ghost themes more quickly with our new VS Code extension

5 min read](/tutorials/build-ghost-themes-more-quickly-with-our-new-vs-code-extension/)







Be the first to know.
---------------------

Join the Ghost developer community — sign up to get early access to the latest features, developer tools, and tutorials.



No spam. Once a month. Unsubscribe any time.
[![](https://ghost.org/tutorials/assets/img/most-helpful.jpg?v=235936095d)

Most helpful
------------

Essential tutorials to get you started](https://ghost.org/tutorials/most-helpful/)
[![](https://ghost.org/tutorials/assets/img/fundamentals.jpg?v=235936095d)

Funda­mentals
-------------

The basics of Ghost theme development](https://ghost.org/tutorials/fundamentals/)
[![](https://ghost.org/tutorials/assets/img/level-up.jpg?v=235936095d)

Level up
--------

Next-level development techniques](https://ghost.org/tutorials/level-up/)
[![](https://ghost.org/tutorials/assets/img/do-more.jpg?v=235936095d)

Do more
-------

Ideas & inspiration for whatever comes next](https://ghost.org/tutorials/do-more/)









