


Adding a custom domain










































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

If you would like to make your site memorable and easy to find with a branded custom domain, then you can map any domain you own directly to your Ghost(Pro) publication. This is done by adding **CNAME** and **A** records within your domain's DNS settings.

Regardless of how a user enters your publication's URL in their browser, they'll always be directed to the correct site.

All Ghost(Pro) sites will automatically be provided with an SSL certificate by default, which simplifies the process and ensures you site is secure.

Popular DNS providers
---------------------

Use the following guides if you are using any of these popular domain name providers:

* [GoDaddy](https://ghost.org/help/godaddy-domain-setup-guide)
* [Namecheap](https://ghost.org/help/namecheap-domain-setup)
* [Google](https://ghost.org/help/google-domain-setup)
* [Hover](https://ghost.org/help/hover-domain-setup)
* [Gandi](https://ghost.org/help/gandi-domain-setup)
* [Squarespace](https://ghost.org/help/squarespace-domain-setup/)

Advanced users may also wish to read more about domain setup via [Cloudflare](https://ghost.org/help/cloudflare-domain-setup).

Otherwise, follow the instructions below to setup a custom domain for your Ghost site.

Before you begin
----------------

Before configuring a custom domain with your publication, decide whether you want to use a subdomain or root domain as the default URL for your site.

**What is a Subdomain?**  
A subdomain is a subdivision of your domain name. For example, if you want to use Ghost(Pro) at [blog.ghost.org](https://ghost.org/blog/), “`blog`,” would be a subdomain of [ghost.org](https://ghost.org). The most common subdomain is “`www`” e.g. `www.ghost.org`.

**What is a Root Domain?**  
A root domain, also known as a “naked domain,” is a domain without a subdomain in front, e.g. `ghost.org` is a root domain. Root domains are assigned in DNS records using the “`@`” symbol, and are considered non-standard setups on Ghost(Pro), as root level CNAME records are only supported by *some* DNS providers, and may interfere with email.

If you'd prefer a root domain and are using a DNS provider that doesn't support this - we recommend routing your DNS through a service such as [Cloudflare](https://ghost.org/help/cloudflare-domain-setup/), which gives you more flexibility.

💡Ghost(Pro) does not support `.eth` domains, or custom domains which utilize special characters.

Step 1: Create a CNAME record
-----------------------------

### Recommended DNS Setup

For a quick and easy setup, we recommend using a **subdomain** (e.g. `www.domain.com`) with Ghost(Pro). To achieve this setup, create the following DNS records with your domain provider:

 Subdomain DNS Configuration | | | || Record Type | Host | Value |
| `CNAME` | `www` | `[subdomain].ghost.io` |
| `A` | `@` | `178.128.137.126` |

The `CNAME` is required. The `A` record is optional - it creates a redirect from your root domain, to the `www` subdomain.

### Root Domain Setup

If you'd prefer to use a root domain (e.g. `domain.com`), create the following DNS records with your domain provider.

 Root Domain DNS Configuration | | | || Record Type | Host | Value |
| `CNAME` | `@` | `[subdomain].ghost.io` |
| `A` | `www` | `178.128.137.126` |

The `CNAME` is required. The `A` record is optional - it creates a redirect from your `www` subdomain to the root domain.

### Non-www Subdomain Setup

If you'd prefer to use an alternative subdomain (e.g. `blog.domain.com`), create the following `CNAME` record with your domain provider.

 Non-www Subdomain DNS Configuration | | | || Record Type | Host | Value |
| `CNAME` | `blog` | `[subdomain].ghost.io` |

Step 2: Activate the Custom Domain
----------------------------------

Login to your publication's Ghost Admin area, and go to the **Ghost(Pro) > Domain** settings.

Click the “Setup” button, enter your custom domain into the custom domain field, and click activate, to activate your custom domain.



### Related articles

 
Learn how to setup a custom domain with Ghost(Pro) and Squarespace



 

 
Passwords can be changed from within a staff user profile, or reset directly from the Ghost Admin login area.



 

Was this article helpful?
-------------------------








 





