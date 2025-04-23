Build A Custom JavaScript App With Headless Ghost + Next.js
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Learn how to spin up a JavaScript app using Ghost as a headless CMS and build a completely custom front-end with the [Next.js](https://nextjs.org/) React framework.

![Diagram of Ghost providing content to Next.js via the Content API](/images/docs/jamstack/admin-api-nextjs-diagram_hu6b6862f95924f13ac7cefb7109ba7c36_20338_1000x0_resize_q100_h2_box_3.webp)
> Hey, I finally have a new website 👋  
>   
> I’m a founder, designer, and filmmaker — and I’m trying to capture a bit more of all of this with my new site.  
>   
> Had a lot of fun making this in Next.js, with [@TryGhost](https://twitter.com/TryGhost?ref_src=twsrc%5Etfw) as backend, deployed on [@vercel](https://twitter.com/vercel?ref_src=twsrc%5Etfw).  
>   
> Check it out → <https://t.co/iawYNTuB8y> [pic.twitter.com/o1i81y5uL6](https://t.co/o1i81y5uL6)
> 
> — Fabrizio Rinaldi (@linuz90) [August 3, 2021](https://twitter.com/linuz90/status/1422574429754822661?ref_src=twsrc%5Etfw)

Prerequisites
-------------

This configuration of a Ghost publication requires existing moderate knowledge of JavaScript and [React](https://reactjs.org/). You’ll need an active Ghost account to get started, which can either be self-hosted or using [Ghost(Pro)](/pricing/).

Additionally, you’ll need to setup a React & Next.js application via the command line:

```
yarn create next-app
cd my-next-app
yarn dev

```

Next.js can also be setup manually – refer to the [official Next.js documentation](https://nextjs.org/docs) for more information.

Getting started
---------------

Thanks to the [JavaScript Content API Client Library](/docs/content-api/javascript/), it’s possible for content from a Ghost site can be directly accessed within a Next.js application.

Create a new file called `posts.js` within an `lib/` directory. This file will contain all the functions needed to request Ghost post content, as well as an instance of the Ghost Content API.

Install the official [JavaScript Ghost Content API](/docs/content-api/javascript/#installation) helper using:

```
yarn add @tryghost/content-api

```

Once the helper is installed it can be added to the `posts.js` file using a [static `import` statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import):

```
import GhostContentAPI from "@tryghost/content-api";

```

Now an instance of the Ghost Content API can be created using Ghost site credentials:

```
import GhostContentAPI from "@tryghost/content-api";
// Create API instance with site credentials
const api = new GhostContentAPI({
  url: 'https://demo.ghost.io',
  key: '22444f78447824223cefc48062',
  version: "v5.0"
});

```

Change the `url` value to the URL of the Ghost site. For Ghost(Pro) customers, this is the Ghost URL ending in `.ghost.io`, and for people using the self-hosted version of Ghost, it’s the same URL used to view the admin panel.

Create a custom integration within Ghost Admin to generate a key and change the `key` value.

![Ghost Admin new Integration view](/images/docs/apikey_huc23d3a1fbe859434094a9db94f574d9a_265920_2920x0_resize_q100_h2_box_3.webp)

For more detailed steps on setting up Integrations check out [our documentation on the Content API](/docs/content-api/#authentication).

### Exposing content

The [`posts.browse()`](/docs/content-api/javascript/#endpoints) endpoint can be used to get all the posts from a Ghost site. This can be done with the following code as an asynchronous function:

```
export async function getPosts() {
  return await api.posts
    .browse({
      limit: "all"
    })
    .catch(err => {
      console.error(err);
    });
}

```

Using an asynchronous function means Next.js will wait until all the content has been retrieved from Ghost before loading the page. The `export` function means your content will be available throughout the application.

### Rendering posts

Since you’re sending content from Ghost to a React application, data is passed to pages and components with [`props`](https://reactjs.org/docs/components-and-props.html). Next.js extends upon that concept with [`getStaticProps`](https://nextjs.org/docs/basic-features/data-fetching#getstaticprops-static-generation). This function will load the Ghost site content into the page before it’s rendered in the browser.

Use the following to import the `getPosts` function created in previous steps within a page you want to render Ghost posts:

```
import { getPosts } from '../lib/posts';

```

The posts can be fetched from within `getStaticProps` for the given page:

```
export async function getStaticProps(context) {
  const posts = await getPosts()
  if (!posts) {
    return {
      notFound: true,
    }
  }
  return {
    props: { posts }
  }
}

```

Now the posts can be used within the `IndexPage` via the component `props`:

```
const IndexPage = (props) => (
  <ul>
    {props.posts.map(post => (
      <li key={post.id}>{post.title}</li>
    ))}
  </ul>
);

```

Pages in Next.js are stored in a `pages/` directory. To find out more about how pages work [check out the official documentation](https://nextjs.org/docs#basic-example).

### Rendering a single post

Retrieving Ghost content from a single post can be done in a similar fashion to retrieving all posts. By using [`posts.read()`](/docs/content-api/javascript/#endpoints) it’s possible to query the Ghost Content API for a particular post using a [post `id` or `slug`](/docs/content-api/#posts).

Reopen the `lib/posts.js` file and add the following async function:

```
export async function getSinglePost(postSlug) {
  return await api.posts
    .read({
      slug: postSlug
    })
    .catch(err => {
      console.error(err);
    });
}

```

This function accepts a single `postSlug` parameter, which will be passed down by the template file using it. The page slug can then be used to query the Ghost Content API and get the associated post data back.

Next.js provides [dynamic routes](https://nextjs.org/docs/routing/dynamic-routes) for pages that don’t have a fixed URL / slug. The name of the js file will be the variable, in this case the post `slug`, wrapped in square brackets – `[slug].js`.

The `getSinglePost()` function can be used within the `[slug].js` file like so:

```
// pages/posts/[slug].js
import { getSinglePost, getPosts } from '../lib/posts';
// PostPage page component
const PostPage = (props) => {
  // Render post title and content in the page from props
  return (
    <div>
      <h1>{props.post.title}</h1>
      <div dangerouslySetInnerHTML={{ __html: props.post.html }} />
    </div>
  )
}
export async function getStaticPaths() {
  const posts = await getPosts()
  // Get the paths we want to create based on posts
  const paths = posts.map((post) => ({
    params: { slug: post.slug },
  }))
  // { fallback: false } means posts not found should 404.
  return { paths, fallback: false }
}
// Pass the page slug over to the "getSinglePost" function
// In turn passing it to the posts.read() to query the Ghost Content API
export async function getStaticProps(context) {
  const post = await getSinglePost(context.params.slug)
  if (!post) {
    return {
      notFound: true,
    }
  }
  return {
    props: { post }
  }
}

```

Pages can be linked to with the Next.js `<Link/>` component. Calling it can be done with:

```
import Link from 'next/link';

```

The `Link` component is used like so:

```
const IndexPage = (props) => (
  <ul>
    {props.posts.map(post => (
      <li key={post.id}>
        <Link href={`/${post.slug}`}>
          <a>{post.title}</a>
        </Link>
      </li>
    ))}
  </ul>
);

```

Pages are linked in this fashion within Next.js applications to make full use of client-side rendering as well as server-side rendering. To read more about how the `Link` component works and it’s use within Next.js apps [check out their documentation](https://nextjs.org/docs/api-reference/next/link).

Examples
--------

The flexibility of the [Ghost Content API](/docs/content-api/javascript/) allows you to feed posts, pages and any other pieces of content from Ghost site into a Next.js JavaScript app.

Below are a few examples of how content from Ghost can be passed into a Next.js project.

Getting pages
-------------

Pages can be generated in the [same fashion as posts](/docs/jamstack/nextjs/#exposing-content), and can even use the same dynamic route file.

```
export async function getPages() {
  return await api.pages
    .browse({
      limit: "all"
    })
    .catch(err => {
      console.error(err);
    });
}

```

Adding post attribute data
--------------------------

Using the `include` option within the Ghost Content API means that attribute data, such as tags and authors, will be included in the post object data:

```
export async function getPosts() {
  return await api.posts
    .browse({
      include: "tags,authors",
      limit: "all"
    })
    .catch(err => {
      console.error(err);
    });
}

```
### Rendering author pages

An author can be requested using the [`authors.read()`](/docs/content-api/javascript/#endpoints) endpoint.

```
export async function getAuthor(authorSlug) {
  return await api.authors
    .read({
      slug: authorSlug
    })
    .catch(err => {
      console.error(err);
    });
}

```

A custom author template file can be created at `pages/authors/[name].js`, which will also prevent author URLs colliding with post and page URLs:

```
import { getAuthor, getAllAuthors } from '../../api/authors';
const AuthorPage = (props) => {
  return (
    <div>
      <h1>{props.author.name}</h1>
      <div dangerouslySetInnerHTML={{ __html: props.author.bio }} />
    </div>
  )
}
export async function getStaticPaths() {
  const authors = await getAllAuthors()
  const paths = authors.map((author) => ({
    params: { name: author.name },
  }))
  return { paths, fallback: false }
}
export async function getStaticProps(context) {
  const author = await getAuthor(context.params.name)
  if (!author) {
    return {
      notFound: true,
    }
  }
  return {
    props: { author }
  }
}
export default AuthorPage;

```
### Formatting post dates

The published date of a post, `post.published_at`, is returned as a date timestamp. Modern JavaScript methods can convert this date into a selection of humanly readable formats. To output the published date as “Aug 28, 1963”:

```
const posts = await getPosts();
posts.map(post => {
  const options = {
    year: 'numeric',
    month: 'short',
    day: 'numeric'
  };
  post.dateFormatted = new Intl.DateTimeFormat('en-US', options)
    .format(new Date(post.published_at));
});

```

The date can then be added to the template using `{post.dateFormatted}`.

Further reading
---------------

Check out the extensive [Next.js documentation](https://nextjs.org/docs) and [learning courses](https://nextjs.org/learn/basics/getting-started) for more information and to get more familiar when working with Next.js.

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

