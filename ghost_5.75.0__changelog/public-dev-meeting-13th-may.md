


Public Dev Meeting 13th May







































This week's meeting kicked off a little differently - with a rough outline of the agenda for the meeting.

* Meeting starts with a progress update covering what has happened over the last week, and catching up with any issues that are outstanding.
* Next there is an opportunity for anyone to bring up anything they want to discuss - anything at all to do with Ghost development be it questions, comments, concerns etc.
* Lastly I wanted to run through the ember admin and discuss where we are with it.

The day after the last meeting, all outstanding Ember PRs were merged, and the ember branch was merged into master. Both the original and ember admin now live side by side in master, the original admin at `/ghost/` and the new ember admin at `/ghost/ember/`.

The past week has seen a lot of activity on GitHub, it's been one of the most active weeks we've seen in a while, with a lot of people picking up bugs and small issues that popped up as we have merged so many API refactors and other bits and pieces. Hopefully, this activity will continue on into next week and become much more focused on Ember.

One issue that is still poking around from the [API project](https://github.com/TryGhost/Ghost/issues?direction=desc&labels=&milestone=19&page=1&sort=updated&state=open&ref=ghost.org) is [#2601](https://github.com/TryGhost/Ghost/issues/2601?ref=ghost.org) which is all about non-RESTful endpoints and how they should work. [@steveklabnik](https://github.com/steveklabnik?ref=ghost.org), one of the co-authors of the [JSON-API](https://jsonapi.org/?ref=ghost.org) format joined us for the meeting to help us decide what to do. The JSON-API standard is almost ready to be released as 1.0, and there have been some interesting changes and improvements as people have started hacking on it, one of which is the option to move the request/response formats to use `data` as a consistent key rather than a plural resource name like `posts`.

We still have an [open discussion](https://github.com/TryGhost/Ghost/issues/2699?ref=ghost.org) on whether we should use Ember Model, Ember Data or something else. [@jgable](https://github.com/jgable?ref=ghost.org) has done a spike on [Ember-Data](https://github.com/TryGhost/Ghost/pull/2718?ref=ghost.org), and we'd love to see one turn up for Ember Model so that we can compare the two. Ideally, we want to make this decision this week so that we can crack on and turn the Ember admin into **the** admin!

During the meeting I walked through some aspects of the API and what is and isn't implemented, as well as some visual and behavioural issues with the new Ember admin. Since the meeting I've gone through and opened many new issues, several of which are marked with the `beginner` tag, as well as added comments or updates to many of the existing issues in the [Ember project](https://github.com/TryGhost/Ghost/issues?direction=desc&labels=epic&milestone=17&page=1&sort=updated&state=open&ref=ghost.org). Most of the issues are linked from the main [Ember Epic](https://github.com/TryGhost/Ghost/issues/2271?ref=ghost.org), and there are quite a few more to open. Please feel free to grab any unassigned issues by dropping a comment on the issue, or letting me know in IRC.

### Full details:

The full logs of the meeting [are available](https://107.20.237.151:8081/logs/%23ghost/20140513?ref=ghost.org#pm44023) from Slimer, our IRC bot (who is also on [GitHub](https://github.com/TryGhost/Slimer?ref=ghost.org) by the way!).

### What is this?

We hold a public development meeting pretty much every Tuesday at 5:30pm London time in the #ghost channel on freenode. In this meeting we discuss progress, important issues, and what is and isn't on [the Roadmap](https://github.com/TryGhost/Ghost/wiki/Roadmap?ref=ghost.org). It's a chance for everyone to get involved and have their say about where Ghost goes next.

Hope to see you at next week's meeting: [Tuesday 20th May, 5:30pm London time](https://everytimezone.com/?ref=ghost.org#2014-5-20,270,6bj).


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





 





 
















 






