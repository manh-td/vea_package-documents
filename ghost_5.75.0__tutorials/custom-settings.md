





Custom settings are the ultimate power-up for Ghost themes









































---


Custom settings are perfect for developers building themes because users can tailor their theme to match their publication without having to touch a line of code. Even if you’re building a theme for yourself, custom settings give you instant control over aspects like typeface, layout, colors, and much more. The following guide will walk you through everything you need to know to make the most of custom settings in your Ghost theme.

An overview of custom settings
------------------------------

Use [custom settings](https://ghost.org/docs/themes/custom-settings/?ref=ghost.org) to create different possibilities for your theme — possibilities that users can configure right from Ghost Admin. For example, let users choose the tone for their publication by giving the option to have a refined serif typeface or a modern sans serif one.

While we’ll go into the details below, here are the essential points to know about custom settings:

* **Define custom settings** in your theme’s `package.json` file
* **Access the values** with the `@custom` helper
* You can have up to **20 custom settings**

How to configure custom settings
--------------------------------

Set up custom settings in the theme’s `package.json` file, under the `config.custom` key. Add each setting as a new key, using `snake_case`. Here’s an example of a custom setting called “typography”:

```
{
    "config": {
        "custom": {
            "typography": {
                "type": "select",
                "options": ["Modern sans-serif", "Elegant serif"],
                "default": "Modern sans-serif",
  			    "description": "Define your site's typography"
            }
        }
    }
}
```

The most important option to set for each setting is its `type` because it determines which other keys are required.

### Understanding types

There are five possible types. Let's look at each in detail.

**Select**

As seen in the example, the `select` type presents the user with a dropdown of options you define in the required `options` key. A `default` key is also required. It must contain a value that matches one of the defined options.

**Boolean**

The `boolean` type presents the user with a true/false toggle. When using the `boolean` type, you must also specify a default value (true or false).

**Color**

The `color` type presents the user with a color picker. A `default` hex color must be provided when using this type.

💡Remember that Ghost already provides the ability for a user to set an accent color in ****Design**** settings that can be accessed via the [`@site.accent_color`](https://ghost.org/docs/themes/helpers/site/?ref=ghost.org) helper.

**Image**

The `image` type presents the user with an image uploader. The output from this type is either an image URL or a blank string. The `image` type works great with the [`img_url` helper](https://ghost.org/docs/themes/helpers/img_url/?ref=ghost.org), which allows you to optimize the uploaded image automatically!

**Text**

The `text` type presents the user with a text input. The `default` value is optional, meaning that it’s possible for the output of this type to be empty.

[Find a full overview of these types in the docs.](https://ghost.org/docs/themes/custom-settings/?ref=ghost.org)

### Add descriptions to share the purpose of custom settings

For each type, it's possible to add an optional `description`. The value provided for this key appears in Ghost Admin with the custom setting. It's a great way to communicate to users what the custom setting is for.

By giving the setting a name, description, type, and any additional required keys, you've defined a custom setting. Oh, yeah! Let's see how to access its user-defined value in the theme.

### Access custom settings within the theme

Gain access to the user-defined value with the [`@custom` helper](https://ghost.org/docs/themes/helpers/custom/?ref=ghost.org) plus the setting name. To access the `typography` setting above, use `@custom.typeface` anywhere in the theme.

To then change the typeface for the theme, use the custom setting to modify the CSS class on the `body` tag in `default.hbs`.

```
<body class="{{#match @custom.typeface "Modern sans-serif"}} has-sans-serif-font{{else}} has-serif-font{{/match}}</body>

```

**Use the match helper**

We use the [`match` helper](https://ghost.org/docs/themes/helpers/match/?ref=ghost.org) above to test the value of the custom setting. Specifically, we’re testing whether the `typeface` value equals “Modern sans-serif.” (When using the `match` helper to test equality, the `=` sign can be omitted.) It’s also possible to test other conditions by using different operators: `!=`, `<`, `>`, `>=`, and `<=`. If the custom setting equals "Modern sans-serif," then the `has-sans-serif-font` class is output. Otherwise, `has-serif-font` is output.

The only other required action on your part is to include the classes in your CSS:

```
.has-sans-serif-font {
  font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir, segoe ui, helvetica neue, helvetica, Cantarell, Ubuntu, roboto, noto, arial, sans-serif;
}

.has-serif-font {
  font-family: Iowan Old Style, Apple Garamond, Baskerville, Times New Roman, Droid Serif, Times, Source Serif Pro, serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol;;
}

```

Now, the user can set their desired typeface right from Ghost Admin (and change it any time if they’re so inclined) 🔠

💡Remembering the exact value you used to name a custom setting can be a drag, requiring you to jump back into your `package.json` file. Use our [official VS Code extension](https://marketplace.visualstudio.com/items?itemName=TryGhost.ghost&ref=ghost.org) to autocomplete your custom settings. When in a Handlebars file, type `custom`, and the extension will autocomplete the property with your settings, even adding the `@` sign.
### Grouping custom settings

There’s one last bit of configuration possible for custom settings: groups. By default, all custom settings are put in the **Site-wide** group, meaning that the setting is applicable across the whole publication.

However, specific groups exist for settings that only apply to the homepage or post pages. For example, with Casper, it’s possible to specify three different layouts on the homepage. Here’s how that option is defined in `package.json` and its group defined:

```
"feed_layout": {
    "type": "select",
    "options": [
        "Classic",
        "Grid",
        "List"
    ],
    "default": "Classic",
    "group": "homepage"
}
```

For settings applicable to post pages, set the `group` to `post`.

And that’s everything you need to know about custom settings. Here’s a visual to help bring it all together.

![Four panel image with a custom settings header. The first panel shows a custom setting defined in package.json. The second panel shows the custom accessible in Ghost Admin. The third panel shows the custom property being used in the theme. The last panel shows the site using the custom setting.](https://ghost.org/tutorials/content/images/2023/08/custom--1-.png)

Custom settings in the wild
---------------------------

Eager for a few more examples? Let's check out two different ways custom settings are used in Ghost’s default theme, Casper.

### Dynamic color scheme

Imagine giving your users the power to switch between light and dark modes, or even automate the color scheme based on OS preferences. Casper does just that!

```
"color_scheme": {
    "type": "select",
    "options": [
        "Light",
        "Dark",
        "Auto"
    ],
    "default": "Light"
}
```

The `color_scheme` custom setting allows users to choose whether they want their site to display in light, dark, or auto mode.

![](https://ghost.org/tutorials/content/images/2023/08/light-mode.png)![](https://ghost.org/tutorials/content/images/2023/08/dark-mode.png)

The custom setting is accessed in `default.hbs` on the `html` tag:

```
<html lang="{{@site.locale}}"{{#match @custom.color_scheme "Dark"}} class="dark-mode"{{else match @custom.color_scheme "Auto"}} class="auto-color"{{/match}}>

```

When the color scheme is set to “Dark,” the `dark-mode` class is added to the element (and `auto-color` is added when that option is chosen). Then, in the theme’s CSS, styles are added with classes to reflect these choices. For example, here’s the rule that sets the background to a dark color and the text to a light color:

```
html.dark-mode body {
    color: rgba(255, 255, 255, 0.75);
    background: var(--color-darkmode);
}

```

The takeaway? You can dynamically add and remove CSS classes based on user preferences, creating multiple styles within a single theme.

### Personalize the sign-up call to action

Custom text for the sign-up CTA (call to action) on Casper’s post page makes the experience more engaging. Here's the setting:

```
"email_signup_text": {
    "type": "text",
    "default": "Sign up for more like this.",
    "group": "post"
},
```

Key insights:

* **Fallback text**: If the user doesn’t provide their own, a default is provided to ensure the CTA text isn’t blank.
* **Group definition**: This setting shows up under the "post" dropdown, making it specific to post pages.

The screenshots below show how this setting appears in Ghost Admin and the default and personalized call-to-actions on the post.

![](https://ghost.org/tutorials/content/images/2023/08/custom-text.png)![](https://ghost.org/tutorials/content/images/2023/08/sign-up-default.png)![](https://ghost.org/tutorials/content/images/2023/08/custom-text-post.png)

These examples illustrate a few of the many possibilities offered by custom settings. Dive in and [explore these features and other custom settings in Casper](https://github.com/TryGhost/Casper/blob/592226b75eae2452877f48e3a3b162dd5a0d85ec/package.json?ref=ghost.org#L91-L173). Learning from official Ghost themes is a fantastic way to level up your theme-building skills 💪

Summary
-------

With custom settings, you can hand the creative reins to your users, allowing them to make your theme their own. Through this guide, you've learned how to define, access, and leverage various types of custom settings, seen practical examples, and grasped precisely how these settings can transform a user's interaction with your theme.

But your adventure is just beginning.

Visit our [official Forum](https://forum.ghost.org/?ref=ghost.org) to see what other developers are up to or [subscribe to our Build with Ghost Newsletter](#/portal/signup/), the best way to keep up with changes in Ghost and find inspiration for your next gorgeous theme.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Build a custom sign-up form

7 min read](/tutorials/form/)

[### The art of the post template

12 min read](/tutorials/post-template/)

[### A complete guide to partials

10 min read](/tutorials/partials/)

[### A comprehensive guide to the index template

9 min read](/tutorials/index/)

[### A comprehensive guide to the default template

9 min read](/tutorials/default/)

[### Essential concepts to know when building a Ghost theme

7 min read](/tutorials/essential-concepts/)

[### How to install Ghost locally

3 min read](/tutorials/local-ghost/)

[### Install Node on macOS, Windows, and Linux

4 min read](/tutorials/node/)

[### How to create a read-next section

10 min read](/tutorials/read-next/)

[### How to build a custom homepage

11 min read](/tutorials/custom-homepage/)

[### Create a custom post template

4 min read](/tutorials/create-a-custom-post-template/)

[### Implementing redirects

5 min read](/tutorials/implementing-redirects/)

[### Show reading time & progress

3 min read](/tutorials/reading-time/)

[### How to build CSS files

2 min read](/tutorials/build-css-files/)

[### How to make a podcast RSS feed

4 min read](/tutorials/custom-rss-feed/)







Be the first to know.
---------------------

Join the Ghost developer community — sign up to get early access to the latest features, developer tools, and tutorials.



No spam. Once a month. Unsubscribe any time.
[![](https://ghost.org/tutorials/assets/img/most-helpful.jpg?v=235936095d)

Most helpful
------------

Essential tutorials to get you started](https://ghost.org/tutorials/most-helpful/)
[![](https://ghost.org/tutorials/assets/img/fundamentals.jpg?v=235936095d)

Funda­mentals
-------------

The basics of Ghost theme development](https://ghost.org/tutorials/fundamentals/)
[![](https://ghost.org/tutorials/assets/img/level-up.jpg?v=235936095d)

Level up
--------

Next-level development techniques](https://ghost.org/tutorials/level-up/)
[![](https://ghost.org/tutorials/assets/img/do-more.jpg?v=235936095d)

Do more
-------

Ideas & inspiration for whatever comes next](https://ghost.org/tutorials/do-more/)









