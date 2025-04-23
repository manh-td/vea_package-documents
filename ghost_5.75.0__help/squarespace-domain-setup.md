


Squarespace domain setup










































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

[← Back to Ghost(Pro)](/help/topic/ghost-pro/)

Activating a custom domain with your Ghost(Pro) site helps establish your professional brand, and makes your site more memorable for readers.

You can connect a custom domain purchased from Squarespace to your Ghost(Pro) publication by creating DNS records within your Squarespace account. Once activated, an SSL certificate will be provisioned for your domain, and renewed each year automatically.

If you own a domain through Squarespace, the following steps below will help explain how you can map your domain to your Ghost(Pro) publication.

Step 1: Access Domain DNS Settings
----------------------------------

The first step to activating your custom domain with your site is to sign in to your [Squarespace](https://squarespace.com) account.

Once logged in click **Domains**, and select the domain you’d like to configure with your Ghost(Pro) site, then click **Edit DNS** from the domain dashboard to access your DNS records for the domain.

![](https://ghost.org/help/content/images/2024/03/squarespace-domain-setup.png)

Step 2: Create DNS Records
--------------------------

In the DNS Settings area of your Squarespace account, you'll want to make sure there aren't any **Squarespace defaults** set. If you don't intend to also host a site with Squarespace, then you will need to delete those first.

Once that's done, you can click on the **Add Record** button in the Custom Records area, to create a new DNS record.

![](https://ghost.org/help/content/images/2024/03/squarespace-edit-dns.png)

You will need to create the following two DNS Records:

| Subdomain DNS Configuration |  |  |  |
| --- | --- | --- | --- |
| Record Type | Host | Value |  |
| CNAME | www | [subdomain].ghost.io |  |
| A | @ | 178.128.137.126 |  |

**Note:** The `A` record will automatically redirect the `http` and `https` root domain to the subdomain you configure.

**Step 3: Activate the Custom Domain**
--------------------------------------

Login to your publication's Ghost Admin area, and go to the **Ghost(Pro) > Domain** settings.

Click **Setup**, and enter your custom domain into the custom domain field, then click **Activate**, to activate your custom domain.



### Related articles

 
Passwords can be changed from within a staff user profile, or reset directly from the Ghost Admin login area.



 

 
Ghost(Pro) is a managed service so you don't need to worry about data backups — but you can export your data anytime!



 

Was this article helpful?
-------------------------








 





