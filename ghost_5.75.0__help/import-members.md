


Import members










































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


Ghost allows you to import your existing audience in an easy way so that they can access content on your new membership website. You can export any external list of supporters, email subscribers or patrons to make sure your audience can access your content on your Ghost site.

### Gather your subscribers list

If you're using an external platform such as [Mailchimp](https://mailchimp.com/help/view-export-contacts/?ref=ghost.org#View_or_export_an_audience), [Substack](https://support.substack.com/hc/en-us/articles/6314498343700-How-do-I-export-my-email-list-on-Substack), or [Patreon](https://www.patreon.com/portal/how-to/export-pledge-data?ref=ghost.org), you'll want to start by exporting your current subscribers or members using the tutorials provided.

### Prepare your CSV file

We've created a [**downloadable template**](https://static.ghost.org/v3.0.0/files/member-import-template.csv?ref=ghost.org) to help you get started. Ensure you clean your data before importing it into Ghost.

Imports should be in a CSV format and support the following fields:

* `email` - email addresses [required]
* `name` - full names
* `note` - member notes
* `subscribed_to_emails` - [true/false] identify which members will receive email newsletters
* `stripe_customer_id` - unique Stripe customer ID to import existing paid subscribers.
* `complimentary_plan` - [true/false] import members who have a free subscription
* `labels` - Labels need to be in quotes and comma separated e.g. `"label 1, label 2"`
* `created_at` - Date format ISO 8601: `2019-10-30T14:52:08.000Z`

The `stripe_customer_id` field can either be a Stripe customer ID (like `cus_GdsYH4fZbHx9hF`) or `auto`. If set to `auto`, Ghost will search the connected Stripe account for a customer with the given email address.

The `email` field is a required field - all other fields are optional.

![](https://ghost.org/help/content/images/2020/12/member-import-example.png)

Multiple newsletters
--------------------

Importing members when you have multiple newsletters works as follows:

**Importing new members**

* `subscribed_to_emails=true` → members will be opted in to all newsletters that have "Subscribe new members on signup" turned on.
* `subscribed_to_emails=false` → members are unsubscribed from all newsletters upon import.

**Importing existing members**

* `subscribed_to_emails=true` → email subscription preferences will be left alone, **unless** they were previously unsubscribed from all.
* `subscribed_to_emails=false` → members are unsubscribed from all newsletters.

Import your CSV file
--------------------

1. Navigate to the **Members** area in Ghost admin

2. Click the **Settings** icon at the top-right of the screen and select **Import members**

3. Upload your CSV file and make any further required changes before clicking **Import members**

![](https://ghost.org/help/content/images/2022/05/CleanShot-2022-05-23-at-11.28.02.gif)

Integrations
------------

It's also possible to automate keeping your members list up to date using our [Zapier integration](https://ghost.org/integrations/zapier/?ref=ghost.org) to automatically send new subscribers that have been added to other apps directly into Ghost, or vice versa.



[Next up
 →](/help/import-members/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





