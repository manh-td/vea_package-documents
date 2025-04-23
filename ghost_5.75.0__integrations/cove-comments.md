Official Ghost + Cove Comments Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![ChartMogul](/images/logos/integrations/chartmogul_hu01c73d47915043033a3a07dcbb830fa7_3078_50x0_resize_q100_h2_box_3.webp)ChartMogul](/integrations/chartmogul/)
* [![Churnbuster](/images/logos/integrations/churnbuster_hudae337c0f674707d1840f4c514d865a7_15531_50x0_resize_q100_h2_box_3.webp)Churnbuster](/integrations/churnbuster/)
* [![Mailchimp](/images/logos/integrations/mailchimp_hucb75d06be88e6331905252c3cff4ebbc_32058_50x0_resize_q100_h2_box_3.webp)Mailchimp](/integrations/mailchimp/)
* [![FirstPromoter](/images/logos/integrations/firstpromoter_hu13330b4d32004712e337efa3113c94c8_6190_50x0_resize_q100_h2_box_3.webp)FirstPromoter](/integrations/firstpromoter/)
[Integrations](/integrations/)
/
[Members](/integrations/?tag=Members)

Add members only comments to your Ghost membership website using an integration with Cove comments

[Cove](https://cove.chat/) allows you to embed fully functional comment threads from your subscribed members, allowing you to build a community for your membership audience on Ghost.

This guide will walk you through how to integrate Cove comments with your Ghost site by creating a custom integration, and adding some pre-defined code to your site’s theme.

### Prerequisites

Cove is only compatible with Ghost version 3.9 and above, please ensure your version of Ghost is [up to date](/docs/update/). You’ll also need to enable Members in Ghost admin and ensure it is configured correctly using [our Stripe documentation](/help/stripe/) for more details.

Create a Cove account
---------------------

[Sign up for Cove](https://cove.chat/) with their 14 day free trial. [See their plans](https://cove.chat/pricing/) for more information on pricing after the trial.

Create a new custom integration
-------------------------------

Add a new custom integration within Ghost Admin:

![Integrations view in Ghost admin](/images/integrations/integrations-view_huc3b14622e4cdab2a1b14b10b2ee9ac83_175711_2000x0_resize_q100_h2_box_3.webp)

For your own reference, add an integration title, description and icon:

![Cover integration in Ghost admin](/images/integrations/cover-integration_hu9e3a0e7e21e8de59c135c2071b3afc8e_34462_912x0_resize_q100_h2_box_3.webp)

**Tip:** You can save the icon from the top of this page and use that!

Set your Ghost integration credentials in Cove
----------------------------------------------

Next, copy and paste your integration details into your [Cove account](https://app.cove.chat/setup/) in the Setup area:

![Cove setup view](/images/integrations/cove-setup_huc3c9840cd3d8364246b69bb51f9fe241_88958_1480x0_resize_q100_h2_box_3.webp)

Add the code to your theme
--------------------------

Next, in your Ghost theme, locate the template file where you want to insert comments on your site. This is usually inside `post.hbs`, right after the content of your posts.

In **Casper**, Ghost’s default theme, you’ll see a line of code specifically reserved for inserting comments. This is where you’ll want to paste the embed code (make sure you remove the comments on line 65 and 69):

![Casper comment area in the code](/images/integrations/casper-comments-area_hu4fc0bd939debe7d76005d758da1f836c_20114_1312x0_resize_q100_h2_box_3.webp)

Copy the [official installation example](https://app.cove.chat/install/) within your Cove account into your `post.hbs` file. It will look something like this:

```
<section class="article-comments gh-canvas">
    {{#if @site.members_enabled}}
    <h2><span id="cove-count"></span> Comments</h2>
    <div id="cove"></div>
    {{#if @member}}
        <p>Signed in as {{@member.email}} · <a href="javascript:" data-members-signout>Sign out</a></p>
    {{else}}
        <p>Become a {{@site.title}} member below to join the conversation. As a member, you will also receive new posts by email (you can unsubscribe at any time).</p>
        <form data-members-form="signin" id="cove-login">
        <input class="cove-input" data-members-email type="email" required="true" placeholder="your@email.com" />
        <button type="submit" class="cove-button">Sign in to comment</button>
        <span class="signin-success" style="display:none">Great! Please check your inbox for a log in link.</span>
        <span class="signin-error" style="display:none">Something didn't work. Please try again.</span>
        </form>
    {{/if}}
    <script>
    const Cove = {
        publication: "YOUR_SITE_ID",
        contentId: "{{id}}",
        memberId: "{{@member.uuid}}",
        memberEmail: "{{@member.email}}"
    }
    </script>
    {{/if}}
</section>

```

Update your theme
-----------------

Once you’ve updated the active version of your theme in the Design view of Ghost Admin, your Cove comments integration will be ready to go 🎉

Here’s an example of what Cove comments look like on a Ghost site:

![Example of Cove comments](/images/integrations/cove-example_hu71a3345bc4b384e732b5c74bfdec73eb_147900_1520x0_resize_q100_h2_box_3.webp)

For further information about using Cove to power your site’s comments, check out [their full documentation](https://cove.chat/help/).

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

