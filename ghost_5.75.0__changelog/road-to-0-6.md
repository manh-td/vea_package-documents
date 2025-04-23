


The Road to 0.6






































Earlier this year we took the time to rewrite major parts of the codebase, which resulted in a big gap between releases. As a project, we need to make up for that by pushing to ship features and reach feature parity with other similar platforms. This guide aims to clarify the [key features](#thetop10featureswevegottahave) that are missing, their importance and current state as well as covering the [infrastructure projects](#infrastructureprojects) that we need to complete in order to ship future features.

The top 10 features we've *gotta* have...
-----------------------------------------

1. [Spell check](#1spellcheck)
2. [Code Injection](#2codeinjection)
3. [Sitemaps](#3sitemaps)
4. [Post Scheduling](#4postscheduling)
5. [Tag Management](#5tagmanagement)
6. [Next/Prev links (the query helper)](#6nextprevlinksthequeryhelper)
7. [Public API (OAuth)](#7publicapioauth)
8. [Navigation menu](#8navigationmenu)
9. [Custom Permalinks](#9custompermalinks)
10. [Post Filtering](#10postfiltering)

These are the top missing features, ordered by importance and determined by a mix of most requests / votes and the value of that feature vs its complexity. Varying technical complexity prevents us from shipping in exactly this order, however it is important to have clear priorities.

Each one of these items has at least one card on the [public roadmap](https://trello.com/b/EceUgtCL/ghost-roadmap?ref=ghost.org), which you can use to keep track of progress and find all of the related GitHub issues. Below is a quick run down of the state of each feature.

### 1. Spell check

This one has always been a bit of an embarrassment so we're super keen to ship it. It has been blocked on our use of CodeMirror in the editor, but recently we developed a plan to get it out the door. It's currently in testing and review, and is expected to ship very soon along with mobile uploads.

### 2. Code Injection

Code Injection provides users with a simple interface in the admin panel to paste code snippets into so they don't have to edit their theme to add things like Google Analytics. This feature is mostly ready, however it was important to test how it behaved with various code snippets and themes. As a result of testing, it seemed best to ship it with the ability to detect if, for example, the active theme has the `{{ghost_head}}` helper. Theme feature detection is tracked in [issue #4319](https://github.com/TryGhost/Ghost/issues/4319?ref=ghost.org).

Moving forward, we should merge the PR with the feature behind a config flag and spec out a minimum shippable version of the theme feature detection concept.

### 3. Sitemaps

A small feature that's important for SEO and therefore key to being an awesome blogging platform. This feature is a WIP at present but is expected to land very soon.

### 4. Post Scheduling

It has become apparent that this feature is blocking bigger organisations from using Ghost. It will be technically challenging to solve in a way that suits the different kinds of environments that Ghost tends to run in. We're currently researching potential ways to solve it and speccing it out.

### 5. Tag Management

The interface for managing, editing and removing tags is going to provide for all kinds of interesting opportunities. It is currently partially implemented behind the config flag 'tagUI', and also requires several updates to the Tag and Post API to make all the features possible.

This is an ongoing WIP with quite a lot of scope, so we intend to focus on shipping a minimum version, as well as ensuring the full set of intended features is documented.

### 6. Next/Prev links (the query helper)

This is for including a link to the next or previous post at the bottom of a post. It depends on an API update (see issue [#4262](https://github.com/TryGhost/Ghost/issues/4262?ref=ghost.org)) and also the query helper.

The API work is planned and marked high priority but not yet in progress. The query helper is currently [being discussed](https://github.com/TryGhost/Ghost/issues/4439?ref=ghost.org) on GitHub and will be relatively straightforward to add once a decision is made on what it should look like.

### 7. Public API (OAuth)

Adding [OAuth](https://github.com/TryGhost/Ghost/issues/4004?ref=ghost.org) to the API so that external apps can access the API safely is receiving a lot of pressure from the community, therefore delivering this should add extra value by encouraging more contributions. It is currently blocked on a tree of dependencies stemming all the way back to permissions and database migrations.

First and foremost, we need to start unblocking progress. The first thing we need to solve is permissions migrations, which is currently a stalled issue. There are also several issues that could be worked on in parallel that will be highlighted in dev meetings.

### 8. Navigation menu

Similar to code injection, allowing users to build a simple navigation menu will help reduce the need to edit themes. The idea is to provide a simple UI to set the title and URL, add a new item and reorder items. The interface is currently being designed.

### 9. Custom Permalinks

Ghost has supported all manner of different permalink formats for some time, but only by editing the setting directly in the DB. The UI for this has been designed and fleshed out in HTML/CSS, so it's ready to wire up in Ember. There is also some functional work needed to ensure all the permutations work 100% and are well-tested.

### 10. Post Filtering

For users with a lot of posts, the content screen doesn't currently cut the mustard. Adding a menu to allow users to filter this is a step in the right direction, but is intended as an intermediary step whilst we work on adding full search capabilities. Work on this has stalled and needs picking up again.

Infrastructure Projects
-----------------------

1. [Permissions Migration](#1permissionsmigration)
2. [File System Abstraction](#2filesystemabstraction)
3. [Image Processing](#3imageprocessing)
4. [DB Migration Improvements](#4dbmigrationimprovements)

Each of these projects will help us to build out major features for Ghost. As they are not user-facing, they don't live on the roadmap, and instead have an issue on GitHub. Below is a quick description of each item.

### 1. Permissions Migration

Issue [#3910](https://github.com/TryGhost/Ghost/issues/3910?ref=ghost.org)

Currently we have a set of permissions fixtures which are loaded into the DB when Ghost is started. These have undergone one wholesale change in the past, so we were able to simply remove the old permissions and create new ones. Now we need to create a simple way to add new permissions for additional endpoints.

Presently, there's no clear plan for what this will look like. We need to research similar existing systems in order to get some inspiration and kickstart the improvement works.

### 2. File System Abstraction

Issue [#2852](https://github.com/TryGhost/Ghost/issues/2852?ref=ghost.org)

Assuming that it's ok to use fs, and that all the images, themes and other bits and pieces will be in the local file system is a bad thing. It makes it hard to use Ghost with a cdn and also has implications for hosts with a transient file system like Heroku.

This work is partly done, we have a storage abstraction for images, but it's not used for everything which it ought to be. We also need to make it pluggable in a simple way so that devs can provide a different storage layer with a simple config change. In order to move forward, the issue will be re-written and split up into smaller tasks.

### 3. Image Processing

Issue [#4453](https://github.com/TryGhost/Ghost/issues/4453?ref=ghost.org)

Adding Imagemagick as a dependency is too complicated, so we need a pure JS way to do resizing, cropping and removing of exif data for images uploaded to Ghost. At present the problem is being researched and discussed on GitHub, with a view to adding image optimisation as a first step.

### 4. DB Migration Improvements

Issue [#4479](https://github.com/TryGhost/Ghost/issues/4479?ref=ghost.org)

So far we're able to add, remove, rename and drop unique constraints on columns in Ghost. In order to make some improvements and build more features we also need to be able to change column types / sizes and we need to make the whole process tonnes easier. Updating the database currently includes a manual process of ensuring we can still import and export, and this complexity needs removing.

The future
----------

There are obviously numerous other features and projects that we need to deliver, like search, i18n, post revisions and diffs, the app platform and tonnes more. After 0.6 the likely focus will be on building one or two bigger features with far-reaching implications like search & i18n. A 'Road to 0.7' issue will appear closer to the time.


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





 





 
















 






