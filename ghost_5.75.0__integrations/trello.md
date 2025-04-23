Official Ghost + Trello Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Instagram](/images/logos/integrations/instagram_hua2b50eb6f034ade3c8b1b1bbd03165af_809353_50x0_resize_q100_h2_box_3.webp)Instagram](/integrations/instagram/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![YouTube](/images/logos/integrations/youtube_hud6a8b6adc63a1086de676a1c87304581_6257_50x0_resize_q100_h2_box_3.webp)YouTube](/integrations/youtube/)
* [![Twitter / X](/images/logos/integrations/twitter_hu844154aeedc321ce71128e37fdffff46_151721_50x0_resize_q100_h2_box_3.webp)Twitter / X](/integrations/twitter/)
* [![Senja](/images/logos/integrations/senja_hubcd17ef19d159794c0e0686efdaaa9ba_14692_50x0_resize_q100_h2_box_3.webp)Senja](/integrations/senja/)
[Integrations](/integrations/)
/
[Content](/integrations/?tag=Content)

Use Trello boards to keep track of ideas, schedules and strategy for your writing, and automatically send approved post ideas directly into Ghost

[Trello](https://www.trello.com) is a popular collaboration tool that enables you to organise and prioritise just about anything in a flexible way. Trello boards, lists and cards can also be used to build effective content calendars for your publication, or to sound out creative writing ideas with your team. If you use Trello to organise your content schedule, it’s possible to integrate directly with Ghost via Zapier.

Here’s how it works:

Create a new Zap
----------------

For this integration you’ll be using [Zapier](https://www.zapier.com/). If you don’t already have an account, create one now, login and create a new Zap:

![](/images/integrations/Create-a-zap_hu6ffeb98fbb95754cc64534518342808e_131060_2044x0_resize_q100_h2_box_3.webp)

Add Trello as the trigger
-------------------------

In your new Zap, search for Trello and connect to your account by logging in.

When presented with the list of Trello triggers, choose something that is suitable for your needs. In this example, we’re using `Card Moved to List`, which is useful when moving approved post ideas into a writing or in-progress list on your board:

![](/images/integrations/Card-move-to-list-trello-integration_hube557a7f885673c1c29a18fc75056709_200050_2000x0_resize_q100_h2_box_3.webp)

On the next page you’ll need to select the board and list that you want to connect to Ghost:

![](/images/integrations/Trello-wire-up-your-board_hue4661ae9ee8ba93091856e1a9ce3c408_53283_1524x0_resize_q100_h2_box_3.webp)

Once you’ve done this, Zapier will show you some sample cards for testing purposes - ensure this is working before moving to the next step.

Add a convert Markdown to HTML action (optional)
------------------------------------------------

It’s possible to send both a title and a description from a Trello card into a new draft post in Ghost. If you’d like to send this content into Ghost with some formatting such as headings, lists, or links, an extra formatting step is required.

Use the built-in Formatter by Zapier, and select the `Text` option:

![](/images/integrations/Zapier-formatter-action_hu2eb9adf274565ffdf36e6669849a251a_83958_1526x0_resize_q100_h2_box_3.webp)

On the next screen, select the `Convert Markdown to HTML` option and add `Card Desc` from the dropdown menu for the values input:

![](/images/integrations/Convert-Markdown-to-HTML_hucf3509e093c2500b1c16ee6278d6080d_43011_1478x0_resize_q100_h2_box_3.webp)

This will convert any Markdown in your Trello card descriptions into HTML - so when it’s sent to Ghost, your post draft will include any headings, lists or links!

Add Ghost as the action step
----------------------------

Add a second action step, search for Ghost and connect your site using your Admin API URL and API key. This information can be found in the Integrations section within Ghost Admin, on the Zapier page:

![](/images/integrations/Zapier-Access-to-Ghost_huadafad7560db892cac53cf4a8eab5a97_69643_1842x0_resize_q100_h2_box_3.webp)

Once access has been granted, Zapier allows you to run a quick test to ensure a connection has been established.

![](/images/integrations/Test-Ghost-in-zapier_hu4435aca5e1e6a4f77309fec2283a45d6_35822_1228x0_resize_q100_h2_box_3.webp)

Now you can customise your post template by filling in the required fields provided:

![](/images/integrations/Set-up-Ghost-post_hu07b90d55e06b6b9e2ed5f25cad828ec5_41368_1454x0_resize_q100_h2_box_3.webp)
### The required fields are:

* `Title` – Use the Trello Card title
* `Status` – Select whether your posts will be drafts, published or scheduled when sent to Ghost
* `Content format` - Use HTML for this integration
* `Content (HTML)` - Select the field in Trello that will populate your draft post in Ghost. For this example, we’ll use the transformed HTML for the card description we just created using the formatter.
* `Authors` - Select at least one author for your post using the dropdown menu

Test & Publish your integration
-------------------------------

Once you’re happy with your integration setup and post template, test it from within the Zapier dashboard and ensure everything is working as it should. When you’re ready, publish your Zap and you’re done.

![](/images/integrations/Your-zap-is-working_hu4e4113b2816ac03396c537abe51dc7d6_37040_1436x0_resize_q100_h2_box_3.webp)

Congrats – you’ve just unlocked a new, powerful workflow for your publication. Every time you move a new post idea into a list on your Trello board, it will automatically be sent to Ghost Admin, ready to be drafted and published.

Advanced action steps
---------------------

It’s possible to adapt the content that you send into Ghost via Zapier using one of the built-in transform functions such as the [formatter functions](https://zapier.com/help/how-use-formatter-functions/) or [code actions](https://zapier.com/apps/code/help). These options require a more involved setup, but allow you to extend the platform to do just about anything. For example, transform incorrect URLs or dates, convert data types and much more!

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

