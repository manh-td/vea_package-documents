


Stripe Tax Integration (Beta)










































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


[Stripe Tax](https://stripe.com/tax) is a paid add-on for Stripe that helps you automatically calculate and collect the correct amount of tax when your subscribers checkout, and access the reporting you need to file returns.

🏦Pricing information for Stripe Tax can be found [here](https://support.stripe.com/questions/understanding-stripe-tax-pricing).

Getting Started
---------------

In order to use the Stripe Tax integration, Stripe Tax must first be enabled and setup from within your Stripe Dashboard, prior to the *beta* being turned on in Ghost.

### Step 1: Enable Stripe Tax

Navigate to the **Tax** section of the Stripe Dashboard, and click “**Get started →**”

![](https://ghost.org/help/content/images/2024/09/stripe-tax-enable-integration.png)
### Step 2: Select a preset product tax code

Once you’ve entered the setup screen, you’ll be prompted to review your product tax code category.

![](https://ghost.org/help/content/images/2024/09/stripe-tax-category-ghost.png)

If you don’t see this prompt, you can also set your category by clicking the three dots ... and selecting settings.

From here, you can choose the product tax code that makes the most sense for your business. The default will always be set to “General - Electronically Supplied Services.”

![](https://ghost.org/help/content/images/2024/09/stripe-tax-code-ghost.png)⚠️If you’re not sure what to choose, we recommend consulting a tax professional.
### Step 3: Add a registration

If you’ve exceeded a threshold in a certain state, province, or country, you’ll need to [register with the local tax authority](https://docs.stripe.com/tax/registering) prior to adding your registration to Stripe.

**How do I know where to register?**  
If you’re setting this up, you may already know one or two places where this will be required, but figuring out the rest isn’t always easy. Stripe helps you identify the correct places based on your past transactions with their Thresholds tool:

![](https://ghost.org/help/content/images/2024/09/CleanShot-2024-09-17-at-12.59.32@2x.png)

Once done, you can add your registration(s) to Stripe from the Tax dashboard:

![](https://ghost.org/help/content/images/2024/09/stripe-tax-registrations-ghost.png)
### Step 4: Contact Ghost to turn on the integration

For **Ghost(Pro)** customers, once everything is setup within your Stripe account, contact `support@ghost.org` and our team will manually enable the integration on your account.

#### I’m a developer, self-hosting my own Ghost instance. How can I try out the beta?

Once the above setup steps have been taken to enable the Stripe Tax add-on in Stripe, those self-hosting Ghost can enable the beta integration in their config.production.json file by adding "stripeAutomaticTax": true in the labs object:

```
{
    ...
    "labs": {
        "stripeAutomaticTax": true
    }
}
```
### How do I know it’s working?

Once enabled, members going through Stripe Checkout will see an additional field to enter their address. If they live in a location in which you’re registered to collect tax, it will be automatically calculated at the appropriate rate for any active tier in Ghost:

![](https://ghost.org/help/content/images/2024/09/CleanShot-2024-09-16-at-16.43.51@2x.png)
### Reporting

Once the integration is up and running, you’ll be able to access reporting for each of your registered jurisdictions directly inside Stripe in the Tax section of the dashboard.

![](https://ghost.org/help/content/images/2024/09/CleanShot-2024-09-17-at-13.06.30@2x.png)

---

Stripe Tax FAQ
--------------

#### Does Stripe remit my taxes for me?


No, Stripe does not remit your taxes for you. You can learn more about filing and remitting when using Stripe Tax [here](https://docs.stripe.com/tax/filing).


#### Will my existing paid members, created prior to Stripe Tax being turned on, also now have taxes applied to their accounts?


No, only newly created paid members will have the tax rate applied to their subscription.





### Related articles

 
Enabling Tips & Donations in Ghost gives your readers an



 

 
When creating tipjars or payment links in Ghost, you are



 

Was this article helpful?
-------------------------








 





