


Primary Tags







































Any post in Ghost can have multiple tags, but Ghost also pays attention to the order of those tags. The first tag entered is considered the most important, and is treated as a special case.

For a while now, you've been able to drag and drop the order of tags in admin to set the correct primary tag, and also access a post's first tag using `{{tags.[0]}}`. This syntax is less than ideal, however, and it's hardly discoverable for theme developers, so we've introduced a new data object: `{{primary_tag}}` - to accomplish the same thing in a more friendly way.

Now if you're developing a theme and you just want to render the single most important categorisation label, you can directly access properties of the first tag with `{{primary_tag.name}}` to easily achieve this. If you want to do more, you can open a block with `{{#primary_tag}}{{/primary_tag}}` to get access to all the context-sensitive helpers like `{{url}}` & `{{img_url}`.

Example usage
-------------

If a post has tags of `News`, `Design`, `Architecture` - there are several ways to work with them:

Using the default `{{tags}}` helper will render a simple list of all post tags, linked to their respective archives: [News](#), [Design](#), [Architecture](#)

If you just wanted to output the primary tag and create a special link for that one case, then you could do what we do in Casper 2.0:

```
{{#primary_tag}}
    <a href="{{url}}">{{name}}</a>
{{/primary_tag}}

```

This way you can still have fairly liberal use of tags to determine posts which are related and belong together, but still keep a neat category-like taxonomy for output on the front end.

Hopefully this gives you a little more power and flexibility when building your next theme. If you're interested in finding out what else you can do, this and other theme API functionality is all documented over on [https://ghost.org/docs/themes/](https://ghost.org/docs/themes/?ref=ghost.org).

---

This change was released in **Ghost 1.2.0**. Self hosted developers can use [Ghost-CLI](https://ghost.org/docs/ghost-cli/?ref=ghost.org) to get this feature by running `$ ghost update` to install the [latest release](https://github.com/TryGhost/ghost/releases?ref=ghost.org). Ghost(Pro) users will be upgraded automatically, soon.


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





 





 
















 






