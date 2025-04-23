


How do I import my data from WordPress?










































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

You can easily migrate your posts and pages from WordPress site to Ghost in just a few clicks, using the WordPress migrator in Ghost Admin.

Run the migration
-----------------

The WordPress migrator allows you to quickly import content from your WordPress site to your Ghost publication. You can access the migrator tool from the **Settings → Advanced →** **Import/Export** area of Ghost Admin.

![](https://ghost.org/help/content/images/2025/02/import.png)

It's helpful to log in to your WordPress site before running the migration in Ghost Admin.

### 1. Enter your WordPress URL

To start the migration process, enter the public URL to your WordPress site, and click **Continue**.

![](https://ghost.org/help/content/images/2025/02/1.png)
### 2. Export content

Next, click **Open WordPress Settings.** If already logged into WordPress, this will take you directly to the location of your WordPress site where an export can be generated.

![](https://ghost.org/help/content/images/2025/02/2.png)

Select **All content,** click **Download Export File**, which will download an XML file with your content in it.

### 3. Upload content

Once your export has been downloaded, return to the migrator window in Ghost Admin, and select **Click or drag file here to upload**, and navigate to the XML file you downloaded from WordPress, once uploaded click **Continue**.

If you're unsure of where the file was saved, check your Downloads folder.

### 4. Review

Ghost will confirm the number of posts and pages that will be imported to your publication. If satisfied, click **Import content** to begin the import of your data.

![](https://ghost.org/help/content/images/2025/02/3.png)

After a few moments, you'll see a confirmation message, confirming that your data was successfully migrated to your Ghost site.

---

### Redirects

ℹ️WordPress categories are converted to [tags](https://ghost.org/help/tags/) during the migration. The first category for any post will also become the [primary tag](https://ghost.org/help/tags/#primary-tags). 

You may need to add redirects to ensure backlinks lead to the correct content.

[RedirectsGhost includes support for implementing URL redirects through the use of a custom redirects.yaml file. Redirects can be useful for: \* Changing your site URL structure – If you’re reorganizing your site’s content, or updating your permalink structure, you may need to set up redirects to ensure that any links pointing![](https://ghost.org/help/content/images/icon/favicon-15.ico)Ghost Help CenterGhost![](https://ghost.org/help/content/images/thumbnail/help-site-cover-1.png)](https://ghost.org/help/redirects/)

Please refer to this list of the [most common redirection rules for WordPress migrations](https://ghost.org/tutorials/implementing-redirects/#common-redirects).

---

If you encounter issues, and you're a **Ghost(Pro)** customer, reach out to our support team for further advice, or head to the [forum](https://forum.ghost.org/) for community support if you're self-hosting.



### Related articles

 
Ghost has built-in tools to migrate content and subscribers from



 

 
When a member's subscription renewal fails, what happens next will vary based on your Stripe account retry settings.



 

Was this article helpful?
-------------------------








 





