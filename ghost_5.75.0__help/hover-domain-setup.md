


Hover domain setup










































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

To make your publication easy to identify you can use a custom domain name with your Ghost(Pro) site.

You can connect any domain or subdomain that you own to your Ghost(Pro) publication by adding a CNAME record to your domain’s DNS records. SSL certificates are automatically provided (and renewed each year).

Regardless of how a user enters your publication's URL in their browser, they'll always be directed to the correct site.

If you own a Hover domain, the following steps explain how you can implement a custom domain with your Ghost(Pro) publication.

Step 1: Access Domain DNS Settings
----------------------------------

Login to your [Hover](https://www.hover.com/signin) account, and access your domains.

Click "Edit" next to the domain you want to configure, and select "Edit DNS" to access the domains' DNS records.

![Edit DNS Records](https://ghost.org/help/content/images/2018/10/hover-edit-dns-records.png)

Step 2: Create a CNAME Record
-----------------------------

Next, you need to create a CNAME record within your domain's DNS settings.

From the domain's DNS settings, click the "Add A Record" button and select `CNAME` as the record type:

 Subdomain DNS Configuration | | | || Record Type | Host | Value |
| `CNAME` | `www` | `[subdomain].ghost.io` |
| `A` | `@` | `178.128.137.126` |

**Note:** The `A` record will automatically redirect both the `http` and `https` root domain to the subdomain you configure.

**Root domain configuration**  
Hover **does not support `CNAME` root domain configurations** and using an `A` record to achieve a root domain is not supported. To setup a root domain configuration, we recommend that you consider using [Cloudflare](https://ghost.org/help/cloudflare-domain-setup/) for additional flexibility.

Step 3: Activate the Custom Domain
----------------------------------

Login to your publication's Ghost Admin area, and go to the **Ghost(Pro) > Domain** settings.

Click **Setup**, and enter your custom domain into the custom domain field, then click **Activate**, to activate your custom domain.



### Related articles

 
Learn how to setup a custom domain with Ghost(Pro) and Squarespace



 

 
Passwords can be changed from within a staff user profile, or reset directly from the Ghost Admin login area.



 

Was this article helpful?
-------------------------








 





