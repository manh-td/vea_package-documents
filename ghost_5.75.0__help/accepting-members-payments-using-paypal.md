


Accepting member's payments using PayPal










































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

[← Back to FAQ](/help/topic/faq/)

Embed payment buttons from PayPal directly into your content in Ghost and collect payments for your membership content.

*Thisguide requires an active [Zapier](https://zapier.com/) account.*

---

If you’re using PayPal as a payment gateway, then you may want to integrate PayPal directly with your Ghost site. It’s possible to embed PayPal buttons on any Ghost site, and you can add new PayPal customers as [Members](https://help-old.ghost.io/members-introduction/) in Ghost to give them direct access to premium membership content.

This guide explains how to create and embed PayPal buttons on a Ghost site using [HTML embeds](https://help-old.ghost.io/using-the-editor/#adding-custom-html), and how to automatically add new customers as members of your Ghost site.

### 1. Create a PayPal business account

In order to create PayPal buttons, you’ll need an active [PayPal business account](https://www.paypal.com/bizsignup/#/checkAccount). You can either create one from scratch or convert an existing personal PayPal account to a business account.

### 2. Create a PayPal button

Navigate to the Seller Tools area of your PayPal dashboard and locate the [PayPal Buttons](https://www.paypal.com/us/smarthelp/article/how-do-i-add-a-paypal-payment-button-to-my-website-faq3629) option:

![](https://ghost.org/help/content/images/2023/05/paypal-button.png)

From here, you can decide whether to create a “Buy Now” button for one-off payments, or a “Subscribe” button for recurring subscriptions.

![](https://ghost.org/help/content/images/2023/05/paypal-buttons.png)

You can embed as many PayPal buttons as you like on your Ghost site, but it’s recommended to keep your pricing structure simple to avoid confusing potential customers. The most popular pricing configuration are two plans for monthly and yearly subscriptions.

In order to create this pricing structure, you’ll need to create two **[Subscribe](https://www.paypal.com/us/brc/article/setting-up-recurring-payments-for-business)** buttons in PayPal. The first step allows you to select a name, currency, amount and billing cycle for your Subscribe buttons:

![](https://ghost.org/help/content/images/2023/05/subscribe.png)

**Tip:** In the advanced settings area, you can optionally redirect people to a custom URL on your site when checkout is complete (such as your site’s homepage, or a custom welcome page), or if someone leaves before completing payment.

![](https://ghost.org/help/content/images/2023/05/advanced-settings.png)
### 3. Use the button embed code

Once you’ve created your button(s), use the embed code provided to add the buttons to your website:

![](https://ghost.org/help/content/images/2023/05/button-embed-code.png)

You can use this code anywhere on your Ghost site, by creating an HTML card in the editor:

![](https://ghost.org/help/content/images/2023/05/CleanShot-2023-05-10-at-10.21.20@2x.png)💡It’s also possible to use the PayPal embed code directly in Ghost theme files, which is useful if you’re creating a custom **`/subscribe/`** page within your theme.
### 4. Create a Zapier automation to add a new member when a payment is made

Connect your PayPal account using a [Zapier](https://ghost.org/integrations/zapier/) automation to give your customers automatic access to member-only content on your site.

Zapier automatically creates new Members in Ghost each time someone makes a successful sale from your PayPal buttons:

### 5. Create a Zapier automation tounsubscribe members when PayPal subscriptions are canceled

It is **highly recommended** that you use this automation to ensure you keep everything in sync. When a customer cancels a PayPal subscription, this zap will automatically:

1. Unsubscribe them from receiving emails in Ghost
2. Remove them from a complimentary plan so they can't access premium content
3. Add a label of "PayPal Cancelled" so you can segment them in the Ghost dashboard

### 6. Disable free member signup

The final step is to turn off **Allow free member signup** in your Members settings inside Ghost:

![](https://ghost.org/help/content/images/2023/05/subscription-access-5.png)

This means you can use the **Members only** content access level to publish premium content, that only your paying Members who subscribed via PayPal will be able to access.



### Related articles

 
Ghost has built-in tools to migrate content and subscribers from



 

 
You can easily migrate your posts and pages from WordPress to Ghost using the WordPress migrator tool.



 

Was this article helpful?
-------------------------








 





