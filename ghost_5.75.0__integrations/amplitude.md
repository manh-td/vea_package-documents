Official Ghost + Amplitude Integration
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
##### On this page

##### You might also like...

* [![Plausible](/images/logos/integrations/plausible_hubdd59c639a2e80e3d62ecbddcb793d1c_52957_50x0_resize_q100_h2_box_3.webp)Plausible](/integrations/plausible/)
* [![Google Analytics](/images/logos/integrations/google-analytics_hu4d123172e6791cf5e37b9720bc0d3de1_1524_50x0_resize_q100_h2_box_3.webp)Google Analytics](/integrations/google/)
* [![Custom Integrations](/images/logos/integrations/custom.svg)Custom Integrations](/integrations/custom-integrations/)
* [![ChartMogul](/images/logos/integrations/chartmogul_hu01c73d47915043033a3a07dcbb830fa7_3078_50x0_resize_q100_h2_box_3.webp)ChartMogul](/integrations/chartmogul/)
* [![Churnbuster](/images/logos/integrations/churnbuster_hudae337c0f674707d1840f4c514d865a7_15531_50x0_resize_q100_h2_box_3.webp)Churnbuster](/integrations/churnbuster/)
[Integrations](/integrations/)
/
[Analytics](/integrations/?tag=Analytics)

Integrate Ghost with Amplitude and gain a better understanding about what makes your members tick using reliable site analytics

It’s possible to get in-depth site metrics with an [Amplitude](https://amplitude.com/) integration for site-wide tracking. Amplitude is a **product analytics** tool that allows you to understand user behaviour across your site to grow your business. This integration is particularly useful for Ghost membership sites, since you can track and measure important member engagement metrics.

Keep reading to find out how to connect Amplitude to your Ghost site.

Prerequisites
-------------

Amplitude offer free and paid-for plans to power your site analytics. If you haven’t already, create a new account, verify it and then follow the instructions to **create an organisation** and a **project**. Once you’re all set up, you’re ready to send data from your site to Amplitude.

> This is an advanced analytics integration which requires editing your Ghost theme, and implementing code. For simple site analytics, you may also want to check out [Plausible](/integrations/plausible/) or [Google Analytics](/integrations/google/).

Copy the Amplitude installation code
------------------------------------

Copy the JavaScript SDK Installation code which can be found in the Amplitude setup dashboard, in their [documentation](https://amplitude.zendesk.com/hc/en-us/articles/115001361248-JavaScript-SDK-Installation), or you can copy it directly from here:

```
<script type="text/javascript">
    (function(e,t){var n=e.amplitude||{_q:[],_iq:{}};var r=t.createElement("script")
    ;r.type="text/javascript"
    ;r.integrity="sha384-+EOJUyXoWkQo2G0XTc+u2DOlZkrMUcc5yOqCuE2XHRnytSyqpFQSbgFZAlGmjpLI"
    ;r.crossOrigin="anonymous";r.async=true
    ;r.src="https://cdn.amplitude.com/libs/amplitude-7.1.1-min.gz.js"
    ;r.onload=function(){if(!e.amplitude.runQueuedFunctions){
    console.log("[Amplitude] Error: could not load SDK")}}
    ;var i=t.getElementsByTagName("script")[0];i.parentNode.insertBefore(r,i)
    ;function s(e,t){e.prototype[t]=function(){
    this._q.push([t].concat(Array.prototype.slice.call(arguments,0)));return this}}
    var o=function(){this._q=[];return this}
    ;var a=["add","append","clearAll","prepend","set","setOnce","unset"]
    ;for(var c=0;c<a.length;c++){s(o,a[c])}n.Identify=o;var u=function(){this._q=[]
    ;return this}
    ;var l=["setProductId","setQuantity","setPrice","setRevenueType","setEventProperties"]
    ;for(var p=0;p<l.length;p++){s(u,l[p])}n.Revenue=u
    ;var d=["init","logEvent","logRevenue","setUserId","setUserProperties","setOptOut","setVersionName","setDomain","setDeviceId","enableTracking","setGlobalUserProperties","identify","clearUserProperties","setGroup","logRevenueV2","regenerateDeviceId","groupIdentify","onInit","logEventWithTimestamp","logEventWithGroups","setSessionId","resetSessionId"]
    ;function v(e){function t(t){e[t]=function(){
    e._q.push([t].concat(Array.prototype.slice.call(arguments,0)))}}
    for(var n=0;n<d.length;n++){t(d[n])}}v(n);n.getInstance=function(e){
    e=(!e||e.length===0?"$default_instance":e).toLowerCase()
    ;if(!n._iq.hasOwnProperty(e)){n._iq[e]={_q:[]};v(n._iq[e])}return n._iq[e]}
    ;e.amplitude=n})(window,document);
    amplitude.getInstance().init("API_KEY");
</script>

```

Add your API key
----------------

Replace `("API_KEY")` with the key provided in your setup dashboard, for the JavaScript SDK source you are creating:

![](/images/integrations/API-key_hu4e97633670e55e59c0908c187fcc88f0_216113_1032x0_resize_q100_h2_box_3.webp)

Add {{@member.email}}
---------------------

If you’re using Amplitude to implement analytics for a Ghost Membership site, the final addition to make to your tracking code is to add `{{@member.email}}`. This allows you to see which members perform events on your site!

You’ll need to add this to the same line as your Amplitude API Key, on the last line before the closing `</script>` tag. This line of code should look like this:

```
amplitude.getInstance().init("a1648c10e905eb99929c61ab923a02a2", "{{@member.email}}");

```

Paste your installation code into your theme
--------------------------------------------

Now that you have your Amplitude tracking code ready to go, it’s time to add it to your theme.

It’s recommended to place your code in the `default.hbs` file before the closing `</head>` tag. When using Members as shown above, wrap the code inside an `{{#if @member}}`.

Here’s an example:

```
{{#if @member}}
<script type="text/javascript">
    (function(e,t){var n=e.amplitude||{_q:[],_iq:{}};var r=t.createElement("script")
    ;r.type="text/javascript"
    ;r.integrity="sha384-+EOJUyXoWkQo2G0XTc+u2DOlZkrMUcc5yOqCuE2XHRnytSyqpFQSbgFZAlGmjpLI"
    ;r.crossOrigin="anonymous";r.async=true
    ;r.src="https://cdn.amplitude.com/libs/amplitude-7.1.1-min.gz.js"
    ;r.onload=function(){if(!e.amplitude.runQueuedFunctions){
    console.log("[Amplitude] Error: could not load SDK")}}
    ;var i=t.getElementsByTagName("script")[0];i.parentNode.insertBefore(r,i)
    ;function s(e,t){e.prototype[t]=function(){
    this._q.push([t].concat(Array.prototype.slice.call(arguments,0)));return this}}
    var o=function(){this._q=[];return this}
    ;var a=["add","append","clearAll","prepend","set","setOnce","unset"]
    ;for(var c=0;c<a.length;c++){s(o,a[c])}n.Identify=o;var u=function(){this._q=[]
    ;return this}
    ;var l=["setProductId","setQuantity","setPrice","setRevenueType","setEventProperties"]
    ;for(var p=0;p<l.length;p++){s(u,l[p])}n.Revenue=u
    ;var d=["init","logEvent","logRevenue","setUserId","setUserProperties","setOptOut","setVersionName","setDomain","setDeviceId","enableTracking","setGlobalUserProperties","identify","clearUserProperties","setGroup","logRevenueV2","regenerateDeviceId","groupIdentify","onInit","logEventWithTimestamp","logEventWithGroups","setSessionId","resetSessionId"]
    ;function v(e){function t(t){e[t]=function(){
    e._q.push([t].concat(Array.prototype.slice.call(arguments,0)))}}
    for(var n=0;n<d.length;n++){t(d[n])}}v(n);n.getInstance=function(e){
    e=(!e||e.length===0?"$default_instance":e).toLowerCase()
    ;if(!n._iq.hasOwnProperty(e)){n._iq[e]={_q:[]};v(n._iq[e])}return n._iq[e]}
    ;e.amplitude=n})(window,document);
    amplitude.getInstance().init("a1648c10e905eb99929c61ab923a02a2", "{{@member.email}}");
</script>
{{/if}}

```
> Read more about editing your theme and deploying it using [GitHub Actions](/integrations/github/)!

Add some events
---------------

The next step is to log an event to complete your setup. The most common events are as follows:

### Viewed homepage

This adds an event so you can see when a member has viewed your homepage. To implement this event, add the following code to the bottom of your `index.hbs` file:

```
{{#if @member}}
<script type="text/javascript">
    amplitude.getInstance().logEvent('Viewed Homepage');
</script>
{{/if}}

```
### Viewed post

This adds an event so you can see when members view posts on your site. Add the following code to the bottom of your `post.hbs` file:

```
{{#if @member}}
<script type="text/javascript">
    var karma = new amplitude.Identify().add('karma', 1);
    amplitude.getInstance().identify(karma);
    amplitude.getInstance().logEvent('Viewed Post');
    $(function () {
        var txt = $(".gh-content")[0].textContent,
            words = txt.replace(/[^\w ]/g, "").split(/\s+/).length + " words, ";
        function numberWithCommas(x) {
            x = x.toString();
            var pattern = /(-?\d+)(\d{3})/;
            while (pattern.test(x))
                x = x.replace(pattern, "$1,$2");
            return x;
        }
        var wordCount = numberWithCommas(words);
        $('.gh-wordcount').html(wordCount);
    });
</script>
{{/if}}

```

Once you’ve added some events to your theme, you can test that your tracking is working from the setup page in your Amplitude account:

![](/images/integrations/event-setup-worked-1_hu3aea5df2fa0d312d904ed57f0b42221f_53149_1173x0_resize_q100_h2_box_3.webp)

These events are just two examples. For more information about how to implement events, visit the [Amplitude developer documentation](https://developers.amplitude.com/docs/).

Summary
-------

**That’s it!** Your site is now fully integrated with Amplitude and you can review your site metrics and start data crunching on the projects dashboard! Create new projects if you need to split up your data into different sections or invite your team to specific reports.

For more detailed information about using Amplitude, check out their [Learning Center](https://help.amplitude.com/).

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

