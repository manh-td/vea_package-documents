


Importing content










































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


Ready to breathe new life into your new Ghost site and import some content? Discover how to import content and images to your publication from other Ghost installs, or other platforms.

💡****Migrating from another platform?**** We can help you import your content and data for free — [****find out more****](https://ghost.org/concierge)!

Imports in Ghost
----------------

The Ghost importer allows you to import content and images directly to your new publication from Substack, Medium, MailChimp and other platforms.

Access the importer from the **Settings → Advanced → Import/Export** area in Ghost Admin.

![](https://ghost.org/help/content/images/2024/06/migration-tools.png)

Migration guides
----------------

[How do I import my data from Substack?You can easily migrate your posts and subscribers from Substack to Ghost using the Substack migrator tool.![](https://ghost.org/favicon.ico)Ghost Help CenterGhost![](https://ghost.org/help/content/images/size/w1200/2023/05/help-site-cover-1.png)](https://ghost.org/help/importing-from-substack/)[How do I import my data from Medium?You can easily migrate your posts and subscribers from Medium to Ghost using the Medium migrator tool.![](https://ghost.org/favicon.ico)Ghost Help CenterGhost![](https://ghost.org/help/content/images/size/w1200/2023/05/help-site-cover-1.png)](https://ghost.org/help/importing-from-medium/)[How do I import my data from Mailchimp?You can easily migrate your subscribers from Mailchimp to Ghost using the Mailchimp migrator tool.![](https://ghost.org/favicon.ico)Ghost Help CenterGhost![](https://ghost.org/help/content/images/size/w1200/2023/05/help-site-cover-1.png)](https://ghost.org/help/importing-from-mailchimp/)

If you're migrating from another Ghost install, the importer will handle the import for you using the **Universal import** option.

If you're migrating from a different platform that is not listed, your content needs to be formatted before it can be imported to Ghost. See our [developer migration docs](https://ghost.org/docs/migration/ghost/) for guidance.

### Image imports

The importer accepts both `JSON` and `zip` files, which means you can import your content and images at the same time by adding your files to the same `zip` file.

### Handling large imports

Because image imports can be high in file size, it is recommended to break up your image import into multiple, smaller `zip` files. You can use the following tools to [split up your zip files](https://github.com/TryGhost/gctools#zip-split) and your [JSON files](https://github.com/TryGhost/gctools#json-split).

If you're migrating from another platform, keep in mind that each import would need to use the same file path structure found in the export generated by the platform (e.g. include the `/content/images/`path).

---

If you encounter issues, and you're a **Ghost(Pro)** customer, reach out to our support team for further advice, or head to the [forum](https://forum.ghost.org/) for community support if you're self-hosting.



[Next up
 →](/help/imports/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





