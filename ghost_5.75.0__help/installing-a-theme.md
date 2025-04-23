


Installing a theme











































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


Ghost allows you to upload pre-built or custom themes to your publication, unlocking the ability to render your site in almost any way imaginable.

Official Ghost themes
---------------------

Your new Ghost publication will be installed with one of our *free* [official themes](https://ghost.org/themes/?category=official&ref=ghost.org). Changing a theme can be done directly from within the Ghost admin.

To install a new official theme, head to the **Settings → Site → Theme** area, and click **Change theme**:

![](https://ghost.org/help/content/images/2024/11/change-theme.png)

Choose a new theme to preview from the options displayed:

![](https://ghost.org/help/content/images/2024/11/official-themes.png)

Once you've selected a theme, click **Install**, then click **Activate** to activate the theme on your publication.

Premium themes
--------------

In the [**Ghost theme marketplace**](https://ghost.org/themes?ref=ghost.org), you'll also find a handpicked selection of premium themes, that have been built by third-party developers.

To purchase and download a premium theme, click the **Purchase** button and follow the instructions provided.

![](https://ghost.org/help/content/images/2023/04/install-premium-theme.png)

**Keep in mind:** Premium themes typically are more complex to use and work with compared to the free, official themes. However, you will also have access to customer support from the theme developer, who can help answer any questions you have about using their theme. All purchases of official themes happen outside of Ghost's Marketplace.

💡On Ghost(Pro), only [official themes](https://ghost.org/themes/?category=official&ref=ghost.org) can be used with the Starter plan.

Installing a theme manually
---------------------------

To install a premium or custom theme manually, use the **Upload theme** button to upload a new theme `.zip` file.

![](https://ghost.org/help/content/images/2024/11/upload-theme.png)

Select the **Installed** option to view your active theme and a list of your installed theme history. You can also download copies of your themes or switch your active theme to one that was previously installed.

![](https://ghost.org/help/content/images/2024/11/download-theme.png)

Editing a theme
---------------

There are two different methods that can be used to edit a Ghost theme depending on what you want to achieve with your publication design:

**Code Injection**  
Code Injection is an easy way to inject custom CSS on your site, to overwrite a theme’s default styles, without having to edit your theme files directly.

![](https://ghost.org/help/content/images/2023/10/Code-injection.png)

This feature is handy if you want to make *small* design changes to your theme, such as changing your font styles or hiding the display of specific elements on your site. Your custom CSS code can be inserted into the Site Header, from the **Settings** → **Code Injection** area of Ghost Admin.

**Editing theme files**  
To make advanced edits to your theme, such as changing the layout of existing templates or adding custom template files to your site, you will want to edit your theme files directly. Though Ghost(Pro) does not provide SSH/FTP access, it’s still possible to access your theme files to make changes.

To edit your theme files, download a copy of the theme from within Ghost Admin, then unzip the theme locally for editing.

Once the theme is unzipped, the files can be edited using an HTML editor. We have full [theme developer documentation](https://ghost.org/docs/themes?ref=ghost.org) available for reference.

When you’ve finished making changes to the theme code, re-zip the theme directory for upload back to the publication, or deploy your theme to the site using [Github Actions](https://ghost.org/integrations/github/?ref=ghost.org).

---

If you’re interested in working with a freelancer or agency to build a custom theme for your site, checkout the [Expert Directory](https://ghost.org/experts?ref=ghost.org) to find a qualified partner to help with your project.



[Next up
 →](/help/installing-a-theme/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





