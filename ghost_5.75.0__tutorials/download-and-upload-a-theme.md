





Download and upload a Ghost theme









































---


Whether you want to customize an existing theme or upload one you created, this tutorial will show you two ways to download and upload Ghost themes.

The **first method** uses Ghost Admin. It's perfect for making quick updates to a theme.

The **second method** uses the terminal. It's ideal for when you're developing a custom theme or making more substantial edits.

Use Ghost Admin
---------------

Ghost Admin provides a convenient interface for downloading and uploading themes.

### Download a theme in Ghost Admin

From your dashboard, go to **Settings**.

![Dashboard with the Settings icon highlighted](https://ghost.org/tutorials/content/images/2023/10/dashboard.png)

Next, go to the **Design** page.

![Settings page with Design option highlighted](https://ghost.org/tutorials/content/images/2023/10/design-1.png)

Click **Change theme**.

![Design page with Change theme option highlighted](https://ghost.org/tutorials/content/images/2023/10/change-theme.png)

Click **Installed**. (If you haven't installed the theme you want to download, do that first.)

![](https://ghost.org/tutorials/content/images/2023/10/installed.png)

Click the overflow menu (**...**) and then **Download**. A copy of the theme will be downloaded to your computer 🥳

![Themes page with Download option highlighted](https://ghost.org/tutorials/content/images/2023/10/download.png)
### Upload a theme in Ghost Admin

⚠️Making changes to CSS and JS files likely requires rebuilding those assets before uploading the theme. [See our tutorial for more info](https://ghost.org/tutorials/build-css-files/).

Zip up your theme files. On the Themes page, click **Upload theme**.

![Themes page with Upload theme button highlighted](https://ghost.org/tutorials/content/images/2023/10/upload-1.png)

Select the theme file to upload from your computer. After the theme uploads, choose whether you want to activate it or not. Your theme is now updated!

![email letter on fire](https://ghost.org/tutorials/content/images/size/w1000/2023/04/flames-of-knowledge.jpg)

Use the terminal
----------------

With the terminal, you have more control over uploading and downloading themes. Note that you'll need [Node installed](https://ghost.org/node?ref=ghost.org) for the steps below.

### Download a theme from the terminal

In your terminal, navigate to where you want the theme to live in your filesystem. For this example, we'll use Ghost's official Starter theme, which offers an amazing jump-off place for creating a custom theme. The method shown here will work for most Ghost themes with a GitHub repository, including [all official Ghost themes](https://github.com/tryghost?ref=ghost.org).

[GitHub - TryGhost/Starter: A development starter theme for GhostA development starter theme for Ghost. Contribute to TryGhost/Starter development by creating an account on GitHub.![](https://github.com/fluidicon.png)GitHubTryGhost![](https://opengraph.githubassets.com/102e9b9b2cc4b43f4b2082ded23c7bed97ac39c839674d8da3c39ee9ab305b0a/TryGhost/Starter)](https://github.com/tryghost/starter?ref=ghost.org)

To copy the theme from GitHub to your machine, we're going to use a tool called [degit](https://www.npmjs.com/package/degit?ref=ghost.org). As the name suggests, it removes git from a repository when copying it. This means that you get a clean slate for development but also that you lose the connection to the original repository. When the Starter theme, for example, gets future updates, those updates won't be automatically added to your theme. That's generally not a problem, and the pros of this method outweigh the cons.

In the terminal, run the following command with whatever you want to call your theme's folder:

```
npx degit https://github.com/tryghost/starter super-sick-ghost-theme
```

As mentioned, this command will copy the Starter theme into a new folder called `super-sick-ghost-theme`.

Next, run `cd super-sick-ghost-theme` to go into the new directory and install the dependencies — the code used by and for the theme — by running `npm install`. Optionally, if you want to track the theme using git, run `git init` to initialize the repository.


0:00
/0:15









Most themes will provide commands (in the `package.json` file) to assist with development.

With Starter, there are two important commands to know:

* `npm run dev` starts the theme in development mode. This sets up a live reload server, which allows you to see changes to your theme in real-time when your theme is linked to a local Ghost install. It also recompiles your JS and CSS whenever you make changes.
* `npm run zip` compiles and optimizes your assets. It then compresses your theme files into a zip file that's ready to upload to your Ghost site.

[Learn more about the Starter theme.](https://github.com/tryghost/starter?ref=ghost.org)

Taking these steps provides an optimal development experience. Before you know it, you'll be ready to show your totally customized Ghost theme to the world.

### How to link your theme and local Ghost site

To take advantage of the live reloading provided by the Starter theme, you need to have Ghost installed locally and ensure that your theme folder is in Ghost's theme folder. However, editing code directly in this folder isn't a best practice:

* If you delete your local Ghost site, you also delete your theme
* If you upload a version of your theme, it'll overwrite your local version (it's happened 😅)
* If you want to try your theme with different local installs of Ghost, perhaps with different options configured, it's much more difficult
* You can't keep all your themes in one place

[Symlinking](https://www.freecodecamp.org/news/symlink-tutorial-in-linux-how-to-create-and-remove-a-symbolic-link/?ref=ghost.org) to the rescue! It allows you to create a symbolic copy of your theme in Ghost's theme folder, no matter where the actual theme files are on your system.

Open the terminal and navigate to your local Ghost install. Then, navigate to `content/themes`. On a fresh install, running `ls` in the directory will show `casper`, the default theme installed with Ghost.

To symlink your theme, run this command:

```
ln -s path/to/your/super-sick-custom-theme .
```

`ln -s` creates a symbolic link between your theme folder and the current directory. Running `ls` again now shows your theme in the directory. Finally, run `ghost restart`. (Ghost needs to restart to recognize the new theme.)

Go to your **Theme** settings. In the **Advanced** dropdown, you're custom theme will be available for activation.

![Advanced dropdown to choose your theme in Ghost Admin](https://ghost.org/tutorials/content/images/2023/04/CleanShot-2023-04-13-at-11.52.12.png)

Once activated and with `npm run dev` running, changes made to your theme code will automatically appear in your browser 💫

### Upload a theme from the terminal

It's possible to automatically deploy changes made to your theme from the terminal using Ghost's GitHub Action. When you push a new change to the main branch on GitHub, the Action automatically uploads the updated theme to your Ghost site.

Complete instructions are available on the [GitHub Action page](https://github.com/TryGhost/action-deploy-theme?ref=ghost.org).

![](https://ghost.org/tutorials/content/images/2023/04/gh-action.png)

Summary
-------

You now know how to download and upload Ghost themes. Whether it's using Ghost Admin for quick edits or the terminal for more involved theme development, you're now ready to ship your super sick theme 🚢

If you're looking for a bit of inspiration on how you can customize your theme, check out these tutorials:

* [Add a table of contents](https://ghost.org/tutorials/adding-table-of-contents/)
* [Build a custom homepage](https://ghost.org/tutorials/custom-homepage/)
* [Create a read-next section](https://ghost.org/tutorials/read-next/)

And, if you're looking for some friends in your theme creation journey, come to [our official Forum](https://forum.ghost.org/?ref=ghost.org), where we chat about all things Ghost!

**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Send a custom welcome email

5 min read](/tutorials/welcome-email/)

[### Open a theme in a code editor

1 min read](/tutorials/open-a-theme-in-a-code-editor/)

[### How to use Code Injection

4 min read](/tutorials/use-code-injection-in-ghost/)

[### Download a code editor

1 min read](/tutorials/download-a-code-editor/)

[### The complete guide to comments

3 min read](/tutorials/adding-comments/)

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









