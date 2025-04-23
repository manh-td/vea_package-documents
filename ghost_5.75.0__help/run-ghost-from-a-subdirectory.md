


Using Ghost(Pro) with a subdirectory










































Search






 
[Help /](/help/) 
Ghost manual
Ghost(Pro)
FAQ

[Ghost manual](/help/manual/)
[Ghost(Pro)](/help/topic/ghost-pro/)
[FAQ](/help/topic/faq/)

 [Ghost manual](/help/manual/)
[Ghost(Pro)](/help/topic/ghost-pro/)
[FAQ](/help/topic/faq/)



##### Topics

### Getting started

* [Site setup](https://ghost.org/help/site-setup/)
* [Invite your team](https://ghost.org/help/managing-your-team/)
* [Importing content](https://ghost.org/help/imports/)
* [Site navigation](https://ghost.org/help/updating-navigation/)

### Publishing

* [Intro to the editor](https://ghost.org/help/using-the-editor)
* [Cards](https://ghost.org/help/cards)
* [Posts](https://ghost.org/help/posts/)
* [Pages](https://ghost.org/help/pages/)
* [Tags](https://ghost.org/help/tags)
* [Protected content](https://ghost.org/help/protected-content)
* [Snippets](https://ghost.org/help/snippets)
* [Post settings](https://ghost.org/help/post-settings)
* [Publishing and scheduling](https://ghost.org/help/publishing-content)
* [Organizing content](https://ghost.org/help/organizing-content)
* [Markdown guide](https://ghost.org/help/using-markdown)
* [Keyboard shortcuts](https://ghost.org/help/keyboard-shortcuts/)
* [Ghost Bookmarker](https://ghost.org/help/ghost-bookmarker/)

### Memberships

* [Setting up members](https://ghost.org/help/setup-members)
* [Customizing Portal](https://ghost.org/help/customize-portal)
* [Importing members](https://ghost.org/help/import-members)
* [Embeddable signup forms](https://ghost.org/help/embeddable-signup-forms/)
* [Welcome pages](https://ghost.org/help/welcome-pages)
* [Comments](https://ghost.org/help/commenting)
* [Member management](https://ghost.org/help/member-management)
* [Member impersonation](https://ghost.org/help/impersonate-members)
* [Recommendations](https://ghost.org/help/recommendations/)

### Payments

* [Connecting Stripe](https://ghost.org/help/stripe)
* [Creating paid tiers](https://ghost.org/help/tiers)
* [Tips & donations](https://ghost.org/help/tips-and-donations/)
* [Free trials](https://ghost.org/help/free-trials)
* [Complimentary plans](https://ghost.org/help/complimentary-plans)
* [Offers](https://ghost.org/help/offers)
* [Google Pay](https://ghost.org/help/google-pay)
* [Apple Pay](https://ghost.org/help/apple-pay)

### Newsletters

* [Setting up email newsletters](https://ghost.org/help/setup-email-newsletters)
* [Newsletter template settings](https://ghost.org/help/email-design)
* [Audience feedback](https://ghost.org/help/audience-feedback)
* [Delivering emails](https://ghost.org/help/delivering-emails)
* [Updating links in newsletters](https://ghost.org/help/updating-links)
* [Deliverability tips](https://ghost.org/help/deliverability-tips)

### Design

* [Design settings](https://ghost.org/help/design-settings)
* [Installing themes](https://ghost.org/help/installing-a-theme)
* [Site search](https://ghost.org/help/search)
* [Announcement bar](https://ghost.org/help/announcement-bar)
* [Adding styles with code injection](https://ghost.org/help/code-injection-styles)

### Advanced settings

* [History log](https://ghost.org/help/history)
* [Redirects](https://ghost.org/help/redirects)
* [Integrations](https://ghost.org/help/integrations)
* [Exports](https://ghost.org/help/exports)
* [SEO](https://ghost.org/help/seo)
* [Spam filters](https://ghost.org/help/signup-spam-protection/)

### Growth & analytics

* [The dashboard](https://ghost.org/help/dashboard)
* [Post analytics](https://ghost.org/help/post-analytics)
* [Creating custom sources](https://ghost.org/help/custom-sources)
* [Website analytics](https://ghost.org/help/website-analytics)

### Labs

* [Social web (beta)](https://ghost.org/help/social-web)

[← Back to Ghost(Pro)](/help/topic/ghost-pro/)

If you have an existing site — for example a shop, or a static site hosted elsewhere — Ghost can be run from a separate location e.g. `yourdomain.com/blog`, otherwise known as a subdirectory.

Subdirectory and proxy setups are a paid add-on for our [Business plan](https://ghost.org/pricing/) and require a specific custom Nginx or Apache configuration. In addition to a proxy, you must contact us to indicate the path to be used with your publication.

Example configurations
----------------------

The following configurations show how to setup a reverse proxy for a subdirectory.

* [Nginx](#nginx)
* [Apache](#apache)
* [CloudFront](#cloudfront)
* [Cloudflare](#cloudflare-workers)
* [Netlify](#netlify)
* [NextJS](#nextjs)

Reverse proxy rules
-------------------

Follow these rules to create a valid reverse proxy to Ghost(Pro). You can use the same setup to proxy if you don't need a subdirectory as well.

**1. Provide a certificate & serve HTTPS traffic.**  
Only HTTPS traffic is supported.

**2. Redirect non-HTTPS traffic to HTTPS.**  
It's more performant for this to be configured at the proxy level.

**3. Proxy to your ghost.io subdomain, leaving it set as the HOST header.**  
Required to get through our security layer.

**4. Have an X-Forwarded-Host header that matches the custom domain in Ghost(Pro) > Domains.**  
Without this, your blog will redirect to your ghost.io subdomain, causing a loop.

**5. Include the X-Forwarded-Proto header set to https not http.**  
Without this your blog will redirect to https, causing a loop.

**6. Include the X-Forwarded-For header, populated with the remote IP of the original request.**  
Without this, we aren't able to detect spam traffic patterns and your site risks being rate limited or incorrectly restricted. Ensure that only the client IP is passed through here rather than appending to the header that the client has sent, otherwise clients will be able to spoof their IP address.

**7. Pass through all requests with the correct methods and headers**  
Your proxy must forward all HEAD, GET, POST, PUT and DELETE requests to your host with the request method, headers, and response intact, and must also pass through all standard HTTP headers and any `x-ghost` headers, including Authorization and set-cookie.

**8. Ensure your DNS is dynamic**   
The underlying IPs of our infrastructure change regularly. If your proxy caches these values and is not able to refresh this dynamically your proxy will go offline without warning. Your proxy should therefore be configured with dynamic DNS resolution.

Validating your configuration
-----------------------------

To verify your proxy is correctly configured, run this command to validate the correct headers are being sent:

`curl -IL -H 'x-ghost-proxy:true' https://<your domain here>/<subdirectory>`

If correct you’ll see a response header of `x-ghost-proxy` set to `VALID`. Otherwise you'll see `INVALID` next to it, and you should start by checking:

1. `x-forwarded-host` must match your base custom domain set within Ghost Admin - if you're configuring `example.com/blog/` then this would be `example.com`
2. `x-ghost-forwarded-proto` must always be `https`
3. `x-ghost-host` must always be their publication’s ghost.io URL - eg. `yoursite.ghost.io`

Once headers have been validated, you should complete the following actions to verify that traffic is being correctly routed and the site is behaving as expected:

* Login to `https://<your domain here>/<subdirectory>/ghost/`
* Upload an image
* Create and schedule a post
* Delete a post
* Verify changes reflected in the sitemap at `https://<your domain here>/<subdirectory>/sitemap.xml`

If everything looks good, you're all set!

### Troubleshooting

These configurations are only *guaranteed* to work in isolation. If you have any pre-existing top-level domain config, this could override the subdirectory. To troubleshoot any issues, review your top-level domain config for conflicts.

---

Nginx
-----

It's possible to setup a reverse proxy using an nginx configuration to establish a subdirectory on Ghost(Pro).

Paste the exact configuration below into your nginx configuration file, updating each line as specified so that it meets our [reverse proxy rules](#reverse-proxy-rules).

```
server {
    listen 80;

    server_name <yourdomain.com>; # Replace with your domain

    # include any global or shared config
    # include /etc/nginx/conf/your-config-here.conf;
 
    # redirect to SSL
    return 301 https://$host$request_uri; 
}

server {
    listen 443 ssl default_server;

    server_name <yourdomain.com>; # Replace with your domain

    # Your SSL Certificate details. Replace with your own SSL setup
    # ssl_certificate /path/to/cert;
    # ssl_certificate_key /path/to/key;

    location /blog/ {
        client_max_body_size 10G; # Required for uploading large files
    
        # Proxy Settings, all required
        resolver 1.1.1.1 8.8.8.8; # Prevent caching the upstream IP - use preferred DNS resolvers or leave as default
        set $ghost_url https://<yoursubdomain>.ghost.io; # Replace with your subdomain
        proxy_pass $ghost_url; # Variable name must match line above, use of variable required for resolver
        proxy_redirect off;
        proxy_set_header Host <yoursubdomain>.ghost.io; # Replace with your subdomain
        proxy_set_header X-Forwarded-Host <yourdomain.com>; # Replace with your domain
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```

This configuration has been tested and works with these exact settings if there are no conflicting top-level config issues.

⚠️Nginx proxies configured without a resolver will cache IP addresses and cause your site to go offline without warning whenever our underlying infrastructure changes. You must use a resolver configuration when proxying with nginx.

---

Apache
------

It's possible to setup a reverse proxy using Apache to establish a subdirectory on Ghost(Pro).

Paste the exact configuration below into your nginx configuration file, updating each line as specified so that it meets our [reverse proxy rules](#reverse-proxy-rules):

```
# You'll need to enable the ssl, proxy and proxy_http modules:
# sudo a2enmod ssl proxy proxy_http

<VirtualHost *:80>
    # Replace with your domain
    ServerName <yourdomain.com> 
    # Replace with your domain
    Redirect permanent / https://<yourdomain.com>  
</VirtualHost>
<VirtualHost *:443>
    # Replace with your domain
    ServerName <yourdomain.com> 
        
    SSLProxyEngine on

    # Your SSL Certificate details. Replace with your own SSL setup
    # SSLCertificateFile /path/to/cert
    # SSLCertificateKeyFile /path/to/key;

    <Location "/blog">
        # Replace with your subdomain, https matters here
        ProxyPass https://<yoursubdomain>.ghost.io/blog
    </Location>
</VirtualHost>
```

This configuration has been tested and works with these exact settings if there are no conflicting top-level config issues.

---

CloudFront
----------

It's possible to use an AWS CloudFront Distribution to setup a subdirectory with Ghost(Pro). Use of CloudFront for a subdirectory setup is considered highly advanced and may require additional technical knowledge and troubleshooting.

The below configuration has been tested and works with these exact settings if there are no conflicting top-level config issues.

### Distribution Settings

![](https://ghost.org/help/content/images/2023/04/cloudfront-distribution-settings.png)

* **Alternate Domain Names** must match the custom domain you want to use
* The **SSL Certificate** must match the desired custom domain (either exact or wildcard).

### Origins & origin groups settings

![](https://ghost.org/help/content/images/2023/04/cloudfront-origin-settings-1.png)

* **Origin Domain Name** must match the ghost.io URL
* **X-Forwarded-Host** must be set to the desired custom domain
* **X-Forwarded-Proto** must be set to https

### Behavior Settings

The default behavior settings for your distribution can be used, however you will need to setup a second behavior with the following settings:

![](https://ghost.org/help/content/images/2023/04/cloudfront-behaviour-settings-2.png)

* The **Path Pattern** field needs to be set with the desired subdirectory, e.g. `blog*`
* The **Viewer Protocol Policy** must be set to Redirect HTTP to HTTPS
* The **Origin,** **Referer and User-Agent** headers must be whitelisted

### Route 53 Settings / DNS

If you are using Route 53 with your domain to manage DNS records, an alias record must be set with a target of the CloudFront Distribution.

![](https://ghost.org/help/content/images/2023/04/aws-cf-route-53-1.png)

If you are using a non-Route 53 DNS provider, you will need to create an alias record that points to your CloudFront Distribution address.

---

Cloudflare
----------

It's possible to setup a reverse proxy using Cloudflare Workers to establish a subdirectory on Ghost(Pro).

Use of Cloudflare Workers for a subdirectory setup is considered highly advanced and may require additional technical knowledge and troubleshooting.

Paste the exact configuration below into the Worker script area, updating each line as specified so that it meets our [reverse proxy rules](#reverse-proxy-rules), and ensure that your setup references the subdirectory path you are wanting to use (e.g. `/^\\/blog/`).

```
addEventListener('fetch', event => {
  event.respondWith(handleRequest(event.request))
})

/**
 * Respond to the request
 * @param {Request} request
 */
async function handleRequest(request) {
     try {
      
        const urlObject = new URL(request.url);

        // If the request is to the Ghost subdirectory
        if (/^\/blog/.test(urlObject.pathname)) {
          // Then Proxy to Ghost
          const GHOST_URL = "subdomain.ghost.io";
          const CUSTOM_URL = "customdomain.com"; 

          let url = new URL(request.url);

          url.hostname = GHOST_URL;

          let proxyRequest = new Request(url, request);

          proxyRequest.headers.set('Host', GHOST_URL);

          //Have an X-Forwarded-Host header that matches the custom domain in my.ghost.org.

          proxyRequest.headers.set("X-Forwarded-Host", CUSTOM_URL);

          //Include the X-Forwarded-Proto header set to https not http.

          proxyRequest.headers.set("X-Forwarded-Proto", "https");

          //Include the X-Forwarded-For header, populated with the remote IP of the original request.

          let ip = proxyRequest.headers.get("CF-Connecting-IP");

          proxyRequest.headers.set("X-Forwarded-For", ip);

          return await fetch(proxyRequest);

        }

     } catch (error) {

        // if no action found, play the regular request

        return await fetch(request);
    }

    return await fetch(request);
}
```

This configuration has been tested and works with these exact settings if there are no conflicting top-level config issues.

---

Netlify
-------

If you're using Netlify, it's possible to setup a reverse proxy using your `.toml` file to establish a subdirectory on Ghost(Pro).

Paste the exact configuration below into your `netlify.toml` file, updating the values to match your `ghost.io` subdomain and custom domain, so that it meets our [reverse proxy rules](#reverse-proxy-rules), and ensure that your setup references the subdirectory path you are wanting to use (e.g. `/blog/`).

```
[[redirects]]
from = "/blog/*"
to = "https://<subdomain>.ghost.io/blog/:splat"
status = 200
force = true
headers = {X-Forwarded-Host = "<yourdomain.com>"}

[[redirects]]
from = "/blog"
to = "https://<subdomain>.ghost.io/blog/"
status = 200
force = true
headers = {X-Forwarded-Host = "<yourdomain.com>"}

```

---

NextJS
------

If you're using NextJS, it's possible to setup a reverse proxy using a custom NextJS configuration file, to establish a subdirectory on Ghost(Pro).

Paste the exact configuration below into your `next.config.js` file, updating the values to match your `ghost.io` subdomain and custom domain, so that it meets our [reverse proxy rules](#reverse-proxy-rules).

```
/** @type {import('next').NextConfig} */
const nextConfig = {
  trailingSlash: true,
  async rewrites() {
    return [     
      {
        source: "/blog/:path*/",
        destination: "https://<subdomain>.ghost.io/blog/:path*/",
      },
      {
        source: "/blog/:path*",
        destination: "https://<subdomain>.ghost.io/blog/:path*",
      }    
    ];
  },
  async headers() {
    return [
      {
        source: "/blog/:path*",
        headers: [{ key: "x-forwarded-host", value: "your-custom-domain.com" }],
      }
    ];
  }
}

module.exports = nextConfig
```


### Related articles

 
Learn how to setup a custom domain with Ghost(Pro) and Squarespace



 

 
Passwords can be changed from within a staff user profile, or reset directly from the Ghost Admin login area.



 

Was this article helpful?
-------------------------








 





