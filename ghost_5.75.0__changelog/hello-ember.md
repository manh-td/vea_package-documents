


Hello Ember







































Today we are announcing that the Ghost Admin UI is going to be rebuilt in [Ember.js](https://emberjs.com/?ref=ghost.org).

![](https://ghost.org/changelog/content/images/2021/01/image-37.png)

For the past couple of weeks, there has been an [epic discussion](https://github.com/TryGhost/Ghost/issues/2144?ref=ghost.org) occuring on Ghost's GitHub. The idea is that we're looking to find the right tool with which to build the next iteration of the Ghost admin UI: the main options being Angular, Ember, React or Backbone + marionette etc. Our existing Backbone implementation has a number of problems, so we've been specifically looking for the tool that will best solve those problems:

* Is it client side? Is it server side? Is it dark side?
* Data binding
* Route/navigation/history management
* View management
* Fragile Code
* Lack of clarity & guidelines on how to approach common problems

The discussion around which tool we should adopt has been amazingly positive and open minded, and has provided a great deal of insight. There is no doubt that any one of the options discussed could do a great job of driving the Ghost admin UI. However, throughout the discussion, there was one tool which shone out as being the right choice for Ghost. That tool is [Ember.js](https://emberjs.com/?ref=ghost.org).

Ember.js stands out from the other choices because it is strongly opinionated. Although seen as a downside by some, for Ghost, this is exactly what we need. As a fast moving open source project, we don't want to spend time discussing and deciding on the best structure, designing a framework & creating documentation and guidelines so that new contributors can get up to speed. With [Ember.js](https://emberjs.com/?ref=ghost.org), the majority of decisions have been made, making it easy to get going, easy to knowledge share, and easy to onboard new developers.

There are many other reasons for Ghost to choose [Ember.js](https://emberjs.com/?ref=ghost.org). It solves all of the hairiest problems we've faced with routing, data binding and view management in a straight forward manner. The tight integration with handlebars is a great fit with Ghost's existing dependence on handlebars. The top-down, URL driven approach is also going to help us push the whole app down to the client side in a much more structured manner.

The involvement of the Ember.js community in our decision making process has also been a great plus. We owe a special thanks to [Trek](https://github.com/trek?ref=ghost.org), [Manuel](https://github.com/manuelmitasch?ref=ghost.org), [Markus](https://github.com/Globegitter?ref=ghost.org), [Stefan](https://github.com/stefanpenner?ref=ghost.org), [Taras](https://github.com/taras?ref=ghost.org), [Erik](https://github.com/ebryn?ref=ghost.org), [Yehuda](https://github.com/wycats?ref=ghost.org), [Tom](https://github.com/tomdale?ref=ghost.org) and everyone else from the Ember.js community who got involved. They've shown that they are a passionate bunch of people and they have been very keen to get stuck in. The importance of their willingness to help us quickly turn around a big re-write cannot be overlooked, but this is not the only reason we are keen to join them. Their community and their approach is one we would love to emulate in Ghost's community, we hope that by working with them, some of their awesomeness will rub off on us!

Our core team is extremely excited to get stuck in with the rewrite. There will be plenty of news and updates here and on [GitHub](https://github.com/TryGhost/Ghost/tree/ember?ref=ghost.org) as the project unfolds. If you want to get involved, the best way is to drop by our IRC channel: #ghost on Freenode. The more the merrier!

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





 





 
















 






