Official Ghost + Disqus Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Discourse](/images/logos/integrations/discourse_hu446d4df4327211d4f32029c85ce50706_6431_50x0_resize_q100_h2_box_3.webp)Discourse](/integrations/discourse/)
* [![Discord](/images/logos/integrations/discord_hu65eeccc91402e292ff2f38d86dc2e280_137720_50x0_resize_q100_h2_box_3.webp)Discord](/integrations/discord/)
* [![Cove Comments](/images/logos/integrations/cove_hucf72b5cab77934e0dbdd62c9151ae31a_24300_50x0_resize_q100_h2_box_3.webp)Cove Comments](/integrations/cove-comments/)
* [![Slack](/images/logos/integrations/slack_hub000cc74b3e4e528278503b6f90bdd3c_4017_50x0_resize_q100_h2_box_3.webp)Slack](/integrations/slack/)
[Integrations](/integrations/)
/
[Community](/integrations/?tag=Community)

If you’re in need of a quick way to get fully-functional commenting on a Ghost site, Disqus may be what you’re looking for

[Disqus](https://disqus.com) allows you to embed comment threads within Ghost posts and pages, including additional functionality like upvoting and adding Emoji reactions. The platform is widely adopted and relatively easy to set up, so you’ve probably come across it before.

Setting up Disqus with Ghost involves installing their comment embed code into your theme, and making some small adjustments.

> **Note**: While Disqus is free, it was [acquired by an ad-tech company in 2017](https://techcrunch.com/2017/12/05/zeta-global-acquires-commenting-service-disqus/) and may inject advertising and ad-trackers on your site.

Copy the Ghost-Disqus comment code
----------------------------------

First, copy this **Ghost-Specific** Disqus comment code onto your clipboard. This is not the same as the Disqus Universal Code, but is customised specifically for Ghost themes:

```
<div id="disqus_thread"></div>
<script>
    var disqus_config = function () {
        this.page.url = "{{url absolute="true"}}";
        this.page.identifier = "ghost-{{comment_id}}"
    };
    (function() {
    var d = document, s = d.createElement('script');
    s.src = 'https://EXAMPLE.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>

```

Paste the comment code into post.hbs
------------------------------------

A good spot for this code is after the content in the template file. In Ghost’s official themes, remove the `{{#if comments}}` block and replace the `{{comments}}` helper with your Disqus code:

![](/images/integrations/disqus-on-casper-code-to-replace_hu2c70a50ee698256f37ffd07778a101f0_646958_2113x0_resize_q100_h2_box_3.webp)

Update the the comments block with your code

![](/images/integrations/disqus-on-casper-code_hu2c70a50ee698256f37ffd07778a101f0_669331_2113x0_resize_q100_h2_box_3.webp)

Comments block updated with Disqus code

Find your Disqus `shortname`
----------------------------

Next you’ll need to visit [Disqus Admin](https://disqus.com/admin/), and create a site or select an existing one. From the site’s settings area, find the `shortname` and copy it.

Insert your `shortname` into the Disqus code
--------------------------------------------

Lastly, find the line of code in your `post.hbs` file which says:

```
s.src = 'https://EXAMPLE.disqus.com/embed.js';

```

and replace `EXAMPLE` with your shortname. Then save the file, upload a fresh copy of your theme, and restart Ghost. Comments should now be loading on your site.

Add automation to comments
--------------------------

To take things further, you might want to add automation to your comments using [Zapier](https://zapier.com). Notifications for new comments posted to your site can be particularly useful! Here are a few ideas to get started:

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

