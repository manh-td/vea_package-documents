




Email deliverability explained for publishers








































Email is the most popular delivery mechanism for content creators of all kinds, so it’s no surprise that email deliverability is a crucial aspect of business for independent publishers. But as you might know, it can be a complex and technical topic with obscure acronyms like DKIM and DMARC.

This no-nonsense article will break down some of these technical concepts in an understandable way. At the end, we’ll share some tips for what you can do to improve email engagement as a publisher.

How emails are delivered
------------------------

When you send an email newsletter to your audience, each email goes on a journey until it (hopefully) ends up in the recipient’s inbox.

Many factors go into deciding whether the email makes it, and if it does, where it will land (inbox, promotions, spam). Some of these factors include:

* The reputation of the sending domain and if it is on any blocklists
* The reputation of the from address
* Whether email authentication records like SPF, DKIM, and DMARC are passed
* Whether the recipient has opened or replied to an email from this sender before
* The content of the email itself
* The number of times your emails have been reported as spam
* The mailbox provider (some are notoriously bad at spam handling, like Outlook and Hotmail).

When sending emails in bulk, they will always be processed, and these factors will be taken into consideration along the way. But if you do things right, you should see the majority of your emails being delivered, a low percentage being sent to spam or junk, and the rest being distributed into the recipient’s inboxes or folders.

SPF, DKIM, and DMARC
--------------------

These three acronyms refer to email authentication protocols designed to keep email recipients safe.

### SPF

An **SPF** (Sender Policy Framework) record is an email authentication standard that allows domains to state which servers may send emails on their behalf. Having an SPF policy helps provide trust signals and protects senders from spam, spoofing, and phishing.

### DKIM

**DKIM** (DomainKeys Identified Mail) is an email security standard to ensure your emails aren’t altered in transit. When an email passes DKIM, it is considered authentic.

Having a DKIM record helps make your email appear more legitimate and reduces the chances of emails landing in spam folders.

### DMARC

**DMARC** is a type of security protocol designed to protect against email spoofing. It's used as an additional layer, combined with SPF and DKIM to improve delivery and prevent abuse.

DMARC is considered an advanced type of security protocol. It requires using a custom sending domain and must be configured correctly to avoid a negative impact on delivery.

Custom sending domains
----------------------

When you implement your own email authentication records, you’re using what is called a custom sending domain.

**What is a custom sending domain?**  
A custom sending domain is where you set up your own authentication records (SPF, DKIM, and DMARC) with your web host and use your own domain to deliver bulk mail. It’s an advanced type of mail delivery setup that tells mailbox providers you are a real business, and that you’ve given permission for your email service provider to send emails using your domain.

**Will a custom-sending domain guarantee deliverability improvements?**  
Not always.

Success with a custom sending domain depends on how well-established your domain is for sending bulk mail, and on your custom DNS records being set up correctly.

Deliverability tips
-------------------

Beyond setting up SPF, DKIM, and DMARC, we have some additional tips for making sure your newsletters reach your readers:

1. Run your email newsletter content through a free [spam checker](https://www.mail-tester.com/?ref=ghost.org) to identify language that can trigger spam filters or cause more emails to land in promotions.
2. Encourage your members to add your address as a safe sender, or even better, encourage them to reply to your emails. This sends positive signals that you’re a trusted sender.
3. Keep your free subscriber list tidy by periodically removing inactive subscribers using filters in the member dashboard.

![](https://ghost.org/resources/content/images/2022/01/filtering-members.png)

Use filters in the member dashboard to find and unsubscribe inactive members.

---

Hopefully, you now have a clear understanding of email deliverability, and how it works behind the scenes.

Technical details aside, the single most impactful thing you can do to achieve and maintain high email engagement is to [focus on your content](https://ghost.org/resources/how-to-increase-email-newsletter-open-rate/).

**On this page**
[Introduction](#intro)




---





[###### — Read this next —

How to switch from Patreon to Ghost](/resources/patreon-vs-your-own-site/)


Get trends & tips delivered to you.
-----------------------------------

A weekly roundup of emerging trends, products and ideas in the creator economy, trusted by **50,000+** readers.



No spam. No jibberjabber. Unsubscribe any time.
[Wow, @Ghost is killing it today with their newsletter. It may just be me, but it seems like more time and care is being spent every week on it. If you can show me a link about my obsession I didn’t know about yet — that’s something.

2:22 PM · 13 Jun 2021](https://twitter.com/cjchilvers/status/1404081746065428483)
[@Ghost has been my favorite company newsletter of 2022

6:21 PM · 4 Apr 2022](https://twitter.com/arsalagrey/status/1511114162729984001?s=20&t=EkPCkPBi5XTtcXo7nDft6w)
[Ok, the Ghost newsletter is hands down the best newsletter in my inbox and it is not even close. There's not a single other one that I am going back to read or look forward to getting. Excellent job!

6:09 PM · 17 Apr 2022](https://twitter.com/LajosNagyUK/status/1515633491492454401)


[![Create your brand: Launching a publication](https://ghost.org/resources/assets/img/building.jpg?v=04c180ed9e)](https://ghost.org/resources/building/)
[![Start publishing: Creating content that works](https://ghost.org/resources/assets/img/publishing.jpg?v=04c180ed9e)](https://ghost.org/resources/publishing/)
[![Grow an audience: Finding your true fans](https://ghost.org/resources/assets/img/growth.jpg?v=04c180ed9e)](https://ghost.org/resources/growth/)
[![Build a business: Earning revenue from your work](https://ghost.org/resources/assets/img/business.jpg?v=04c180ed9e)](https://ghost.org/resources/business/)
















