Ghost reverse proxy configuration - avoiding infinite redirect loops
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Ghost is designed to have a reverse proxy in front of it. If you use Ghost-CLI to install Ghost, this will be setup for you using nginx. If you configure your own proxy, you’ll need to make sure the proxy is configured correctly.

The configuration used by [Ghost CLI](https://github.com/TryGhost/Ghost-CLI/tree/master/extensions/nginx/templates) looks like this:

```
location / {
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header Host $http_host;
    proxy_pass http://127.0.0.1:2368;
}

client_max_body_size 50m;

```

If you run into an infinite redirect loop when trying to configure your own proxy with nginx, apache, cloudfront or any other proxy and serving Ghost over HTTPS, this is due to the `x-forwarded-proto` header being set incorrectly. Your proxy will handle SSL termination and proxy to Ghost using http. To tell Ghost that the requests coming into the proxy are secure, set the `x-forwarded-proto` header to `https`. Without this, Ghost will think the requests are insecure, attempt to redirect to the https version of a URL and cause an infinite redirect loop.

If you’re using nginx, don’t forget to also increase the max body size if you need to allow for large uploads of images, themes or imports.

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

