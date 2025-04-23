


New for themes in 0.4.2






































There's an exciting release just around the corner - Ghost 0.4.2 is scheduled for release this week - likely the 25th March.

Usually, patch releases contain little more than a few bug fixes and refactors, but in this case, we're taking advantage of being pre 1.0 and pushing out some serious features in 0.4.2. The majority of these features will impact on theme and other developers.

New features
------------

### package.json

Ghost themes now support having a [package.json](https://www.npmjs.org/doc/json.html?ref=ghost.org) file. At the bare minimum, this file needs to contain a `name` and `version` number, which will be used in the Ghost admin theme dropdown. This file is not required in Ghost 0.4.2, but will likely be required in a future version.

Here's the example package.json from Casper:

```
{
  "name": "Casper",
  "version": "0.9.3"
}

```

You can choose to add any other fields to your package.json, the [npm docs](https://www.npmjs.org/doc/json.html?ref=ghost.org) detail several options such as description, keywords, homepage and repository. As Ghost develops we'll make more and more use of these fields both in Ghost and on our marketplace. In addition, very soon Ghost will allow you to add the version of Ghost which your theme supports/requires and will have internal tools to ensure that themes are compatible and help managing upgrades.

### The `{{log}}` helper

Handlebars supports the use of a log helper, but until now this hasn't done anything useful in Ghost. Now, when you're running Ghost in development mode you can use `{{log}}` to output debug messages to the server console. Perhaps the most interesting example of this is using `{{log this}}` to output the current handlebars context.

### Tag Pages

Perhaps the single most exciting addition in 0.4.2, is the long awaited tag pages feature. Tag pages contain a paginated lists of posts which have a particular tag. If you use the default `{{tags}}` helper in your theme, tags will now automatically link to their tag page.

If you're not using the `{{tags}}` helper you'll probably want to update your theme to wrap tags in `<a href="{{url}}"></a>` to take advantage of this new feature.

In addition to the updated helpers, you can also add a `tag.hbs` file to your theme. This template will be used to render tag pages, so it's possible to control exactly how these look. Tag pages use the `index.hbs` file by default if no `tag.hbs` file can be found.

### Custom Page Templates

As well as the shiny new `tag.hbs` template, Ghost now also supports custom templates for your individual pages giving you tight control over exactly how your static pages render. If you have a special page on your blog called 'About' with the url `/about/`, you can create a template called `page-about.hbs` with a custom layout and this template will only be used to render the About page, and nothing else.

### The `{{#has}}` helper

The brand new `{{#has}}` helper has been created to provide a bit more flexibility in creating different layouts for posts in Ghost. The overall goal of the `has` helper is to allow you to ask questions about what the current context looks like. For the time being this only covers determining which tags are present, here's an example:

```
{{#post}}
    {{#has tag="photo"}}
        ...do something if this post has a tag of photo...
    {{else}}
        ...do something if this posts doesn't have a tag of photo...
    {{/has}}
{{/post}}

```

Furthermore, the `has` helper will accept a comma separated list of tags so that you can ask if a post has any one of a list of tags a.k.a an 'or' query. For example, if a post has a tag of photo or video or audio:

```
{{#has tag="photo, video, audio"}}
...do something if this post has a tag of photo or video or audio...
{{else}}
...do something with other posts...
{{/has}}

```

We hope that these new features give theme developers a better idea of just how powerful the Ghost theming system can become. We're super excited about all the features that are yet to come, and are committed to continuously and incrementally adding theme features with each and every Ghost release.

Changes
-------

### `pageUrl` -> `page_url`

In 0.4.2 we've renamed all of our helpers to consistently use underscores rather than camelCase. The majority of this affected internal helpers, but the `pageUrl` helper (used in custom `pagination.hbs` templates) also needed changing. To prevent compatibility problems, we've kept the old `pageUrl` helper around, but deprecated it in favour of `page_url`. Using `pageUrl` will result in a deprecation warning.

`pageUrl` will be removed in a future release of Ghost (likely 0.6 to make sure there is plenty of overlap), so theme developers are encouraged to make the switch shortly after 0.4.2 is released.

### `{{tags}}` helper supports HTML prefix & suffix

The `{{tags}}` helper has been modified to permit the use of HTML in the `prefix` and `suffix` attributes, as well as the `separator` attribute, allowing for more flexibility in customising tag output without having to breakout from using the `{{tags}}` helper.

Active discussions
------------------

I believe it is very important that theme developers are actively involved in decision making around the theme API. We try as much as possible to provide an opportunity for discussion and debate around new features, so that we can build the best toolset possible. The following are some currently open theme API discussions that you may wish to get involved in:

* Have an option 'append' to the content helper: [#2163](https://github.com/TryGhost/Ghost/issues/2163?ref=ghost.org)
* [Feature] Improved post excerpts / previews  
  
  [#2166](https://github.com/TryGhost/Ghost/issues/2166?ref=ghost.org)
* body\_class overhaul  
  
  [#1967](https://github.com/TryGhost/Ghost/issues/1967?ref=ghost.org)
* Improve handlebars' ability to be context aware  
  
  [#2249](https://github.com/TryGhost/Ghost/issues/2249?ref=ghost.org)

A cheeky request
----------------

I'm over the moon that so many theme developers are offering fantastic themes for free, and many of those are being openly maintained on GitHub. I cannot begin to explain how happy seeing Ghost themes on GitHub makes me! However, I'd like to ask all theme developers using this mechanism to provide a clear link at the top of the readme which downloads a version of the theme which is compatible with the currently released version of Ghost.

I ask this because some of you are super-proactive, and update your themes for the next version of Ghost before it is released. As we start to introduce backwards in-compatible changes, we're getting a few people trying to use those new versions of your themes and getting confused. Unfortunately, what tends to happen in these cases is the user switches away to another theme... not what you want at all!


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





 





 
















 






