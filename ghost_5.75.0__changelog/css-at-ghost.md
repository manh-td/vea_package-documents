


How we do CSS at Ghost





































The CSS community is a wonderful thing to be part of. Everyone from [GitHub](https://markdotto.com/2014/07/23/githubs-css/?ref=ghost.org) to [Lonely Planet](https://ianfeather.co.uk/css-at-lonely-planet/?ref=ghost.org) has shared how they write CSS. Every time I read one of these posts, I learn something new; something I can use in my own day-to-day work.

The current state of CSS at Ghost is one of flux. We have rewritten [Ghost's CSS](https://github.com/TryGhost/Ghost/tree/master/core/client/assets/sass?ref=ghost.org) a couple times to make it leaner and easier to learn. But there's more to the health of a code-base than it's quality. Comments and learnability are absolutely crucial to helping new contributors get involved and help Ghost grow more and more.

This post is a primer on how we do CSS at Ghost, and how parts *will* be done going forward. So, with all that said, let's dive in!

Contents
--------

* [Introduction](#introduction)
* [Pre-Processor](#preprocessor)
* [Folder Architecture](#folderarchitecture)
* [Naming Things](#namingthings)
* [Media Queries](#mediaqueries)
* [Comments](#comments)
* [Linting](#linting)
* [Documentation](#documentation)

Introduction
------------

As a rule, our CSS is purposefully kept as lean & clean as possible. We don't prefix properties, we don't nest deeply, and we don't use any pre-packaged libraries – if you exclude [Normalize](https://github.com/necolas/normalize.css?ref=ghost.org).

**A quick note on browser support.** We aim to target the last 2 versions of popular browsers. At the time of writing, that means IE 10 & IE 11. Other target browsers automatically update which makes them a non-issue.

Pre-Processor
-------------

We use Sass as our pre-processor. It is the most popular pre-processor around today and has the widest network of support and collective knowledge. We use [Libsass](https://github.com/sass/libsass?ref=ghost.org) via a [node-sass](https://github.com/sass/node-sass?ref=ghost.org) Grunt task.

We use Libsass instead of Ruby-Sass, principally so we don't have a Ruby dependency. It's also much faster, taking an average of 3 seconds to generate 2 minified files and 2 source maps. One set for Ghost, the other for docs.

Prefixing is handled by [Autoprefixer](https://github.com/postcss/autoprefixer?ref=ghost.org) which is configured to only prefix the browsers we want to support. This means the only prefixed properties in the code are very specific to a particular browser; namely `-webkit-` stuff for a majority of mobile browsers.

Folder Architecture
-------------------

The file structure we've adopted is simple but suits the *reusability* of various components very well.

```
core/client/assets/sass
|-- screen.scss
|-- vendor/
|-- modules/
|-- patterns/
|-- components/
|-- layouts/

```

* `screen.scss` is where everything is `@include`'d, including Normalize from Bower
* `vendor/` is for CSS related to some JavaScript libraries
* `modules/` is for mixins, variables and utilities (such as icons)
* `patterns/` is for global styles, buttons, and forms
* `components/` is for groups of patterns with small bits of layout
* `layouts/` is where page layouts go and any page-specific changes to patterns and components

File Layout
-----------

Files have a strict layout, at least in terms of the way comments are written, blank lines added, and nesting is handled.

To help illustrate how, here's a full example showing every guideline and below is a list explaining each.

**Note:** This is not a real example, or well-crafted code. It's a guide to how code should be laid out and architected.

```
// ------------------------------------------------------------
// The Sass Example
//
// This is a brief example of how to structure a `.scss` file.
//
// * Define animations
// * Classed to use these animations
// ------------------------------------------------------------


//
// A wrapper for Element, extending %other-wrapper
// --------------------------------------------------

.element-wrapper {
    @extend &other-wrapper;

    padding: 15px 20px;
    border: 1px solid $lightbrown;

    @media (min-width: 801px) {
        margin: 10px;
        border-color: $midbrown;
    }

    // Variations
    &.darker {
        border-color: $midbrown;

        &.variation {
            padding-left: 10px;
            padding-right: 10px;
        }
    }

    .element-edit {
        border: 1px solid $lightbrown;
        border-radius: $rounded;

        @include icon($i-edit, 2rem, $lightbrown){
            transition: color linear 0.15s;
        };

        &:hover {
            border-color: $midbrown;

            &:before {
                color: $midbrown;
            }
        }
    }

}//.wide

//
// Another element
// --------------------------------------------------

.another-element {
    font-size: 1.6rem;
    line-height: 1.325;
    color: $darkgrey;
}

```

* Every file has a title, and a slug it the file is specific to one place
* Never style ID's and `.js-` classes
* Use short-hand notation where possible
* Blocks longer than 25 lines get a closing comment
* Keep nesting to a minimum, and no deeper than 3 levels, including pseudo selectors (`:nth-of-type` and `:after`)
* Group related properties together
* Media queries always go after properties, in order of small to large width/height values
* Don't be clever with selectors. Aim for readability over complexity

Naming Things
-------------

**Variables**

We've (rather unconventionally) decided not to use abstract variable names. As an example, we have `$red` instead of `$error`. It's much easier to understand and significantly lowers the barrier to entry.

**Classes**

We favour longer classes names and more of them over nesting selectors. So instead of a selector like `.navigation ul li a`, we would use a `.navigation-link`.

**Files**

If you stick to the rules explained in the [folder architecture](#folder-architecture), the name for a new file should become fairly obvious. The name of the file should directly relate to its contents. If you find a single file has 2 very separate chunks of code in it, they should probably be abstract out into separate files.

Media Queries
-------------

In very rare cases we detect the type of device (desktop or touch *device*), but everything else is based on viewport width and sometimes feature availability. As such, there's plenty of media queries dotted around the code.

So far, we've chosen not to use variables in media queries in lieu of more readability. However - thinking forward - there are several places that would benefit from having a variable in the MQ.

Comments
--------

> Code Tells You How, Comments Tell You Why  
> 
> *Jeff Atwood - [Coding Horror](https://blog.codinghorror.com/code-tells-you-how-comments-tell-you-why/?ref=ghost.org)*

There will be times when the code has to be complex, be it the necessary implementation, sheer complexity of properties, or inherited values.

If any CSS you write is not immediately obvious in context, it should be commented - not explaining how it works, but why its there in the first place.

```
.sample-component {
    @extend .other-component;

    transform: translate(0,0,0); // Resets `translate` inherited from `.other-component`
}

```

Linting
-------

Currently, Ghost's Sass is not linted. That has to change. Linting the JavaScript of Ghost has helped keep the quality high before it even gets committed to the code base. Doing the same with CSS will ensure the code is consistent throughout.

Things that should be linted, include:

* Levels of nesting & indentation
* Flag uses of ID selectors and classes beginning with `.js-`
* Spacing after selectors, properties, and values
* Use of single & double quotes
* Formatting and order of properties
* Selector formatting, preferring all lowercase with hyphens
* Null values with a unit (e.g. `0px` should be `0` or `none`)
* Use of colour names, preferring `$red` over `red`
* Duplicate properties
* Duplicate selectors on the same level

At the time of writing, there are no libraries that will lint `.scss` files that *dont* require a Ruby dependency, but this should serve as a list of requirements for tools that crop up in the mean time.

Documentation
-------------

We do have some documentation, but it's far from ideal. It's currently a Jekyll site deep in the folder structure [core/client/docs](https://github.com/TryGhost/Ghost/tree/master/core/client/docs?ref=ghost.org). Right now, it houses examples of reusable components, or `patterns` in our terms.

I'm not convinced that having it auto-regenerate is the greatest of ideas, but it certainly needs some love.

You Can Help
------------

We think (once all this is implemented), Ghost's CSS will be really easy to work on. However, there is *always* room to improve. If you want to help out or make the CSS even better, there's [plenty of ways](https://github.com/TryGhost/Ghost?ref=ghost.org#community) to talk to the awesome contributors.


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





 





 
















 






