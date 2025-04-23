


How to use Apple Pay with Ghost










































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


Apple Pay is a contactless payment option supported by Stripe. This payment method offers your customers a seamless payment option using a card they’ve already attached to their Apple Wallet.

There is no difference in Stripe payment fees when using Apple Pay. To add support for this payment option on Ghost(Pro) it does require enabling the [Additional payment methods *beta*](https://ghost.org/help/payment-methods/) feature, from the **Settings → Advanced → Labs** area within Ghost Admin.

Enable Apple Pay
----------------

Apple Pay can be configured from the Wallets section, within the [**Settings** → **Payment Methods**](https://dashboard.stripe.com/settings/payment_methods) area of your Stripe account.

![](https://ghost.org/help/content/images/2022/09/enable-apple-pay.png)

To configure Apple Pay, expand the option from the **Wallets** area, and click **Configure domains**.

![](https://ghost.org/help/content/images/2024/12/apply-pay-configure-domain.png)

In your Apple Pay configuration settings, click **Add a new domain**:

![](https://ghost.org/help/content/images/2024/12/add-new-domain.png)

Enter in your domain and click **Save**.

Once your domain has been entered, you should see this added to your list of domains, and that it has been verified.

When Apple Pay is configured, an Apple Pay badge appears if Stripe checkout detects the customer's device and the region that supports Apple Pay.

![](https://ghost.org/help/content/images/2022/09/apple-pay.png)
### You’re all set!

With Apple Pay fully configured, you can allow Stripe’s checkout to do the rest and offer the payment method to your customers when available. If you’d like to test this out, try going through your payment flow in a private window on a device where you have Apple Pay setup.



[Next up
 →](/help/apple-pay/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





