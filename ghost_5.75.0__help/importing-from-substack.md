


How do I import my data from Substack?










































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

You can easily migrate your posts and subscribers from Substack to Ghost in just a few clicks, using the Substack migrator in Ghost Admin.

💡****Migrating paid memberships from Substack?**** You will need to set up Stripe first — [****find out more****](https://ghost.org/help/stripe/). Make sure to use the same Stripe account that is connected to your Substack.

Run the migration
-----------------

The Substack migrator allows you to quickly import content and members from your Substack to your Ghost publication. You can access the migrator tool from the **Settings → Advanced →** **Import/Export** area of Ghost Admin.

![](https://ghost.org/help/content/images/2024/01/admin.png)

It's helpful to log in to your Substack account before running the migration in Ghost Admin.

### 1. Enter your Substack URL

To start the migration process, enter the public URL to your Substack, and click **Continue**.

![](https://ghost.org/help/content/images/2023/12/enter-url.png)
### 2. Export content

Next, click **Open Substack Settings.** If already logged into Substack, this will take you directly to the location of your Substack account where an export can be generated.

![](https://ghost.org/help/content/images/2023/12/import-content.png)

Click **Create new export**, and then download the zip file that's generated after the export is completed in Substack.

### 3. Upload content

Once your export has been downloaded, return to the migrator window in Ghost Admin, and select **Click or drag file here to upload**, and navigate to the zip file you downloaded from Substack, once uploaded click **Continue**.

If you're unsure of where the file was saved, check your Downloads folder.

### 4. Export free subscribers

Next, it's time to import your Substack subscribers. Click **Download free subscribers from Substack**, to trigger a CSV file download of your subscriber list.

Once downloaded, select **Click or drag CSV file here to upload** and navigate to the CSV download, and click **Continue**.

![](https://ghost.org/help/content/images/2023/12/import-free-subscribers.png)
### 5. Export paid subscribers

Next, it's time to import your Substack subscribers, if you have them. Click **Download paid subscribers from Substack**, to trigger a CSV file download of your subscriber list.

Once downloaded, select **Click or drag CSV file here to upload** and navigate to the CSV download, and click **Continue**.

![](https://ghost.org/help/content/images/2023/12/import-paid-subscribers.png)
### 6. Review

Ghost will confirm the number of posts and members that will be imported to your publication. If satisfied, click **Import content and subscribers** to begin the import of your data.

![](https://ghost.org/help/content/images/2023/12/summary.png)

After a few moments, you'll see a confirmation message, confirming that your data was successfully migrated to your Ghost site.

### Substack fees

Ghost does not take a cut of your revenue. Substack will continue to take **10% fees** on your existing paid subscriptions. If you would like help getting payment fees removed, contact [concierge@ghost.org](mailto:concierge@ghost.org).

### Statement descriptor

The statement descriptor is what's shown on bank statements, and depending on how the account was set up, might include 'Substack' in the name. We recommend updating this in your [Stripe public details settings](https://dashboard.stripe.com/settings/update/public/support-details).

---

If you encounter issues, and you're a **Ghost(Pro)** customer, reach out to our support team for further advice, or head to the [forum](https://forum.ghost.org/) for community support if you're self-hosting.



### Related articles

 
Ghost has built-in tools to migrate content and subscribers from



 

 
You can easily migrate your posts and pages from WordPress to Ghost using the WordPress migrator tool.



 

Was this article helpful?
-------------------------








 





