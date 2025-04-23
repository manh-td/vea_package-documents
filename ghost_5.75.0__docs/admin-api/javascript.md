Admin API JavaScript Client
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Admin API keys should remain secret, and therefore this promise-based JavaScript library is designed for server-side usage only. This library handles all the details of generating correctly formed urls and tokens, authenticating and making requests.

Working Example
---------------

```
const api = new GhostAdminAPI({
  url: 'http://localhost:2368',
  key: 'YOUR_ADMIN_API_KEY',
  version: "v5.0",
});
api.posts.add({
    title: 'My first draft API post',
    lexical: '{"root":{"children":[{"children":[{"detail":0,"format":0,"mode":"normal","style":"","text":"Hello, beautiful world! 👋","type":"extended-text","version":1}],"direction":"ltr","format":"","indent":0,"type":"paragraph","version":1}],"direction":"ltr","format":"","indent":0,"type":"root","version":1}}'
});

```

Authentication
--------------

The client requires the host address of your Ghost API and an Admin API key in order to authenticate.

* `url` - API domain, must not end in a trailing slash.
* `key` - string copied from the “Integrations” screen in Ghost Admin
* `version` - minimum version of the API your code works with

The `url` and `key` values can be obtained by creating a new `Custom Integration` under the Integrations screen in Ghost Admin.

![Get Ghost Admin API credentials](/images/docs/apikey_huc23d3a1fbe859434094a9db94f574d9a_265920_2920x0_resize_q100_h2_box_3.webp)

See the documentation on [Admin API authentication](/docs/admin-api/#authentication) for more explanation.

Endpoints
---------

All endpoints & parameters provided to integrations by the [Admin API](/docs/admin-api/) are supported.

```
// [Stability: stable]
// Browsing posts returns Promise([Post...]);
// The resolved array will have a meta property
api.posts.browse();
api.posts.read({id: 'abcd1234'});
api.posts.add({title: 'My first API post'});
api.posts.edit({id: 'abcd1234', title: 'Renamed my post', updated_at: post.updated_at});
api.posts.delete({id: 'abcd1234'});
// Browsing pages returns Promise([Page...])
// The resolved array will have a meta property
api.pages.browse({limit: 2});
api.pages.read({id: 'abcd1234'});
api.pages.add({title: 'My first API page'})
api.pages.edit({id: 'abcd1234', title: 'Renamed my page', updated_at: page.updated_at})
api.pages.delete({id: 'abcd1234'});
// Uploading images returns Promise([Image...])
api.images.upload({file: '/path/to/local/file'});

```

Publishing Example
------------------

A bare minimum example of how to create a post from HTML content, including extracting and uploading images first.

```
const GhostAdminAPI = require('@tryghost/admin-api');
const path = require('path');
// Your API config
const api = new GhostAdminAPI({
    url: 'http://localhost:2368',
    version: "v5.0",
    key: 'YOUR_ADMIN_API_KEY'
});
// Utility function to find and upload any images in an HTML string
function processImagesInHTML(html) {
    // Find images that Ghost Upload supports
    let imageRegex = /="([^"]*?(?:\.jpg|\.jpeg|\.gif|\.png|\.svg|\.sgvz))"/gmi;
    let imagePromises = [];
    while((result = imageRegex.exec(html)) !== null) {
        let file = result[1];
            // Upload the image, using the original matched filename as a reference
            imagePromises.push(api.images.upload({
                ref: file,
                file: path.resolve(file)
            }));
    }
    return Promise
        .all(imagePromises)
        .then(images => {
            images.forEach(image => html = html.replace(image.ref, image.url));
            return html;
        });
}
// Your content
let html = '<p>My test post content.</p><figure><img src="/path/to/my/image.jpg" /><figcaption>My awesome photo</figcaption></figure>';
return processImagesInHTML(html)
    .then(html => {
        return api.posts
            .add(
                {title: 'My Test Post', html},
                {source: 'html'} // Tell the API to use HTML as the content source, instead of Lexical
            )
            .then(res => console.log(JSON.stringify(res)))
            .catch(err => console.log(err));
    })
    .catch(err => console.log(err));

```

Installation
------------

`yarn add @tryghost/admin-api`

`npm install @tryghost/admin-api`

### Usage

ES modules:

```
import GhostAdminAPI from '@tryghost/admin-api'

```

Node.js:

```
const GhostAdminAPI = require('@tryghost/admin-api');

```
##### On this page

Launch your site
----------------

Last week, 5,069 brand new  
publications got started with Ghost.

Today, it's your turn.

[Start a free trial now →](https://account.ghost.org/signup/)Product

* [Creator platform](/)
* [Theme marketplace](/marketplace/)
* [Integrations](/integrations/)
* [Experts](/experts/)
* [Ghost for news](/news/)
Developers

* [How to install Ghost](/docs/install/)
* [Core concepts](/docs/)
* [Ghost hosting](/pricing/)
* [API documentation](/docs/content-api/)
* [Security overview](/docs/security/)
* [Source code](https://github.com/TryGhost/Ghost)
Resources

* [Ghost tutorials](/tutorials/)
* [Resources](/resources/)
* [Node.js CMS guide](https://nodecms.guide)
* [Open Subscription Platforms](https://opensubscriptionplatforms.com)
Comparisons

* [Ghost vs Substack](/vs/substack/)
* [Ghost vs WordPress](/vs/wordpress/)
* [Ghost vs Medium](/vs/medium/)
* [Ghost vs Memberful](/vs/memberful/)
* [Ghost vs Patreon](/vs/patreon/)
* [Ghost alternatives →](/alternatives/)
Support

* [Help center](/help/)
* [Community forum](https://forum.ghost.org/)
* [Status  
  Triangle
  
  
  
   99.9%](https://status.ghost.org/)
[![Non-Profit Foundation](/images/logos/indie.svg)](/about/)
[![Open Source](/images/logos/opensource.svg)](https://github.com/tryghost)
[![Carbon Neutral](/images/logos/carbonneutral.svg)](https://climate.stripe.com/6MNofu)

