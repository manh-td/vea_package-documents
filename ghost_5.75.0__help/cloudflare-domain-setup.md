


Cloudflare domain setup










































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

Cloudflare is a DNS management service and content delivery network (CDN). Ghost(Pro) users commonly route their DNS through Cloudflare for its support of root-level CNAMEs and flexible redirects, known as page rules.

The following steps will walk you through how to set up a root domain or subdomain with your Ghost(Pro) publication, using Cloudflare to manage your domain's DNS records.

Regardless of how a user enters your publication's URL in their browser, they'll always be directed to the correct site.

Step 1: Connect Your Domain to Cloudflare
-----------------------------------------

The first step for both types of configuration is to create a [free Cloudflare account](https://dash.cloudflare.com/sign-up) and follow a few steps. There are paid options available but you only need a *free* account to set up a custom domain with Ghost.

Enter the domain name that you own, when creating your new Cloudflare account, and it will query your existing DNS records and port them over. Review these records and port any over that are required.

![](https://ghost.org/help/content/images/2023/03/add-site.png)

Update your Nameserver (NS) with your domain provider to the NS records that Cloudflare requests during the setup process.

💡If you're unsure where to update your domain's NS records, you may need to contact your domain provider directly.

When your Cloudflare Overview shows a status of "Active" you are ready to configure your domain's DNS to point to your Ghost(Pro) publication - this can take a few minutes.

Once active, to access your domain's DNS records in Cloudflare, click **DNS** from the admin menu on the left.

![](https://ghost.org/help/content/images/2023/03/access-DNS-records.png)

Step 2: Create a CNAME record
-----------------------------

Before configuring a custom domain with your publication, decide whether you want to use a subdomain or root domain as the default URL for your site.

**What is a Subdomain?**  
A subdomain is a subdivision of your domain name. For example, if you want to use Ghost(Pro) at blog.ghost.org, “`blog`,” would be a subdomain of [ghost.org](https://ghost.org/). The most common subdomain is “`www`” e.g. `www.ghost.org`.

**What is a Root Domain?**  
A root domain, also known as a “naked domain,” is a domain without a subdomain in front, e.g. `ghost.org` is a root domain.

Whether you use a root domain or subdomain with your publication is a matter of personal preference, however, there are different setup steps for each that must be followed.

### DNS Only

When using Cloudflare it is important to have all records you set for Ghost, to a Proxy status of **DNS only**.

![](https://ghost.org/help/content/images/2023/10/Proxy-status-DNS-only-Cloudflare.png)
### Subdomain Setup

To use a subdomain with your publication (e.g. `www.domain.com`) go to your DNS settings in Cloudflare and create the following DNS records:

 Subdomain DNS Configuration | | | || Record Type | Host | Value | Proxy status |
| `CNAME` | `www` | `[subdomain].ghost.io` | `DNS only` |
| `A` | `@` | `178.128.137.126` | `DNS only` |

### Root Domain Setup

If you'd prefer to use a root domain (e.g. `domain.com`), go to your DNS settings in Cloudflare and create the following DNS records:

 Root Domain DNS Configuration | | | || Record Type | Host | Value | Proxy status |
| `CNAME` | `@` | `[subdomain].ghost.io` | `DNS only` |
| `A` | `www` | `178.128.137.126` | `DNS only` |

Step 3: Activate the Custom Domain
----------------------------------

Log in to your publication's Ghost Admin area, and go to the **Ghost(Pro) > Domain** settings.

Click **Setup**, and enter your custom domain into the custom domain field, then click **Activate**, to activate your custom domain.



### Related articles

 
Learn how to setup a custom domain with Ghost(Pro) and Squarespace



 

 
Passwords can be changed from within a staff user profile, or reset directly from the Ghost Admin login area.



 

Was this article helpful?
-------------------------








 





