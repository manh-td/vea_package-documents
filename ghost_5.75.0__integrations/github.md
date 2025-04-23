Official Ghost + GitHub Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Zapier](/images/logos/integrations/zapier_hu76c04ccfd9407fb306e44c2572d39c65_1450_50x0_resize_q100_h2_box_3.webp)Zapier](/integrations/zapier/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![Netlify](/images/logos/integrations/netlify_hu1b4209e1158b533f7cea6d5e486e460d_36182_50x0_resize_q100_h2_box_3.webp)Netlify](/integrations/netlify/)
* [![Raycast](/images/logos/integrations/raycast.svg)Raycast](/integrations/raycast/)
* [![Buffer](/images/logos/integrations/buffer_hu2190af463302b978f69c864b508a1040_12312_50x0_resize_q100_h2_box_3.webp)Buffer](/integrations/buffer/)
[Integrations](/integrations/)
/
[Automation](/integrations/?tag=Automation)

Set up simple continuous integration of your Ghost theme to deploy directly to your Ghost website with [GitHub Actions](https://github.com/features/actions). Share code snippets with [GitHub Gists](https://gist.github.com/).

Use GitHub Actions to deploy your theme
---------------------------------------

GitHub Actions allow you to build simple automation on top of any repository, including running a build command on a theme and pushing the compiled zip file to the Ghost Admin API.

### Create a new Ghost custom integration

In Ghost Admin, navigate to **Integrations** and create a new custom integration called **GitHub Actions**:

![](/images/integrations/github-custom-integration_hu3bc328918044c8950b03c14ae184532a_85071_1668x0_resize_q100_h2_box_3.webp)
### Set your Ghost integration credentials in GitHub

Next, copy and paste your integration details into your GitHub repository’s secrets. You can find these under **Settings** → **Secrets and variables** → **Actions**.

![](/images/integrations/github-secrets_hub68cf85b270cab31f74f5039cf79ed4c_170114_1284x0_resize_q100_h2_box_3.webp)

Create one secret called `GHOST_ADMIN_API_URL` with the **API URL** from your custom integration and another secret called `GHOST_ADMIN_API_KEY` with the **Admin API Key** from your custom integration.

### Install the Ghost Theme Deploy Action

Last step! Copy and paste the following code into a new file in your repository under `.github/workflows/deploy-theme.yml` - this will automatically use the official [Ghost GitHub Action](https://github.com/marketplace/actions/deploy-ghost-theme) from GitHub’s Marketplace:

```
name: Deploy Theme
on:
  push:
    branches:
      - master
      - main
jobs:
  deploy:
    runs-on: ubuntu-22.04
    steps:
      - uses: actions/checkout@v3
      - name: Deploy Ghost Theme
        uses: TryGhost/action-deploy-theme@v1
        with:
          api-url: ${{ secrets.GHOST_ADMIN_API_URL }}
          api-key: ${{ secrets.GHOST_ADMIN_API_KEY }}

```

Now, every time you push changes to your theme repository, your theme will automatically build and deploy to Ghost Admin.

Navigate to **Settings** → **Theme** in Ghost Admin to make sure that the theme you’re uploading from GitHub is the currently active theme, and you should be all set!

---

Use GitHub Gists to share code snippets
---------------------------------------

[GitHub Gists](https://gist.github.com) are a simple way of sharing code snippets with other developers. Once you’ve created a new public Gist, it will be available to be shared with others.

![](/images/integrations/Creating-a-Gist_hub8da29b5d9669ec306af3ac5d3174d09_181447_2060x0_resize_q100_h2_box_3.webp)
### Grab the embed code

To share a Gist in Ghost, locate the embed option from the dropdown in the top navigation and copy the HTML embed code to your clipboard:

![](/images/integrations/Gist-embed-code-1_hu669c0a0d6696b82e108cf9e093da1f4c_79471_1600x0_resize_q100_h2_box_3.webp)
### Paste it into a HTML card in the editor

Create a new HTML block in the Ghost editor on the post you would like to embed your code snippet and paste in the embed code.

![](/images/integrations/Ghost-cards_huedc570934e065d9fb5514b16c7852436_24138_1872x0_resize_q100_h2_box_3.webp)
### Publish your post

That’s all there is to it! Ghost allows you to paste embed code directly into the HTML block to share a Gist code snippet with your readers.

This is the quickest way to embed a Gist in Ghost. If you’re using the default theme, Casper, then this will look great without further styling. For other themes, you may want to make some styling adjustments in your theme.

Here’s an example of the end result:

Do more with Zapier
-------------------

Power up your site even further using [Zapier](https://zapier.com). If you’re already using GitHub, then you might also like some of these complimentary automations:

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

