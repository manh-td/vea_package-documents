


Ghost Theme Tips: Defining Content Blocks






































In recent weeks I've seen a question popping up regularly:

> If I've got some area in my `default.hbs` file, but I want it to contain information that changes depending on the post or page I'm viewing (for example meta data), can I do that and if so how?

The answer is **yes**, you can! It's also really quite straightforward, however the feature is hidden away in the depths of how Ghost works, and not (yet) covered by our documentation. The following examples hope to demonstrate common Ghost-specific use cases and how to achieve them.

There is a feature of [express-hbs](https://github.com/barc/express-hbs?ref=ghost.org#syntax) called *content blocks*. This will allow you to define a placeholder block in a layout file (e.g. `default.hbs`), and then define the content for that block in a template file (e.g. `post.hbs`). A common example of this is wanting to set Open Graph and other meta tags for posts:

In `default.hbs`:

```
<head>
    {{{block "metaTags"}}}
</head>

```

In `post.hbs`:

```
{{#post}}
    {{#contentFor "metaTags"}}
        <meta property="og:title" content="{{title}}" />  
        <meta property="og:url" content="{{url absolute="true"}}"/>  
        <meta property="og:type" content="article" />
        <meta property="article:author" content="{{author.website}}">

    {{/contentFor}}
    ... rest of post output ...
{{/post}}

```

You could define something different to be output in `index.hbs`:

```
{{#contentFor "metaTags"}}
    <meta property="og:title" content="{{meta_title}}" />  
    <meta property="og:url" content="{{url absolute="true"}}"/>  
    <meta property="og:type" content="website" />  
{{/contentFor}}

```

There are a few interesting and potentially confusing points to note about how this works. The `block` helper looks like `{{{block "name"}}}`, where `name` is the name of the placeholder you are defining. The name here needs to match the name you use with the `contentFor` helper.

Additionally, if you are going to define HTML to be output by the block as in the example above, the `block` helper needs three braces (`{` and `}`) not two as with most helpers. If you only use two, the HTML will be escaped, using three tells handlebars to trust the output and render it as HTML instead of escaping.

The `contentFor` helper is a block helper - this means it has opening and closing parts rather than being a single helper. It looks like `{{#contentFor "name"}}content here{{/contentFor}}`, where `name` matches the name defined in the `block` helper, and the content you want to output in the block is between the opening and closing parts.

*Note: confusingly the `block` helper is not a handlebars block helper so it doesn't have a `#` at the beginning.*

Another example of how you might use this would be to add extra classes to the body tag:

In `default.hbs`:

```
</head>
<body class="{{body_class}} {{block "customBodyClass"}}">
...

```

In `post.hbs`:

```
{{#post}}
    {{#contentFor "customBodyClass"}}
        {{~#if featured~}}
            {{#if page~}}
                featured-page
            {{~/if}}
        {{~/if~}}
    {{/contentFor}}
{{/post}}

```

This time, the content I'm outputting is just a class, no HTML, so my `{{block}}` helper only needs two braces. Adding three wouldn't do any harm, but in this case I don't need them. However, the content I'm outputting does need to be free from additional whitespace so I'm making use of handlebars' new whitespace control feature which uses a `~` character to remove whitespace.

Hopefully, these examples open up some new possibilities for theme developers. For more details of what is possible with Ghost themes, be sure to get familiar with the [handlebars](https://handlebarsjs.com/?ref=ghost.org), [express-hbs](https://github.com/barc/express-hbs?ref=ghost.org#express-hbs) and [Ghost](https://ghost.org/docs/themes/?ref=ghost.org) documentation - all of these resources are updated regularly. Happy theming!

**Update 27/10/15**: If you need some additional information on how to use layout templates, check out [this section](https://ghost.org/docs/themes/?ref=ghost.org) of the Ghost theme docs


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





 





 
















 






