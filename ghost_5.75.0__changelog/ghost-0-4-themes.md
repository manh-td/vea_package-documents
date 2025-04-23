


What's new for Themes in Ghost 0.4?






































With the release of Ghost 0.4.1 yesterday, I wanted to take the time to finish this long put-off post detailing what has changed in the world of Ghost themes since 0.3.3. Yesterday's release included an upgrade to handlebars 1.3.0, so I'll cover highlights of what's new there as well.

### The tech

Before we dive into features and fixes, I wanted to quickly outline the technology behind Ghost themes. Theme templates are written in [handlebars.js](https://handlebarsjs.com/?ref=ghost.org), but handlebars is wired into Ghost using another library called [express-hbs](https://github.com/barc/express-hbs?ref=ghost.org). Express-hbs provides additional features which we depend on such as the ability to have a layout file like `default.hbs`. As both of these tools evolve, so do the possiblities for Ghost themes.

Ghost 0.3.3 used express-hbs 0.2.2, and that in turn used handlebars 1.0.10. Ghost 0.4.1 uses express-hbs 0.7.6 which in turn uses handlebars 1.3.0. This information is useful when trying to determine where and when things have changed.

### New features in 0.4

Ghost 0.4 brings many new features which impact on themes. The following outlines how themes should use and cater for those features.

#### Featured posts

On the content screen in the Ghost admin, it is now possible to mark posts as featured with the 'star' button. This adds a property of `featured` to those posts, and also outputs a class of `featured` via the `{{post_class}}` helper. This allows themes to do interesting things with how these posts are displayed.

So in a theme, you might have something like:

```
{{#posts}}
    {{#if featured}}
    	...
    {{else}}
        ...
    {/if}
{{/posts}}    

```

Equally, if you just need to target the post with CSS, you can with `.featured`.

Featured posts do not move from their place in the chronological post list. We have been asked how to show featured posts separately, or list just featured posts, but unfortunately this isn't quite possible yet.

What you can do is loop through the post count twice, that way if any posts on the current page are featured, you can display them at the top of the current page. This isn't a perfect solution, and we will be providing tools to customise post lists very soon, however it is worth nothing that looping through the post count twice will have minimal performance impact, as the list is already fetched from the database.

#### Static Pages

Static pages are posts which don't appear in the chronological post list. They are intended to be used for simple content pages, like an 'about' page. By default, Ghost will render pages using `post.hbs` the same as posts. However, if your theme includes a `page.hbs` template, Ghost will use that instead. Static pages also get a class of `.page` from the `{{post_class}}` helper.

There is no way to build a menu in Ghost, so there is no helper to output one and therefore links to static pages have to be hardcoded into a theme. We recommend including an optional partial for adding a menu to themes, or hardcoding common pages like 'about' pages, and include instructions for how to change it in your README.

#### Custom Error pages

By adding an `error.hbs` file to your theme, you can customise the way that Ghost displays errors. Currently this works for both 404 and 500 errors, although there is some discussion around whether it should only be for 404 errors as the most common 500 error that can occur is an error with a theme.

The error page gets very specific information, namely the error `{{code}}`, an error `{{message}}` and in some cases a stack trace. There is an example of how to template the stack trace in Ghost's default error template `/core/server/views/user-error.hbs`.

Be careful what you put in an `error.hbs` template. Having errors on the error page is never a good situation!

#### Subdirectory support

URLs in config.js can now contain a subdirectory, meaning users can set their blog to appear at `https://my-ghost-blog.com/blog` which was not possible before. Although nothing to do with theming, this has implications for creating links to assets. Ghost themes frequently have to add references to script, style, image and other files which they depend upon. Currently those links are static, hard-coded references that break if the Ghost url contains a subdirectory.

The [asset helper](https://ghost.org/docs/themes/helpers/asset/?ref=ghost.org) solves this problem, as well as allowing us to improve the caching of static assets so that themes load faster. We highly recommend that all Ghost themes upgrade to use the `{{asset}}` helper for all asset URLs. Casper 0.9.2 has this improvement, and it's as simple as switching out a static url like `/assets/css/screen.css` to `{{asset "css/screen.css"}}`. The asset helper assumes that assets are kept in a folder inside your theme called `assets`.

#### Customisable favicon

With the addition of the asset helper, it is now also possible to add a custom `favicon.ico` file to a theme. For full details please see the section on favicons under the asset helper in the [theme docs](https://ghost.org/docs/themes/helpers/asset/?ref=ghost.org)

### Changes to the Ghost helpers

For full details of the helpers, see the [theme docs](https://ghost.org/docs/themes/helpers/?ref=ghost.org).

##### New:

`{{assets}}` - allows you to build robust links to your asset files - [asset helper docs](https://ghost.org/docs/themes/helpers/asset/?ref=ghost.org).

`{{encode}}` - provides for encoding data, for example when building links to sharing services - [encode helper docs](https://ghost.org/docs/themes/helpers/encode/?ref=ghost.org).

##### Updated:

`{{tags}}` - added prefix and suffix options - [tags helper docs](https://ghost.org/docs/themes/helpers/tags/?ref=ghost.org).

`{{excerpt}}` - added unicode character support - [excerpt helper docs](https://ghost.org/docs/themes/helpers/excerpt/?ref=ghost.org).

### Bug Fixes

Support for template partials in Ghost 0.3.3 was really sketchy. They often didn't work properly in production mode, definitely didn't work if a theme was symlinked, and it was just generally buggy. Even worse, in 0.4, empty partials would completely crash Ghost.

0.4.1 includes a number of improvements to partial handling, template caching and also error handling, so that Ghost will keep running even when themes do unexpected and broken things. When things do go wrong, instead of crashing with an error in the console, you'll get a proper Ghost error page with a stack trace. Even if the theme is completely unavailable (i.e. if you rename or delete the theme) Ghost will start and run so you can access the admin panel and change which theme is active.

### What's new in handlebars?

Note, handlebars has undergone many changes, these are just a couple of highlights:

#### Subexpressions

It is now possible to pass the output from one helper into another helper. This feature is called subexpressions and is achieved by using parentheses. This is particularly useful in Ghost if you want to encode a URL for use in a share link:

`{{encode (url absolute="true")}}`

#### Whitespace Control

Handlebars has added the ability to strip additional whitespace from around a helper by adding a `~` character to the helper.

For example, when outputting a post list you may wish to add whitespace control like so:

```
{{#posts ~}}
	<ul>
        ...
    </ul> 
{{~/posts}}

```
### A note to all theme developers

During the development of 0.4 it came to our attention that an enterprising theme developer had discovered an interesting 'feature'. If you use `{{content words="0"}}` instead of returning nothing, Ghost will return the first image or video if one appears in the post before the text content. Although this is technically a bug, we decided not to fix it until there is an alternative way to provide a cover image for a post - this 'feature' is now covered by our test suite so that it can't accidentally disappear in the same way as it accidentally appeared.

If you stumble across other hacks, workarounds or potential bug-features like this, please do let us know! That way we can ensure that we don't accidentally remove things you are relying on without warning. Equally, if you ever manage to break Ghost whilst theming it, please do raise a bug on GitHub, we want to make Ghost indestructible.

Thank you for all the amazing themes you have created so far. We look forward to seeing what you do with the new features in 0.4, and hope you'll come and help us test the features we are [building in 0.5](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org#wiki-themes).


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





 





 
















 






