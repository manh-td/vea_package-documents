


Understanding the dashboard











































Search






 
[Help /](/help/) 
Ghost manual
Ghost(Pro)
FAQ

[Ghost manual](/help/manual/)
[Ghost(Pro)](/help/topic/ghost-pro/)
[FAQ](/help/topic/faq/)

 [Ghost manual](/help/manual/)
[Ghost(Pro)](/help/topic/ghost-pro/)
[FAQ](/help/topic/faq/)



##### Topics

### Getting started

* [Site setup](https://ghost.org/help/site-setup/)
* [Invite your team](https://ghost.org/help/managing-your-team/)
* [Importing content](https://ghost.org/help/imports/)
* [Site navigation](https://ghost.org/help/updating-navigation/)

### Publishing

* [Intro to the editor](https://ghost.org/help/using-the-editor)
* [Cards](https://ghost.org/help/cards)
* [Posts](https://ghost.org/help/posts/)
* [Pages](https://ghost.org/help/pages/)
* [Tags](https://ghost.org/help/tags)
* [Protected content](https://ghost.org/help/protected-content)
* [Snippets](https://ghost.org/help/snippets)
* [Post settings](https://ghost.org/help/post-settings)
* [Publishing and scheduling](https://ghost.org/help/publishing-content)
* [Organizing content](https://ghost.org/help/organizing-content)
* [Markdown guide](https://ghost.org/help/using-markdown)
* [Keyboard shortcuts](https://ghost.org/help/keyboard-shortcuts/)
* [Ghost Bookmarker](https://ghost.org/help/ghost-bookmarker/)

### Memberships

* [Setting up members](https://ghost.org/help/setup-members)
* [Customizing Portal](https://ghost.org/help/customize-portal)
* [Importing members](https://ghost.org/help/import-members)
* [Embeddable signup forms](https://ghost.org/help/embeddable-signup-forms/)
* [Welcome pages](https://ghost.org/help/welcome-pages)
* [Comments](https://ghost.org/help/commenting)
* [Member management](https://ghost.org/help/member-management)
* [Member impersonation](https://ghost.org/help/impersonate-members)
* [Recommendations](https://ghost.org/help/recommendations/)

### Payments

* [Connecting Stripe](https://ghost.org/help/stripe)
* [Creating paid tiers](https://ghost.org/help/tiers)
* [Tips & donations](https://ghost.org/help/tips-and-donations/)
* [Free trials](https://ghost.org/help/free-trials)
* [Complimentary plans](https://ghost.org/help/complimentary-plans)
* [Offers](https://ghost.org/help/offers)
* [Google Pay](https://ghost.org/help/google-pay)
* [Apple Pay](https://ghost.org/help/apple-pay)

### Newsletters

* [Setting up email newsletters](https://ghost.org/help/setup-email-newsletters)
* [Newsletter template settings](https://ghost.org/help/email-design)
* [Audience feedback](https://ghost.org/help/audience-feedback)
* [Delivering emails](https://ghost.org/help/delivering-emails)
* [Updating links in newsletters](https://ghost.org/help/updating-links)
* [Deliverability tips](https://ghost.org/help/deliverability-tips)

### Design

* [Design settings](https://ghost.org/help/design-settings)
* [Installing themes](https://ghost.org/help/installing-a-theme)
* [Site search](https://ghost.org/help/search)
* [Announcement bar](https://ghost.org/help/announcement-bar)
* [Adding styles with code injection](https://ghost.org/help/code-injection-styles)

### Advanced settings

* [History log](https://ghost.org/help/history)
* [Redirects](https://ghost.org/help/redirects)
* [Integrations](https://ghost.org/help/integrations)
* [Exports](https://ghost.org/help/exports)
* [SEO](https://ghost.org/help/seo)
* [Spam filters](https://ghost.org/help/signup-spam-protection/)

### Growth & analytics

* [The dashboard](https://ghost.org/help/dashboard)
* [Post analytics](https://ghost.org/help/post-analytics)
* [Creating custom sources](https://ghost.org/help/custom-sources)
* [Website analytics](https://ghost.org/help/website-analytics)

### Labs

* [Social web (beta)](https://ghost.org/help/social-web)


The dashboard in Ghost admin is a place to get member, revenue, engagement, and email stats at a glance, so you can see how your content and business are performing.

![screenshot of the Ghost dashboard](https://ghost.org/help/content/images/2022/05/dashboard.png)

To help you better understand the stats provided on your dashboard, here’s a breakdown of everything you need to know.

👉The dashboard is generated based on your publication — so you only see information that is relevant to you. For example, if you don’t have paid subscriptions you won’t see any MRR stats, and if you don’t use email newsletters, you won’t see any email stats.
### Member totals

At the top of the dashboard, you can see a breakdown of the types of members you have, split into three groups.

Here’s how each member segment is calculated:

* **Total members** includes all members of your site, free and paid.
* **Paid Members** includes all members on any paid or complimentary subscription. Canceled accounts are included until the end of the period paid for.
* **Free members** includes all members who do not have an active paid subscription, including members who have previously canceled and their billing period has ended.

Each of these metrics shows an increase or decrease compared to the previous period set in the top right corner, to help you see how each segment of your members list is growing.

![close up of member totals in Ghost dashboard, focus on time period selection](https://ghost.org/help/content/images/2022/05/time-period-select.png)

You can also see how these data trend over time, and adjust the graph to show total, paid, or free members.

![membership trend graph in Ghost dashboard](https://ghost.org/help/content/images/2022/05/graph-select.gif)
### MRR

Monthly Recurring Revenue (MRR) is a forward-looking metric that is calculated using the normalized amount of monthly recurring payments from all active subscriptions.

> **For example:** An annual subscription for $120 counts as +$10 MRR ($120 / 12 months). A monthly subscription for $19 counts as +$19 MRR.

* **Cancellations** are removed from MRR calculations at the time a member cancels their subscription, thereby canceling the recurring payment.
* **Subscriptions created with an offer** with a duration of “forever” have the discount removed for MRR calculations. Temporary discounts are not considered when calculating MRR.

![MRR graph in Ghost dashboard](https://ghost.org/help/content/images/2022/05/MRR-ghost-dash.png)

MRR is displayed as a figure, alongside a graph to show how MRR is trending over time. The percentage figure shows how your MRR has increased or decreased compared to the previous time period set on your dashboard.

### Paid subscribers

New and canceled paid subscriptions for the currently selected time period are shown as a bar chart.

### Paid mix

This shows the current ratio of paid subscriptions based on either **cadence** (annual or monthly) or **tiers**.

### Engagement

The engagement section of the dashboard measures the percentage of members that have interacted with your content, whether that is opening an email or browsing content on your site, in the past 7 and 30 days.

![engagement statistics in Ghost dashboard](https://ghost.org/help/content/images/2022/05/engagement-dash.png)

If you’re using paid memberships in Ghost, you can break engagement down further by total, free, and paid members.

### Sources

The top sources section will show you exactly what is driving audience growth from around the web. These stats are filterable by 7, 30, and 90 days, and show top sources for both free and paid signups.

![](https://ghost.org/help/content/images/2022/10/top-sources-widget.png)💡It’s possible to manually set the source that is recorded in Ghost for each signup — [read more](https://ghost.org/help/custom-sources/).
### Recent posts and member activity

The recent posts and member activity section shows you the latest stats including open rates for the most recent newsletters, and recent member activity.

![recent posts and member activity list in Ghost dashboard](https://ghost.org/help/content/images/2022/05/recent-posts-dash.png)

It also looks great in dark mode 🌶

![](https://ghost.org/help/content/images/2022/05/dashboard-darkmode.png)

---

### Further reading

[The metrics every successful publisher needs to knowHere’s what all of those confusing acronyms actually mean.![](https://ghost.org/resources/favicon.png)Ghost NewsletterDavid Ramos![](https://images.unsplash.com/photo-1551288049-bebda4e38f71?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDR8fGNoYXJ0fGVufDB8fHx8MTYyNjk5MTU0NA&ixlib=rb-1.2.1&q=80&w=2000)](https://ghost.org/resources/subscription-business-metrics/)


[Next up
 →](/help/dashboard/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





