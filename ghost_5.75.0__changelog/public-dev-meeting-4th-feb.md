


Public Dev Meeting 4th Feb







































Today's meeting focused specifically on the 'Apps' section of [milestone 0.5](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org#wiki-apps), as further described by the [epic issue #1474](https://github.com/TryGhost/Ghost/issues/1474?ref=ghost.org). The purpose of the epic is to track progress and provide visibility by grouping the work into related issues with clear & measurable goals.

The majority of the meeting focused around discussing issues to do with 'App Safety and Security'. The Ghost app platform is intended to be stable, reliable and safe to use with a clear one way of doing things. Apps should not be able to gain direct access to either the file system or the database, they should instead make use of the APIs provided by Ghost. This is intended to provide both security as well as making it less likely that Apps break as Ghost evolves as the provided APIs will be maintained abstractions which can be depended upon by App developers.

We accept that it isn't possible to prevent malicious use of the platform in all cases. However, the apps will be [sandboxed](https://github.com/TryGhost/Ghost/pull/2091?ref=ghost.org) to prevent access to blacklisted modules in order to deter app developers from using those tools instead of the provided APIs. We aren't 100% sure if this is a good balance between security and creativity, so want to try to land this as early as possible so that app developers can try it out and feed back to us.

The creation of the app platform requires us to roll out [ACL](https://github.com/TryGhost/Ghost/issues/2060?ref=ghost.org) across the API and other aspects of Ghost. There are still various aspects of how this will work, specifically with regard to determining which app or user is requesting permission at any given time, which are not clear. We discussed creating clear examples so that the work becomes less theoretical.

Work on the [Data API](https://github.com/TryGhost/Ghost/issues/2124?ref=ghost.org) is already on-going. We believe that this will have a big impact on the reliability of Ghost, and give us further room to improve the codebase. [Documenting](https://github.com/TryGhost/Ghost/issues/2125?ref=ghost.org) the API is going to be an interesting challenge - we are aware of the limitations of the current format of our documentation, and are in the process of improving this.

### Full details:

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20140204?ref=ghost.org#pm53924) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next weeks meeting: Tuesday 11th February, 5:30pm London time.


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





 





 
















 






