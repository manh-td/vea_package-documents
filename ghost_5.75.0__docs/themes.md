Ghost Handlebars Themes - Building a custom Ghost theme - Docs
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

The Ghost theme layer has been engineered to give developers and designers the flexibility to build custom publications that are powered by the Ghost platform.

Theme development
-----------------

Ghost themes use the Handlebars templating language which creates a strong separation between templates (the HTML) and any JavaScript logic with the use of helpers. This allows themes to be super fast, with a dynamic client side app, and server side publication content that is sent to the browser as static HTML.

Ghost also makes use of an additional library called `express-hbs` which adds some additional features to Handlebars, such as layouts and partials.

If you’ve previously built themes for other popular platforms, working with the Ghost theme layer is extremely accessible. This documentation gives you the tools required to create static HTML and CSS for a theme, using Handlebars expressions when you need to render dynamic data.

Our tutorial on the [essential concepts to known when building a Ghost theme](https://ghost.org/tutorials/essential-concepts/), provides a fantastic introduction to everything you need to know to start building beautiful themes.

Handlebars
----------

The Handlebars templating language provides the power to build semantic templates effectively.

* [Handlebars documentation](https://handlebarsjs.com/guide/expressions.html)

Installation of Handlebars is already done for you in Ghost ✨

Custom settings
---------------

Offering customization options to theme users can be done using custom settings. This allows theme developers to empower non-developers to make controlled changes.

Head to the [Custom settings documentation](/docs/themes/custom-settings/) to learn more.

GScan
-----

Validating your Ghost theme is handled efficiently with the [GScan tool](https://gscan.ghost.org/). GScan will check your theme for errors, deprecations and compatibility issues.

* The [GScan site](https://gscan.ghost.org/) is your first port of call to test any themes that you’re building to get a full validation report
* When a theme is uploaded in Ghost admin, it will automatically be checked with `gscan` and any fatal errors will prevent the theme from being used
* `gscan` is also used as a command line tool

### Command line

To use GScan as a command line tool, globally install the `gscan` npm package:

```
# Install the npm package
npm install -g gscan
# Use gscan <file path> anywhere to run gscan against a folder
gscan /path/to/ghost/content/themes/casper
# Run gscan on a zip file
gscan -z /path/to/download/theme.zip

```

What’s next?
------------

That’s all of the background context required to get started. From here, take a look at the [structure](/docs/themes/structure/) of Ghost themes and templates, and learn everything you need to know about the `package.json` file.

For community led support about theme development, visit [the forum](https://forum.ghost.org/c/themes/).

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

