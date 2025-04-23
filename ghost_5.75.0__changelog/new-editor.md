


The new Ghost editor











































Faster and more robust than ever before, we just shipped a complete rewrite of the Ghost editor. This is our third major iteration of the Ghost editor, packed with new features, including:

* [**Native image editing**](https://ghost.org/changelog/image-editor/) - so you can adjust photos on the fly
* [**Post history**](https://ghost.org/changelog/post-history/) - so you can see who edited what, when, and restore old versions
* [**Landing page cards**](https://ghost.org/changelog/create-landing-pages/) - so you can build beautiful custom experiences
* [**Bookmarking**](https://ghost.org/changelog/bookmarker/) - so you can collect links from around the web for your posts

And some fixes for longstanding issues with our previous editor, like:

* **Faster overall performance** - things just feel more *snappy*
* **Improved handling of very large posts** - which, in the past, was... painful
* **Better undo/redo chaining** - a smoother experience when fixing mistakes
* **Much improved mobile editing** - so you can write on the go in iOS / Android
* **Nested lists** - for structuring your bulleted thoughts
  + Which wasn't possible before
    - But is now
* **More keyboard shortcuts** - find the full list in the post settings menu

The new editor is now available across all Ghost installs. [**Ghost(Pro)**](https://ghost.org/pricing/?ref=ghost.org) users can log into their sites to give it a try. If you're a developer, self-hosting Ghost, you'll need to [update](https://ghost.org/docs/update/?ref=ghost.org) to the latest version to get access to everything that's new.

---

Developer changes
-----------------

Keep reading below if you're curious about the technical details behind the new editor, and what it means if you're building API integrations with Ghost.

![](https://ghost.org/changelog/content/images/2023/10/Frame-1--4-.png)

As we worked on this new editor, one of our main goals was to keep things the same. We made a few visual tweaks here and there, but for the most part it's still the same editor you know and love... it just works better than it did before.

Under the hood, though, the technical changes we've made to the editor unlock exciting possibilities for the future.

Ghost's editor, called Koenig, was previously built in [Ember.js](https://emberjs.com/?ref=ghost.org) on an open JSON-based document storage format called [MobileDoc](https://github.com/bustle/mobiledoc-kit?ref=ghost.org). We loved how it worked, but MobileDoc never became widely adopted, so the technology underpinning our editor became a bit stagnant. This limited our ability to build new features, or solve frustrating core bugs (like better mobile support).

Koenig has now been rebuilt on a new stack: [React.js](https://react.dev/?ref=ghost.org) and [Lexical](https://lexical.dev/?ref=ghost.org) — both of which are open source frameworks developed by Meta. So, Ghost is now using the same underlying technology that powers every single editor, comment box, or user input for billions of users across Facebook and Instagram.

![](https://ghost.org/changelog/content/images/2023/10/Screenshot-2023-10-23-at-16.44.43@2x.png)

Try the new Koenig editor for yourself — [https://koenig.ghost.org](https://koenig.ghost.org/?ref=ghost.org)

Ghost is the first independent company outside of Meta to build a full-scale dynamic editor on top of Lexical, and we worked directly with the Lexical core team to make it happen. Today's announcement reflects over a year of quiet, dedicated work by both teams to get to where we are now.

We have lots of plans for continuing to improve Ghost's editing experience, and this shift in architecture has opened a lot of new doors for what's possible next.

For developers building integrations with Ghost, check out our updated API docs, which cover how to interact with Lexical content stored in the database:

[Ghost Admin API DocumentationManage content via Ghost’s Admin API, with secure role-based authentication. Read more on Ghost Docs 👉![](https://ghost.org/favicon.ico)Ghost - The Professional Publishing Platform![](https://ghost.org/images/meta/ghost-docs.png)](https://ghost.org/docs/admin-api/?ref=ghost.org#posts)
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





 





 
















 






