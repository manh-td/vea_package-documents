


Ghost 0.8.0







































[Ghost 0.8.0](https://github.com/TryGhost/Ghost/releases/tag/0.8.0?ref=ghost.org) is now available on GitHub, npm and Ghost.org. Ghost 0.8.0 contains a major database upgrade, some breaking changes to the theme API and several new features for you to test out.

Highlights
----------

* **[New]** Subscribers (Beta) - enable in labs to collect email addresses from your blog
* **[New]** Slack integration - notify a slack channel whenever a new blog post is published
* **[New]** Twitter & Facebook support - add your social profiles to your blog and users, get a meta data boost
* **[New]** HTTP2 Preload headers - get super speed with CloudFlare
* **[Changed]** Image uploader - improved editor performance and a smoother upload experience
* **[Changed]** theme API **breaking changes** - [see here](https://ghost.org/changelog/get-your-theme-ready-for-0-8-0/) for the details
* **[Fixed]** Errors in JSON-LD structured data output on blog posts & author pages
* And much, much more...

You can see the [full change log](https://gist.github.com/ErisDS/9adeb395d3e8caec192622270600c8b1?ref=ghost.org) for the details of every change included in this release.

In Detail
---------

This release contains some new features and all of the theming & API tools needed to make the most of them.

The new slack integration allows you to automatically post to slack when a post is published. This feature will likely move to an internal app, and then a default installed external app over the coming months. This is our first experiment with integrations and we're looking to do more.

The subscribers feature is implemented, as much as possible, as an internal app. The tools it provides, such as the subscribe page, theme helpers & API endpoint, are only available when the feature is enabled in labs and there's a new helper for detecting if it is enabled from within a theme as well. See the [support guide](https://ghost.org/help/members-introduction/?ref=ghost.org) and [theme docs](https://ghost.org/docs/themes/members/?ref=ghost.org) for more details.

Twitter & facebook fields have been added both to users, and to the general settings screen. These store only the unique part of the URL - the twitter username and facebook page name or username. These values are available via the API and also in themes, where helpers have been added to create URLs.

Support for HTTP2 Preload headers have been added, but are currently off by default. To enable them, you need to set `preloadHeaders` to a numerical value in your `config.js` file, where the value represents the number of entries stored in the cache: e.g.

```
production: {
  url: 'https://my-ghost-blog.com',
  preloadHeaders: 100,
  ...
}

```

Long term, this feature will likely be enabled by default. Short term, users on Ghost(Pro) can contact [support@ghost.org](mailto:support@ghost.org) to ask for this feature to be enabled.

### Theme API Changes

**Breaking Changes**

The breaking changes to the theme API are explained in detail in [this blog post](https://ghost.org/changelog/get-your-theme-ready-for-0-8-0/).

**Other Changes**

The theme API has a few additions in 0.8.0 in line with the new feature additions:

* The new `{{@labs}}` global allows you to detect if a labs feature is enabled.
* Both `{{@blog}}` and `{{author}}` now have `twitter` and `facebook` properties which contain the unique username / page name provided in the admin panel. Two new helpers: `{{facebook_url}}` and `{{twitter_url}}` have been added to make it easy to convert the usernames into full URLs in themes.
* You can now add a new `subscribe.hbs` template to override the one provided by Ghost when the subscribers feature is enabled in labs. This comes with a full suite of helpers such as `{{subscribe_form}}` as well as adding a new context.

See the [theme API docs](https://ghost.org/docs/changes/?ref=ghost.org) for full details of what changed in Ghost 0.8.0. The theme documentation is frequently updated with more details and better examples. Please also use the **suggest edits** feature if you find something is missing or out of date.

### Public API Changes

The addition (and removal) of several new database fields in Ghost 0.8.0 will result in minor changes to the Public API:

* posts, tags and users all now have a `visibility` field
* tags no longer have a `hidden` field
* users & settings contains a `twitter` & `facebook` field
* posts have a currently unused `mobiledoc` field

As the hidden field was not yet in use, this is not expected to result in any breaking changes.

How to Upgrade
--------------

All Ghost(Pro) users are being **automatically updated** and will be running Ghost 0.8.0 shortly. You're welcome :)

For people running Ghost on their own servers, you can [download Ghost 0.8.0](https://ghost.org/docs/?ref=ghost.org) and then check out the [upgrade documentation](https://ghost.org/docs/update/?ref=ghost.org) over on our [support site](https://ghost.org/help/?ref=ghost.org).

Enjoy!

Credits
-------

This release was lovingly crafted by Hannah Wolfe, Kevin Ansfield, Austin Burdine, Katharina Irrgang, Aileen Nowak, Jason Williams, Joerg Henning, Sebastian Gierlinger, Terin Stock, David Balderston and Brian Tedder.


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





 





 
















 






