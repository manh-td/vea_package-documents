


1.0.0 Beta is out!






































After **21** alpha releases, we just released the first 1.0 beta version 😀.

Please read the [previous post](https://ghost.org/changelog/lts/) about the difference between 1.0 and LTS. The official support for LTS will end on the **31st of August 2017**.

How to install the beta?
------------------------

The [Ghost-CLI](https://github.com/TryGhost/Ghost-CLI?ref=ghost.org) is the recommended way to install Ghost 1.0 beta, but it's not yet suitable for production.

We already mentioned in a [previous post](https://ghost.org/changelog/alpha-9-objectid-cli/), which system stack we recommend. The CLI is able to setup NGINX and SSL for you **soon** - pretty cool, hm? 🙃

We've created a new [Ghost CLI install guide](https://ghost.org/docs/install/?ref=ghost.org) that covers installing Ghost via the CLI.

Migration from LTS to 1.0 beta
------------------------------

We have written a [1.0 migration guide](https://ghost.org/docs/update/?ref=ghost.org) for migrating from LTS to 1.0 beta. You basically have to install the 1.0 beta via the CLI, export your LTS database via the admin panel and import the file into the 1.0 blog.

Breaking changes
----------------

Here is an overview of the **most important** breaking changes. Lay back and enjoy!

### ghost.org/docs

We have removed our Github wiki and disabled support.ghost.org, both now live now at **[https://ghost.org/docs/](https://ghost.org/docs/?ref=ghost.org)**. Having a centralised place for all our documentation is very useful. The documentation is for self hosters, theme developers and contributors - if you notice anything missing please let us know!

The new docs are hosted on readme.io so please send us suggestions if you notice anything that's incorrect or confusing.

### A new editor

Ghost 1.0 is sticking with a markdown-only editor for now (although it saves to [mobiledoc](https://github.com/bustle/mobiledoc-kit/blob/master/MOBILEDOC.md?ref=ghost.org) format internally for future extensibility) but that doesn't mean the editor experience has stood still.

The key changes:

* there's a toolbar!
* the editor pane shows formatting directly rather than requiring a preview pane to give a less cluttered writing experience (don't worry, there's still a split-pane editor too for the full markdown preview)
* image uploads are now initiated directly from the toolbar or by dragging and dropping images onto the editor pane (and yes, it supports multiple images at once!)
* we now use [markdown-it](https://github.com/markdown-it/markdown-it?ref=ghost.org) instead of a very old customised version of Showdown fixing a lot of annoying markdown rendering bugs

### 1.0 Themes

If you import a theme, which worked on 0.11.9, it **might** not work with 1.0 anymore because there have been couple of breaking changes in the theme API. However there are tons of themes which will still work.

To improve the migration experience when you upload your theme into Ghost 1.0 beta and it fails to import, it will show you a detailed report of why the import failed.

As a theme developer you can use [gscan](https://gscan.ghost.org/?ref=ghost.org) to find out what adaptations you have to make for your theme to work with 1.0 beta.

Here is an overview of what has changed:

* `package.json` is required and must contain a valid name, version and an author email address ([docs](https://ghost.org/docs/themes/structure/?ref=ghost.org#packagejson))
* the `{{image}}` helper was removed
* therefore we have added a `{{img_url}}` helper ([docs](https://ghost.org/docs/themes/helpers/img_url/?ref=ghost.org))
* `{{pageUrl}}` helper was renamed to `{{page_url}}` helper ([docs](https://ghost.org/docs/themes/helpers/pagination/?ref=ghost.org))
* `{{meta_description}}` in `<head>` is not allowed anymore
* use `@config.posts_per_page` instead of `@blog.posts_per_page`
* you can define `posts_per_page` in your theme `package.json` ([see](https://ghost.org/docs/themes/structure/?ref=ghost.org#packagejson))
* `{{content words="0"}}` does not work anymore, use `{{img_url}}` instead
* we renamed some css classes ([docs](https://ghost.org/docs/themes/helpers/img_url/?ref=ghost.org))

Please read through the [1.0 theme documentation](https://ghost.org/docs/themes/?ref=ghost.org) for full details.

### Configuration with nconf

The old `config.js` file will no longer work. Instead we have added [nconf](https://github.com/indexzero/nconf?ref=ghost.org) as configuration management tool.

Checkout our [configuration documentation](https://ghost.org/docs/ghost-cli/?ref=ghost.org) or the [previous post](https://ghost.org/changelog/nconf/) about using nconf.

### Storage adapters

The location of storage adapters has changed and we added proper class inheritance. The base adapter was extracted to it's own npm module and now lives [here](https://github.com/TryGhost/Ghost-Storage-Base?ref=ghost.org).

If you made use of a custom storage adapter in the past, this adapter won't work anymore. The maintainer will need to update it for 1.0.

Further details are available [here](https://ghost.org/integrations/?tag=Storage&ref=ghost.org).

### A new migration tool

Before 1.0, the database population and migration were part of Ghost core itself. The logic was [extracted](https://github.com/TryGhost/knex-migrator?ref=ghost.org) and lives in it's own npm module.

When installing or using Ghost 1.0 regularly, the Ghost CLI takes care of **any** database upgrades. You don't have to execute any extra command.

However, in case you would like to manually re-initialise your database or test the new migration tool, please read more about it [here](https://ghost.org/docs/ghost-cli/?ref=ghost.org).

Beta tester
-----------

We are very happy about beta testers and **any** feedback is **very** welcome. If you find a bug, please raise it on our [Github repository](https://github.com/TryGhost/Ghost/issues?ref=ghost.org). If you have any questions or problems with installing the 1.0 beta, please swing by our [forum](https://forum.ghost.org/?ref=ghost.org) and say hello 🙃.

What's next?
------------

The official release of 1.0 depends on the number of bugs and feedback we get back during the beta. We would like to release it as soon as possible to concentrate on the next features so if you are able to test it please do!

Final things that didn't quite make the beta cut but are expected to be in the final 1.0 release:

* we have welcomed a [new contributor](https://github.com/juan-g?ref=ghost.org), who has implemented the [i18n (translation) for themes](https://github.com/TryGhost/Ghost/issues/5345?ref=ghost.org)


### Get notified when we ship new features.






 
### You might also like...

Apr

08


![Custom content for every subscriber](/changelog/content/images/size/w750/2025/04/Ghost-Call-to-action-card.png)

Custom content for every subscriber
-----------------------------------

Calls to Action got an upgrade, now you can fine-tune the design and who sees them in more detail.
Apr 8, 2025


New





 
Apr

01


![Social web (beta)](/changelog/content/images/size/w750/2025/04/image--1-.png)

Social web (beta)
-----------------

Increase your reach by connecting your publication to the Fediverse
Apr 1, 2025


Beta





 





 
















 






