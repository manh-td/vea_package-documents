Why do I have to set up Mailgun for newsletters?
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Ghost has the ability to deliver posts as email newsletters natively. A bulk-mail provider is required to use this feature and SMTP cannot be used — read more about [mail config](/docs/config/#mail).

![Sending mail in Ghost](/images/docs/faq/ghostmail-3_hu687dca5c8777b3e1e045d59018a01864_58121_1318x0_resize_q100_h2_box_3.webp)

**Transactional** email in Ghost can be configured to send with any SMTP, or another mail service that you prefer, using Ghost’s [standard](/docs/config/) configuration setup.

**Bulk email** delivery for newsletters is a new feature which requires a bulk mail API. Currently the only bulk mail API we support is Mailgun.

If you *don’t* want to deliver posts to members by email, you do not need a Mailgun account and you can safely ignore the email newsletter settings completely!

#### Why can’t I just use SMTP mail config to send email newsletters with Ghost?

Sending a bulk email to many recipients using basic SMTP will result in your IP address being instantly blacklisted and marked as spam by all mail providers. You should never, ever send bulk mail using basic SMTP, which is why Ghost does not support it.

More info [here](https://serversmtp.com/smtp-server-newsletter/), and [here](https://help.campaignmonitor.com/how-why-isps-block-emails), and [here](https://www.mailgun.com/blog/email-blasts-dos-donts-mass-email-sending/), and [here](https://webmasters.stackexchange.com/questions/19168/how-to-send-mass-email-and-not-get-treated-as-spam).

#### Did you know Mailgun doesn’t have free accounts anymore??

Mailgun recently updated their pricing, including the removal of a free tier. However, under their new pricing, invoices are not sent if they total less than $0.50 - which is still more than 600 emails. For most people who are getting started Mailgun remains free, and subsequent rates are extremely generous. It would cost far, far more (money as well as time) to run your own bulk mail delivery infrastructure, or use most other providers.

#### I still want to use a different provider to send email newsletters, why can’t I do that?

You can. There is no requirement to use Ghost’s built in newsletter delivery feature. Before we released this feature, thousands of people sent their newsletter using all sorts of other services such as Mailchimp, Sendgrid, Convertkit, and many others. You can easily sync your members database to an external newsletter provider via [Zapier](/integrations/zapier/), or by following our [detailed integration guides](/integrations/?tag=email).

#### Do you have any affiliation with Mailgun? Are you on their referral program or something?

No. We have no partnership with Mailgun, we are not on their referral or affiliate program, they do not provide us with free service, and we do not benefit in any way (financial or otherwise) from people using them. We pay full-price for our own Mailgun account

#### I still don’t want to use Mailgun, can you support something else?

Adding additional bulk mail providers is not on the core team’s immediate roadmap, but Ghost is open source, so if anyone is particularly motivated to support other proviers then you can certainly get involved and contribute to the product to make this happen sooner.

[More details about our product development process, here →](/docs/product/)

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

