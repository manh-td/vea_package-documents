


Ghost 1.0.0 - React, redux and redis??








































*jk lol* 🤓 *here's what really happened...*

[Ghost 1.0.0](https://github.com/TryGhost/Ghost/releases/tag/1.0.0?ref=ghost.org) is now available on GitHub, npm and Ghost.org.

No seriously. It's done! In fact... there's a 1.0.2 😬!

Highlights
----------

* **[New]** Editor, default theme, new user tour, nightshift mode, and many other admin improvements. More details in the announcement blog post [here](https://ghost.org/changelog/1-0/)
* **[New]** Config with [nconf](https://github.com/indexzero/nconf?ref=ghost.org), logging with [bunyan](https://github.com/trentm/node-bunyan?ref=ghost.org), and debug output using [debug](https://github.com/visionmedia/debug?ref=ghost.org).
* **[Improved]** Publish menu which brings scheduling front and centre, instead of it being an after thought
* **[Improved]** Simplified content screen with filtering makes it easier to find
* **[Improved]** The importer has had a complete overhaul, is now more robust and outputs much, much better error & warning messages when things do go awry
* **[Changed]** Internal tags is no longer in labs, and the Public API Beta is now enabled by default (we're getting there!)
* **[Changed]** Various aspects of the Theme API, see the [theme changelog](https://ghost.org/docs/themes/?ref=ghost.org) for more details...
* **[Fixed]** Addressed many issues with session handling, so you get logged out far less often or maybe even not at all
* And much, much, much more...

You can see the [full change log](https://gist.github.com/kevinansfield/44cca4727892fcfc9e4d9a1aeab97dcc?ref=ghost.org) for the details of all changes included in this release.

In Detail
---------

Ok everyone, grab yourself a coffee and settle down - this is gonna be a big one! ☕️

Ghost 1.0.0 is a major rework and as a result there are a plethora of developer-facing changes that should make both our, and *your* life easier. Here's the ins and outs of what's changed...

### Simplifying Installs & Upgrades

We always dreamed of a Ghost that was easy to install & upgrade. This was the original thought behind picking SQLite3 - no need to configure or setup databases. Unfortunately the binary dependency has always caused more problems than we ultimately solved.

Time for an entirely new approach & the introduction of [Ghost CLI](https://ghost.org/docs/ghost-cli/?ref=ghost.org).

The main aim of Ghost CLI is to make it possible to install and update Ghost with a *single command*.

To achieve this, we've simplified things and focused on creating a single path to success, with a [recommended stack](https://ghost.org/docs/hosting/?ref=ghost.org) that should always result in a smooth, robust install & upgrade process.

The TL;DR instructions for Ghost-CLI are:

* on your server, with a non-root user, run
* `sudo npm install -g ghost-cli`
* in an empty folder, run
* `ghost install`
* fill out the info you are prompted for
* the end 💥

When a new version of Ghost is released, you'll be able to upgrade by going to your ghost directory and running `ghost update`.

The [developer docs](https://ghost.org/docs/?ref=ghost.org) feature a full step-by-step guide to preparing your server and getting Ghost [installed](https://ghost.org/docs/install/?ref=ghost.org) as well as a [cli reference guide](https://ghost.org/docs/ghost-cli/?ref=ghost.org) and details of [the configuration](https://ghost.org/docs/config/?ref=ghost.org) options available to you.

### Rethinking Databases

As I mentioned earlier, one of the biggest drivers for using SQLite3 was to make Ghost installs easy. With the introduction of Ghost CLI we now have a new approach, and had the opportunity to rethink our database support.

As of Ghost 1.0.0 we no longer support PostgreSQL. This change was explained in detail in [this blog post](https://ghost.org/changelog/dropping-support-for-postgresql/), the TL;DR being that the maintenance overhead was too high.

We are also now defaulting to MySQL for production blogs as a future-proofing measure. Ghost works great on SQLite3 right now, however we envisage building features that will be better suited to MySQL.  SQLite3 is still available as a development option.

If you inspect your database in Ghost 1.0.0 you may also notice that we've switched away from using standard auto-incrementing integer IDs to using ObjectID for all primary keys. ObjectID comes from MongoDB and creates a 24-char unique sequential string ID. This provides many benefits, including making it easier to replicate databases, providing us some interesting options for handling import/exports and much more.

We've also moved a lot of the migration and initialisation code out of Ghost itself and into [knex-migrator](https://github.com/TryGhost/knex-migrator?ref=ghost.org). A command line tool that makes it easy to reset, initialise & migrate databases. Ghost CLI uses this tool, but if you're doing manual installs or contributing, you'll need to install it in order to manage your databases 💾 .

### Overhaul of core tooling

Inside of Ghost itself, we've replaced and improved the core tooling to make it easier to both configure and debug.

#### Config with nconf

One of the biggest changes that self-hosters will encounter with Ghost 1.0.0 is the change to using [nconf](https://www.npmjs.com/package/nconf?ref=ghost.org) for configuration. Gone is the old `config.js` file with multiple environments in one file, and in its place are shiny new `config.[env].json` files, which are only required if you need to override the defaults and so are no longer generated by Ghost.

Ghost CLI will automatically create any config files that you need. If you're installing without Ghost CLI or developing on Ghost core you may need to create a `config.development.json` or `config.production.json` file in the root of Ghost.

The default configuration for Ghost lives in [/core/server/config](https://github.com/TryGhost/Ghost/tree/master/core/server/config?ref=ghost.org), but you should never edit these core files. Always create your own config file in the Ghost root folder. There are more details of how configuration has changed in the [nconf blog post](https://ghost.org/changelog/nconf/) and in the [config docs](https://ghost.org/docs/config/?ref=ghost.org).

#### Logging & Debugging

We have added a much better system for logging, using [bunyan](https://github.com/trentm/node-bunyan?ref=ghost.org) to create configurable logging output. By default in development mode, Ghost will output to stdout and stderr. In production mode, log files will be written to `/content/logs`. All of this behaviour is [configurable](https://ghost.org/docs/config/?ref=ghost.org#section-logging).

We are also now using the popular [debug module](https://github.com/visionmedia/debug?ref=ghost.org) in Ghost, which is also used by several of our dependencies. If you're trying to debug Ghost, you can start it with the debug environment variable set, E.g. `DEBUG=ghost:*` or `DEBUG=*` to get additional output.

### Errors

Although less visible, we have also overhauled our error objects in 1.0.0. We now have a GhostError class with extended properties, and all other types of error extend this. This allows us to provide more detailed and consistent error messages throughout Ghost.

Many of these changes - logging, debug and errors - are being provided through a new module called [Ignition](https://github.com/TryGhost/Ignition?ref=ghost.org), which is a collection of reusable tools that we are using across multiple projects (including Ghost, Ghost-CLI & GScan) to provide consistency. Ignition also provides a generalised wrapper for nconf that is used in several projects but not Ghost, which has a slightly special setup ✨.

### Better structure

Ghost's server side now has the admin, API and blog frontend split into 3 separate express apps each with their own middleware, routes and error handling. This will reduce weird bugs and regressions and make it far easier for us to add new features.

In addition, we've now been able to fully separate the Ghost-Admin Ember.js app so that it is no longer dependent on Ghost injecting data into the base template 🤓. This means that developers can run the Ember.js app independently with full support for tests and live reload. Everything a Ghost client needs is now fully provided via the API, which gives us lots of scope for the future.

In Ghost-Admin, the underlying code has been heavily componentised and reusable data like settings & config have been moved into synchronous services. This significantly reduces complexity in the codebase, and should result in fewer regressions.

We've also added proper loading states and unified our networking, so all calls go through our own ajax service instead of being split between custom ajax and ember data. Meanwhile, we've upgraded through 6 major Ember.js versions and we've switched to using SVG icons to improve performance.

We have also upgraded the concept of adapters to a first class citizen. Custom storage or scheduling adapters can be added in `/content/adapters/`, more information about that [here](https://github.com/TryGhost/Ghost/tree/master/content/adapters?ref=ghost.org). We'll be using adapters to improve our email support in future, and making it possible to install them with Ghost CLI. Awesome things are coming 🦄 !

### New Editor and the API

As explained in the [announcement post](https://ghost.org/changelog/1-0/) the new editor is based on the [MobileDoc](https://github.com/bustle/mobiledoc-kit?ref=ghost.org) format. After extensive research, we decided that the most important factor in any WYSIWYG editor is the underlying data format. This change is explained in detail in the [original issue](https://github.com/TryGhost/Ghost/issues/7429?ref=ghost.org).

MobileDoc is a great example of collaborative Open Source development in action. It's an MIT project being worked on by [Bustle](https://www.bustle.com/?ref=ghost.org), [Ghost](https://ghost.org/?ref=ghost.org), [201Created](https://www.201-created.com/?ref=ghost.org), and a number of other [contributors](https://github.com/bustle/mobiledoc-kit/graphs/contributors?ref=ghost.org). Every time one of us makes an improvement, everyone benefits.

It's a great shame when multiple open source projects end up developing the same functionality due to hostile license choices - and this is often the case with editors. Our biggest hope is that more open source applications are able to take our work from both MobileDoc and Koenig and freely benefit from using it in their projects.

### Public API Changes

From Ghost 1.0.0 the Public API Beta feature is enabled by default. This is a step towards moving it out of labs, please let us know if you find any problems and please be aware there *will* be one last set of [breaking changes](https://github.com/TryGhost/Ghost/issues/8605?ref=ghost.org) when we do finally move it out of beta.

Note: If you're using the Public API on a 3rd party site you will need to update your site after upgrading to Ghost 1.0.0 so that it is still able to pull data from your Ghost site. See the [API migration guide](https://ghost.org/docs/update/?ref=ghost.org) for the details.

There are also several changes to the fields & resources provided by the API. With the new editor, the `markdown` field has been removed in favour of a new `mobiledoc` field, which you can read more about in the [API docs](https://ghost.org/docs/concepts/posts/?ref=ghost.org#document-storage). We also introduced a new `plaintext` field added a new `formats` param to the posts API, to make it possible to select which formats, E.g. html, plaintext, mobiledoc, that you want to fetch.

In addition, each image field that was called simply `image` or `cover` has been renamed to be more descriptive, E.g. posts image is now called `feature_image`. The unused `language` field that appeared on posts and users was renamed to `locale`. Users now have a `last_seen` instead of a `last_login` and invited users are no longer stored in the `users` table until they accept their invite - they live in the `invites` table instead.

### Theme API Changes

Themes have had a lot of love in 1.0.0 ❤️. All of the code for managing, uploading and activating themes has been rewritten and moved to a single [location](https://github.com/TryGhost/Ghost/tree/master/core/server/themes?ref=ghost.org) & this coupled with the express app restructuring should help to reduce the number of cache related theme issues.

We also now validate all themes using [GScan](https://github.com/TryGhost/gscan?ref=ghost.org). GScan is a tool which runs a set of checks to make sure a theme will work before it is activated. You can always test a theme by visiting [https://gscan.ghost.org](https://gscan.ghost.org/?ref=ghost.org) and uploading it there first or by installing gscan on your machine and using it as a [cli tool](https://github.com/TryGhost/gscan?ref=ghost.org#cli-usage).

There are quite a few changes to the theme API in Ghost 1.0, most notably removing features that were previously deprecated, changing the names of image-related properties and introducing the concept of theme config.

The [theme changelog](https://ghost.org/docs/themes/?ref=ghost.org) has full details of what has changed, and the [theme migration guide](https://ghost.org/docs/update/?ref=ghost.org) will talk you through step by step how to update your theme for 1.0.

### Developer tooling

All Ghost & Ghost-Admin dependency management is now done with [yarn](https://yarnpkg.com/lang/en/?ref=ghost.org), which is not only much faster, but also gives us reliable idempotent installs.

Lastly, we've switched our recommended Node.js version to the **Node.js v6 LTS** and suggest using at least **v6.11.1**. We highly recommend upgrading to v6 before installing 1.0.0, if you haven't already. The docs have full details of our  [supported Node.js versions](https://ghost.org/docs/faq/node-versions/?ref=ghost.org).

How to upgrade to Ghost 1.0
---------------------------

This is our first major release which breaks backwards compatibility, so the upgrade process is more involved than usual.

**If you don't have a Ghost site:** Try it out for free with our [14 day trial on Ghost(Pro)](https://ghost.org/pricing/?ref=ghost.org). All new sites automatically run on Ghost 1.0.

**If you have an existing Ghost(Pro) site:** The upgrade process will be mostly automated for you, with a couple of steps. We're upgrading people in batches over the coming weeks and once your account is ready to be migrated, you'll see an "Upgrade to Ghost 1.0" button when you log into Ghost.org, with instructions for what to do next.

![](https://ghost.org/changelog/content/images/2021/01/upgrade.png)

**If you self-host Ghost:** You will need to set up a new Ghost 1.0 install, and export/import your content over. We've put together [a full migration guide](https://ghost.org/docs/update/?ref=ghost.org) which should help.

Because the upgrade process is more complex this time around, we've marked Ghost 0.11 as a Long Term Support (LTS) release. We will continue to provide maintenance and security updates for Ghost 0.11 for the next 6 months.

Credits
-------

This release was lovingly crafted by Kevin Ansfield, Katharina Irrgang, Hannah Wolfe, Aileen Nowak, Austin Burdine, John O'Nolan, David Wolfe, Ryan McCarvill, Tobias Bieniek, Vivek Kannan, Patrick Kim, Sebastian Gierlinger, Kenneth Ashley, John O'Mahoney, Felix Rieseberg, vitalie maldur, sahand12, janvt, ivan sebastian, Rodney Folz, Rei, Rabbi Hossain, Myles Braithwaite, Matt Enlow, Marc Bachmann, Jimmy Cai, Gabor Javorszky, Fixer, David Balderston, Cezary Kluczyński, Ben Vibhagool and André Borud.

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





 





 
















 






