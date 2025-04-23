


Markdown guide










































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


The Ghost editor automatically parses any [Markdown](https://commonmark.org/) typed in directly, which means you can write your content in Markdown if you prefer. If you want to keep your content formatted in Markdown for editing later, or you'd like to include footnotes in your post, then you can also use the Markdown card.

![](https://ghost.org/help/content/images/2024/06/markdown-guide-menu.png)

Markdown reference
------------------

| Result | Markdown | Shortcut |
| --- | --- | --- |
| **Bold** | \*\*text\*\* / \_\_text\_\_ | Ctrl/⌘ + B |
| *Emphasize* | \*text\* | Ctrl/⌘ + I |
| ~~Strike-through~~ | ~~text~~ | Ctrl + Alt + U |
| Testtext | ^supertext^ |  |
| Textsubtext | ~subtext~ |  |
| [Link](https://ghost.org/help/using-markdown/) | [title](https://) | Ctrl/⌘ + K |
| `Inline Code` | `code` | Ctrl/⌘ + Shift + K |
| Image | ![alt](https://) | Ctrl/⌘ + Shift + I |
| List | \* item | Ctrl + L |
| Ordered List | 1. item | Ctrl/⌘ + Alt + L |
| Blockquote | > quote | Ctrl + Q |
| Highlight | ==Highlight== |  |
| H1 | # Heading |  |
| H2 | ## Heading | Ctrl/⌘ + H |
| H3 | ### Heading | Ctrl/⌘ + H (x2) |

Adding footnotes using the Markdown card
----------------------------------------

Footnotes allow you to add notes and references to your content without cluttering the body of your post. To add footnotes using the Ghost editor, insert a Markdown card into your post and use the following Markdown:

1. Add a caret and an identifier inside brackets for example: `[^1]`
2. Then add the footnote anywhere in the same card using the following Markdown: `[^1]: My footnote`

**For example:**

```
Here's a short footnote,[^1] and here's a longer one.[^longnote]

[^1]: This is a short footnote.

[^longnote]: This is a longer footnote with paragraphs, and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }` add some code, if you like.

    Add as many paragraphs as you need.

```

**Here's how that would look:**

Here's a short footnote,[[1]](#fn1) and here's a longer one.[[2]](#fn2)

---


1. This is a short footnote. [↩︎](#fnref1)
2. This is a longer footnote with paragraphs:
   
   Indent paragraphs to include them in the footnote.
   
   `{ my code }` add some code, if you like.
   
   Include as many paragraphs as you need. [↩︎](#fnref2)

💡Footnotes will always appear beneath the markdown card, when rendered on the published post or page they've been added to. 


[Next up
 →](/help/using-markdown/)
### Related articles

 
💡Currently in public beta on Ghost(Pro)
This feature is



 

 
Configure custom spam filter settings, to prevent specific email domains from signing up to your publication.



 

Was this article helpful?
-------------------------








 





