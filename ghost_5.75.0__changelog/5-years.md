


After 5 years and $3M, here's everything we've learned from building Ghost











































Last week marked the fifth anniversary since the Ghost Kickstarter campaign which started it all.

It's always fun to use these milestones to take a step back and reflect on the journey so far. On previous birthdays I've talked about revenue milestones and product updates, but this year I'm going to focus more on all the things we've learned since we started.

Just for context though, here's a quick overview of where we are today:

---

* **MRR:** $82,000
* **Annual Net Revenue:** $1.2million
* **All-time Revenue:** $3million
* **Github Stars:** 25,000
* **Releases:** 173
* **Sites using Ghost:** 512,000
* **Biggest users:** Apple, Tinder, DuckDuckGo, Mozilla, OpenAI, OkCupid, Square, Vevo, DigitalOcean, Napster, CloudFlare and [many, many more](https://ghost.org/customers/?ref=ghost.org).
* **Runway:** Just kidding, we've been profitable since year 1

---

We started working on Ghost because we wanted to build a great open source publishing platform which would empower independent creators, but we also started this company as a social experiment. We wanted to know: What would it look like if you built a technology startup which could *not* make anyone rich. If you eliminated all the promises of wealth from the roadmap up front, and tried to build a *good* company, how would that affect the product, business, customers, and every little decision in between?

We wanted to find out. So we set out to build the company we wish we could do business with, as well as the organisation we wished we could work for. Ghost was set up from day 1 as a non-profit foundation, and released all of its code under the open source MIT license.

To this day, 90% of people who hear this still have the same reaction: "What??" followed closely by "Why??" — so it might be worth recapping briefly:

---

Being a non-profit means that the company has no shares. I don't own it. Hannah doesn't own it. Nobody owns it - it's an independent entity. The company makes money and pays expenses, salaries and taxes as normal - but there's no way for it to be bought or sold either in part (investment) or as a whole (acquisition). Any profit the company makes can only ever be reinvested, not distributed. We can't cash out. Ever. Also the entire product is open source and has no copyright. Anyone can do whatever they want with our code, for free.

So, when we do anything you can be absolutely certain it's in the sole interest of building the best product we can for the right reasons. We want to build great open software to support sustainable journalism, publishing and a more open web. There is no other reason we have for doing anything.

Anyone can say they want to "change the world" and that "it's not about the money" — but talk is cheap — so we made our mission legally binding. At a time when the world sometimes seems totally devoid of integrity, we really just wanted to create something with unquestionable integrity.

Also — Being paid to work on Ghost is, to me, the equivalent of being paid to play videogames. Or go scuba diving. Or play with kittens or something.

It turns out that a funny thing happens when you build a company you can never sell: You end up building a company you would never *want* to sell.

---

While the first few years were pretty frantic to get everything off the ground and make the business sustainable - about a year ago we actually stopped tracking revenue as a primary goal. It's now a health metric, like uptime or performance. We keep an eye on it, of course, but for the most part it doesn't drive decision making. Decision making is centred around where we think we can have an impact, what people are asking for, and what we enjoy doing.

What we've created is a business and a product in a structure which we can see ourselves working on indefinitely. There are no investors putting pressure on us to generate a return, pump up numbers for an IPO, or work on features which would make us more attractive for an acquisition.

We're just a small team working on something we care deeply about. Thanks to all this unapologetic focus, we don't need to try to be the biggest. Instead, we can focus on being the best.

![](https://ghost.org/changelog/content/images/2021/01/stats-1.jpg)

So what lessons have we learned in the last 5 years?
----------------------------------------------------

Profit or non, building a business is hard. Doing open source is hard. Making a product which people actually care about is hard. And let me tell you, hosting websites is exceptionally hard.

There are far too many lessons to share in a single post, but I'd like to share a handful of the most significant things we've learned from 5 years of building a popular open source product, profitable SaaS business, major hosting platform, productive remote team, and large community.

Centralised wins on simplicity, Open source wins on flexibility
---------------------------------------------------------------

This is the really big one.

When we started out, we tried to make everything as simple and user-focused as possible. Our intent was to make the app as easy to use as any closed source platform, but with the added bonus of actually being open source with a socially positive business model.

Most open source software has terrible UI design, so we would have great UI design and it would be the best of both worlds!

This falls apart almost immediately. For example: if you build a centralised service - you can solve authentication, search and image optimisation pretty easily with OAuth, Algolia and imgix. It costs you minimal engineering time and a few dollars to set up so your users have a wonderful experience with absolutely no overhead.

Try to build the same thing as a decentralised product and every one of your users has to set up their own Twitter developer apps, Algolia API keys and imgix accounts + configurations. Each service has to be set up, connected and paid for. A significantly high level of technical expertise is required to even get it all slightly working. The average non-technical user doesn't have a single hope in hell of getting it working let alone having a good experience.

We spent several years trying to engineer our way out of this in increasingly complex ways, so that people could set up a publication on Ghost with the same level of ease as they do on Medium. In part, because that's what people were demanding. We never even got close. It's just not how modern web technology works.

Decentralised platforms fundamentally cannot compete on ease of setup. Nothing beats the UX of signing up for a centralised application.

##### But

Centralised platforms fundamentally cannot compete on power and flexibility. In the long run, nothing beats owning your technology and controlling your destiny.

Yes, setting up a Squarespace site or a Medium blog is easy. You can get the basics up and running in a matter of minutes. However, you are also explicitly limited to what those platforms allow you to do. The second you want to step outside the confines of their design, or functionality, or do anything outside the little box which they let you play in: You're stuck.

Also, they can and *will* [pull the fucking plug on you at a moment's notice](https://www.niemanlab.org/2018/05/medium-abruptly-cancels-the-membership-programs-of-its-21-remaining-publisher-partners/?ref=ghost.org).

We spent a very long time trying to compete on convenience and simplicity. This was our biggest mistake and the hardest lesson to learn - because user feedback told us that this was what was most important. We deliberately limited flexibility in the product to try and make it more simple. But it ended up being still not simple enough for the average user, and not powerful or flexible enough for the professional user — the worst of both worlds.

So the biggest takeaway after 5 years is that we have been moving, and will continue to move up market, toward professional users who value power and flexibility over ease of signup. This is where we can win compared to the competition. This is where Ghost comes into its own.

We're really, really excited about the future of Ghost as a product.

Our biggest marketing wins and losses
-------------------------------------

The best marketing we've done has been to launch, over and over again. At least twice a year we try to make something big and launch it publicly. Sounds really obvious but most people don't do it. Beyond that we focused purely on having a good website (insane that this is a differentiator in 2018, but welcome to open source), a reliable product, great support, and a lot of care.

Our biggest marketing failure has been our documentation and resources. They exist. They're just not very good. We're actually [hiring right now](https://careers.ghost.org/?ref=ghost.org) for someone to help us fix this and make using Ghost a really fantastic developer experience.

Another thing that has worked really well for us is to invite a small group of people to have early access to things months ahead of launching them. For instance: We're currently looking at testing an affiliate program whereby we'll pay out a 30% commission every single month on the lifetime revenue of anyone referred to Ghost(Pro). We're currently looking for just 3 people to beta test who have a large/relevant audience. [Interested?](https://ghostjournalism.typeform.com/to/KJ92XR?ref=ghost.org)

Building a distributed team is both easier and harder than you might imagine
----------------------------------------------------------------------------

Our team is spread all over the world, and we have no office in any country. After 5 years I would summarise the overall experience as very positive. The stuff you might imagine is hard generally turns out to be a non-issue, like: How do you know if people are working? How does anything get done? How do you pay people if they live in different countries? What about contracts? — The things people ask about most often all have straightforward answers. In summary: You hire people you can trust, you trust them, and the logistics in between are solved mostly with Slack, Zoom and Github.

The stuff which is actually hard, nobody ever asks about. For instance: How do you know when someone is in a bad mood? How do you deal with loneliness? How do you foster camaraderie? How do you achieve urgency? How do you ever get to know people outside of work when you never spend time with them outside of work?

Real challenges of being remote are more human, than business.

![](https://ghost.org/changelog/content/images/2021/01/gh--1-.jpg)

Open source development is largely more broken than ever
--------------------------------------------------------

The least fun part of working on Ghost is dealing with Github, which is really sad.

Everyone has their pet issue, whether design or accessibility or security or internationalisation or performance or SEO or or or... the list goes on. Everyone thinks theirs is most important and that we should work on right *now* and they can't *believe* that we would ignore it. It's always absolutely *outrageous*.

How open source works is: If you want something, **you** can build it.

That's the freedom which open source gives you. We build a base product which you can adapt, extend or integrate however you want. You can't do that with closed source platforms. Open source code = the freedom for *you* to do things with it. But that's not how many people understand it.

Developers regularly show up on Github, rage at us for something like not supporting Postgres - and then we say "ok so are you going to write and maintain Postgres support for Ghost?" and they say "of course not, I don't have time for that!" - and then occasionally they'll go on Twitter and tell all their followers to give us hell. As if organising a mob and shouting louder is the best way to get a bunch of people writing free code to do what you want.

Unfortunately I think Github itself has a lot to do with this. The product has become too transactional - more support tool than collaboration. And Github themselves show remarkable disinterest in the open source community as a whole - they give us beta access to test new features every so often. That's about it. There's no wider involvement at all.

Our core team tends to do the "real work" in private issues nowadays. The signal to noise ratio is just too overwhelming.

We're always adapting to the market
-----------------------------------

When we started out, the focus of Ghost as a product was squarely on the publishing experience. Improving the ease of publishing online seemed, in 2012 and the several years before, like something that could be much better. All of this was at a time when Svbtle was the popular new thing, and Medium didn't exist!

Ghost has changed a lot in 5 years, but of course the market has also changed a lot beneath us. Adapting our business and our strategy to the direction of the industry as a whole is something we've gotten fairly good at. Many things which were a good idea in 2013 are no longer a good idea in 2018.

The most exciting area we're looking at for the coming 5 years is in building and supporting new business models for publishing. Particularly around memberships, subscriptions and community. It feels like there are a lot of meaningful opportunities there which have yet to be discovered.

Ghost is a very different company now to when it first launched, and it's hard to imagine what things might look like on our 10th anniversary.

But we're as excited as ever about the journey :)

There are seemingly no good nonprofit funding options for journalism/tech
-------------------------------------------------------------------------

One big surprise in the last 5 years has been discovering that there are really no good funding options for journalism/tech. We've bootstrapped from day 1 and always planned to be totally self-sufficient. But initially we did think that there might be grant funding or support that we might be able to benefit from. It turns out: No. Absolutely none.

I thought between the Knight Foundation and the Mozilla Foundation and the Ford Foundation and the Google News Initiatives — there might be a path to getting a lil' help. However, they all seem to be limited to helping only projects in their own countries (mostly the US) and selecting who is awarded grants appears to be often more about who you know, than what you do.

I'm still curious about this. Are we missing something? Are there organisations who do grant-funding who we should be talking to? Or is there a viable form of ICO which would support our company structure, to engage our own community directly, without being sketchy? Like a follow-up to the Kickstarter, maybe something like [Brewdog](https://www.brewdog.com/uk/?ref=ghost.org).

Would love any advice. Given that we're profitable, we don't especially need funding, but we have very large ambitions and very limited resources. We'd love to do more. Send me a note [on Twitter](https://twitter.com/johnonolan?ref=ghost.org) if you have ideas.

Your Questions Answered
-----------------------

Last week I mentioned on Twitter that I was writing this post and asked people what they wanted to know. There were tons of responses, so Hannah and I recorded our biggest *ever* podcast going through all the best ones!

**Know someone who would be interested? Share this:**

> After 5 years, $3Million, and no investors: Here's everything we've learned from building the #1 CMS on Github 🔥 <https://ghost.org/changelog/5/>

or enjoy these 1-click links for *Ultimate Efficiency* TM: [Tweet this](https://twitter.com/share?text=After+5+years%2C+%243Million%2C+and+no+investors%3A+Heres+everything+weve+learned+from+building+the+%EF%BC%831+CMS+on+Github+%F0%9F%94%A5&url=https%3A%2F%2Fghost.org%2Fchangelog%2F5%2F&ref=ghost.org) or [Buffer it](https://bufferapp.com/add/?url=https%3A%2F%2Fghost.org%2Fchangelog%2F5%2F&text=After+5+years%2C+%243Million%2C+and+no+investors%3A+Heres+everything+weve+learned+from+building+the+%EF%BC%831+CMS+on+Github+%F0%9F%94%A5&ref=ghost.org)

Thank You
---------

To everyone who has ever been a customer, subscribed to a newsletter, backed us on Kickstarter, reported a bug, made a suggestion, opened a pull request or sent us a friendly email. We wouldn't be here without you. I should also mention our [partners](https://ghost.org/partners/?ref=ghost.org) who have been so generous with their time and resources to support Ghost. I'm not sure we ever could've made it without [Digital Ocean](https://digitalocean.com/?ref=ghost.org) and [Cloudflare](https://cloudflare.com/?ref=ghost.org) in particular. We are indebted to their belief in us.

Most of all, I want to thank our team and core contributors over the years. It might be my face which you see most often on Twitter and Hannah's name most frequently on Github - but in truth all of the best bits of Ghost - the bits worth talking about, weren't made by us. They were made by the wonderful team and contributors who we have been so fortunate to work with.

If you're interested in being a part of the journey, we're hiring for [full stack JavaScript developers](https://careers.ghost.org/?ref=ghost.org) right now :)

![](https://ghost.org/changelog/content/images/2021/01/IMG_0279.jpg)

**Particular Thanks To:**


Sarah Frantz, Kevin Ansfield, Katharina Irrgang, Jason Williams, Sebastian Gierlinger, Paul Adam Davis, Austin Burdine, Matt Enlow, Fabian Becker, Aileen Nowak, David Wolfe, Matthew Harrison-Jones, Jacob Gable, Felix Rieseberg, Gabor Javorszky, Georgina Lusby, Harry Wolff, Ryan McCarvill, Robert Jackson, David Arvelo, William Dibbern, Maurice Williams, Tim Griesser, David Balderston, Ricardo Tomasi, Nazar Gargol, Jakob Gillich, Peter Szel, Christopher Giffard, Kevin P, Steve, Manuel Mitasch, jamesbloomer, John O'Mahoney, Lucas Holmquist, Ian Mitchell, Adam Howard, nicoburns, Tobias Bieniek, Michael Bradshaw, James Inman, vdemedes, Zach Schneider, JT Turner, CriticalRespawn, ericterpstra, Zach Geis, Vikas, Matthew Beale, Lukas Strassel, Joe Wegner, Jilles Soeters, Connor Tumbleson, Seth Lilly, Sebastian Gräßl, Sebastian, Rosco Kalis, Rem Zolotykh, Nicola Mustone, Mattias Cibien, Marco Otte-Witte, Kyle Nunery, Delgermurun, David Blurton, Alex Kleissner, Łukasz Kliś, surgesoft, shindakun, buddhamagnet, Vivek Kannan, Vijay Kandy, Taras Mankovski, Shashank Mehta, Patrick Garman, Michael Schmidt-Voigt, Lev Gimelfarb, Kate von, Jonathan Johnson, James Seymour-Lock, Jake Wright, Harry Hope, Gary Cao, Eugene Kulabuhov, Daniel Hanson, Dane Springmeyer, Brad Dougherty, Alan Richards, mattse, king6cong, juan-g, Xie JinBin, Tony Gaskell, StevenMcD, Sean Hellwig, Sam Saccone, Patrick Kim, Pascal Borreli, Matt DuVall, Leonard Camacho, Kowsheek Mahmood, Katie Fenn, Johan Stenehall, Jason Sturges, Hey24sheep, Benjamin Chodoroff, Andrew Chilton, 汪磊, zinyando, sjama, remixz, redwallhp, quangtt, nicksahler, lennerd, jomahoney, joeldrapper, germanrcuriel, fabfou, b1nd, andy matthews, abe33, Will Glynn, Vikhyat Korrapati, Vikas Potluri, Victor Szeto, Thomas Faurbye, Talon, Szél Péter, Syaiful Bahri, Stefan Baumgartner, Seb Gotvitch, Sarah, Robert Rhoades, Richard King, Renyu Liu, Peter Dave, Mikkel Hoegh, Michael Nason, Matt Hughes, Martín González, Martin H., Martijn Swaagman, Mark Berger, Marcos Ojeda, Manuel Gellfart, Lucas Churchill, Lucas, Kirill Yakovenko, Kenneth Ashley, Karolis Dzeja, Karl Mikkelsen, Justin Yek, Josh Vanderwillik, Josh Kalderimis, Joerg Henning, Jeremiah Hoyet, Jeff Jewiss, Jarrod Mosen, Jamie Knight, Jaiden Mispy, Ilya Radchenko, Ihab Khattab, Harry V., Garrett Murphey, Erik Hanchett, Erik Bryn, Enrique Chavez, Devin Doolin, Declan Cook, David Robson, Cameron Viner, Brian Tedder, Brandon Hops, BlueHatbRit, Ben Gladwell, Ashish Dixit, Artyom Fedenko, Andy, Andrej Mlinarević, AileenCGN, Aia Patag, Adam Hess, Abijeet Patro, 1Pete, “kirrg001”, zhenkyle, zethraeus, vitalie maldur, tamura shingo, starcwl, sessa, sanddudu, sahand12, rmfx, rfpe, rektide, rambii, polygonix, oregami, omeid, nicovalencia, nason, moritz haarmann, meowtec, lmoe, jtw, janvt, ivan sebastian, hwdsl2, hoxoa, hiroshi kobayashi, enahs, danschumann, cristears, baogechen, balduv, ali, aimingoo, Zlatan Vasović, Yury Michurin, Yann Verry, Yanke Guo, William Golden, Wilhansen Li, WangSai, Waleed Ali, Vineet Sinha, Victor Truong, U-nico-laptopnico, U-nico-laptop\nico, Tushar Bhushan, Tom Gillett, Tim Walling, Tim Mansfield, Thai Phan, Terin Stock, Szu Yaung, Steven Cochrane, Steven B, Stephan Bönnemann, Simone D'Amico, Silvio Fernández, Sem, Sean Hussey, Sarah Frantz, Samuel Goodwin, Sam Wilskey, Ryan Seys, Ryan Powell, Roy van, Rodney Folz, Rob Graeber, Reinoud Kruithof, Rei, Rafael Corrêa, Rabbi Hossain, Polygonix, Peter deHaan, Peter Zimon, Peter Garland, Pedro Teixeira, Paul Connolley, Paul, Oliver Schneider, Nick Schonning, Nick Pfisterer, Nick Donohue, NetPuter, Naoya Kanai, Myles Braithwaite, Mo Valipour, Misha Wakerman, Mikael Brockman, Micheil Smith, Michael Auer, Matthew DuVall, Matt Florence, Matheus Azzi, Markus Siemens, Mark Stosberg, Mark Stacey, Marc Bachmann, Mante Bridts, Luke Shiels, Luke Arduini, Kumar Abhinav, Kenny Meyer, Julien Gilli, Joris Berthelot, Jorge Niedbalski, Jordan Sexton, Jono Warren, JonathanKryza, John-David Dalton, John Nguyen, John Cruikshank, Joel Rosenberg, Joel Fischer, Joe Cannatti, Jimmy Hsu, Jimmy Cai, Jesse Tane, Jesse Dijkstra, Jeff Escalante, Jay Beavers, Jason Friedrich, Jarrett Cruger, Jacques Marneweck, Jacob Kaplan-Moss, Ivan Votti, Ian Lopshire, Hugo Marisco, Hugo Jobling, Henning Sprang, Hendrik Schaeidt, Harry Walter, Harry Mills, Guillem Andreu, Grant Winney, Glen E., Gergely Nemeth, Fixer, Filippo Conti, Farhad, Fabian Miiro, Ethan Garofolo, Eric Schultz, Eric Ellingson, Emerson Keenan, Dmitry Mazuro, Derek Myers, Declan cook, Daniel Tsui, Daniel Niccoli, Dan Schnau, Damien Dormal, Clinton Ryan, Clay Diffrient, Chuck Lam, Chris Pearce, Chris Morgan, Chris Maddox, Cezary Kluczyński, Brian White, Blaine Bublitz, Ben Vibhagool, Augustus Yuan, Antuan Khanna, André Borud, Andrew Schwartzmeyer, Alex Cusack, Adrian Estrada and Aaron Kau.



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





 





 
















 







