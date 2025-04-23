


Post analytics










































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


Post analytics in Ghost admin gives you easy access to track your audience’s engagement with the content you publish.

To help you get the most out of post analytics, here’s an overview of the data that Ghost collects and displays.

![](https://ghost.org/help/content/images/2022/10/Post-List-Screenshot.png)

The post list displays metrics that you can see at a quick glance, including:

* **Opens** — The number of members that opened your newsletter. The open rate, shown as a percentage, is the number of openers divided by the number that received the newsletter
* **Clicks** — a count of the number of unique members that clicked *any* link contained within your newsletter. The click rate, also shown as a percentage, is the number of members that clicked a link divided by the number that received the newsletter.

Both open and click analytics can be disabled in **Settings → Membership → Analytics** area of Ghost Admin.

Post analytics
--------------

Clicking the graph icon next to each post provides even more insight on member engagement and click data for the content you publish and send on your site.

![](https://ghost.org/help/content/images/2022/10/post-analytics.png)

These analytics provide an overview of how well each email newsletter has performed, how many member conversions each piece of content has driven, and the referral sources for those conversions.

### Engagement

The Engagement section of your stats gives you a high level overview of:

* **Emails sent** — The number of members who were sent your newsletter.
* **Emails opened** — The open rate percentage and number of opens.
* **Clicks** — The click percentage and number of clicks to links in your newsletter.
* **Feedback** — A breakdown of the feedback your members provided when reading your newsletter. Find out how to [enable audience feedback](https://ghost.org/help/audience-feedback/).
* **Conversions** — A list of members who signed up or started a paid subscription after reading the post and the source for each signup.

![](https://ghost.org/help/content/images/2022/10/post-analytics-conversions.png)

Conversions include new free and paid members who signed up from your post. You can also dig into which members signed up from each post or page by using filters on the members dashboard. Read more about [managing members](https://ghost.org/help/member-management/) in Ghost.

The source shows where each new member signup came from, giving you a better idea of how people are discovering your work online—or it’s also possible [to set your own custom source](https://ghost.org/help/custom-source/).

### Newsletter clicks

The Newsletter clicks section gives an overview of the links within your content that members are interacting with the most.

Each link within the newsletter appears in this section, alongside how many unique members have clicked on it. You can also [edit links in newsletters](https://ghost.org/help/how-to-update-links-in-email-newsletters/) after they've been sent if you need to make a correction.

💡Member clicks are only tracked once for each unique link. This means if a single member clicks on the same link multiple times, it will still only be recorded as one click.
### Exporting post analytics

Post analytics can be exported in CSV format, giving you the ability to analyze your data in the spreadsheet tool of your choice, and giving you deeper insight into how your content is performing on your site.

The CSV file contains the following metrics:

| Data | Description |
| --- | --- |
| ID | Each post's unique identifier in Ghost |
| Post title | The full title of each post |
| URL | The full URL of each post |
| Author | Comma separated for multiple authors |
| Status | Published, published and sent, email-only |
| Created date | The date the post was first created |
| Last updated date | The date the post was last updated |
| Published date | The date the post was published |
| Featured | True/false |
| Tags | Comma separated, including internal tags |
| Post access | Public, members-only, paid members-only, etc... |
| Email recipients | Free members, paid members, labels, etc... |
| Newsletter name | Shown if multiple newsletters are setup |
| Sends | How many people the post was delivered to |
| Opens | How many members opened the email |
| Clicks | How many members clicked the email |
| Free Signups | How many free signups the post generated |
| Paid conversions | How many paid subscriptions the post generated |
| Feedback: more like this | Available when using [audience feedback](https://ghost.org/changelog/audience-feedback/) |
| Feedback: less like this | Available when using [audience feedback](https://ghost.org/changelog/audience-feedback/) |

To export of your post metrics, go to the **Settings → Analytics** area of Ghost Admin, and click **Export** post analytics.

Turning off analytics features
------------------------------

All tracking features in Ghost, including newsletter opens, newsletter clicks, member sources and outbound link tagging can be turned off directly in your settings. Just go to **Settings** → **Membership →** **Analytics** to disable any feature.

![](https://ghost.org/help/content/images/2023/10/CleanShot-2023-10-17-at-11.57.51@2x.png)


[Next up
 →](/help/post-analytics/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





