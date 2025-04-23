Email Newsletters — Ghost Developer Docs
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Sites using the Members feature benefit from built-in email newsletters, where all posts can be delivered directly to segments of your audience in just a few clicks.

Overview
--------

Email newsletters in Ghost can be scheduled and delivered to free and paid members, or a segment of free *or* paid members. Newsletters are delivered using a beautiful HTML template that is standardised for most popular email clients.

Ghost sites have a single newsletter by default but additional ones can be created and customised. Multiple newsletters allow you to tailor content for specific audiences and your members to choose which content they receive.

Bulk email configuration
------------------------

In order to send email newsletters from a Ghost site, email needs to be configured.

### Ghost(Pro)

When using [Ghost(Pro)](/pricing/), email delivery is included and the configuration is handled for you automatically.

### Self-hosted

Self-hosted Ghost installs can configure bulk email by entering Mailgun API keys from the **Email newsletter** settings.

Delivering bulk email newsletters can’t be done with basic SMTP. A bulk mail provider is a requirement to reliably deliver bulk mail. At present, Mailgun is the only supported bulk email provider. Mailgun is free for up to 600 emails per month, and has very reasonable pricing beyond that. [More info here](/docs/faq/mailgun-newsletters/)

![Configure email newsletters with Mailgun API keys](/images/docs/members/configure-email-mailgun_huadcebd46ebc845ccc560c91272939bbb_16705_1770x0_resize_q100_h2_box_3.webp)
### Auth email

The Members feature uses passwordless email-link based logins for your members. These auth emails are not delivered in bulk and are sent using the standard mail configuration in Ghost.

Self-hosted Ghost installs can [configure mail](/docs/config/#mail) using Mailgun or other providers if preferred.

##### On this page

Launch your site
----------------

Last week, 5,069 brand new  
publications got started with Ghost.

Today, it's your turn.

[Start a free trial now →](https://account.ghost.org/signup/)Product

* [Creator platform](/)
* [Theme marketplace](/marketplace/)
* [Integrations](/integrations/)
* [Experts](/experts/)
* [Ghost for news](/news/)
Developers

* [How to install Ghost](/docs/install/)
* [Core concepts](/docs/)
* [Ghost hosting](/pricing/)
* [API documentation](/docs/content-api/)
* [Security overview](/docs/security/)
* [Source code](https://github.com/TryGhost/Ghost)
Resources

* [Ghost tutorials](/tutorials/)
* [Resources](/resources/)
* [Node.js CMS guide](https://nodecms.guide)
* [Open Subscription Platforms](https://opensubscriptionplatforms.com)
Comparisons

* [Ghost vs Substack](/vs/substack/)
* [Ghost vs WordPress](/vs/wordpress/)
* [Ghost vs Medium](/vs/medium/)
* [Ghost vs Memberful](/vs/memberful/)
* [Ghost vs Patreon](/vs/patreon/)
* [Ghost alternatives →](/alternatives/)
Support

* [Help center](/help/)
* [Community forum](https://forum.ghost.org/)
* [Status  
  Triangle
  
  
  
   99.9%](https://status.ghost.org/)
[![Non-Profit Foundation](/images/logos/indie.svg)](/about/)
[![Open Source](/images/logos/opensource.svg)](https://github.com/tryghost)
[![Carbon Neutral](/images/logos/carbonneutral.svg)](https://climate.stripe.com/6MNofu)

