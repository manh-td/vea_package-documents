


Namecheap domain setup










































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

Perhaps the single best thing you can do for any publication is to give it an identity with a custom domain name.

It’s possible to connect any domain or subdomain that you own to your Ghost(Pro) publication by adding a CNAME record to your domain’s DNS records. SSL certificates are automatically created (and renewed each year) for you.

Regardless of how a user enters your publication's URL in their browser, they'll always be directed to the correct site.

If you own a Namecheap domain, the following steps explain how you can implement a custom domain with your Ghost(Pro) publication.

Before you begin
----------------

Before configuring a custom domain with your publication, decide whether you want to use a subdomain or root domain as the default URL for your site.

**What is a Subdomain?**A subdomain is a subdivision of your domain name. For example, if you want to use Ghost(Pro) at blog.ghost.org, “`blog`,” would be a subdomain of [ghost.org](https://ghost.org/). The most common subdomain is “`www`” e.g. `www.ghost.org`.

**What is a Root Domain?**A root domain, also known as a “naked domain,” is a domain without a subdomain in front, e.g. `ghost.org` is a root domain. Root domains are assigned in DNS records using the “`@`” symbol, and are supported on Namecheap, however they are considered non-standard because they can interfere with email configuration and require an ALIAS instead of a CNAME.

Step 1: Access Domain DNS Settings
----------------------------------

The first step in setting up your custom domain is to login to your Namecheap account and access your DNS records. To do this, you'll need to click on your **Domain List**, then click **Manage** next to the domain you want to configure.

![](https://ghost.org/help/content/images/2020/05/namecheap-manage-dns.png)

Step 2: Create DNS Records
--------------------------

### Subdomain Setup

To achieve a subdomain setup for your publication (e.g. `www.domain.com`), create the following DNS records within your domain DNS settings:

 Subdomain DNS Configuration | | | || Record Type | Host | Value |
| `CNAME` | `www` | `[subdomain].ghost.io` |
| `A` | `@` | `178.128.137.126` |

**Note:** The `A` record will automatically redirect the root domain (e.g. the non-www domain) to the subdomain you configure.

### Root Domain Setup

To achieve a root domain setup for your publication (e.g. `domain.com`), create the following DNS records below within your domain DNS settings. If you have other records configured at the root of your domain, such as `MX` records, use an `ALIAS` record as opposed to a `CNAME`:

 Root Domain DNS Configuration | | | || Record Type | Host | Value |
| `CNAME` or `ALIAS` | `@` | `[subdomain].ghost.io` |
| `A` | `www` | `178.128.137.126` |

**Note:** The `A` record will automatically redirect the subdomain (e.g. the www version of the domain) to the root domain you configure.

Step 3: Activate the Custom Domain
----------------------------------

Login to your publication's Ghost Admin area, and go to the **Ghost(Pro) > Domain** settings.

Click **Setup**, and enter your custom domain into the custom domain field, then click **Activate**, to activate your custom domain.



### Related articles

 
Learn how to setup a custom domain with Ghost(Pro) and Squarespace



 

 
Passwords can be changed from within a staff user profile, or reset directly from the Ghost Admin login area.



 

Was this article helpful?
-------------------------








 





