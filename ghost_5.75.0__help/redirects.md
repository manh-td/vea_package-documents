


Redirects










































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


Ghost includes support for implementing URL redirects through the use of a custom `redirects.yaml` file.

Redirects can be useful for:

* **Changing your site URL structure** – If you're reorganizing your site's content, or updating your permalink structure, you may need to set up redirects to ensure that any links pointing to old URLs are automatically redirected to the correct *new* URL. This can help preserve your site's SEO, and ensure that readers are able to find the content they're looking for.
* **Updating or removing content** – If you have content on your site that is outdated or no longer relevant, you may want to remove it or replace it with new content. In this case, you can set up a redirect to automatically send readers to a new page or post that is related to the old content.
* **Fixing broken links** – If you have links on your site that are broken, or no longer work, you can set up a redirect to automatically send readers to a working page or post that is related to the broken link.

Ghost supports `301` and `302` redirects. `301` redirects are for permanent redirects, and `302` redirects are for temporary redirects.

To implement redirects, go to the **Settings → Advanced → Labs** area of Ghost Admin. **Open** the Labs area using the **Open/Close** toggle, and select the **Beta features** tab.

![The beta tab, in Ghost's labs settings area](https://ghost.org/help/content/images/2023/10/Labs-Beta-features-in-Ghost.png)

Download your existing `redirects.yaml` file.

![The redirects options in Ghost's labs settings](https://ghost.org/help/content/images/2023/10/redirects2-1.png)

Once downloaded, open the file in a code editor to add custom redirect rules to the file in YAML format. Be sure to use **spaces** and not tabs to indent rules.

For example:

```
301:
  /permanent-redirect-from: /permanent-redirect-to
  /permanent-redirect-from-2: /permanent-redirect-to-2

302:
  /temporary-redirect-from: /temporary-redirect-to
  
```

Upload your edited file in the labs area.

![The upload redirects file button in Ghost's labs settings](https://ghost.org/help/content/images/2023/10/redirects3-1.png)

For additional information on setting up redirects in Ghost, check out our [Implementing Redirects](https://ghost.org/tutorials/implementing-redirects/#implementing-redirects-in-ghost) tutorial.



[Next up
 →](/help/redirects/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





