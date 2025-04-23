


Make Your Theme Multi-User Ready






































We're into the final stages of preparing for releasing Ghost 0.5. The second Release Candidate has been [published](https://github.com/TryGhost/Ghost/releases/tag/0.5.0-rc2?ref=ghost.org), and we've announced our plan to release on Monday 11th August. Unlike the [last major release](https://ghost.org/changelog/ghost-0-4-themes/), this time I wanted to give theme developers a heads-up on what's changing in advance.

Ghost 0.5 has largely been a refactoring project, finished off with the implementation of Multi-User. Although there haven't been many general improvements to the theme API, the additon of multiple user support to Ghost provides some new toys for theme developers to play with.

What is Multi-User?
-------------------

Until now, Ghost has been a single-user blog. That meant that all the posts were always written by the same person - the blog owner. All that is about to change.

From 0.5, it will be possible to invite people to join your blog, so posts can have different authors. From a theming perspective, this has two main effects: first, a post's author has more significance if the blog is multi-user and second, the difference between blog settings such as the title, cover image and logo are now clearly different to a user's cover image and logo.

What's new?
-----------

### Author Pages

Similar to the [tag pages](https://ghost.org/changelog/new-for-themes-0-4-2/#tagpages) feature that was released in 0.4.2, Ghost 0.5 supports author pages. An author page contains a paginated list of posts for a specific author, and can be accessed by visiting the url: `/author/author-slug/`. Authors also have an RSS feed for their posts.

Author pages will be rendered by either the new `author.hbs` template, or default to `index.hbs` if `author.hbs` is not present. Similarly to tag pages, author pages have access to an `author` object as well as a `posts` object.

As usual, the `{{url}}` helper will generate a correct url for an author page, when in an author context:

```
{{#author}}
<a href="{{url}}">{{name}}</a>
{{/author}}

```

The `{{author}}` helper will now output this `<a>` tag structure, as opposed to just the author's name as it did in 0.4.2.

**Note:** there is a difference between the `{{author}}` helper, and the `{{#author}}{{/author}}` context block. You can see an example of these features in use in the updated [Casper theme](https://github.com/TryGhost/Casper/tree/8fd21ea939a264b44710cd76b88bcd6a9f38c6a3?ref=ghost.org)

### The `{{plural}}` helper

The only non-multi-user specific new feature for themes in 0.5, the `{{plural}}` helper has been aded to make formatting meta information about posts, tags etc a little nicer.

`{{plural pagination.total empty='No posts' singular='% post' plural='% posts'}}`

The plural helper takes a number and three strings to output depending on whether the number is zero, singular or plural. The most common usecase for this is outputting information about how many posts there are in total in a collection. For example, themes have access to `pagination.total` on the homepage, a tag page or an author page.

### New `home.hbs` and `author.hbs` templates

Author pages will be rendered with the new `author.hbs` if one is available, or alternatively fall back to `index.hbs`.

Similarly, there's a new template you can use to do something different with your homepage. If present, `home.hbs` will be used to render only the very first page of a blog. If it is not present `index.hbs` will be used, and `index.hbs` is still used for the second, and third etc pages of the blog.

### Updates to the `{{#has}}` helper

The final new thing for 0.5, the `{{#has}}` helper has been updated to support an author attribute. This means you can check if a post is authored by a particular user:

```
{{#post}}
    {{#has author="Joe Bloggs"}}
        ...do something if the author is Joe Bloggs
    {{else}}
        ...do something if the author is not Joe bloggs
    {{/has}}
{{/post}}

```

See the [0.4.2 post](https://ghost.org/changelog/new-for-themes-0-4-2/#thehashelper) or the [documentation](https://ghost.org/docs/themes/helpers/has/?ref=ghost.org) for more details of the `{{#has}}` helper.

Potentially breaking changes
----------------------------

### `{{author}}` now outputs HTML

As explained above, prior to 0.5 the `{{author}}` helper would output the author's name in string form. In 0.5 this has been updated to output a link to the author page, the equivalent of doing:

```
{{#author}}
<a href="{{url}}">{{name}}</a>
{{/author}}

```

If you do not want the author tag to output a link you can use `{{author autolink="false"}}`.

### `{{author.email}}` no longer accessible

It [was felt](https://github.com/TryGhost/Ghost/issues/2330?ref=ghost.org) that the author's email address being publicly available was a privacy violation. Rather than adding an option to enable or disable this, it has been removed. `{{author.email}}` will now output an empty a string.

Get ready for Multi-User
------------------------

We recommend that all themes make the following three amends:

1. Add a new `author.hbs` template for awesome author pages
2. Ensure that your post output features the `{{author}}` tag so that readers can easily navigate to these pages
3. Take this opportunity to check your theme is up-to-date with features from [0.4.0](https://ghost.org/changelog/ghost-0-4-themes/) and [0.4.2](https://ghost.org/changelog/new-for-themes-0-4-2) as we are transitioning to a much faster release cycle, and deprecated features will be removed soon.

Although the changes required to support Multi-User are small and quick, [Casper](https://github.com/TryGhost/Casper?ref=ghost.org) has had a significant upgrade for 0.5 to make authors more prominent in the design. We hope that many of you will also take this opportunity to upgrade your themes to help make Multi-User an awesome new feature for Ghost bloggers.


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





 





 
















 






