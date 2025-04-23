


No more jQuery in {{ghost\_foot}}






































*The time has come to remove jQuery from the `{{ghost_foot}}` helper.*

Ghost's `{{ghost_foot}}` helper has provided a local copy of jQuery since the very first release of Ghost. At the time, it seemed like having easy access to jQuery would be beneficial for the majority of theme developers - making it something worth adding to core. However it has since become clear that this wasn't a great decision - it not being possible to customise this means many theme developers have been excluding the required `{{ghost_foot}}` helper.

In ~~a near-future~~ *the next (0.7)* version of Ghost, jQuery will be removed.

To mitigate the fact that many, many themes depend on jQuery and simply removing it would break countless blogs, we're going to remove it in such a way that **only new blogs are affected**. Existing blogs will have the `<script>` tag moved to the `ghost_foot` section of the [Code Injection](https://ghost.org/help/using-the-editor/?ref=ghost.org#using-code-injection) screen in Ghost.

If you're interested in following along with the technical whys and hows this will be done, you can follow along with the issue [issue on GitHub](https://github.com/TryGhost/Ghost/issues/5298?ref=ghost.org). We'll make a further announcement here on the blog to let you know which version of Ghost will contain the switch.

How to Update Your Theme to be Forwards-Compatible
--------------------------------------------------

If you make and distribute themes for Ghost that depend on jQuery to function, you'll need to update them so that they become forwards compatible.

There is no harm in including jQuery twice (beyond the waste of resources), but it is possible to conditionally load jQuery if it doesn't exist already with a snippet like this:

```
<script type="text/javascript">
  if (typeof jQuery == 'undefined') {
    document.write('<script type="text/javascript" src="https://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.1.min.js"></'+'script>');
  }
</script>

```

We highly recommend updating your themes to include jQuery themselves as soon as you can. Additionally, if you're a developer who has been dropping `{{ghost_foot}}` because of jQuery, please add it back! We'll soon be displaying warnings and errors for themes which fail to include the [required helpers](https://ghost.org/docs/themes/helpers/?ref=ghost.org).

**If you need any help or would like to chat about updating your themes, please drop by the #themes channel on our [Slack community](https://forum.ghost.org/?ref=ghost.org).**

**Update 24th Aug:** jQuery will be removed from the next version of Ghost, which will be 0.7, and will be released VERY soon.


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





 





 
















 






