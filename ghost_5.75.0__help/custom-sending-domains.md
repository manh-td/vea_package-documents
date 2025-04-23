


Custom sending domains










































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

All Ghost(Pro) sites are configured to deliver newsletters in bulk using `ghost.io` as the verified sending domain, which is optimized for the best possible deliverability rates.

Ghost also includes support to optionally configure a custom sending domain for newsletters sent from your publication. This is useful for customizing the from-address of your emails to match your custom domain, or if your organization requires a DMARC policy to be configured with the domain activated on your Ghost(Pro) site.

💡Custom sending domains are only supported on the ****Creator**** plan or higher on Ghost(Pro).

How to setup a custom sending domain
------------------------------------

Go to the **Ghost(Pro) → Domain** area within Ghost Admin, and click **Setup**, in the Custom sending domain section.

![](https://ghost.org/help/content/images/2024/01/custom-sending-domain-setup.png)💡The option to configure a custom sending domain is only available if you have [setup a custom domain](https://ghost.org/help/using-custom-domains/) with your publication. 

Next, you will need to create a set of custom DNS records with your domain provider. You can copy these DNS records directly from within Ghost Admin, after clicking **Setup**:

![](https://ghost.org/help/content/images/2024/01/custom-sending-domain-dns-records.png)💡If you’re unsure of how to create the DNS records required to activate a custom sending domain, contact your domain provider for assistance.
### Using DMARC

**DMARC** (**D**omain-based **M**essage **A**uthentication, **R**eporting, and **C**onformance) is an open security protocol that helps protect your email domain from being used for things like email spoofing and phishing scams.

⚠️Setting up a DMARC policy record on your domain is required for using a custom sending domain on Ghost.

Your DMARC policy lets inbox providers know how to handle incoming messages that don’t verify against your domain, and can be set to three levels of strictness:

1. **None (p=none):** This policy signals that you have DMARC in place, but takes no action against emails that fail DMARC checks.
2. **Quarantine (p=quarantine):** Emails failing checks are placed in the recipients' spam or junk folder, providing a balance between security and email delivery.
3. **Reject (p=reject):** The strictest policy where emails that don’t pass the DMARC checks are rejected and not delivered at all.

To help get you started, we've provided an example of a DMARC policy record with the *least* strict settings directly in the setup process:

| **Record Type** | **Name** | **Value** |
| --- | --- | --- |
| `TXT` | `_dmarc.example` | `v=DMARC1; p=none;` |

When implementing DMARC, it’s generally recommended to start with the *least* strict policy first, in order to ensure your email deliverability stays high.

For those interested in learning more about DMARC or setting up a more advanced policy, we recommend the following resources:

* [Understanding DMARC](https://dmarcian.com/why-dmarc/)
* [Check your domain for an existing DMARC record](https://dmarcian.com/dmarc-inspector/)
* [Build a more advanced DMARC record](https://dmarcian.com/dmarc-record-wizard/)

### Finish setup

Once the required DNS records are in place, click **Activate.**

* A green checkmark indicates that your DNS records were successfully detected.
* A red exclamation mark indicates that we were unable to detect your DNS records. DNS propagation can take anywhere between 15 minutes to 24 hours to fully resolve.

When successfully configured, you will see custom sending domain appear in green, from the **Ghost(Pro) > Domains** area:

![](https://ghost.org/help/content/images/2024/01/custom-sending-domain-activated.png)
### Deliverability for new custom sending domains

Email deliverability is the term used to describe whether a newsletter ends up in your subscriber’s inbox, or their spam folder. Mailbox providers, such as Gmail and Yahoo, evaluate lots of different parameters to decide whether to allow your message into a recipient’s inbox, and one of the factors they look at is your sending domain.

Your sending domain’s reputation is built up over time as people engage with emails you send. If people open and reply to your emails, your reputation goes up. If they mark your emails as spam, your reputation goes down.

When you set up a new sending domain, you don’t have any reputation at all to start. This means that your first few emails from a new domain may have lower deliverability rates than normal until people start to engage positively with the emails you send.

So, if you’re setting up a *brand new* sending domain, don’t be surprised if your deliverability is lower at first while your reputation is being established. It should return to normal after you send your first few emails. Encouraging people to reply to those first few emails can also be a great way to get your sender reputation off to a strong start.



### Related articles

 
Learn how to setup a custom domain with Ghost(Pro) and Squarespace



 

 
Passwords can be changed from within a staff user profile, or reset directly from the Ghost Admin login area.



 

Was this article helpful?
-------------------------








 





