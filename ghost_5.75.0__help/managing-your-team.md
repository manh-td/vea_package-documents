


Invite your team










































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


Once your site is up and running, it's time to invite your team to sign up as staff users. To invite new users to your publication, go to the **Settings → General → Staff** settings in the Ghost admin and click **Invite people**.

Ghost has a number of different user roles that you can assign to staff user profiles:

* **Contributors** — This is the base user level in Ghost. Contributors can create and edit their own draft posts, but they are unable to edit the drafts of others, or publish posts.
* **Authors** — Trusted staff users who can write, edit, and publish their own posts.
* **Editors —** Editors can do everything that an Author can do, but they can also edit and publish the posts of others. Editors can also invite new Contributors and Authors to the site.
* **Administrators —** Administrators can do everything that Authors and Editors can do, but they can also edit all site settings and data, not just content. Administrators have full access to invite, manage, or remove any other site user, and import, view, and manage members.

Read more about [staff user roles](https://ghost.org/help/managing-staff-user-profiles) and how to delete or suspend staff users.

🛠️If running a self-hosted instance of Ghost, ensure your [email config](https://ghost.org/docs/concepts/config/#mail) is set up correctly so that invitations are delivered successfully.

Staff user information
----------------------

Each staff user of your publication has their own profile, with settings that can be managed from the **Settings → General → Staff** area in Ghost Admin. It's a good idea to ask your staff users to fill out their profiles, as this populates structured data for posts, and creates more opportunities for themes to fully populate their design.

![](https://ghost.org/help/content/images/2023/05/kevin-indig-author.png)![](https://ghost.org/help/content/images/2023/05/creator-science-author.png)![](https://ghost.org/help/content/images/2023/05/lever-author.png)



Examples of staff user profile pages



### Profile pictures

If one is available, Ghost automatically uses the [Gravatar](https://gravatar.com/?ref=ghost.org) picture tied to your email address as the author profile image. This is used across your publication’s theme by default. To use a different image, click on the current profile image to upload a new one using the image uploader.

![](https://ghost.org/help/content/images/2023/10/CleanShot-2023-10-17-at-11.45.55@2x.png)
### Cover photo

Cover photos can be uploaded which will be displayed on the users profile page on your site, if your theme supports it.

![](https://ghost.org/help/content/images/2023/10/CleanShot-2023-10-17-at-11.45.55@2x-1.png)
### Full name

The full name configured within the staff user profile can be set to a real name, or a pseudonym. The full name entered will appear in the byline with content published by the staff user on the site.

### Email

The email configured with the staff user can be altered at any time by the staff user, and is used to login to Ghost Admin for the site, or receive email notifications from your publication.

### Slug

The slug configured for a staff user can be customized from the default that is automatically generated using the users full name. The slug will be used for each staff users profile page, `example.com/author/slug`.

### Location

An optional location can be configured with each staff profile and is displayed on the profile page if your theme supports it.

### Website

A custom website URL can be configured alongside the staff user’s profile, which is handy if you’ve invited contributors to your site, and they’d like to include a link to their own publication.

### Facebook & X profiles

Custom Facebook and X (formerly Twitter) profile links can be included with each staff user and displayed on the user profile page if your theme supports it, so visitors can find the social profiles of the people who publish content on your site.

### Bio

A custom bio of up to 200 characters can be included for each staff member.

### Email notifications

Staff users can receive email alerts for the following events which occur on your site:

* Comments
* Recommendations
* New signups
* New paid members
* Paid member cancellations
* Milestones
* Tips & donations

Each of these can be toggled on and off from the **Email notifications** area of any staff profile.

![](https://ghost.org/help/content/images/2024/09/email-notification-options.png)
### Staff access token

Staff access tokens can be used with some [custom integrations](https://ghost.org/integrations), as well as the Ghost [Admin API](https://ghost.org/docs/admin-api/) for authentication.

### Password

Staff user passwords can be updated directly from the staff user profile when needed.



[Next up
 →](/help/managing-your-team/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





