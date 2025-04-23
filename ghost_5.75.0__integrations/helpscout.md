Official Ghost + Help Scout Integration
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

Keep your customer support inboxes in sync and integrate Ghost with Help Scout – embed contact forms and live chat widgets directly

If you’re using Help Scout to manage customer support emails and enquiries, you’ll probably want to integrate your support inbox with your Ghost publication to keep everything aligned and provide reliable ways for your customers to get in touch!

Using Help Scout’s Beacons feature, you can add a contact form or live chat widget to your Ghost publication via sensible code injection. Follow this guide to find out how!

Create a new Beacon in Help Scout
---------------------------------

Users with the correct permissions in Help Scout have access to a variety of features including Beacons:

![](/images/integrations/Manage-beacons_hu1bd1366f53aa89c1e85e57ceec87103d_19516_1204x0_resize_q100_h2_box_3.webp)

Create a new Beacon, give it a name, select a colour to match your site design and select the correct mailbox from the drop down menu:

![](/images/integrations/Create-a-beacon_hu47f05d7c71cbab749230a2de5df2c114_36446_1452x0_resize_q100_h2_box_3.webp)

Customise your Beacon
---------------------

Help Scout walks you through all of the customisation options for your Beacon and provides a handy preview of what it will look like:

![](/images/integrations/Beacon-preview-2_hu7ba97419751d218d7bfe9df0f883b778_42521_1905x0_resize_q100_h2_box_3.webp)

Once you are happy with your settings, it’s time to integrate your Beacon with your Ghost publication.

Paste the HTML Code into Ghost
------------------------------

Locate the HTML embed code and copy it to your clipboard:

![](/images/integrations/Install-a-beacon_hu95c102bcf733638892aa4e1a282b5166_116685_1458x0_resize_q100_h2_box_3.webp)

If you would like your Beacon to appear across your entire site, you can use the site-wide code injection feature inside Ghost Admin to implement this.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)

Hit save and you’re done - head to your site to test your new contact form or chat widget!

### Embed your Help Scout Beacon across multiple pages

On the other hand, you can also insert the HTML into the appropriate template files within your theme. This is useful if you want more fine-grained control of where your contact form or live chat appears.

Locate the template file where you want to insert the beacon code. It’s usually `post.hbs` - right after the content. In Ghost’s official themes, add the code after the line that reads `{{content}}`.

![](/images/integrations/theme-add-after-content_hu79aa78900b555549c8bdcc6b8e03c24d_256374_2004x0_resize_q100_h2_box_3.webp)

Add custom content to a Ghost theme

After editing, save the file, upload a fresh copy of your theme, and (if you’re self-hosting) restart Ghost. The beacon’s now visible on every post!

Do more with Zapier automation
------------------------------

Connect Help Scout to many more of your favourite tools and align all of your processes using Zapier. Get started with lots of commonly used Zaps, or if you can’t find what you’re looking for you can build your own:

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

