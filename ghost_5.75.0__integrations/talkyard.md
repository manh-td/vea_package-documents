Official Ghost + Talkyard Integration
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
* [![Discourse](/images/logos/integrations/discourse_hu446d4df4327211d4f32029c85ce50706_6431_50x0_resize_q100_h2_box_3.webp)Discourse](/integrations/discourse/)
* [![Discord](/images/logos/integrations/discord_hu65eeccc91402e292ff2f38d86dc2e280_137720_50x0_resize_q100_h2_box_3.webp)Discord](/integrations/discord/)
* [![Cove Comments](/images/logos/integrations/cove_hucf72b5cab77934e0dbdd62c9151ae31a_24300_50x0_resize_q100_h2_box_3.webp)Cove Comments](/integrations/cove-comments/)
[Integrations](/integrations/)
/
[Community](/integrations/?tag=Community)

Add comments to your Ghost posts without ads or tracking, with a Talkyard integration

[Talkyard](https://www.talkyard.io?utm_source=ghost&utm_campaign=integration) allows you to embed fully functional comment threads on Ghost posts and pages without any ads or tracking. It’s an open source project which can be self-hosted, or you can use their [hosted service](https://www.talkyard.io/blog-comments?utm_source=ghost&utm_campaign=integration).

This guide will walk you through how to integrate Talkyard with your Ghost site using their hosted service. For further information about self-hosting read their [technical guide](https://www.talkyard.io/for-developers?utm_source=ghost&utm_campaign=integration).

Create a Talkyard account
-------------------------

Sign up for [Talkyard Blog Comments](https://www.talkyard.io/plans-blog-comments?utm_source=ghost&utm_campaign=integration) and choose an appropriate plan for your needs.

Enter your site
---------------

Upon signing up, you will be prompted to enter your site’s domain where you can set up your Ghost publication with Talkyard:

![](https://lh6.googleusercontent.com/sDcAMVxfdS3eGpcIUI_6VoE_tHdz0Pr4PEjyL2v7Vb8yoauCt1dAtdLBhjDC_EFct22eshc4Re3WP666fJID6_bvGwJXkvp2R_2p-bJ6Sk68FvMvN-Drql8Evq4CMP_poA)

Select Ghost in the settings
----------------------------

Once you have reviewed the intro tour of the Talkyard tool, head to the embedded comments section of the settings in Talkyard. From here you should choose Ghost, and copy the HTML code provided to your clipboard:

![](https://lh4.googleusercontent.com/KH8xMeVMGjNwl7qLfsRXaVU08qJGkaD9-FnMRgWmRjiXEvk7rHA6DMOAMEyHsw9GojggVs8xpEOXt_2RnGol5e7u4b7_yu7Udo5gVjgsiX83t4vkSRLhct7PW61d6T5jgg)

Add the code to your theme
--------------------------

Next, in your Ghost theme, locate the template file where you want to insert comments on your site. This is usually inside `post.hbs`, right after the content of your posts.

In **Casper**, Ghost’s default theme, you’ll see a line of code specifically reserved for inserting comments. This is where you’ll want to paste the embed code:

![](https://lh6.googleusercontent.com/SImD1dK2C8yrGiExpbnUpL6P8i-8WbO_tiUuCR3TBIBSynaFnsasAZ44L-yJVrSnQZdFsg_yrxnPT0Qfm9hktOBxJCJMJ-hY_lTGVNie-_6buntC-tvxgRIzGsyXIBxWLA)

Make sure you remove the comments on line 65 and 69. Afterwards, you’ll see something like this:

```
<section class="post-full-comments">
    <script>talkyardServerUrl='https://comments-for-yoursite.com.talkyard.net';</script>
        <script async defer src="https://c1.ty-cdn.net/-/talkyard-comments.min.js"></script>
        <!-- You can specify a per page discussion id on the next line, if your URLs might change. -->
        <div class="talkyard-comments" data-discussion-id="ghost-{{comment_id}}" style="margin-top: 45px;">
        <noscript>Please enable Javascript to view comments.</noscript>
        <p style="margin-top: 25px; opacity: 0.9; font-size: 96%">Comments powered by
        <a href="https://www.talkyard.io">Talkyard</a>.</p>
        </div>
</section>

```

Update your theme
-----------------

Once you’ve updated the active version of your theme in Ghost Admin, your Talkyard integration will be ready to go.

![](https://lh6.googleusercontent.com/nzKx33-czlrdIDEQdwPehUWlV17KoPfBvAG8keEOlThyDaINuqvt--jlHI6gbXGb1x1nWRAWnC4wsZ5u_xrOtMFIFzvS1ebom-nVXuD15YmnlgPABakIeO0yveribv_ieQ)

Here’s an example of what Talkyard comments look like on a Ghost site:

![](https://lh4.googleusercontent.com/q1UTDm46nT68I7QosHNHvCufULI55nAXISyxWBTETEKqffKbkgIIwgsA_MqicyA0Lshg7lrM3GXKKMCuCryqj07weaW8PNDGECgX6ohIgQG_f-08rsYAXEvRJXNH77i9CQ)

For further help with using Talkyard to power your site’s comments, head to their dedicated [support forum](https://www.talkyard.io/forum/latest/support?utm_source=ghost&utm_campaign=integration).

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

