




How to setup and manage your Stripe account








































Subscription-based businesses benefit from a revenue source that is predictable and sustainable, which is why so many online companies gravitate towards this model.

Most publishers who use subscription commerce to generate revenue from their content use Stripe to power their subscriptions and payments. To help your business run smoothly, we've provided some essential tips for managing your Stripe account effectively.

How Stripe subscriptions work
-----------------------------

Stripe is the leading online payment processing service for internet businesses. It allows companies of every size to accept payments and manage customer data.

When using Ghost to run a subscription-based business, you benefit from a native Stripe integration that allows you to connect your Ghost publication to your Stripe account in a few clicks.

[![](https://ghost.org/resources/content/images/2025/03/connecting-ghost-to-stripe.png)](https://ghost.org/help/stripe/?ref=ghost.org)

****Settings → Memberships → Tiers → Connect with Stripe****

Once Stripe is connected, you can create premium subscription prices directly inside Ghost Admin — these products and prices will be automatically added to your Stripe account.

[![](https://ghost.org/resources/content/images/2023/10/pricing-memberships-ghost-1.png)](https://ghost.org/help/tiers/?ref=ghost.org)

If you're unsure how to price your publication, ask yourself [these four questions](https://ghost.org/resources/pricing-subscription-newsletter/).

From here, you can configure Portal to display your subscription products on your website and invite your audience to support your work financially.

[![](https://ghost.org/resources/content/images/2023/10/portal-settings.png)](https://ghost.org/help/customize-portal/?ref=ghost.org)

****Settings**** → ****Membership**** → ****Portal settings**** → ****Customize****

This setup process makes starting a subscription revenue business accessible to all — whether you’re a solo creator, an indie publisher, or a small team.

Next, you’ll want to understand how to get the most out of your Stripe account so you can maneuver support requests, handle taxes, and understand your business metrics.

Fortunately, plenty of Stripe features and integrations can help you do this, and many are often missed or overlooked, so let’s dive in.

#1 Add branding to the checkout page
------------------------------------

By default, the Stripe checkout page — the page where visitors land when they choose to subscribe to your content — will have a default appearance:

![](https://ghost.org/resources/content/images/2022/02/branded-stripe-checkout.png)

However, you can update this checkout page to include your branding from your Stripe dashboard:

[![](https://ghost.org/resources/content/images/2022/02/stripe-branding.png)](https://dashboard.stripe.com/settings/branding?ref=ghost.org)

You can update your branding within Stripe [here](https://dashboard.stripe.com/settings/branding?ref=ghost.org).

This allows you to add an icon, logo, and accent colors to give your Stripe checkout page more personality.

![](https://ghost.org/resources/content/images/2022/02/browser-checkout-1.png)

Here's an example of a customized Stripe checkout page.

#2 Set up email receipts
------------------------

It’s best practice to deliver email receipts with an invoice to customers every time they make a payment. Thankfully, Stripe has a feature that handles this for you, and the automated emails use the brand settings you have already put in place from the previous tip. 🎉

To set this up, head to the [Billing page](https://dashboard.stripe.com/settings/billing/automatic?ref=ghost.org) and ensure that **Email finalized invoices to customers** is checked:

![](https://ghost.org/resources/content/images/2022/02/email-reciepts-stripe.png)

#3 Apply discounts
------------------

Knowing how to apply a discount to an existing customer’s subscription will help you manage several scenarios. For example, you may want to create short-term discounts for specific groups of customers or offer a discount as a gesture of goodwill in a support scenario.

First, create a coupon in the **Products** section:

![](https://ghost.org/resources/content/images/2022/02/create-coupon.png)

Next, find the customer to whom you’d like to apply a discount by searching for their email address. Open up their customer information in the dashboard and navigate to **Apply coupon** from the **Actions** menu:

![](https://ghost.org/resources/content/images/2025/03/apply-coupon.png)

Then, select the coupon you created from the menu and apply it. You can also use these same steps to revoke a coupon if necessary.

![](https://ghost.org/resources/content/images/2025/03/select-coupon-1.png)🎁If you’d like to run a special offer for new customers, you can use the [Offers feature](https://ghost.org/help/offers/?ref=ghost.org) in Ghost to create sharable discounts.

#4 Providing refunds
--------------------

Handling refunds in Stripe is a crucial admin task for support scenarios. To process a refund, locate the customer's profile from the Stripe dashboard. Under the **Payments** section, click the three dots to open the actions menu and select **Refund payment**.

![](https://ghost.org/resources/content/images/2025/03/refund-payment-1.png)

The refund screen asks for a reason for the refund, which can be useful for your records. Choose a reason if applicable and hit the **Refund** button.

![](https://ghost.org/resources/content/images/2025/03/refund-reason-1.png)

After you process the refund, be sure to let your customer know that it can take 5-10 business days to appear on their statement.

You can also have Stripe automatically deliver refund notification emails by updating your email settings:

[![](https://ghost.org/resources/content/images/2022/02/email-about-refunds.png)](https://dashboard.stripe.com/settings/emails?ref=ghost.org)

You can set up customer refund notification emails within Stripe [here](https://dashboard.stripe.com/settings/emails?ref=ghost.org).

#5 Connect ChartMogul
---------------------

While Stripe has its own [billing metrics feature](https://dashboard.stripe.com/billing?ref=ghost.org), you may want to consider additional tools that will help analyze your business performance.

A platform like ChartMogul can help you do this. Creating a ChartMogul account is **free** for users with less than $120K in MRR (monthly recurring revenue), so you can [get started immediately](https://chartmogul.com/pricing/?ref=ghost.org).

The ChartMogul dashboard offers a clean, visual way to monitor business performance over time:

![](https://ghost.org/resources/content/images/2022/02/chartmogul.webp)

Connect your Ghost publication with ChartMogul using [our dedicated integration](https://ghost.org/integrations/chartmogul/?ref=ghost.org).

Learn more about the business metrics that matter in this resource:

[The metrics every successful publisher needs to knowHere’s what all of those confusing acronyms actually mean.![](https://ghost.org/resources/favicon.png)Ghost NewsletterDavid Ramos![](https://images.unsplash.com/photo-1551288049-bebda4e38f71?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDR8fGNoYXJ0fGVufDB8fHx8MTYyNjk5MTU0NA&ixlib=rb-1.2.1&q=80&w=2000)](https://ghost.org/resources/subscription-business-metrics/)

#6 Keep your business finances in check
---------------------------------------

For an easier way to manage your finances, we recommend creating a brand new bank account for your business and connecting that bank account to Stripe.

Stripe has launched [some tax features](https://stripe.com/tax?ref=ghost.org), but they are not yet suitable for a no-code setup with external platforms. As always, the best course of action is to seek professional legal and accounting advice at your discretion.

#7 Minimize churn
-----------------

In subscription commerce, churn reveals the percentage of people who stop being customers, whether by unsubscribing or canceling their product.

However, not all customers churn because they made a conscious decision to leave. Many will churn **passively** for several reasons, including credit card expirations, failed payments, processor problems, or fraud protection.

Passive churn can make up a significant amount of your overall churn rate since your customers often don’t realize their subscription payments have failed. For this reason, subscription businesses opt to implement strategies to minimize this type of churn:

* Consider a dedicated dunning service, like **Churnbuster**, which [integrates directly](https://ghost.org/integrations/churnbuster/?ref=ghost.org) with your Stripe account.
* **Dunning** is the practice of business owners communicating with customers to remind them of payments due. Tools like [Churnbuster](https://churnbuster.io/?ref=ghost.org) help automate this process and create personalized emails for failed payments.
* Stripe has native features that define parameters for how you’d like to manage failed payments, like **Smart Retries** and automated emails for failed card payment methods, which you can find in the [Billing](https://dashboard.stripe.com/settings/billing/automatic?ref=ghost.org) section.

[![](https://ghost.org/resources/content/images/2022/02/manage-failed-payments.png)](https://dashboard.stripe.com/settings/billing/automatic?ref=ghost.org)

#8 Ensure you understand Stripe's policies
------------------------------------------

Consider reviewing Stripe's [tipping policy](https://support.stripe.com/questions/requirements-for-accepting-tips-or-donations?ref=ghost.org) and [prohibited and restricted business policy](https://stripe.com/en-de/legal/restricted-businesses?ref=ghost.org). Content and activities that violate these rules are against Stripe’s SSA.  Please familiarize yourself with their policies to ensure you do not accept tips or donations for anything prohibited or restricted.

**On this page**
[Introduction](#intro)




---





[###### — Read this next —

Customizing your Ghost site even further](/resources/custom-themes/)


Get trends & tips delivered to you.
-----------------------------------

A weekly roundup of emerging trends, products and ideas in the creator economy, trusted by **50,000+** readers.



No spam. No jibberjabber. Unsubscribe any time.
[Wow, @Ghost is killing it today with their newsletter. It may just be me, but it seems like more time and care is being spent every week on it. If you can show me a link about my obsession I didn’t know about yet — that’s something.

2:22 PM · 13 Jun 2021](https://twitter.com/cjchilvers/status/1404081746065428483)
[@Ghost has been my favorite company newsletter of 2022

6:21 PM · 4 Apr 2022](https://twitter.com/arsalagrey/status/1511114162729984001?s=20&t=EkPCkPBi5XTtcXo7nDft6w)
[Ok, the Ghost newsletter is hands down the best newsletter in my inbox and it is not even close. There's not a single other one that I am going back to read or look forward to getting. Excellent job!

6:09 PM · 17 Apr 2022](https://twitter.com/LajosNagyUK/status/1515633491492454401)


[![Create your brand: Launching a publication](https://ghost.org/resources/assets/img/building.jpg?v=04c180ed9e)](https://ghost.org/resources/building/)
[![Start publishing: Creating content that works](https://ghost.org/resources/assets/img/publishing.jpg?v=04c180ed9e)](https://ghost.org/resources/publishing/)
[![Grow an audience: Finding your true fans](https://ghost.org/resources/assets/img/growth.jpg?v=04c180ed9e)](https://ghost.org/resources/growth/)
[![Build a business: Earning revenue from your work](https://ghost.org/resources/assets/img/business.jpg?v=04c180ed9e)](https://ghost.org/resources/business/)
















