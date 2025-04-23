


Ghost Desktop's JavaScript Underbelly











































Have you checked out Ghost Desktop yet? It's our little app for Windows, macOS, and Linux, allowing users to work on their publications without being confined by the limits of a browser. We already implemented a host of native features, and we have even bigger plans for the future.

However, the app is still written in JavaScript, using mostly the same guidelines and technologies used by both the Ghost backend and frontend. In this post, I'd like to give you a quick tour of how we're building Ghost Desktop.

![](https://ghost.org/changelog/content/images/2021/01/screenshot.png)
### Node.js on the Desktop

Ghost Desktop stands on the shoulders of giants. We use [Electron](https://electron.atom.io/?ref=ghost.org), a framework combining Chrome, Node.js, and a thick layer of native integrations with Windows, macOS, and Linux. Initially developed by GitHub for the code editor [Atom](https://www.atom.io/?ref=ghost.org), it is now one of the hot newcomers in the JavaScript ecosystem, powering [Visual Studio Code](https://code.visualstudio.com/?ref=ghost.org), [Slack](https://slack.com/downloads?ref=ghost.org), or [WhatsApp](https://www.whatsapp.com/download/?ref=ghost.org). It is popular with good reason: Thanks to the strong cross-platform foundation in both Chrome and Node.js, one can easily create an app for all popular platforms.

In addition, Electron apps get to use the collective goodness available on npm, enjoy the latest and greatest in modern JavaScript, and allow for the same convenience in development we JavaScript developers are used to.

Building cross-platform means that we can focus our energy on building one great app rather than dividing our resources to build multiple less polished apps. In addition, we at Ghost 💖 JavaScript: Using Electron means that we can use the same style, the same skills, the same learnings, and the same familiar environment to build our Desktop app we use to build our backend and our frontend. Technically, it's a combination: Ghost Desktop is an Ember App that get's to use Node modules - even native ones, written in C++, useful for difficult operations like spellchecking.

### Willy Wonka's App Factory

Let's take a look at the source. It starts with a `package.json`, just like Node developers are used to. As you can tell from the dependencies, we're using Ember and a handful of Node modules. We even built [ember-electron](https://github.com/felixrieseberg/ember-electron?ref=ghost.org), integrating Ember Cli with Electron.

To understand how it all comes together, let's follow the path of the app booting up. To start the app as a developer, you run `npm start`, which in turn calls `ember electron`. Electron starts with a simple file, much like a Node.js application - in our case, that's `main/app.js`. Note that when Ghost Desktop starts, it initially does not have a visible window - the main process does not have a user interface. In there, we wait for the application to finish its native boot process before creating a new [`BrowserWindow`](https://electron.atom.io/docs/api/browser-window/?ref=ghost.org). Like the name suggests, that window is a Chromium window, with one important caveat: In addition to Chrome's JavaScript features, Node is also in play. The loaded page is not just limited to the usual HTML, CSS, and JS - you can also call `require('fs')`.

In that `BrowserWindow`, we fire up an Ember application - it manages the addition of blogs, the quick switcher on the left, and everything else you can see. If you browse the source code, you will even see us requiring Node modules, including native ones.

However, due to the tremendous power available to the code that runs inside the window, we do not simply load your blog. [We use a special HTML element called a `<WebView />`](https://electron.atom.io/docs/api/web-view-tag/?ref=ghost.org) - which is sort of like an `Iframe` and at home inside the Chromium engine. When you add a blog, we create a new `<WebView />`.

Before a blog gets to load, we pre-load a series of functions, augmenting the APIs available to the blog. Once we have augmented the global scope, we remove Node privileges inside the `<WebView />`. In this moment, Ghost Desktop becomes a slightly more powerful browser, tailored specifically to the needs of the Ghost Admin interface. From there, Ghost Desktop has full control over Ghost Admin, while Ghost Admin is able to call a set collection of APIs made available to it.

We have big plans for the future: A powerful offline mode, allowing to work on posts without an active connection. Native integration with your favorite editors, whether that is Microsoft Word or Sublime. Easier management for those creative souls who manage multiple blogs. If you'd like work on some Open Source code with us, join us in our GitHub repository!

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





 





 
















 






