Official Ghost + Discourse Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Disqus](/images/logos/integrations/disqus.svg)Disqus](/integrations/disqus/)
* [![Discord](/images/logos/integrations/discord_hu65eeccc91402e292ff2f38d86dc2e280_137720_50x0_resize_q100_h2_box_3.webp)Discord](/integrations/discord/)
* [![Cove Comments](/images/logos/integrations/cove_hucf72b5cab77934e0dbdd62c9151ae31a_24300_50x0_resize_q100_h2_box_3.webp)Cove Comments](/integrations/cove-comments/)
* [![Slack](/images/logos/integrations/slack_hub000cc74b3e4e528278503b6f90bdd3c_4017_50x0_resize_q100_h2_box_3.webp)Slack](/integrations/slack/)
[Integrations](/integrations/)
/
[Community](/integrations/?tag=Community)

Connect your Ghost site with your forum and unlock a fully-functional commenting feature on posts and pages on your publication

[Discourse](https://www.discourse.org/) is a modern forum solution that allows you to build a community forum. The software is 100% free and open source, or you can use their paid forum hosting options. If you’re using Discourse to run a community forum, then you might want to integrate this with Ghost to unlock comments on your posts.

Setting up a Discourse integration with Ghost involves a few steps and a basic knowledge of code – but don’t worry, this guide has got you covered!

Create an embeddable host on Discourse
--------------------------------------

The first step is to login to your Discourse account and create an embeddable host, since this is where your comments will be hosted and embedded into your Ghost posts.

Go to **Admin > Customise > Embedding** in your Discourse instance and create a new host and enter some information:

![](/images/integrations/New-host-Discourse_hub9bf732ab8c14603d32bae9178c2328a_46700_2236x0_resize_q100_h2_box_3.webp)

* **Allowed Hosts** should be the hostname (your Ghost domain) where you want to embed your comments - note the lack of `http://` and path.
* **Class Name** is a class name that will be attached every time your iframe is rendered. You can use this for styling purposes.
* **Path Whitelist** allows you to specify the paths that will accept your embed. In this example, we want the embeds to appear on the `/blog/` path.
* **Post to Category** - if you supply a category alongside the host you are entering, posts imported from that host will automatically end up in that category.

Once you save your new host, you should also ensure that there is a correct user entered in the settings menu. This is the Discourse user who will create topics, and is usually populated with the admin user:

![](/images/integrations/Embed-settings-username_hu3f66301c1e7d5039a8ba08aba8b6c428_15569_1248x0_resize_q100_h2_box_3.webp)
> 💡 **Tip**: Use multiple hosts to post comment threads to different categories on discourse. For example, you could create a different host for different tag paths on your Ghost site, and have the comments appear in the relevant category on Discourse.

Edit the HTML provided
----------------------

Once your new host is created, Discourse will provide the following snippet of code:

```
<div id='discourse-comments'></div>
<script type="text/javascript">
    if (window.location.pathname.indexOf('/p/') < 0) {
        DiscourseEmbed = {
            discourseUrl: 'https://forum.ghost.org/',
            discourseEmbedUrl: 'REPLACE_ME'
        };
        (function() {
            var d = document.createElement('script'); d.type = 'text/javascript'; d.async = true;
            d.src = DiscourseEmbed.discourseUrl + 'javascripts/embed.js';
            (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(d);
        })();
    }
</script>

```

It will automatically enter your `discourseUrl` and leave a `REPLACE_ME` line where you’ll need to enter the URL where your comments will be embedded. Since we want to embed comments across all posts on the `/blog/` route, we’ll need to use a helper to automatically generate the values, for example: `{{url absolute="true"}}`.

Paste the embed code into post.hbs
----------------------------------

Once your code is good to go, the next step is to paste it into the `post.hbs` template in your theme files. This template is for all posts on your site. Here’s what our final code snippet looks like in this example:

```
<div id='discourse-comments'></div>
<script type="text/javascript">
    if (window.location.pathname.indexOf('/p/') < 0) {
        DiscourseEmbed = {
            discourseUrl: 'https://forum.ghost.org/',
            discourseEmbedUrl: '{{url absolute="true"}}'
        };
        (function() {
            var d = document.createElement('script'); d.type = 'text/javascript'; d.async = true;
            d.src = DiscourseEmbed.discourseUrl + 'javascripts/embed.js';
            (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(d);
        })();
    }
</script>

```

A good spot for this code is after the content in the template file. In Ghost’s official themes, replace the `{{comments}}` helper with your Discourse code:

![](/images/integrations/theme-replace-comments-helper_hu0c29dd7fb66b77e2f53cbfd3a1b64bea_249652_2058x0_resize_q100_h2_box_3.webp)

Replace the the comments helper with your code

Update your active theme
------------------------

Once you’ve done this, all that’s left is to update your active theme by uploading a fresh `.zip` in Ghost Admin in the Design settings. The next time your existing posts are visited, the Discourse thread will be created, and you’ll be able to see the comments function at the bottom of your posts. Here’s an example of what it looks like on [Coding Horror’s site](https://blog.codinghorror.com/what-does-stack-overflow-want-to-be-when-it-grows-up/#discourse-comments):

![](/images/integrations/Coding-Horror-blog-comments_hu232f6b5f11eef0df73f08e30a4c89859_148085_1484x0_resize_q100_h2_box_3.webp)

Finally, when you create a new post on your site, it automatically has the comments feature once you hit publish 🎉

### Styling your Embedded content (Optional)

On the latest build of Discourse it is possible to add a stylesheet for your embedded comments. Visit **Admin > Customise > CSS/HTML > Embedded CSS** and you can add a custom styling for your comments threads.

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

