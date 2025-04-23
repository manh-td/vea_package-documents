Official Ghost + Google Docs Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Ulysses](/images/logos/integrations/ulysses_hu89ac0130727389662312f692acb35eb9_44367_50x0_resize_q100_h2_box_3.webp)Ulysses](/integrations/ulysses/)
* [![iA Writer](/images/logos/integrations/iawriter_hu5342b37a24a825d9c0811df1cdac773a_3726_50x0_resize_q100_h2_box.webp)iA Writer](/integrations/ia-writer/)
* [![Setka Editor](/images/logos/integrations/setka_hu0bd831be49a95b64fe5cb9f6b567b0e3_4268_50x0_resize_q100_h2_box_3.webp)Setka Editor](/integrations/setka/)
* [![Ghost Bookmarker](/images/logos/integrations/google-chrome_hu2f6e18ea46f665f63682403bf03b5d37_26870_50x0_resize_q100_h2_box_3.webp)Ghost Bookmarker](/integrations/bookmarker/)
[Integrations](/integrations/)
/
[Writing](/integrations/?tag=Writing)

Create and collaborate on your content using Google Docs and then send it directly to your Ghost publication with a powerful, time-saving automation

Google Docs is a popular browser-based writing tool that allows writers and editors to create, collaborate and store content effectively. If you enjoy writing in Google Docs, it’s possible to create a custom integration via Zapier that will send your writing directly into your Ghost publication, including any formatting.

Here’s how it works:

Create a new Zap
----------------

For this integration you’ll be using [Zapier](https://www.zapier.com). If you don’t already have an account, create one now, login and create a new Zap:

![](/images/integrations/Create-a-zap_hu6ffeb98fbb95754cc64534518342808e_131060_2044x0_resize_q100_h2_box_3.webp)

Create a new Google folder
--------------------------

Create a new folder in your Google Drive account where you’d like to store content that will be sent to your Ghost site. If you’re creating a brand new folder, it’s also important to create a test document in here so that Zapier has access to some data for testing purposes.

![](/images/integrations/Google-Drive-1_hu4ce9e4e026fa00e6f1a0fdc1cc7fe9f4_131065_1830x0_resize_q100_h2_box_3.webp)

Add Google Docs as the Trigger
------------------------------

Back in Zapier, add Google Docs as the initial Trigger step:

![](/images/integrations/Google-Docs-trigger-step_hu78babdf249971e04d01b2895e0a3d77b_170409_2098x0_resize_q100_h2_box_3.webp)

In order to do this, sign in to your Google account to grant access to Zapier, and use the “New Document in Folder” option. Then select the folder you just created for your Ghost content. Before continuing to the next step, Zapier will search for a sample document in your folder:

![](/images/integrations/Zapier-pick-a-sample-google-docs_hu16cc44a864645fea0847d29fe4585806_46660_1234x0_resize_q100_h2_box_3.webp)

Add Ghost as the Action Step
----------------------------

Next you’ll be prompted to add an action step. Search for Ghost and connect your site using your Admin API URL and API key. This information can be found in the Integrations section within Ghost Admin, on the Zapier page:

![](/images/integrations/Zapier-Access-to-Ghost_huadafad7560db892cac53cf4a8eab5a97_69643_1842x0_resize_q100_h2_box_3.webp)

Once access has been granted, Zapier allows you to run a quick test to ensure a connection has been established.

![](/images/integrations/Test-Ghost-in-zapier_hu4435aca5e1e6a4f77309fec2283a45d6_35822_1228x0_resize_q100_h2_box_3.webp)

Now you can customise your post template by filling in the required fields provided:

![](/images/integrations/Create-a-template_hu39cd8a87a63b741729e456782886c33b_237423_2056x0_resize_q100_h2_box_3.webp)
### The required fields are:

* `Title` – Use the Google Docs title
* `Status` – Select whether your writing will be sent to Ghost as drafts, published or scheduled
* `Content format` - Use HTML for this integration
* `Content (HTML)` - Select `File Raw HTML Content` in order for your Google Docs content to parse correctly in the Ghost editor
* `Authors` - Select at least one author for your post using the dropdown menu

Optionally, add some tag(s) to your workflow by using the dropdown menu to select tags that exist on your Ghost site.

Test & Publish your integration
-------------------------------

Once you’re happy with your integration setup, test it from within the Zapier dashboard and ensure everything is working as it should. When you’re ready, publish your Zap ⚡

![](/images/integrations/Zap-is-turned-on---google-docs-and-ghost-integration_huab42ab0914229e0ce55e1c3497b07fc4_32803_1226x0_resize_q100_h2_box_3.webp)

Congrats – you’ve just unlocked a new, powerful workflow for your publication. Every time you move a new Google Docs file into your Ghost folder, it will automatically be sent to Ghost Admin as a new post.

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

