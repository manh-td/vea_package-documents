


Get your theme ready for 0.8.0






































Ghost 0.8.0 is set to land soon, and with it come a few **breaking changes** to how the theme API works. These changes come from upgrades to the underlying [handlebars](https://github.com/wycats/handlebars.js?ref=ghost.org) and [express-hbs](https://github.com/barc/express-hbs?ref=ghost.org) libraries. As the changes affect rare use cases, they should not impact on many themes. This post is a guide on what has changed and how to check if your theme will be affected.

TLDR; The three breaking changes in 0.8.0
-----------------------------------------

1. All partial files **MUST** use the `.hbs` file extension.
2. Handlebars helpers provided to HTML attributes **MUST** be quoted, e.g. `<div class="{{post_class}}">`
3. `../` in handlebars now behaves naturally and doesn't require multiples when using nested if statements.

The first two changes lock down behaviour that is considered bad practice and are easy to spot. The change to `../` probably only affects you if you've had to unexpectedly use multiples (e.g. `{{../../pagination.total}}`) to retrieve a value in your theme.

In detail...
------------

Here's a full breakdown of what's changing, why, how to fix and how to find more information. If you have any questions please drop by the #themes channel on the Ghost [slack community](https://forum.ghost.org/?ref=ghost.org).

#### 1. Partials now require the `.hbs` extension

Previously, there was no enforcement around the file extension used for partial files, although the extension `.hbs` is what has been documented and expected.

This lack of enforcement has caused problems, for example some editors create backup files with names like `loob.hbs~`, `loop.hbs.bk` or `loop.hbs.swp` and these backup files can be loaded by Ghost instead of the correct file. The result is frustrating issues where changes to template files don't appear to work no matter what you change! Matching the file extension exactly fixes the issue, but also has the side effect of requiring the extension be correct.

Impact: Any partial which has an incorrect extension will not be found after the upgrade and this could cause problems rendering pages of a blog. Additionally backup files which were previously incorrectly rendered will be dropped in favour of the correct file.

Solution: Check your `/partials/` directory for any file with an extension other than `.hbs`. Look for any sort of backup file and check that the correct file is being rendered already, if not it will be after 0.8.0 so be sure you're happy with that change.

You can find out more about this change from the [Ghost bug](https://github.com/TryGhost/Ghost/issues/2459?ref=ghost.org) that it fixes, and also the [pull request](https://github.com/barc/express-hbs/pull/88?ref=ghost.org) which solves the underlying problem.

#### 2. Handlebars helpers passed to HTML attributes must be quoted

It has always been best practice to use quotes to surround any handlebars being passed to an HTML attribute, for example:

`<div class="{{post_class}}">` or `<time datetime="{{date format="YYYY-MM-DD"}}">`

In 0.8.0 we're upgrading to the latest version of handlebars (v4.0.5). This version additionally HTML escapes the `=` symbol in order to prevent XSS attacks and address a potential security risk. This addition makes it even more important to always use quotes when passing handlebars helpers to HTML attributes.

Impact: Following this change, in any case where quotes are not used and the value includes an `=`, the `=` will now be HTML escaped. This will cause minor rendering issues in templates.

For example, imagine outputting a link to a post which has the title "Me => Abroad":

`<a href={{url}} title={{title}}>click me</a>`

This would result in HTML like:

`<a ... title="Me" =&gt;="" abroad="">click me</a>`. The url will be output correctly as it cannot contain a `=` character, but the title will not be output correctly. This is incorrect but will not stop the page loading or link working.

Solution: Search your theme for handlebars helpers not being quoted, E.g. search for instances of `={{`. If you find any, it is recommended to add double quotes as you normally would with HTML.

More information can be found in the [handlebars pull request](https://github.com/wycats/handlebars.js/pull/1083?ref=ghost.org) and in the [handlebars v4 compatibility notes](https://github.com/wycats/handlebars.js/blob/master/release-notes.md?ref=ghost.org#v400---september-1st-2015).

#### 3. handlebars `../` paths now behave naturally

If used in a file system, the path expression `../` means go back one folder. It's not needed often in Ghost, but handlebars has a similar path syntax e.g. `{{../pagination.total}}` that is intended to let you reference values up one level in the tree of JSON data associated with a template. However, in the previous versions of handlebars, there were cases where `../` didn't go back one level as you'd expect and the expression would need repeating like `../../`.

This case most commonly happened with the combination of opening a block and also using an if statement. In this situation, handlebars was not working as you would expect. Take the following example:

```
{{#tag}}
  {{#if description}}
    {{description}}
  {{else}}
    A {{???pagination.total}}-post collection
  {{/if}}
{{/tag}}

```

Here, the pagination object is one level higher than the `tag` object we're currently inside be cause we opened a `{{#tag}}{{/tag}}` block. So to output the pagination total we'd expect to have to do `{{../pagination.total}}`. However, handlebars would get confused by the `{{#if}}` and require you to go back twice to get to pagination, e.g. `{{../../pagination.total}}`. This is really unnatural, and this behaviour has been fixed in Handlebars v4.

Impact: Anywhere where extra `../`'s were added to work around this problem will result in the wrong data (or rather no data) being output after the upgrade to 0.8.0.

Solution: Check your theme templates and partials for places where `../` is used in a nested block. In most cases, it will be instances of multiple `../`'s e.g. `{{../../pagination.total}}` that felt unnatural in the first place. You can remove any additional instances of `../` as these won't be needed any more.

**Update 13/05:** The easiest way to fix this issue, is to use `{{@root.pagination.total}}` to reference the root of the JSON data first, and reference pagination from there.

The full explanation & discussion around this change can be found in the [original handlebars issue](https://github.com/wycats/handlebars.js/issues/1028?ref=ghost.org).


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





 





 
















 






