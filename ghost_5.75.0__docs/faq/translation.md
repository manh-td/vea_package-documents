A guide to translation and internationalization in Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Creators from all over the world use Ghost. Publications abound in German, French, Spanish, Sinhalese, and Arabic—and the list keeps going!

Below, we have collected together essential concepts, strategies, and known limitations when working with languages other than English in Ghost.

Theme translation
-----------------

Ghost fully supports the ability to translate themes into different languages. This means that text in a theme is translated based on the language set in Ghost Admin.

![Choose publication language in Ghost Admin](/images/docs/faq/publication-language_hu12bd91634ea8eca345aacde59c0bf609_192891_1392x0_resize_q100_h2_box_3.webp)

Theme developers can use the `translate` helper to make a theme translatable—see [our docs](https://ghost.org/docs/themes/helpers/translate/) for instructions on usage and examples.

Some premium themes—like [Tripoli](https://ghost.org/themes/tripoli/), [Galerie](https://ghost.org/themes/galerie/), and [Basho](https://ghost.org/themes/basho/)—include translation support out of the box.

Best practices and strategies
-----------------------------

Some of the complexity involved in building Ghost sites in languages other than English can be lessened by implementing the following best practices and strategies:

* Keep hardcoded text to a minimum. The less hardcoded text in a theme, the less there is to translate. For example, instead of having “by” and “por” in the byline, consider just listing the author’s name.
* Use [custom theme settings](https://ghost.org/docs/themes/custom-settings/) to allow your users to translate text themselves.
* Create multiple newsletters to target different languages.

UI translations
---------------

Ghost has native support for translated system text in transactional emails, the Portal membership system, search, and comments.

*Ghost Admin does not yet support internationalization.*

Multi-language content
----------------------

A multi-language content site supports multiple languages at the same time, like publishing in Spanish and English.

If you plan on publishing different content in each language, we recommend one Ghost install per language. Our experience shows that this approach is not only the easiest to get off the ground, but it’s also the most sustainable long-term.

If you’re publishing the same content in different languages, then we recommend using a service like [WeGlot](https://ghost.org/integrations/weglot/) or [Transifex](https://ghost.org/integrations/transifex/).

Note that the `translate` helper mentioned above **doesn’t work** for multi-language content sites, as its purpose is entirely different.

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

