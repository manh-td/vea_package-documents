


Accepting member's payments using Patreon










































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

Connect your Patreon account to Ghost and give your supporters access to members-only content on your custom Ghost site.

*Thisguide requires an active [Zapier](https://zapier.com/) account.*

---

If you’re running a membership site on Ghost, it’s possible to import or connect your Patreon creator account and invite all of your existing supporters to your brand new Ghost website, where they will be able to access members-only content using a simple email-based login flow.

This unlocks additional ways to deliver content to your audience, or offer premium benefits to your existing supporters. The best thing: this integration takes a few minutes and zero coding knowledge to implement.

### 1. Import your members using our Members Importer

If you're using the [members feature](https://help-old.ghost.io/members-introduction/) in Ghost and you already have a list of existing supporters from Patreon, you can import these them directly into your Ghost site. This is made possible using our [import members](https://help-old.ghost.io/import-members/) tool which allows you to list all of your users into a simple CSV file and upload them directly to Ghost.

In your Patreon creator account, go to the **Patrons > Relationship manager** to view and filter your patrons accordingly. Then use the CSV button to download your list.

![](https://ghost.org/help/content/images/2023/05/Patreon-exports.png)

In Ghost, you can import a CSV file with three headings: `email`, `name` and `note`. Email is the only required field to make this integration work, but if you have names or additional notes we’d recommend importing them now.

If you're not sure how to structure this file, we've created a handy pre-built template which you can download [**here**](https://static.ghost.org/v3.0.0/files/member-import-template.csv).

Once your CSV is good to go, log in to your Ghost site’s admin area and click the settings icon in the member's dashboard to import your file:

![](https://ghost.org/help/content/images/2023/05/member-importer.png)

You can now let your Patrons know that they can head to your website and enter their email address to access members-only content.

### 2. Sync Ghost members with Patreon

If you’re running a membership publication with Ghost, it’s possible to link this with your Patreon account using Zapier to ensure everything stays in sync. This means new Patrons will automatically be sent to Ghost, unlocking access to your members-only content.

This saves tons of time manually updating your member list and can be set up using a simple Zapier automation:

### 3. Disable free member signup

If you would like the content on your Ghost publication to only be available to your patrons or paid-members that you import from any other platform, you can prevent free member signup in a couple of clicks.

Navigate to **Settings → Memberships** in Ghost admin and turn the “allow free member signup” setting to "Only people I invite".

![](https://ghost.org/help/content/images/2023/05/subscription-access-settings.png)

This means any public visitors to your site will be unable to signup for free access to content. The only way people will be able to login to their member's account is if they have been imported via an integration with Patreon or other members list.

**Default post access**

To run your Ghost members site in this way, you should also consider setting your default post access to members only.

![](https://ghost.org/help/content/images/2023/05/default-post-access.png)

You can also publish paid-members only content on your Ghost site if you wish to provide new visitors to your site with a way to subscribe without having to go through Patreon.

---

### Further reading

[How to switch from Patreon to Ghost [Tutorial]Built an audience on Patreon but looking for more ownership of your revenue and content?![](https://ghost.org/resources/content/images/size/w256h256/2021/10/ghost-orb-pink-transparent-01-1.png)Ghost ResourcesKym Ellis![](https://images.unsplash.com/photo-1581462050168-00c97ee89d1f?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=2000&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ)](https://ghost.org/resources/patreon-vs-your-own-site/)


### Related articles

 
Ghost has built-in tools to migrate content and subscribers from



 

 
You can easily migrate your posts and pages from WordPress to Ghost using the WordPress migrator tool.



 

Was this article helpful?
-------------------------








 





