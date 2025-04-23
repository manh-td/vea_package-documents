


Additional payment methods (beta)









































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


By default Ghost supports payments from members via Credit Card, Apple Pay and Google Pay.

Enabling the Additional Payment Methods (beta) in **Ghost** → **Settings** → **Labs** will allow you to select more payment methods your members can use from within your Stripe Dashboard. You must enable the setting in Ghost first in order to use this feature.

💡This is a beta, which means we're still testing this feature. If you run into any issues using additional payment methods, please report them over on <https://forum.ghost.org>

Why set up additional payment methods
-------------------------------------

Different payment methods are popular in different parts of the world. In the US it's common to pay for things online with a credit card. In The Netherlands almost nobody uses credit cards, people there prefer iDEAL, a payment system that connects directly to their bank account. In China, AliPay and WeChat Pay are much more popular payment methods than any other.

Unsurprisingly, when a site supports the payment method their customers are most accustomed to and comfortable with, their conversion rates tend to be much higher.

If your audience is predominantly based in a specific region, you will likely want to make sure you support that region's most popular payment methods.

If your audience is international, you may want to consider supporting a wide range of payment methods to appeal to lots of different regions.

How to set up payment methods in Stripe
---------------------------------------

First, visit the **payment methods** settings in your Stripe dashboard, here:  
<https://dashboard.stripe.com/settings/payment_methods>

Ensure that you're editing settings for "Ghost" using this dropdown:

![](https://ghost.org/help/content/images/2024/07/CleanShot-2024-07-01-at-12.34.12@2x.png)

Scrolling down, you'll find payment methods compatible with Ghost can be enabled and will automatically start working on your site.

Payment methods which are not compatible with Ghost are marked as `Blocked`.

![](https://ghost.org/help/content/images/2024/07/CleanShot-2024-07-01-at-12.40.22@2x.png)

---

Payment method compatibility
----------------------------

Some quick notes on compatibility for payment methods in Ghost.

### Non-recurring payment methods

Ghost is *not* able to support payment methods that don't support recurring payments, such as **Bank Transfers**, **PayNow**, **Swish**, and **Crypto Currencies**.

### Recurring payment methods

When there is a "Recurring payments" setting (eg. iDEAL/Bancontact), you must enable it for these methods to work.

They will also only show up in a checkout session if the Tier being sold is in a compatible currency. Usually this is EUR, but you can click on each payment method in the Stripe Dashboard to discover which currencies it supports.

![](https://ghost.org/help/content/images/2024/06/CleanShot-2024-06-19-at-15.31.55.png)


### Related articles

 
Stripe Tax allows you to automatically calculate and collect tax when your subscribers checkout for paid membership.



 

 
Enabling Tips & Donations in Ghost gives your readers an



 

Was this article helpful?
-------------------------








 





