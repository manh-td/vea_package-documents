





How to update CSS in a Ghost theme










































---


Have you ever edited a CSS file in your Ghost theme and then wondered why those changes didn't show up on your site? You probably missed the important build step.  
  
In this tutorial, you'll learn how to use the development tool Gulp to build CSS, so that you can make stylistic changes to your theme.

🚧If you're only looking to make minor updates to a theme, code injection may be enough.

What's Gulp?
------------

[Gulp](https://gulpjs.com/?ref=ghost.org) is a tool for streamlining your CSS, which is what determines your theme's style. It's a developer tool that makes your code more consistent and compatible.

Nearly every website has CSS, and Ghost themes are no different – they rely on CSS to provide layout and style.

All of the free and official Ghost themes and many premium themes use Gulp to compile CSS files. By learning just two commands, you'll have the knowledge you need to customize any theme that makes use of Gulp.

🚦The instructions in this tutorial will work with all official Ghost themes. With custom themes, YMMV. 

How to update CSS and JS
------------------------

Navigate to the theme's folder in your terminal. If [you're using VS Code](https://ghost.org/tutorials/download-a-code-editor/) as your code editor, then you can use its built-in terminal.

If you haven't installed Node, you'll [need to install it first](https://ghost.org/tutorials/node/). Then, install Gulp and any other required software for your theme (dependencies),  
typing the following command in the terminal and hit `enter`.

```
npm install
```

Once dependencies are installed, process the CSS to reflect the changes you made by running:

```
npm run zip
```

This command tells Gulp to pull together the changes made in your CSS files, optimize them, and add everything to a zip file located in the theme's `dist` folder.

The video below shows the commands in action.

0:00/

Running npm install and npm run zip

You only need to run `npm install` once to download the necessary dependencies in each theme. After that, just run `npm run zip` whenever you're making stylistic changes and want to upload a new version of your theme.

All that’s left to do now is to upload the zip file in Ghost Admin. Refresh your site and voilà – your changes are active!

Conclusion
----------

Knowing how to use a development tool like Gulp is essential for more advanced Ghost theme development – and you now have that knowledge!

You are well on your way to creating your own version of an official Ghost theme or even creating a theme entirely from scratch. Come, learn, and discuss the process [in our Forum](https://forum.ghost.org/?ref=ghost.org) with creators and developers from around the world.

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Essential concepts to know when building a Ghost theme

7 min read](/tutorials/essential-concepts/)

[### How to install Ghost locally

3 min read](/tutorials/local-ghost/)

[### Open a theme in a code editor

1 min read](/tutorials/open-a-theme-in-a-code-editor/)

[### How to add social media icons to your site

4 min read](/tutorials/add-social-media-icons/)

[### How to add an offer banner

4 min read](/tutorials/offer-banners/)







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









