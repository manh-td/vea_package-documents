Importing content from other platforms to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

The only strictly required field when importing posts/pages is the title. Ghost will automatically generate slugs and set every other field to the default or empty.

To import a valid post with content, published at a specific time, the bare minimum fields to provide are title, mobiledoc, status and published:

```
{
    "title": "my blog post title",
    "mobiledoc": "{\"version\":\"0.3.1\",\"atoms\":[],\"cards\":[],\"markups\":[],\"sections\":[[1,\"p\",[[0,[],0,\"You're live, nice!\"]]]]}",
    "status": "published",
    "published_at":  1283780649000
}

```

The `status` field defaults to `draft`. Set it to `published` and set `published_at` to a past millisecond timestamp in order to import an already published post with the correct date. You can also set `status` to `scheduled` and set `published_at` to a future date to create a post that will be scheduled in future.

Mobiledoc is the data format used internally by Ghost to represent your content. See the section on [mobiledoc](#mobiledoc) below for more details on converting content.

Mobiledoc
---------

Mobiledoc is a standardised JSON-based document storage format, which forms the heart of publishing with Ghost. In order to import content into Ghost, it must first be converted to mobiledoc.

Although mobiledoc is a JSON format, the mobiledoc field in the import file should be serialised into a string, which can be done by calling `JSON.stringify()`.

Ghost’s importer is not able to accept other formats, such as HTML or markdown. Instead, there are tools available for converting from these formats into mobiledoc prior to importing.

### Converting HTML

The easiest way to convert HTML to mobiledoc is to generate a Ghost JSON file with `html` fields containing your content for each post instead of `mobiledoc`.
You can then use Ghost’s standalone migration tool to convert the `html` field to a `mobiledoc` field.

1. Requires Node.js v10 installed locally
2. `npm install @tryghost/migrate -g` - install the migration tooling
3. `migrate json html /path/to/your/import.json` - will convert the HTML fields in your JSON file
4. The tool will output a path to a converted JSON file - use this to import your content
5. Run `npm uninstall @tryghost/migrate -g` to cleanup

This should work well for most semantic HTML, and result in a series of populated cards in the editor, making it easy to update your content in future.

#### Mobiledoc HTML card

If your html consists of tables or other non-semantic markdown, you may have a better experience wrapping the HTML in a single HTML card:

```
mobiledoc = JSON.stringify({
    version: '0.3.1',
    markups: [],
    atoms: [],
    cards: [['html', {cardName: 'html', html: '<p>HTML goes here</p>'}]],
    sections: [[10, 0]]
});

```
### Converting Markdown

There are two approaches for converting markdown to mobiledoc. The first is to convert your markdown content to HTML first using the tool of your choice, and then follow the steps above for converting HTML to mobiledoc.

The second is to wrap your markdown content in a single markdown card:

```
mobiledoc = JSON.stringify({
    version: '0.3.1',
    markups: [],
    atoms: [],
    cards: [['markdown', {cardName: 'markdown', markdown: 'markdown content goes here...'}]],
    sections: [[10, 0]]
});

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

