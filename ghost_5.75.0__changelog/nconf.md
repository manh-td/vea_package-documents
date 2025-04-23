


Introducing nconf for configuration









































It seems these blog posts have become a Friday thing 😁 . Although it wasn't the original plan, Friday posts make for a more standard week. We're going to try to get into more of a rhythm and aim for lunch time 🍴. Any thoughts or questions? Let us know in the comments 📢

### What's occurring?

Whilst our public repositories have a bit of a 👻 🏘 (ghost town) feel this week, rest assured it's because our entire team is crazy busy working away behind the scenes on some internal, supporting projects. Ghost v1.0 is already packing some punch, so I thought this week I'd take this opportunity to cover one of the new developer features: our much improved config system.

Next week, the team is heading to Thailand for our biannual company retreat ✈️. Stay tuned for details of what we get up to!

#### Configuration with nconf

Ghost v1.0 has been in development for a couple of months now. In that time we've made some hefty changes, one of the most undocumented of which, is the change to our configuration system.

Originally, Ghost's config file was a `config.js` file located in the root directory, which contained configuration for the various environments. It was hard to override, and there wasn't much support for alternative configuration mechanisms such as command line flags or environment variables.

Enter [nconf](https://github.com/indexzero/nconf?ref=ghost.org) - this handly node library provides a simple way to support configuration via files, flags and env vars. In Ghost v1.0 you'll find a whole set of small `*.json` files in `core/server/config` and `core/server/config/env` that make up the base configuration. To add customisations, create a `config.<env>.json` file in the root of your Ghost install. Any of the settings can be overridden, except those in `overrides.json`.

So for example, let's imagine you've just cloned the Ghost repo to do some light hacking, but you want to have a subdirectory and use local password authentication instead of our new Ghost Auth service\*:

First, you'd create a new `config.development.json` file in your project root.

Then, open the file and add the following JSON:

```
{
    "url": "https://localhost:2368/blog",
    "auth": {
       "type": "password"
    }
}

```

The config options available for the url, database, etc are all much the same as they were previously, only in JSON format rather than a plain javascript file. The new `auth` config lets you switch between the new Ghost Auth service, and the old style password authentication [[1]](#fn1)[[2]](#fn2).

The important differences between the old and new config, are:

1. Make sure all strings, including keys, are surrounded by double quotes, else you'll get "unexpected token" errors.
2. Name your config file `config.<env>.json`, where `<env>` is one of `development` or `production` and the extension is `.json`, not `.js`.
3. There's only one set of config per file. If you need both a development and production config, provide them in two separate files.
4. Bonus: you *can* supply config via command line flags and environment variables, however until we have finished auditing the options and written up new documentation, you will need to use the [nconf docs](https://github.com/indexzero/nconf?ref=ghost.org) to figure out how to do this 🤔

**Got suggestions?**

So far, we've switched the underlying technology that drives our config. We still have an [open issue for v1.0](https://github.com/TryGhost/Ghost/issues/7488?ref=ghost.org) to revisit the config options that we provide. So, if you have ideas for configuration options you've always wished Ghost had, or a way to improve existing options, let us know on the issue or in the comments 💬

**Try it for yourself...**

If you haven't seen already, you can now install Ghost using our [CLI tool](https://ghost.org/docs/ghost-cli/?ref=ghost.org). Two quick commands: `npm install -g ghost-cli` to install the cli, change to an empty directory and run `ghost install local`. It takes seconds, and it sets up the initial config for you.

When it comes to tweaking the config, there are two ways to do it. The first is to run `ghost config`, which will prompt you for your url, and mysql credentials (this command is still a work in progress). The second is to manually edit the `config.development.json` file that will have been created by the install process.

Releases
--------

* Ghost-Desktop 1.1.0
* passport-ghost [2.0.0](https://github.com/TryGhost/passport-ghost/releases/tag/2.0.0?ref=ghost.org)
* Ignition [2.2.0](https://github.com/TryGhost/Ignition/releases/tag/2.2.0?ref=ghost.org)

Follow us!
----------

Want to find out more about Ghost development? Subscribe to the [updates feed](https://ghost.org/changelog/tag/updates/rss/) for to the [alpha feed](https://ghost.org/changelog/tag/alpha/rss/) if you're more interested in how v1.0 is progressing. Alternatively, follow us on [twitter](https://twitter.com/TryGhost_dev?ref=ghost.org) 🐦 or sign up to get our weekly newsletter in your inbox 📬.

---


1. As we're still actively developing Ghost Auth, it is currently the default option in development mode, however this will change to password based auth before v1.0 ships as it makes more sense for development blogs 🚢. [↩︎](#fnref1)
2. **Update 26th July 2016:** Ghost Auth was pulled from 1.0.0, and so for now password auth is again the only supported option. [↩︎](#fnref2)


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





 





 
















 






