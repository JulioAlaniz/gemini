
Preguntas frecuentes sobre el Proyecto Géminis

Última actualización: 2023-09-02

Estas preguntas frecuentes se actualizaron sustancialmente en julio de 2023, en parte para hacerlas mucho más accesibles para una amplia variedad de lectores. Está organizado aproximadamente de menor a mayor contenido técnicamente detallado. Debería poder comenzar desde el principio y continuar leyendo hasta el punto en que sienta que su curiosidad está satisfecha o que se ha vuelto loco.

A pesar de esto, las preguntas frecuentes siguen siendo un documento largo y detallado y puede que no sea la mejor manera de tener una idea rápida y sencilla de qué es Géminis si solo está levemente interesado. Consulte la pregunta 1.14 para ver algunos enlaces a otros recursos introductorios proporcionados por la comunidad, incluida una descripción general en video.

También puede simplemente leer o vincular a las personas a las secciones individuales de preguntas frecuentes que sean más relevantes para usted o para ellos. Cada sección está disponible como un documento individual:

Intruducción y resumen general

Empezando en Geminispace

Historia, organización y curiosidades del proyecto.

Diseño de protocolo

Contribuyendo al proyecto Gemini

Tecnologías y culturas adyacentes a Géminis

Respuestas y refutaciones a críticas comunes a Géminis

Puede consultar en el enlace a continuación las traducciones de estas preguntas frecuentes a otros idiomas además del inglés, aunque la versión traducida más recientemente puede no ser tan reciente como la última versión en inglés.

Traducciones de documentación del Proyecto Gemini

1. Introducción y descripción general

	1.1 ¿Qué es Gémini?

Here are two answers to this question. One for computer geeks who really want to know right away how Gemini works under the hood and are happy to extrapolate from there, and one for everybody else, geeky or otherwise, who are less interested in how Gemini works and more interested in what it is and why somebody might want to use it. Feel free to read only one of them!

1.1.1 The dense, jargony answer for geeks in a hurry

Gemini is an application-level client-server internet protocol for the distribution of arbitrary files, with some special consideration for serving a lightweight hypertext format which facilitates linking between hosted files. Both the protocol and the format are deliberately limited in capabilities and scope, and the protocol is technically conservative, being built on mature, standardised, familiar, "off-the-shelf" technologies like URIs, MIME media types and TLS. Simplicity and finite scope are very intentional design decisions motivated by placing a high priority on user autonomy, user privacy, ease of implementation in diverse computing environments, and defensive non-extensibility. In short, it is something like a radically stripped down web stack. See section 4 of this FAQ document for questions relating to the design of Gemini.

1.1.2 The gentler answer for everybody else

Gemini is a group of technologies similar to the ones that lie behind your familiar web browser. Using Gemini, you can explore an online collection of written documents which can link to other written documents. The main difference is that Gemini approaches this task with a strong philosophy of "keep it simple" and "less is enough". This allows Gemini to simply sidestep, rather than try and probably fail to solve, many of the problems plaguing the modern web, which just seem to get worse and worse no matter how many browser add-ons or well meaning regulations get thrown at them.

Gemini might be of interest to you if you:

    Value your privacy and are opposed to the web's ubiquitous tracking of users
    Value your attention and your time and want to read with deep focus, free from distractions
    Are sick and tired of nagging newsletter subscription pop-ups, obnoxious adverts, autoplaying videos that chase you as you scroll and other misfeatures of the modern web
    Live somewhere with slow internet, can't afford fast internet, or live off-grid and need to conserve precious battery power and minimise expensive satellite data use
    Are a hobbyist programmer with a "do it yourself" attitude who enjoys building their own tools and getting real use out of them every day

If multiple points above apply to you and you've been finding the web an increasingly unpleasant place for several years, Gemini might feel like a real breath of fresh air, even an oasis - but it's not necessarily for everybody. In order to make sure that Gemini remains a simple, lightweight technology which respects its users' privacy and autonomy not just now but into the future, the feature set has been deliberately kept quite minimal. It's definitely not too minimal to be useful, but it certainly can't do everything you might be used to, and maybe it's missing something that's a deal-breaker for you. Keep an open mind, give it a try, and see how you feel. Plenty of people have been surprised at how quickly they stop missing things they thought they couldn't live without!

1.2 Does it come with cool new lingo?

Sure, but all you need to know to read and understand the rest of this FAQ are the following:

    "Geminispace" is simply the total collection of every single file that is served via the Gemini protocol. If you know what "Gopherspace" means, well, this is the obvious equivalent for Gemini. There's not really an equivalent term for the web, people just say "you can find that on the web". The term "webspace" usually refers to a hosting service, like "I pay $5 a month for some webspace from Foo Corp". You can use "Geminispace" that way too!
    A "capsule" is just a collection of pages in Geminispace that belong together, often but not always under the control of a single person. It's the same thing as a "website" on the web, or a "gopherhole" in Gopherspace.
    A "gemlog" is Gemini's equivalent term for what is called a "blog" on the web, or a "phlog" in Gopherspace.
    Some enthusiastic Gemini users refer to themselves as "Geminauts".

A lot of the terminology in Geminispace, like "capsule" and "Geminaut", is related to space exploration, see question 3.9 below for why.

1.3 What's with all the rodent talk?

"Gopher" is an internet protocol from the early 90s. In the long term, it "lost out" to the web, which was both better looking than Gopher and could do more things, and most people today have never heard of it, yet alone used it. But Gopher does the things it can do perfectly well and it never completely disappeared. In fact, in recent years, Gopher has been undergoing a small but real resurgence in popularity, as more and more people seek refuge from an increasingly user hostile web.

Project Gemini was started by Gopher users, and most of the early adopters were Gopher users, too. The protocol design itself is inspired by the design of Gopher and informed by years of experience using Gopher in the 21st century. For quite a while, Gopherspace was the only place, aside from Geminispace itself, where people could find out about Gemini. Due to this history, lots of people who want to learn about Gemini are coming from a Gopher perspective and want to know specifically how it compares to Gopher, and so some parts of this FAQ cater to that audience. If you don't know what Gopher is and you don't care, that's fine, just ignore these parts.

1.4 Oh, so this is some kind of 90s nostalgia retro hipster thing?

Well, not really. A lot of inspiration comes from a thirty year old protocol, it's true, and lots of people enjoy Gemini because they don't enjoy the direction the web has taken in the past ten years or so, but it's not really about trying to turn back the clock. After all, Gopher is still right there, alive and kicking (and NNTP and finger, too!), for anybody who wants a totally authentic, period-correct late 20th century internet experience. No new protocols are required for that! And from a Gopher enthusiast's perspective, Gemini is very clearly an attempt at modernisation, not historical re-enactment.

Rather than trying to decide whether Gemini is about turning the clock forward or backwards, it's better to think of it as trying to deliver a particular online user experience that its fans think of as not being old fashioned, out of date, or obsolete, but not modern, cutting edge, or innovative either. It's simply timeless, no less useful or valuable today than it was 30 years ago or than it will be 30 years from now. It's an experience which ought to be easily available to anybody who wants it, without sacrificing every development made since the 90s or feeling out of place on modern devices.

1.5 What kind of timeless user experience?

In a word, reading!

Reading text with a simple, clear, uncluttered layout without any animation or embedded videos or sidebars full of distracting, unrelated extras. If you use the "Reader Mode" in your web browser a lot and you love it because you think that 99% of the time it makes webpages ten times easier to use by throwing out all the useless clutter and just giving you what you want, you'll probably be excited to hear that everything in Geminispace looks that way all the time by default.

Reading that starts as soon as the page loads, without you first having to carefully click past a pop-up window which actively tries to mislead you into "consenting" to something nobody actually wants or needs, and which continues right to the end of the page without being interrupted by another pop-up begging you to subscribe to a newsletter. Gemini pages are downloaded once and rendered once, and then they stay that way for as long as you care to look at them. Nothing changes in response to you scrolling around or time passing.

Reading in peace because there's no way for a page to play music or make a sound without you actively inviting it to, so you're free to enjoy your own background music, or maybe to just keep quiet if you're reading somewhere with other people around. It's up to you, like it should be; it's your computer, and they're your ears.

Reading in private because your reading software doesn't tell the servers you get your reading material from anything about who you are or what else you've read, so nobody can follow you around and build up a record of your reading habits to sell to others without asking or even telling you.

Reading whatever sounds like it might be interesting, clicking links from one page to another page in the same relaxed, carefree way you might put one book back on a library shelf and open up another one, because it only takes a second and there's no risk. The average Gemini page is at least ten times smaller than the average webpage, and a hundred times smaller than worst ones, so they load almost instantly even on old computers or flaky internet connections. There's absolutely no question of accidentally ending up at a shady capsule which starts using your computer to mine cryptocurrency for somebody else, because what kind of insane person would design document reading software where that's a thing that could possibly happen under any circumstances? You can explore Geminispace at your leisure without fear.

If you wish that browsing the web felt more like browsing a library than wandering through a shopping mall or a casino, Gemini could be right up your alley.

1.6 So it's just words, then? No pictures, no sound?

Not quite. Like HTTP or Gopher, Gemini can serve any filetype at all, including images, audio, video and computer programs. There are tens of thousands of images in Geminispace, about five thousand PDF documents, and thousands of audio files!

But the only thing that a Gemini document can do with those files is link to them. You can't embed images or videos inside a page, sticking them in the background or between bits of text. Nothing ever plays automatically. All you can do is say to your reader, "Hey, here's a link to a picture, or a video, or some music". It's up to them whether they click the link or not - in Geminispace, the reader is always in control, not the author.

By default, your readers will just see the link text that you choose to use to describe the file. If your image is clearly relevant to the content of your page, and that content is interesting, at least some folks will follow that link! If you just put links to a big generic stock photo of an ocean sunset at the top of every page in your capsule "just so there is something there", nobody will bother.

1.7 So it's just links to static content, no interactivity?

Well, no. Gemini pages can provide visitors with a written prompt and ask them to type in some text to use as input. This is basically there to make search engines possible, because you need to have some way to enter your search terms. Even Gopher had support for search term input, before Google existed!

But there's nothing special about search engines and search terms, so it's really just a mechanism for pages to get a little bit of user input. People can, and have, used them as a way to let their readers leave comments, sign guestbooks, and that sort of thing.

Gemini even has a way for readers to voluntarily start (and end, whenever they want) a "session", so that applications can maintain server-side state. If you know what CGI apps from the early days of the web are, well, most CGI apps which work with text can be replicated to some extent with Gemini.

1.8 There are apps in Geminispace? What kind of apps?

Well, there are a lot of games! Obviously there are no graphics as such, but ASCII art and/or emojis can brighten up text-based games, which of course can be fun enough on their own. There are single player games, games where you play against the computer, games where you play against another person, and "puzzle of the day" type games where many people independently work on the same problem. Interactive fiction is also a perfect fit to the capabilities of Gemini.

There are some more social style apps, too, like link sharing apps. Microblogging works over Gemini just fine! We have our own native microblogging service, and people are building interfaces to the Fediverse, too.

1.9 Sounds like you oversold the "calm reading in a library" angle!

Well, yes and no.

You can do more than just serve and consume written material with Gemini, but that really is the technology's core strength. When all you want to do is read some text and you want it to be fast and safe and clean, without any distracting bells and whistles that spin up your laptop fan or devour your mobile data, then a good Gemini client offers a truly world-beating user experience. Plenty of Geminauts sincerely believe Gemini is a better tool for this job than the modern web is, and plenty of them use Gemini for nothing more than this, love every moment of it, and have no interest in apps at all.

When you try to use it for more than that, with every additional step you take away from the "online library of text documents" starting point in the direction of something fancier, it becomes less and less clear that Gemini is a better tool for what you are doing than the web, or something else, would be. At some point, Gemini clearly becomes the wrong tool for the job - it is not supposed to do everything and anything! Exactly where that limit lies is different for different people. Some people just want things to be simple and straightforward, other people take a kind of pleasure in pushing technology to its limits and are happy to jump through some hoops for the sheer thrill of seeing how far they can go. No matter what kind of person you are, though, the capabilities of Gemini certainly "bottom out" at something simpler, plainer, quieter, stiller and wordier than what the web has come to be. But those capabilities are still plenty to do a whole range of interesting, useful or entertaining things.

In short, Gemini isn't truly "text only", but it's very much "text centric", and happily so. Putting an emphasis on reading sets newcomers' expectations just a little lower than the truth, which is better than too high.

Besides, it's been a long time since libraries only loaned books. Modern libraries offer music and films and sometimes even video games. The similarities between a library and the online experience Gemini tries to prioritise are much deeper than just media types. Libraries make a wide range of resources available to anybody who wants them, and that's about it. What you access, when you access it and how often is up to you. You can explore the shelves solo, or you can join a book club and read alongside others. Libraries themselves generally don't make much effort to promote specific resources over others, and they certainly don't do so in cahoots with publishers. Libraries don't tell authors who is reading their works. If you stop visiting a library, the librarians don't chase you down and try to lure you back. A good library enhances your life without intruding on it, and the internet ought to be able to supercharge this relationship without inverting it.

1.10 What kind of content, and what kind of people, will I find in Geminispace?

It would be difficult and probably not even a good idea to try too hard to explicitly codify some kind of "Gemini culture". After all, computer protocols can't actually enforce any kind of behaviour in the humans who use them, or exclude some humans but not others. But they can make some things easy and other things hard, and this can incentivise some people to use them and disincentivise others, and this in turn influences what kind of content is common and which is rare. In this way tools often shape the "culture" of their users, albeit in a way that's implicit and unenforceable. Because Gemini is such a simple tool and makes a lot of things not just hard but impossible, this culture-shaping effect is quite pronounced, and for many Geminauts this is a big part of the appeal.

Gemini gives more control to the person reading a page than the person writing it. Because by default it only presents users with text, and because authors have no way to control the font or size or colour of that text, Gemini is naturally resistant to advertising and marketing. It's very difficult to "establish a brand identity" or to "grab somebody's attention" in Geminispace. You can't fall back on a fancy logo or a pretty face or elegant typography to make up for not having anything meaningful to say, and it's very hard to make text hypnotic in the same way that video easily can be. Advertising in Geminispace is by no means impossible, but the reward to effort ratio is orders of magnitude lower than on the web or social media mobile apps, and that's a powerful disincentive. Consequently, Geminispace is currently an entirely non-commercial part of the internet. Even if it doesn't stay entirely non-commercial forever, it's extremely likely that it will remain much, much, much less commercialised than other spaces.

Geminispace also lacks any kind of mechanism whereby somebody can begin publishing and quickly end up having their content appear on the screens of most of the other people using Gemini. It's a distributed library of documents, not a platform. You can still acquire a large, dedicated readership on Gemini and maybe even become some kind of "thought leader" in some circles, but this happens rarely, slowly and organically, largely via electronic word of mouth. There's no overarching algorithmic architecture which makes it a foregone conclusion that this will happen to a minimum number of people per year no matter what. As a result, people tend not to turn up in Geminispace and immediately begin spamming "clickbait" or acting weird or offensive just to stand out, because there's no real pay off. People will just ignore you.

These two aspects of Geminispace combined have a definite influence on the people and content that turns up in it. Naturally there are exceptions, but people choosing to publish in Geminispace are typically internally motivated to do so. They're not chasing fame or fortune or followers, they're writing because they want to write, they're writing about the things they care about most, and are just generally being themselves. Consequently, Geminispace has been variously described as being more authentic, genuine, human, intimate and personal than other online spaces, and has been called charming and even precious. But you shouldn't forget that it's technology, not magic. You might still run into arrogant people, rude people, narcissists and bigots, just like anywhere else on the internet. Those people exist in the world, and no network protocol can change that.

(Oh, you'll also find a lot of people who like talking about computers and the internet a lot. Surprise! You don't have to read that stuff if you don't want to.)

1.11 I bet eventually there'll be a Gemini v2.0 with cat GIFs and banner ads and infinite scrolling

No way, no how, not never, at least not on our watch.

It's not just there are no plans to officially make Gemini any more powerful than it already is. Design decisions were actually made since day one to make future extensions as difficult as possible. We know nobody can be forced to implement our specifications exactly to the letter, and we know that "embrace, extend, extinguish" happens to technologies all the time. We've done our best to preemptively fight back against this, in more ways than one.

Sometimes people are shocked, and strangely enough sometimes even angry, at how minimalistic Gemini seems, and they wonder why anybody would deny themselves some harmless seeming little features that web users are used to seeing every single day. More often than not, this preemptive fight against extension is the reason. The average Geminaut isn't some kind of fanatical ascetic, trying to resist temptation in order to purify their soul or anything weird like that. We just think that what we have right now is something pretty special, we'd hate to see it slowly eroded over the years as well-meaning changes end up pushing us down slippery slopes, and we think it's worthwhile giving up some small luxuries to reduce the odds of that happening, even a little.

1.12 So it's completely 100% finished, then?

Not quite. There are still some technical details for the geeks to work out with regard to how some things work from behind the scenes. It's not exactly minor stuff, and if you're a programmer who might be interested in implementing Gemini software you should keep an eye on things. But from the perspective of a regular end user, Gemini is finished. It's very unlikely than new features that would matter to you as somebody either reading or writing pages in Geminispace will be added during the finalisation process. If any do squeeze in, you can be sure that they'll be minor. So you should feel confident that you can dive in to reading and writing today, and the whole thing won't shift violently under your feet next year and become unfamiliar. Today's overall user experience is here to stay.

1.13 Do you really think you can replace the web with this?

Not for a minute! Nor does anybody involved with Gemini want to destroy Gopherspace. Gemini is not intended to replace either Gopher or the web, but to co-exist peacefully alongside them as one more option which people can freely choose to use if it suits them. In the same way that some Gopher users serve the same content via both Gopher and the web, people can "bihost" or "trihost" content on whichever combination of protocols they think offer the best match to their technical, philosophical and aesthetic requirements and those of their intended audience.

An even better answer to this question is "so what if we can't?". Gemini doesn't need to be able to do every single thing that the web can do to be worthwhile. Geminauts can use the web to accomplish tasks which can only be accomplished on the web, and when they're done they can close their browser down, let their computer catch its breath, then open their Gemini client and spend the rest of their online time enjoying the very different experience of reading interesting or useful or funny content in Geminispace. This is no more weird or futile than using a bike to run errands in your neighbourhood or for fun and exercise on weekends even though you still need to drive your car to work on weekdays, or growing some vegetables in your backyard or herbs on your windowsill even though you still need to buy most of your food at the supermarket. Even part time relief is still relief!

1.14 Where can I learn more?

(aside from continuing to read this FAQ, of course!)

1.14.1 Official resources

The official home of Project Gemini is the gemini.circumlunar.space server. It serves the latest version of this FAQ document, as well the protocol specification, recommended best practices and other official documentation via Gemini, Gopher and HTTPS, on IPv4 and IPv6.

There's an official Project Gemini news feed which you can keep an eye on if you are interested in following official project developments:

Official Project Gemini news feed

If you really want to do a deep dive into Gemini's history, see question 3.6 below for links to the archives of the now defunct official mailing list, where many official decisions and announcements were made.

1.14.2 Community resources

There is also a wide range of community provided content about Gemini, both on the web and in Geminispace itself. There are some links below, but the FAQ can't possibly provide an exhaustive or fully up to date list.

Gemini Quickstart! (Web version)

Gemini Quickstart! (Gemini version)

"What is Gemini?" YouTube video

"Awesome Gemini", a community maintained list of software and resources

"Gemini, le protocole du slow web", a French language introduction to Gemini

"Was ist Gemini?", a German language introduction to Gemini

Casual discussion regarding Gemini also happens in the #gemini channel on the tilde.chat IRC server:

View IRC logs via Gemini

You can also check the #gemini hashtag in the Fediverse.

2. Getting started in Geminispace

2.1 I'm curious about Geminispace, how can I check it out?

2.1.1 Using a web portal

The lowest commitment way to explore Geminispace is to use a web proxy or "portal", such as one of the following:

The mozz.us Gemini portal

Wobbly

Tildeverse Gemini Proxy (powered by Wobbly)

This will allow you to use a regular web browser, like Chrome, Edge, Firefox or Safari, to explore Geminispace. This is very quick, very easy, and if you don't like what you see you can just close the tab and forget Gemini exists and that'll be that. If you *do* like what you see, you should consider installing a dedicated Gemini client, which will offer a better and more complete browsing experience. Read on to find out how to do that.

2.1.2 Test-drive terminal clients using the SSH kiosk

If you know what SSH is and how to use it, you can try out some terminal-based Gemini clients without installing them on your own machine first by running:

    ssh kiosk@gemini.circumlunar.space 

No password is required, and once connected you'll be able to use an interactive menu to choose a client.

This Gemini kiosk was inspired by the Gopher kiosk at bitreich.org!

2.1.3 Install a client

Thanks to its ease of implementation, there is a wide range of Gemini clients available for a wide range of clients. This client diversity is one of Gemini's strengths and we're proud of it, but it can be a little overwhelming if you are used to the monopoly situation that exists on the web. Below is a small list of some of the most widely used clients you might like to try as starting points:

Amfora is a terminal client for Windows, macOS and Linux

Geminaut is a GUI client for Windows with native UI

Elaho, an iOS client available in the Apple App Store.

Kristall is a multi-protocol GUI client for Windows, macOS, Linux and *BSD

Lagrange is a beautiful GUI client for Windows, macOS and Linux

A relatively complete list of all known Gemini clients can be found in the "Clients" section of the Gemini software list below, but beware that this list is not well curated. It contains very high quality, fully featured clients under active development and bare bones hobby projects that haven't been touched in years.

Gemini software list

2.2 Okay, I've got a client, where can I find content?

There's plenty of content in Geminispace, but finding it is not as instant or straightforward as some might hope or expect. Exploring Geminispace is not like exploring a new social media app or a multiuser website like Reddit, where everything exists in one place and you are immediately presented with big lists of people and topics. It's more like the entire web, where there are many websites spread out across many different servers, and some of them have lots of users who use the site to interact with one another, and some of them belong to one person alone. There is no single, central "front page" to the entire thing. You need to use a combination of search engines, subscribing to feeds, sharing links with friends and simple random exploration to find things, and you can use bookmarks to keep track of what you've found. It can feel slow and frustrating at first if you're used to being able to pull up an endless stream of fresh content whenever you feel like it, but the careful exploration and surprise discoveries are something a lot of people come to enjoy.

Geminispace is relatively new, and definitely still growing and changing. Capsules come and go over time, and tools for finding them come and go over time, too. This FAQ provides some links below to some popular and relatively well-established locations you can use as a starting point for your explorations of Geminispace, but it's inevitable that it won't always be totally up to date, so don't take anything below as the final word.

2.2.1 Aggregators

There are a number of public aggregators which attempt to make it easier to find recently-updated material in Geminispace. Because these pull in content from a wide range of different kinds of servers, they are one of the easiest ways to find long lists of recently posted content:

Antenna, which aggregates manually submitted individual pages

bot en deriva, an aggregator of Spanish language content

CAPCOM, which aggregates a different 100 random capsules each month

Cosmos, a Gemini "super-aggregator"

gmisub aggregator

Spacewalk, which uses change-detection to find new content

2.2.2 Directories and lists

In earlier days, when Geminispace was smaller, simple lists of servers or categorised directories of capsules were a popular way to find content. As the space has grown, these have become more difficult to maintain, and some have disappeared or stopped being updated, but some are still online and maintained and can prove useful:

The Collaborative Directory of Geminispace has a hierarchical category system

The medusae.space Gemini directory has a list of capsules divided into thematic categories

The Treeblue Review curates themed feeds and lists of links aggregated from across Geminispace

The geminispace.info search engine's list of known Gemini hosts

2.2.3 Search engines

If you are looking for something in particular, Gemini has search engines you can try:

geminispace.info

Gemplex Gemini Search Engine

Kennedy search

Totally Legit Gemini Search

The geminispace.info search engine is powered by the same software behind the first ever Gemini search engine, the now sadly defunct GUS, which was launched surprisingly early in Gemini's life by Natalie Pendragon.

2.2.4 Multi-user servers

There are a number of multi-user Gemini servers with large userbases where you can find a lot of content in one place, and exploring these is a good way to find interesting content. Some of these services are listed in the answer to question 2.4 below.

2.2.5 Read some zines

There are a number of "zine" projects in Geminispace, which is well suited to the medium. At least one of them, smolZine (with, at time of writing, 39 issues published over more than two years), regularly links to "hidden (and not so hidden) gems" for its readers to check out:

smolZINE

2.2.6 Stroll through some link gardens

Once you've found a capsule you enjoy via one of the above means, be sure to check whether the author has shared a list of links. Many Geminauts maintain a so-called "link garden" in their capsule, tending a collection of pointers to other capsules that they enjoy. These are a great way for related parts of Geminispace to stitch themselves together.

2.2.7 Explore at random

If you really want to find content that you can't easily stumble upon by any other means, it's also possible to explore Geminispace at random. A number of projects, like search engines, which "crawl" the entirety of Geminispace, also publish lists of every single server they have discovered. You can just click links on these lists at random and see where you end up!

Gemini hosts known to geminispace.info

Gemini hosts known to Kennedy

Gemini hosts known to TLGS

Gemini hosts known to Lupa

This process has even been automated! DiscoGem is a capsule which publishes a new page every day which links to five capsules selected entirely at random from the list of capsules known to the Lupa research crawler. Spending just a few minutes checking in on DiscoGem every day can very rapidly expand your Geminispace horizons.

DiscoGem - Discover new capsules every day

Of course, random exploration will still sometimes land you somewhere you've been before. To reduce the odds of this happening, you can limit your selections to relatively new servers. The geminispace.info search engine maintains, in addition to its list of all known hosts, a list of its fifty most recently discovered hosts:

Newest Gemini hosts discovered by geminispace.info

2.2.8 Mirrored web content

Some Geminauts write tools to mirror content from the web into Geminispace. Sometimes that mirrored content is Creative Commons or otherwise permissively licensed, making this totally legitimate so it can be mentioned in an official FAQ! For example, among other mirrored resources, Geminauts are lucky to enjoy an excellent interface to Wikipedia.

A Gemini mirror of The Anarchist Library

A Gemini mirror of textfiles.com

A partial Geminimirror of the SCP Foundation collaborative writing project

Gemipedia: A Gemini frontend to Wikipedia

2.2.9 Browse Gopherspace and the web via proxies

If you like, you can run some helper programs on your local machine which respond to Gemini requests for URLs corresponding to other protocols, like Gopher or the web, by fetching that content and translating it, as best they can, from its original content in a Gemini-compatible form. Many Gemini clients support passing non-Gemini requests to such translating proxies. Gopher proxies work very well as Gemini and Gopher are both text-centric protocols with similar approaches to linking. Web proxies work well for some content but not well for others. It goes without saying that a Gemini client can never work as anything close to a general replacement for a web browser, but if there's a relatively small number of text-centric websites you like to frequent, using one of these proxies can make it a lot easier to make the switch from spending most of your online time in a web browser to most of your time in a Gemini client.

Agena: A Gemini-to-Gopherspace proxy

Duckling: A Gemini-to-HTTP proxy

Duckling Proxy Quick Setup Guide For Local Hosting

Public Stargate Proxy: A Gemini-to-HTTP gateway

2.3 I'm finding a lot of dead links and empty capsules, what's up with that?

Gemini underwent an explosive surge of growth after being featured on the popular "Hacker News" website in 2020, at around the same time that the global Coronavirus pandemic meant that a lot of people were stuck at home, feeling disconnected and looking for something to do online that wasn't a Zoom meeting or doom-scrolling news websites. A lot of the capsules launched during this boom time are still online and active, but many of them were eventually abandoned and the domain registrations are starting to expire. A lot of people opened accounts at multi-user hosting providers and never did anything more than make a few "Hello, world!" or "Testing..." posts, but the provider as a whole is still going strong and staying online without clearing these capsules out. It's a little unfortunate, but it's also not at all surprising or problematic that not everybody who tries Gemini out decides to stick around for the long term. It's also not necessarily a healthy expectation that everything published on the internet stays up forever and ever by default, even after the responsible person has lost interest in or even forgotten about the content.

Of course, because Gemini pages are just individual, fully self-contained text files which by design cannot depend upon external resources to function, it's absolutely trivial to save a local copy of one if you are worried about it disappearing in the future. There's even a Gemini client which automatically maintains a persistent local cache of all pages you visit as you visit them! The main intent is to facilitate reading content while offline (to avoid distraction, or while travelling without connectivity, for example), but the mechanism also works just as well, at the level of an individual user, for protecting against link rot in those parts of Geminispace that you visit regularly:

Offpunk, an offline-first command line client for Gemini and other protocols

As of late 2021, there's a Geminispace archiving service, known as Delorean, which is similar to the web's (in)famous Wayback Machine:

Delorean, the Time Machine for Geminispace

If you really want to track down some older missing content, there are some earlier archives you can try, but you'll need to download an file containing the entirety of Geminispace at the time and hunt locally:

2020 Geminispace archives by mozz

2.4 How large is Geminispace?

It's difficult to know exactly. Counting unique hostnames of Gemini servers is likely to exaggerate the size of the space, since some multi-user sites give each user their own subdomain. On the other hand, counting unique IP addresses is likely to underestimate the size, as Gemini allows multiple different domains to be served from the same IP.

At any rate, as of mid 2023, there are about 425,000 known Gemini URLs, spread across about 2,500 capsules, about 1,700 domains, and about 1,200 IP addresses.

In early 2022 there were about 284,000 URLs across 1,900 capsules, 1,300 domains and 1,000 IP addresses, while in early 2021, there were about 200,000 URLs across 750, 500 domains and 600 IP addresses. So, no matter which way you care to measure it, Geminispace has been expanding steadily since day one.

You can find the latest statistics as the link below:

Geminispace statistics provided by Stéphane Bortzmeyer's "Lupa" crawler

2.5 How can I put some content of my own in Geminspace?

There are many options for getting content into Geminispace. The choices below are listed in approximately increasing order of required technical skill and expense.

2.5.1 Multi-user services with easy interfaces

There are a number of multi-user hosting services where all you need to open an account and start publishing content is either a standard web browser or a Gemini client which supports client certificates. You don't need to open a terminal or use the command line or mess about with file permissions or even know what any of these things are.

The very simplest way to start publishing in Gemini is to use a service which has a web-based front end. You don't even need a Gemini client installed to use one of these services! Although of course, you'll need one to actually view what you publish, and also to explore what's been published by your fellow users! Note that Gemlog Blue is the only one of these services where you content ends up published exclusively in Geminispace. The others make content available over Gemini and other protocols simultaneously, either the web or Gopher or both.

Services allowing to publish to Geminispace using a web browser:

Flounder, where your content will be available via Gemini and the web simultaneously

Gemlog Blue, featuring an ultralight web interface with no cookies or Javascript

The Midnight Pub,

The Smol Pub

There are also some purely Gemini-based multi-user services with easy interfaces. To use one of these, you'll need a Gemini client which supports something called "client certificates". All of the most popular GUI clients support this, so these services generally "just work". You only need a Gemini client to publish, and you can only access the content with a Gemini client. The whole experience of reading and writing within one of these services can happen from inside the same program, so the overall user experience is very familiar and not that different from using a web browser to access, say, Reddit or Twitter.

Technical limitations of Gemini protocol mean that platforms which work this way are largely limited to letting their users post relatively short, text-only content. The length restriction is not as severe as Twitter's 280 character limit so it's definitely not true that this paradigm cannot support large and active communities. But if you want to write long form content, more like what you would find on the web at Medium or Substack, or you want to be able to upload images or other non-text content to your capsule, then for now you will need to move further down the list of options in this section.

Services allowing to publish to Geminispace using a Gemini client with client certificate support:

Bubble: Discussion forums, microblogging, and Git issue tracking

Station: "Where capsuleers hang out"

2.5.2 Public access unix and tilde communities

A growing number of "pubnix" or "tilde" communities (multi-user unix systems where users interact with one another by SSHing in and using local email, chat and BBS applications) also offer Gemini hosting (typically alongside web and/or Gopher hosting). This is generally not quite as immediately easy and intuitive a way to setup a Gemini capsule as using one of the services listed in 2.3.1, but on the other hand most of these communities are actively interested in helping their users learn more about computing in a unix environment and will have chat rooms and/or bulletin boards in place where you can ask for help. If you are interested in publishing in Geminispace and you have been wanting to try to improve your general computing skills and know-how as well, joining a pubnix can be a great way to move toward both of these goals simultaneously!

You may be able to get an account at one of the communities in the (non-exhaustive!) list below. Please note that most of these communities are older than Gemini itself, and may be more focussed on other services, or may be specific to a particular theme or interest. Research your choices carefully and join somewhere you think you might fit in well overall, rather than just treating these amazing little worlds as free space to dump your stuff.

Ctrl-C.club

envs.net

Raw Text Club, aka RTC

Super Dimensional Fortress, aka SDF

Texto-Plano (a Spanish-language community)

tilde.club

tilde.pink

If you belong to a pubnix community which doesn't offer Gemini hosting, it can't hurt to ask the admin(s) if they are interested in adding this service!

2.5.3 Shared hosting via SFTP and/or git

If you already have a relatively high level of computer proficiency, and you are not interested in the community aspect or additional services of a pubnix/tilde server, but you also don't want the hassle or expensive of running your own server (see 2.5.4 below), then there are some providers who just offer Gemini hosting via either SFTP or Git repositories:

SourceHut (including support for custom domains!)

Un bon café, providing free SFTP hosting for French-speaking Geminauts

2.5.4 Self-hosting

The option offering you the most independence, freedom and control over your Gemini presence is to set up your own Gemini server on a VPS or a computer in your home (small SBCs like the RaspberryPi are perfectly capable of acting as Gemini servers!). Even if you use a computer in your home, you will probably still need to buy a domain from a registrar at a yearly cost, so some financial commitment is required, but this can often be relatively low.

There is a wide range of server software available to choose from in the "Servers" section of the Gemini software list below:

Gemini software list

It's true that you need a good level of technical knowledge to host your own Gemini capsule, and it's definitely not an option for everybody. At the same time, even if you've never done something like this before, you shouldn't think of it as an impossible hurdle and discount the possibility. Even old dogs can learn new tricks, and the desire to setup your own capsule can act as a motivator to learn new skills. In you succeed, the sense of achievement and feeling of self-empowerment will be a great reward, and even if you don't, chances are good that you will still come away from the experience having learned some things you didn't know previously. Ask the community questions about things you don't understand, and maybe write helpful guides for others about the thing things you do understand:

HOWTO Setup and Manage a Capsule on a Server You Own

2.6 I got some hosting space, what kind of files do I upload there?

Gemini uses its own very lightweight markup language for pages, commonly referred to as "gemtext" and served with the unregistered MIME type text/gemini. Gemtext looks an awful lot like the popular Markdown language, but is in fact distinct and simpler (see 4.3.4 if you're wondering why we didn't just use Markdown). You can learn more about gemtext at the links below:

A quick introduction to "gemtext" markup

Gemtext cheatsheet

It's important to understand that most of the features provided by gemtext are not there to let you control the way your capsule looks when somebody visits it, at least not directly. Gemini differs radically from the web in that it puts complete control over what capsules look like not in the hands of the person publishing the capsule, but in the hands of the person viewing it. The same capsule might appear in ten distinct ways if ten different people look at it using ten different clients. We're completely okay with that! See question 4.3.3 if you're curious as to why.

For example, you can use lines beginning with # to place headers in gemtext documents, but don't think of this as "a way to make some text big and bold". It's supposed to be a semantic thing. Gemini clients and a lot of other Gemini tooling relies heavily on headers to do things like present user interface elements that assist with quick and easy navigation of long documents with complicated structure, or to figure out how to title links appearing a subscription tool. If you use headers stylistically instead of semantically, this might have unintended consequences.

Of course, most clients do also put headers in a larger font or whatever, but they are not at all required to.

2.7 Okay I published something...how do I know if anybody has seen it?

Some people find it disconcerting to publish something and not receive any immediate feedback, in the form of "likes" or comments or upvotes or boosts or follows to let them know what people thought of it, or even whether anybody saw it all! Posting to Geminispace can feel like shouting into the void, or throwing a message in a bottle into the ocean, especially when it's your first time. People have a wide range of feelings and reactions to this, all of them valid.

2.7.1 Embrace throwing bottles!

Some Geminauts (especially those of the "small internet" persuasion, see 6.3) actually consider the "bottle in the ocean" nature of a Gemini page a benefit. When you receive immediate feedback in the form of "likes" or similar, you inevitably, even if only a little, even if you are actively trying not to, allow your future postings to be influenced by it. You start skewing your writing in the direction of what you think your readers want to read, even though your mental model of your readers is constructed on the basis of very flimsy feedback, that people leave quickly, easily, often anonymously, often with no real consequence for them, often after their own response has been inevitably influenced by what they have seen of everybody else's response. When you're tossing bottles into the electronic sea, you're much more likely to actually be your authentic self and write what you actually think about what you actually want to write about. It can be therapeutic for the author at the very least, or help them straighten out and give concrete form to some ideas that have been floating around in their head. But even as a reader, stumbling upon something which really resonates with you that you found in a random old bottle floating in an obscure corner of the internet, maybe many years after it was written, with no prospect of any further contact with the author, can be an surprisingly emotional experience. There's a kind of raw human intimacy involved that, despite being shared over great distance and great time, feels more profound than anything achieved with quicker, seemingly more "connected" forms of online contact. Pubnix/tilde communities are a great place to hunt for ancient bottles, as they tend to stay online for years, even decades.

2.7.2 Leave a contact address

Many Geminauts choose to leave an email address or a Fediverse or XMPP username (maybe one created just for the purpose) on their capsule, so that readers who want to let them know that they liked their post or that they disagree with an idea can reach out to them. This can be a bit scary, but it often works out very well. It's a higher barrier to feedback than a drive-by upvote or downvote, meaning you get them a lot less often, but when you do get them to tend to be of much higher quality. Because it's less convenient, they only come from people who really genuinely care about what you wrote. They didn't necessarily agree with everything you said, but even criticism tends to be "better" in this system; when people aren't leaving their feedback in a public forum where the feedback can itself get feedback, they feel less need to ham it up and make cruel jokes to score points with an audience. And when the feedback is positive, it can grow into a long term correspondence relationship because you're communicating from the get go over a general purpose medium that isn't linked to Gemini at all. If you're hosting your content somewhere like a pubnix server (see 2.5.2), it's likely that most of this kind of contact will come from fellow users of the same system, since they will peruse the user listings more often than outsiders, which means you already have a least one thing in common with most of the people you hear from.

2.7.3 Participate in an aggregator's response community

Many Geminauts "reply to" or "comment on" a post they find simply by writing a post of their own in their own capsule, linking back to the original post to provide context. This helps readers of the second author discover the content of the first author, which is a useful function of this approach. There's no guarantee that the first author is already aware of the second author and will see the reply (an email might help with this, if the second author really considers it important). However, many people find posts to reply to on some kind of aggregator service (see 2.2.1), and as a rule of thumb, people tend to keep an eye on aggregators which include their own content (though of course there are exceptions), and so it's not unusual at all for back-and-forth "conversations" between groups of people to organically spring up on large aggregators. In this way, some popular Geminispace aggregators actually function something like a slower-paced decentralised social network, without there actually being any kind explicitly social infrastructure in place. For many Geminauts, this is actually their main form of interaction in Geminispace and they don't feel a need for anything more. This approach won't necessarily scale well to large and diverse communities, but there's no obstacle to and nothing wrong with setting up more aggregators with specific focal topics and different community norms as the need arises.

2.7.4 Get social, even in Geminispace!

Not all Geminauts have strong negative attitudes toward the idea of "social" feedback, although for now they are probably in the minority. There are certainly social options available for those who wand them, though.

If you are self-hosting your Gemini content, you have the option to use CGI applications or some kind of framework to add likes, comments, "mentions" or other such functionality to your capsule. Some available resources for this are:

gemlikes, a liking and commenting system

Gemini Mentions, a standard method for capsule owners to communicate the existence of responses

You can also make use of some of the more "social" style Gemini apps which have recently appeared (see 2.5.1), where likes and replies are available and function more or less just like on the web. You can either actually post most of your content in these spaces and participate in the surrounding social interactions, or you can just use these places as a venue to solicit feedback and engage with our readers.

2.8 I don't really care about feedback, but I'd like to attract readers, how can I do that?

The most important thing you can do to attract and maintain a readership in Geminispace is to write content that people actually want to read! Without that, nothing will really help.

If you've set up your own Gemini server to host your content, you should probably consider submitting your URL to at least one of the Gemini search engines (see 2.2.3) so that your capsule gets indexed in the future. If you are using somebody else's hosting, chances are good the search engines will pick your content up without you having to do anything yourself.

Submitting either your entire capsule or some individual posts to one of the large Geminispace aggregators (see 2.2.1) will help people to discover your work. Depending on the aggregator, doing this might require you to either generate an Atom feed for your capsule, or else format some parts of your capsule to facilitate subscription.

Making it easy for people to subscribe to your capsule increases the chances that somebody who enjoys something you've already written will read things you write in the future. It's worth doing even if you aren't interested in being featured on one of the large, popular aggregators. Plenty of Geminauts do not check those aggregators regularly, preferring instead to curate their own reading experience by subscribing directly to capsules they enjoy.

The quickest and easiest way to make your capsule subscribable is to follow the relevant Gemini companion specification, linked to below. In short, any page containing links whose link text begins with a date in the YYYY-MM-DD can be subscribed to, either via aggregating tools or directly within some Gemini clients. If you format your links this way, you should also give the page a header line, as most subscription software will use this as a "feed" title and/or to format links.

Companion spec: Subscribing to Gemini pages

2.9 I'm kind of on the fence about publishing in Geminispace...

If you like the sound of Gemini in principle and you're tempted to set up a capsule but you're worried that it'll be a waste of time because you'll only have a tiny audience compared to publishing on the web, or you don't want to feel like you are excluding people who don't know about Gemini yet or don't want to use it, don't despair! You can bihost your content in Geminispace and the web simultaneously. Read more about this in question 2.11.2.

If you build your capsule as a capsule first and foremost and use a tool like Kineto to automatically mirror it to the web, it's kind of like building a website using a very opinionated CMS that stops you building anything other than a very simple, clean, functional website. You can use CSS to style the generated HTML for a little bit of visual identity if that is important to you (you'll only have a handful of tags to work with, so it'll be hard to create anything too excessive), and then anybody with a web browser will be able to see it, possibly without having even the slightest idea that it's a Gemini capsule behind the scenes. Meanwhile, Geminauts will also be able to see it natively without having the slightest idea that it's also on the web. Both "teams" can see your content the way they presumably like best, and you can feel good about doing your individual part to make the average website a tiny bit less awful than the status quo.

Later, if you decide you'd like to go "all in" on Gemini, you can just stop running the mirroring tool and replace the mirror with a single static page letting people know you've gone Gemini only. Or, if for some reason you decide you don't want your content to be in Geminispace anymore, you can reconfigure your Gemini server to listen to connections from localhost only, so that the mirroring tool is the only way to access it. That way you can take as long as you need to convert your content to some kind of web-only CMS.

What have you got to lose, other than the power to build noisy, cluttered, invasive websites?

2.10 I set up my own Gemini server, is there anything I should do?

In addition to submitting your URL to search engines (see 2.2.3), you may wish to consider creating a robots.txt file in an effort to control how automated Gemini clients access your server:

Companion spec: robots.txt for Gemini

2.11 What are my options for "bihosting" or "trihosting" content in Geminispace?

2.11.1 Bihosting on Gopher and Gemini

If you already have a presence in Gopherspace, then you can very quickly and easily transition to bihosting the same content in Gopherspace and Geminispace simultaneously using the GeGoBi (for "Gemini-Gopher Bihosting") tool. It takes care of translating Gopher menus into gemtext documents. You can continue to simply maintain your Gopherhole in whatever way you are used to, and the Gemini mirroring is entirely automated.

GeGoBi, a Gemini-Gopher bi-hosting tool

20.11.2 Bihosting on Gemini and the web

You can do this in one of two ways.

It's easiest if you begin by creating a Gemini capsule. Then you can quickly and easily bihost the same content on Gemini and the web simultaneously using the Kineto tool, which mirrors a single domain Gemini capsule into the web:

Kineto: A single domain HTTP-to-Gemini proxy

This is the way the gemini.circumlunar.space website works. Solderpunk only maintains the Gemini version, and Kineto takes care of the rest.

The other way is to start with a website. This way is trickier, because mapping from the web to Gemini is "lossy". But some people have managed to e.g. convince the Hugo static site generator to output both HTML and Gemtext versions of a site:

"Gemini and Hugo" blog post Sylvain Durand

Blurring the distinction between these two approaches is a minimalistic web CMS called Lichen, which uses gemtext as its storage format (much like many other CMSes would use MarkDown). With a little configuration, you can take advantage of this design to serve the same content via Gemini and the web simultaneously:

Lichen, an extremely lightweight web CMS based on gemtext

20.11.3 Trihosting

It's no problem to point GeGoBi at a Gopherhole and then point Kineto at GeGoBi to "lift" content from Gopherspace into Geminispace and the web, establishing a quick and easy presence on all three protocols. Doing this, though, doesn't let you take advantage of some of the ways that Gemini has tried to improve on the usability of Gopher. You would have to write Gophermaps instead of gemtext, for example, and your text would be hard-wrapped at 70 or 80 columns in order to look good in Gopher clients, which means that Gemini clients can't wrap it to fit the small screens of mobile devices.

If you treat a Gemini capsule as the "starting point" rather than a Gopherhole, you can use Kineto to get your content on the web, but then you need a way to translate "down" to Gopher. There doesn't seem to be any existing tools for this yet. It's a subtler problem than it seems at first. It's easy to take a gemtext file, wrap the lines to a specified number of columns, leave the rest as it is and just serve it as an item type 0 text file over Gopher. This forces your Gopher audience to read raw gemtext, which is not exactly difficult or ugly, but feels a little disrespectful toward the space. On the other hand, it's easy to go a step further and automatically translate gemtext pages to Gopher menus, so that the links become selectors and can be followed without copying and pasting URLs, and it's not even immediately obvious that the content has originated from Geminispace. But then you've created one of those Gopherholes where absolutely everything is a menu, and as discussed in question 4.2.2 that's also not really in the spirit of Gopher (although plenty of people who are active only in Gopherspace do it anyway, so it can't really be considered the act of a "foreign barbarian"). Doing "Gemini-first tri-hosting" in a really respectful and thoughtful way toward Gopherspace requires a little bit of thought and may need some custom tooling for your presence.

3. Project history, organisation and trivia

3.1 How old is Gemini?

Project Gemini started in June 2019. While the protocol itself is largely finalised, the available software, resources and community are still in a relatively early (though thriving!) state of development. If you'd like to know a lot more about the history of the project, you can find the dates of some major milestones and occurrences at the official project history linked below:

Project Gemini history

3.2 Who is behind Project Gemini?

Project Gemini was originally started by Solderpunk <solderpunk _at_ posteo _dot_ net>, who remains the "Benevolent Dictator" of the project.

However, the protocol has been designed in collaboration with a loose and informal community of many interested parties via private emails, public mailing lists, posts made in Gopher's "phlogosphere" (which is where Gemini originated) and toots in the Fediverse. So while the project has a single leader, Gemini should certainly not be thought of as the work of a single person.

In particular, the following individuals were very active during the earliest stages of the project, and without their contributions Gemini would either look quite different to how it looks today, or perhaps would not even be around today at all:

    Julien Blanchard
    Sean Conner
    Jason McBrayer
    Mozz
    Sloum
    James Tomasino

Specifically, each person on the list above satisfies at least three of the following criteria:

    Participated in Gopher-based discussion of Gemini before the mailing list was established
    Was one of the 10 most active posters on the mailing list before the post-Hacker News surge
    Runs or ran one of the first 10 public Gemini servers
    Wrote one of the the first 10 Gemini client or server implementations

If you believe you meet at least two of those criteria and your name is not above, please contact Solderpunk!

3.3 What is the leadership structure and decision making procedure?

As mentioned, Solderpunk functions as a Benevolent Dictator and decision making authority lies with him. Decisions are generally made on the basis of consultation with the community and Solderpunk strives to maintain transparency and to justify decisions in terms of the project's goals.

In February 2021, long time Gemini contributor Sean Conner was granted some decision making authority to help finalise the Gemini specification during a time when Solderpunk was unable to dedicate the necessary time and energy to the project. Later in 2021, Solderpunk returned to leadership duties.

3.4 Wait, that's it? No committees, no elections, no annual reports?

The administrative structure of Project Gemini has been deliberately kept lightweight for two reasons.

Firstly, Gemini is an "opinionated" project with arguably a clearer idea of what it doesn't want to ever become rather than exactly what it should be. It errs strongly on the side of minimalism in order to stick to these ideas. Large and bureaucratic "design by committee" processes can be fatal to projects like this.

Secondly, unlike the majority of modern technical projects, Project Gemini does not aim to stay active at a constant or increasing level of activity for as long as possible, continually making changes, but rather to try to finish something small and bounded as quickly as possible and then leave it finished forever after. A project like this should require a lot less administrative overhead than, say, developing a Linux distribution.

3.5 Sounds nice in theory, but Solderpunk disappears a lot and nothing gets done

It's true! But as of 2023 he seems to be getting better. He begs forgiveness, patience, and trust.

Delays are frustrating, but there shouldn't be a sense of urgency around Gemini. Thanks to both the lack of easy extensibility of the protocol and the healthy diversity of client implementations, it's very difficult for the project to get "hijacked" in any meaningful sense during periods of "leadership vacuum". This is by design, and in some sense Solderpunk's burn out hiatus period has functioned well as stress test of this design philosophy. Gemini passed with flying colours! People just kept using it to build cool things.

3.6 What happened to the mailing list? Will it come back?

Quite early in the project's life (in August 2019), an official Project Gemini mailing list was established, and for many years this was essentially the "heart" of the project. The mailing list infrastructure was provided to the project free of charge by the admin of the now defunct orbitalfox.eu domain. This act of kindness had a tremendous impact on the project.

Unfortunately, the approach of having a single unmoderated mailing list where everything happened did not scale well as interest in the project grew rapidly. As the community expanded from a relatively small group of Gopher users with a common technical and cultural background and at least a vaguely shared vision to a large and growing group of people with a variety of backgrounds and expectations, disagreements grew increasingly common, and the overhead of having to continually explain and justify the overall philosophy become burdensome. Sometimes discussion became heated. A lot of people who had been active in the project since its earliest days unsubscribed from the list and drifted away from the project.

Sometime during the final days of 2021, the orbitalfox.eu server suffered a hardware failure and the mailing list went offline. The server was never fully resurrected and the mailing list remains defunct. Thankfully, multiple members of Gemini community had local archives of the list, and every post can still be read today:

View full list archives via web

View partial list archives via Gemini

It would be hard to deny that ultimately the mailing list "didn't work out", and to this day the list can be a little bit of a touchy subject for some Geminauts. Despite the unfortunate end, it's just as undeniable that in many ways it served the community well, and lots of important discussions were had on the list which fed directly into the protocol design. The project certainly would not have been better off without it.

It's not clear that bringing the mailing list back would be a substantial boon for the project, at least not as a means for conducting official work on finalising the protocol design. As a community resource for announcing projects and sharing links and other information, the idea has more merit. If somebody with a proven track record of positive community involvement wants to volunteer to operate and moderate such a list and take responsibility for it not devolving into endless arguments about supposedly missing features, they may contact Solderpunk.

3.7 What stage of its lifecycle is the project in?

The current (informal) specification of the protocol is largely frozen, modulo small changes to remove ambiguity and address edge cases. Suggestions for new features will not be considered, as the protocol is considered feature complete. Going forward, the main focus of the project now is on growing the community around the protocol, as well as working on translating the existing specification into a more precise and formal version which might be considered for submission to internet standards bodies such as IETF and IANA.

3.8 I found a GitLab repository with a different spec from gemini.circumlunar.space, what is it?

This is neither the current official spec nor a rogue fork. Rather, the repository was setup during the time of Sean Conner's decision making authority (see 3.3 above) to help keep track of outstanding issues while working towards a finalisation of the spec. As part of that process, the single, informal document that was and is the official specification was split into two parts, one for the network protocol and one for the text/gemini file format, and both were being worked into more formal versions.

In principle, the two different specifications should be identical or close to it, and where they differ the changes in Sean's newer version ought to be things that Solderpunk agrees with, but this can't be completely guaranteed.

Solderpunk has made it an explicit goal to resolve this situation by the end of 2023 by carefully examining all versions and eventually switching to two separate formal documents derived from those at the GitLab repository as the new official specs and hosting them at the official project documentation.

3.9 What's with the name?

It's a reference to the pre-shuttle era of US manned spaceflight, which consisted of three projects. The first was Project Mercury, which was a fairly minimalist "proof of concept" and part of the race to put a human in space soonest (which the Soviet Union won with their Vostok project). Mercury was a one-man capsule with no ability to adjust to its own orbit after launch and only one Mercury flight lasted longer than a single day. The last was Project Apollo, which was large, heavy, complicated and expensive but could, of course, fly three men to the moon and back.

Less well known to the modern public, Project Gemini was the "middle child": a two person capsule which could rendezvous and dock with other craft in orbit, could be depressurised and repressurised in orbit to facilitate spacewalks, and whose longest flight was almost two weeks - longer than any Apollo mission! In terms of size, weight and cost Gemini was much closer to Mercury than to Apollo, but in terms of capabilities it was the other way around - there were even plans (which never eventuated) to do circumlunar Gemini flights!

Hopefully the analogy is obvious: Gopher is akin to Mercury, and the web is akin to Apollo. Gemini hopes to sit between the two, doing more with less.

Gemini very deliberately didn't receive a name which had *anything* to do with gophers, or other rodents, or even other animals. During the earliest phlog-based discussions which eventually grew into Project Gemini, a lack of careful writing meant it was sometimes unclear whether people were talking about replacing Gopher outright, or adding unofficial, compatibility-breaking upgrades into existing Gopher clients and servers. When idle discussion turned into an actual project, it seemed wise to send a clearer message.

4. Protocol design

4.1 Comparisons to Gopher and the web

4.1.1 I'm familiar with Gopher. How is Gemini different?

Compared to Gopher, Gemini allows for:

    Unambiguous use of arbitrary non-ASCII character sets.
    Identifying content using MIME types instead of a small set of badly outdated item types, and this information comes from the server together with and at the same time as the content, rather than being stored in a separate menu.
    Clearly distinguishing successful transactions from failed ones, in a machine-readable way to allow for more robust automated user agents.
    Linking to resources served over other protocols via simple URLs, without ugly hacks (item type h plus "URL:").
    Redirects to prevent broken links when content moves or is rearranged.
    Domain-based virtual hosting.

Text in Gemini documents is wrapped by the client to fit the device's viewport, rather than being "hard wrapped" at ~80 characters with newline characters. This means content displays equally well on phones, tablets, laptops and desktops.

Gemini does away with Gopher's strict dichotomy between menus and text files, and lets you intermingle text and links in a single "item type". Increasingly many phloggers try to push Gopher in this direction by serving everything as item type 1. At the level of the Gopher protocol, this is ugly and inefficient, with phony selectors, hostnames and port numbers transmitted along with every line of text in a post. In Gemini, there's no penalty for this, it's normal. Of course, if you really like the Gopher way, nothing in Gemini stops you from duplicating it. You can serve "item type 0" content with a MIME type of text/plain, and you can write text/gemini documents where every single line is a link line, replicating the look and feel of a RFC1436-fearing Gopher menu without that pesky non-standard i item type.

Gemini mandates the use of TLS encryption. It even provides a way for servers to request a client certificate for clients, which is a way to establish a "session" of requests. This allows developing simple, textual applications where all the state is maintained server-side without relying on fragile mechanisms like binding sessions to IP addresses.

4.1.2 I'm familiar with HTTP and HTML. How is Gemini different?

The Gemini network protocol looks kind of like something between HTTP 0.9 and HTTP 1.0. There's only one kind of request, analogous to GET, and the request itself is nothing but a URL. It's sort of like a HTTP request where the only header allowed is Host. The response is kind of like a HTTP response where the only header allowed is Content-type. By design, the request and response formats are not extensible, so these are the only HTTP header-esque things that will ever be there. This is considered a good thing: Gemini does not and never will contain an equivalent of the Cookie, Referer or User-Agent headers, which goes a very long way to preventing user tracking.

This freedom from the threat of tracking comes with downsides: Gemini has no support for caching, compression, or resumption of interrupted downloads, and as such it's not very well suited to distributing large files, for values of "large" which depend upon the speed and reliability of your network connection. Without an equivalent of HTTP's POST method, Gemini does not really support uploads, at least not in a simple and straightforward way. That doesn't mean that user input is totally impossible; queries included in URLs can be used to, e.g. send a search term or a username to a server. But it does mean you can't use Gemini itself to put content into Geminispace. You need to use something else, such as (S)FTP, SSH, rsync, git, a web interface, an email interface, etc.

The "native content type" of Gemini (analogous to HTML for HTTP(S)) never requires additional network transactions (there are no inline images, external stylesheets, fonts or scripts, no iframes, etc.). This allows for quick browsing even on slow connections and for full awareness of and control over which hosts connections are made to. The native content type is also strictly a document, with no facility for scripting, allowing for easy browsing even on old computers with limited processor speed or memory. Complete control over the visual styling of these documents is granted to the reader, not the author. There's nothing like CSS for Gemini. That doesn't mean Geminispace is ugly. Beautiful graphical clients exist which allow you to style the whole of Geminispace to look the way that looks and works best for you.

Gemini mandates TLS encryption for all transactions. In lieu of cookies, Gemini allows using TLS client certificates as a way for the user to authenticate themselves to apps. Compared to passwords and cookies, this is far less vulnerable to brute force attacks and session hi-jacking, and users always have the right to instantly, irrevocably and unilaterally delete their private key, permanently ending a session.

4.2 What were the design principles for Gemini?

Gemini looks very unusual to a lot of people, and sometimes they assume that some aspect of the design is a mistake that arose because the designers didn't know what they were doing. It's true that Gemini is an amateur project (see question 7.5), but more often than not these supposed "defects" and "oversights" are actually things which were designed in very deliberately with full awareness of the consequences, because the consequences were something we actively wanted. The reason Gemini looks strange is that it wasn't designed according to "usual" principles, such as:

    Make sure it can do as many different things as possible
    Make sure it appeals to the widest possible audience
    Make sure it can have extra features added gracefully at any time
    Make sure it can effortlessly scale up to the entire planet

We had very different ideas in mind. It's true those ideas weren't always made explicit and crystal clear, and there wasn't a clear ranking of design principles in order of priority, so that when two principles were in conflict and a trade-off had to be made we always bent in a consistent direction. Gemini might not be provably optimal for anything, but ultimately we ended up pretty close to the mark we were intuitively aiming for. It may not be perfect, and it may not suit your favourite use case for the web, but for people who hold our community's values and are interested in using Gemini for the kinds of things it was intended for, it's far and away the best game in town.

The following principles have left a strong mark on Gemini's design.

4.2.1 User privacy

Gemini was designed with an acute awareness that the modern web is a privacy disaster, and that the internet is no longer a safe place for plaintext. It's not enough to simply refrain from from deliberately designing in tracking features, which is easy. The history of the web proves that user tracking can and will be snuck in via the backdoor using protocol features which were never designed to facilitate it. Thus, the designers of Gemini assumed active malicious intent and tried to avoid designing in anything which could be subverted to provide effective tracking.

Any bit of information which is capable of making a round trip from a server to a client and then back to the server again without being modified has the potential to be a privacy threat, allowing the server to recognise a client as a repeat visitor even if their IP address has changed between visits. Such round trips are common in HTTP. The contents of a Last-Modified or Etag response header can end up in a subsequent If-Unmodified-Since or If-None-Match request header. When used as intended, these headers don't serve to uniquely identify a user in isolation, but they leak a non-zero quantity of information. They can be combined with other such identity leaks (such as the many well-known browser fingerprinting techniques) to help narrow down a user's identity. Far worse, they can and have been abused for the express purpose of uniquely tracking users. You can read about Etag-based "supercookies" on the web to learn more.

A protocol which is seriously committed to user privacy must be designed in such a way as to "break all loops", ensuring that nothing contained in a server's response has any way of ever ending up in a client's request. Gemini achieves this by the simple expedient of making the client request as simple as possible. It consists of nothing other than the URL which is being requested, which is of course necessary for the request to be unambiguous. Gemini requests convey literally the bare minimum of information. This not only breaks all loops between server and client, it also thwarts efforts at client fingerprinting (although fingerprinting becomes possible when clients choose to supply a client certificate).

Of course nothing is perfect. A truly malicious Gemini capsule can still track a user by programmatically inserting random unique IDs as path components of all URLs, but even Gopher is vulnerable to this.

4.2.2 User autonomy

Gemini is designed to put client users in the driving seat, not server admins or content publishers. On the web, it's impossible for you to know in advance or exert any meaningful control over whether clicking on a link will cause your computer to connect to one remote sever, or ten, or a hundred, or what information it will send to them, or how many files of what type it will download. Web "pages" are allowed by default to run calculations on your CPU and store files on your hard drive. No facility is provided for you to impose fine-grained control over any of this. If it were, most websites would break if you tried to exercise this control, because they're designed on the assumption of a submissive relationship with the user, that the web is just a way for you to hand them control of your computer. Heck, you don't even get to decide whether you read dark text on a light background or vice versa unless the web designer decides to do extra work on their end to offer you the choice.

Gemini completely inverts this relationship. When you click on a link, your client connects to exactly one server (specified in advance in the link URL) and that server gets to send you exactly one file, and chances are very good it'll be a file of gemtext (the only type of file guaranteed to be handled correctly by every Gemini client and overwhelmingly the most commonly served type), and all your client can do with that file is put some text on your screen and offer you some links to other files. How the text is formatted is almost entirely under the client's control. About the only the thing the document author can do is clarify that some sections of text really ought to be presented in a fixed width font, so that computer code or ASCII art looks like it's supposed to. Text size and font and colours are entirely up to the client.

It's not just visual styling that is under the user's control. The gemtext document was designed without any way for a document to "pull in" any other file, allowing authors to cause your computer to connect to arbitrary third parties. This doesn't just safeguard your privacy (although of course we were thinking about that, see section 4.2.1), but because gemtext documents are standalone entities which cannot meaningfully "contain" any other file or depend upon any other file to specify the appropriate way of handling them, it's impossible to to break them by exerting control. A Gemini client can be configured to refuse to connect to certain servers, or to refuse to download files with certain MIME types, or to terminate downloads which exceed a certain file size, and it's impossible for these decisions to have unintended consequences. Any document which makes it past your chosen restrictions will look and function exactly the same way it would without your restrictions. You can pick and choose at will.

The firm commitment to the principle of "one network transaction per click", which has left a few marks on the protocol design, isn't just in aid of user autonomy. It also contributes to user privacy (see answer 4.2.1), because if processing a document served from one host could trigger the automatic fetching of another file from another host, that could be used to facilitate tracking.

4.2.3 Non-extensibility

The web has slowly but very surely mutated from an electronic library of interconnected documents - which is what Gemini first and foremost aims to be - into a general purpose computing platform. User privacy (see answer 4.2.1) and user autonomy (see answer 4.2.2) have necessarily suffered, since the changes along the way have invariably given more control and more abilities to those doing the publishing but none to those doing the browsing. The web was not designed from day one to be anything like what it is today, and yet it's continued to be built on the same foundation of HTML and HTTP the whole time. How was such a dramatic and unforeseen change able to happen without needing to complete replace the foundation? The mutation was possible because HTML and HTTP are both extremely extensible.

If you know a little HTML, it's easy to see this. Suppose that the only three tags that existed were <a>. <b>, <i> and <p>. Later, if somebody wants to add a new feature, it's extremely obvious how to do it. Just pick a new letter and re-use the angle bracket syntax, say, <u>. You don't even need to stick to one letter, so the space of possible tags which could exist is literally infinite. A parser which can parse a version of HTML with 100 tags isn't much more complicated than one that can parse a version with 10 tags. Browser implementers can, and did, add tags that weren't designed into HTML. Browsers that didn't support the tag didn't crash when rendering pages that used it. After all, even if no wild HTML extensions are out there, users will make typos sometimes, so browsers have to be robust against unfamiliar tags.

Suppose there are only two browsers in the world, A and B, each with exactly 50% of the userbase. If browser A adds support for a new HTML tag, the first sites to use it won't work as intended for users of browser B. But because half the world uses A, some users of browser B will see the new site working correctly on the computer of a friend or co-worker. Maybe 10% of them will think the new tag is so cool, they switch browsers. Now browser A has 55% of the userbase. They can tell web authors that their cool new tag works for "the majority of users", so more people start using it. Browser B continues to lose users to browser A. Eventually, they cave in and add support for the new tag. Now it's for all intents of purposes a part of HTML. Rinse and repeat for a few years, and the tags can multiply out of control. It doesn't matter if the people in charge of the official definition of HTML don't want this to happen for very good reasons. They can stomp their feet and yell all they want, but you can't throw browser developers in jail for ignoring a spec, so extensions will happen.

If you know a little about HTTP, you'll see how the same is true of response and request headers, and request methods.

Even Gopher is extensible by design. The items in a Gopher menu are assigned an item type, indicated by a single number, a single symbol (like +) or a single letter, with uppercase and lowercase letters distinguished. That makes for over 62 possible item types! At least that's a finite number. And RFC 1436 explicitly encourages "local experiments" (as long as they aren't machine specific). In practice, despite being around for even longer than the web and never completely dying out, remarkably little extension of Gopher has actually happened. Two item types, i and h, which are not in RFC 1436 are widely used and widely supported, but that's it.

Why didn't Gopher undergo the same uncontrolled ballooning of the web? Part of the reason might be that because Gopher is such a simple protocol it's very easy to write your own client. If something is easy, more people do it, so there are a lot of Gopher clients out there. The dynamic between the two big web browsers A and B described above wouldn't play out anywhere near the same if there were 10 different browsers each with roughly 10% of the userbase. An extension can only become universally adopted in that scenario if almost everybody is in agreement that it really is for the best. This probably isn't the whole story behind Gopher's stability (once the web came along, Gopher would only have appealed to people who liked it as it was, and were less prone to want to extend it), but it has surely played some role. The principle that client diversity induces protocol stability is real.

Gemini was designed from the beginning with all of the above very clearly in mind. We didn't want to design a protocol around user privacy and user autonomy and then watch those things slowly erode as Gemini mutated in the wild once it left our control, so we went all out on non-extensibility. We tried to design a protocol that was hard to extend. We didn't just refuse to add any deliberate "hooks" to the protocol for people to hang arbitrary additional features off in the future; we tried to avoid inadvertently leaving any slightly pointy bits that weren't intended as hooks but might still function that way if you took care to hang something small enough at just the right angle. We tried to design a smooth, shiny protocol with a mirror polish that any attempted extensions would just slide right off. We really didn't want to take any chances, so in addition to making it smooth and shiny we also tried to make Gemini very simple to implement (see answer 4.2.4), to encourage as many different clients as possible for extra stability.

Our twin commitments to non-extensibility and simplicity of implementation are the reason that a lot of "nice things" from the web are missing in Gemini. Fewer features and the occasional rough edge are the prices we've knowingly and willingly paid to stand our ground as firmly as we can on the things that are most important to us.

4.2.4 Simplicity of implementation

Gemini's design strives for ease of implementation on two levels, conceptual and practical.

On the conceptual level, Gemini is designed to be "radically familiar". It is based on a very traditional internet architecture of clients and servers, requests and responses. There's no peer to peer networking, no distributed hash tables, no blockchains, no content based addressing or any other exciting, fun new technologies you might expect from a young, modern protocol. That's not because we think those things are necessarily bad, but just because they are unfamiliar. A lot of programmers don't understand how they work in any kind of detail. Even the ones who do have a decent theoretical understand may not have any practical experience. The concepts behind Gemini are really bread and butter stuff in comparison. Anybody who has worked with either the web or Gopher can get a pretty solid handle on Gemini in a single sitting without having to look something up on Wikipedia even once.

On the practical level, Gemini's design is basically a novel way of connecting together some very non-novel technological primitives; mature, standardised and widely used technologies like TLS (1999), URLs (1994) and UTF-8 (1993). You can typically find good support for these technologies in just about any programming language on just about computing platform that you care to name. As a result, writing Gemini software can feel a lot like joining together Lego bricks. Most of the hard work has already been done. When new languages and new platforms appear, would-be Gemini implementers just need to be patient. Somebody else, probably somebody who hasn't even heard of Gemini, will soon replicate all our required bricks for us, because they are necessary for so many other things.

Another practical aid to implementation is that Gemini was designed with a lot of "opt out" details. For example, Gemini response status codes are two digits long, but are designed so that minimal clients can decide how to handle the response on the basis of the first digit alone in a way which does not impair core functionality. Similarly, the gemtext markup language defines multiple line types, but these are split into basic and extra line types, with clients being permitted to treat extra line types as equivalent to the simplest of the basic types.

All these design decisions paid off when Gemini was featured on the popular Hacker News website in May of 2020. There was a Cambrian explosion of Gemini software in a variety of languages. Serious interoperability issues never emerged.

In the early days of Project Gemini, simplicity and minimalism were emphasised as much out of aesthetic and philosophical preference as a practical means to encourage diverse implementations to induce protocol stability. That preference for austere elegance is still there for a lot of Geminauts, but it's probably fair to say we've fallen short of some of our earliest aspirations, which were:

    It should be possible for somebody who had no part in designing the protocol to accurately hold the entire protocol spec in their head after reading a well-written description of it once or twice.
    A basic but usable (not ultra-spartan) client should fit comfortably within 50 or so lines of code in a modern high-level language. Certainly not more than 100.
    A client comfortable for daily use which implements every single protocol feature should be a feasible weekend programming project for a single developer.

Even if Gemini isn't quite this simple, it is several orders of magnitude closer to being this simple than it is to being as complicated as the web. In the early days, we also talked about striving to maximise "power to weight ratio" rather than striving to "minimise weight". That's probably still a good way to describe Gemini.

4.3 Questions about the response and request headers

4.3.1 Why is there only one kind of request, wouldn't something like POST be nice?

This is a deliberate decision made in direct service of the guiding principle of non-extensibility (see answer 4.2.3).

In order for Gemini to support more than one kind of request, there would need to be some way to specify in a request which kind it was, similar to how HTTP requests begin with the name of a method, like GET or POST. As soon as there such a way, it is immediately obvious how to easily add new kinds of request. The door to extension is wide open. This is how the web went from only GET (HTTP/0.9) to GET, HEAD and POST (HTTP/1.0), to GET, HEAD, POST, PUT, DELETE, CONNECT, OPTIONS and TRACE (HTTP/1.1). We wanted to exclude that possibility.

If there's only one kind of request, there's no need to specify which kind it is. That information can be left implicit. Then the door to extension is closed, which is how we like it.

If there's only going to be one kind of request, something analogous to GET is the obvious choice. After all, GET was the first and originally only method in HTTP.

Gemini is in this regard no different to Gopher, and nobody in Gopherspace ever complains about it.

4.3.2 Why isn't there an equivalent of the HTTP Content-length header?

This is a deliberate decision made in direct service of the guiding principle of non-extensibility (see answer 4.2.3).

If the response header for a successful Gemini transaction were to include multiple different kinds of information, it would be necessary to specify some kind of delimiter to separate the components. Once a delimiter is specified, there is an obvious path to extending the design of the header to include additional pieces of information, simply by reusing the same delimiter. The door to extension is wide open.

If there's only one kind of information, there's no need to specify a delimiter. Then the door to extension is closed, which is how we like it.

If there's only going to be one kind of information about a response, an equivalent of HTTP's Content-type is a better choice than Content-length. Among other advantages, this makes it straightforward for a server to convey information about how a text response is encoded. That information is missing in Gopher, and this complicates writing a robust client which needs to be able to handle an undeclared mix of ISO/IEC 8859-1, UTF-8, KOI8-R and more.

Gopher also has no equivalent of the Content-length header, and unlike the lack of specified text encodings, this has not proven to be a practical obstacle in Gopherspace. Unlike Gopher clients, Gemini clients can distinguish between a transaction which has completed successfully and one which has dropped out mid-transfer due to a network fault or malicious attack even in the absence of Content-length information, via the presence or absence of a TLS Shutdown message.

It is true that the inability for clients to tell users how much more of a large file still has to be downloaded and to estimate how long this may take means Gemini cannot provide a very user-friendly experience for large file downloads. This would be true even if Content-length were specified, as such an experience would also require other complications to be added to the protocol e.g. the ability to resume interrupted downloads. Gemini documents can straightforwardly link to resources hosted via HTTPS, BitTorrent, IPFS, DAT, etc. and this is the better option for very large files.

It is true that the lack of Content-length makes it difficult to reuse a connection to reduce network overhead, but that is no great loss for a protocol dedicated to the idea of "one network connection per click" (see answer 4.2.2).

It is true that with a little care, a "self-terminating" response header could be designed which included more than one kind of information without leaving the door to extension wide open. Since MIME media types are permitted to include whitespace, using whitespace as a delimiter and putting something like Content-type as the final component in a sequence of other components which cannot include whitespace would have resulted in a response header which could not be unambiguously extended. This would allow a simple pair of Content-size and Content-type. This possibility was genuinely overlooked. It would have slightly complicated serving dynamically generated content, where the Content-size is not known in advance, and would render impossible some of the interesting "streaming" experiments which have appeared in Geminispace. It's unclear whether this would have been a good trade-off, given the lack of obvious problems caused by the missing Content-size information in either Geminispace or Gopherspace.

4.3.3 Why isn't a protocol version number included with requests or responses?

This is a deliberate decision made in direct service of the guiding principle of non-extensibility (see answer 4.2.3).

Since Gemini was designed from day one to resist any efforts at extension, it would be entirely self-defeating to include a facility for a smooth upgrade to "Gemini 2.0" in the future. There will never be a Gemini 2.0.

It is true that a method for signalling protocol version would be useful even in the absence of a desire for adding new features, by allowing corrections to defects which are discovered in the future. The hope is that Gemini is sufficiently simple that all but the most obscure and inconsequential of bugs can be discovered through extensive testing by the early adopters prior to freeing the specification. We are betting on being able to "get it right the first time", or at least getting close enough to right that we don't find it unbearable to live forever after with our small mistakes.

It is not true that the specification of Gemini follows a "living document" philosophy of eternal changeability. It was planned from day one that the specification would eventually be very clearly and very loudly finished and frozen.

This "one and done" approach to protocol design may seem radical or unwise, but we're cautiously optimistic. As ever, we take direct inspiration from Gopher, a simple protocol whose specification has not been changed in about 30 years, yet remains as functional and useful as it ever was and is still winning hearts and minds today. We see no reason Gemini can't follow a similar path, and we're not the only recent tech project to try something like this. The Hare programming language has a similar philosophy:

    we plan to freeze the language once it reaches 1.0 and cease development of new language features. Following 1.0, the only specification changes will be clarifications and minor corrections. We won’t have the perfect language, and we’ll have to live with our oversights, but that’s okay: we’ll let the next language improve on our ideas. What we want is a language that we can rely on for as long as possible, and that requires a deep commitment to stability. 

Quoted from "Hare is a boring programming language"

The idea of anything software-related being "finished" is anathema to the modern computing mentality, but it shouldn't be. We'll finish the Gemini protocol once and for all, and then the clients and servers will asymptotically tend toward being finished once and for all as well as the bugs get discovered and squashed. An ever-increasing length of time between subsequent versions of a program ought to be considered a mark of quality and good design, and we look forward to being proud of good quality Gemini programs which are reliable and stable finished products. It will sure beat being strong-armed into restarting our browsers every week or two to install yet another apparently essential update to continue doing the same old thing.

4.4 Questions about text/gemini

4.4.1 Why doesn't text/gemini have support for inline links?

There are multiple reasons for this, but this design is primarily in service of the guiding principle of simplicity of implementation (see answer 4.2.4). Because text/gemini is an entirely new format defined specifically for Gemini, client authors will typically need to write their own code to parse and render the format from scratch, rather than being able to rely on a pre-existing, well-tested library. Therefore, it is important that text/gemini the format is extremely simple to handle correctly. A strictly line-based format where text lines and link lines are separate concepts achieves this. There is no need for clients to scan each line character-by-character, testing for the presence of some special syntax to detect a link. Even the simplest possible inline link syntax would introduce the possibility of malformed syntax, e.g, forgetting to close a tag before opening a new one, which clients would need to be robust against. It would likely also introduce various edge cases whose handling would either need to be explicitly specified (leading to a longer, more tedious spec which was less fun to read and harder to hold in your head), or left undefined (leading to inconsistent behaviour across different clients). A simple line-based format is much, much easier to work with.

Using a system of text lines and link lines isn't just easy to parse, though. It tends to result in very clean document layouts. It encourages including only the most important or relevant links, organising links into lists which group related links together, and allows you to give each link a maximally descriptive label without having to worry about whether or not that label fits naturally into the flow of your main text. It takes some getting used to, but it's worth it. Gopher menus exert the same influence, and the ease of navigating a Gopherhole is something that lots of Gopher users appreciate and which it was considered worthwhile carrying forward into Gemini. It's not an arbitrary limitation for the sake of toughness, it really bears fruit.

If you're a unix geek, you should appreciate how nice it is to work with a line-based markup format using standard command line tools! Given a group of text/gemini documents, you can extract the URLs from all the links in all the documents, remove the duplicates and then list them in order from most to least commonly linked to using just grep, awk, sort, and uniq. Think how much more involved this task would be with HTML documents!

4.4.2 Why doesn't text/gemini have support bold or italic text?

Basically for the same reason it doesn't support inline links (see question 4.4.1). It seems on the face of it like it would be a trivial extra little thing to add, but it would force a switch from line-by-line parsing of the format with a single bit of state ("am I in pre-formatted mode or not?") to character-by-character, or at least word-by-word, parsing of the format with three bits of state, introduce a bunch of edge cases and make it easy to accidentally mangle a document.

4.4.3 Why doesn't text/gemini support inline images?

This is a deliberate decision made in direct service of the guiding principle of user autonomy (see answer 4.2.2), specifically the idea that text/gemini documents should have no way to trigger additional network requests. Images are one particular case where this priciple also overlaps substantially with our guiding principle of user privacy (see answer 4.2.1). So-called "tracking-pixels" have been a standard tool of the internet's surveillance marketing complex for many years. These tiny, invisible images abuse the web's behaviour of automatically downloading image files from arbitrary third-party servers to effectively trick your computer into "pinging" surveillance servers, reporting your movements as you explore the web.

Gemini is in this regard no different to Gopher, and nobody in Gopherspace ever complains about it. On the contrary, just like Gopher users enjoy the quick, easy and transparent navigation of Gopherholes that results from a hierarchical menu system rather than inline links, Gopher users enjoy a strongly text-centric space for distraction-free reading without sensory overload caused by excessive gratuitous imagery, and for it's encouragement of substance over style (nothing could be more discouraging for advertisers). All of this was considered worth carrying forward into Gemini.

4.4.4 Why doesn't text/gemini have support for styling?

This is a deliberate decision made in direct service of the guiding principle of user autonomy (see answer 4.2.2).

Gemini takes the position that visual styling of Gemini content belongs under the sole and direct control of the reader, not the writer. Not everybody has the same taste in colours and fonts, and no single way of styling a page will be optimal for all readers, all devices and all lighting conditions. There's much more at stake here than the age old-divide in preference for dark text on a light background or vice versa. People with reading disabilities like dyslexia may benefit tremendously from using specially designed fonts, for example, and people with impaired vision may have difficulty reading text if the contrast between background and foreground is too low, no matter whether it's closer to dark mode or light mode. A "one size fits all" styling system where content looks the same everywhere is guaranteed to perform poorly for a lot of people. A complicated styling system like CSS which can specify different styling for different devices and contexts would not only violate the guiding principle of simplicity of implementation (see answer 4.2.4), it would burden every individual author with the task of making sure their capsule works well everywhere and for everyone. Experience from the web suggests that accessibility issues will typically be an afterthought at best. It's much simpler, and in fact much more liberating for content authors, to let content just be content, and leave styling to the user, who after all knows their own preferences and needs better than anybody else.

Defining something like a simplified CSS would also violate the principle that following a link in Geminispace should result in downloading a single file from a single server, known in advance, and that the functionality of any one downloaded file should be in no way influenced by refusing to download any other file (see answer 4.2.2 again).

It's a myth that without some equivalent of CSS Geminispace is doomed to be visually dull and uninteresting. There are graphical Gemini clients with high quality font rendering and beautiful typography. People who value those things can enjoy that reading experience absolutely everywhere in Geminispace, even when reading content written by authors who don't care about styling at all. Beautiful Gemini clients don't even necessarily have to make capsules look good but all the same, without any individual personality. Clients like GemiNaut and Lagrange use parts of the URL as a seed for random number generators that control subtle automatic variations in capsule styling. All the pages from the same capsule look the same, and pages from different capsules look slightly different. Over time, you subconsciously learn these cues so that your favourite capsules end up looking familiar and comforting, and you can tell when you've ended up somewhere new, or even get a vague sense of "Hey, haven't I been here once before?". This is actually cutting edge UI stuff, and the Gemini community can be rightly proud of it.

4.4.5 Why didn't you just use Markdown instead of defining text/gemini?

The text/gemini markup borrows heavily from Markdown for its syntax. There are lots of Markdown libraries for all major languages and platforms, just like there are TLS libraries, so on the face of it it would seem that adopting Markdown as the "native content type" of Gemini would not be incompatible with the guiding principle of simplicity of implementation (see answer 4.2.4). But actually there are multiple reasons not to do this.

For one, there are actually many subtly different and incompatible variants of Markdown in existence, so unlike TLS all the different libraries are not guaranteed to behave similarly. There is an obvious candidate for a clearly specified "standard Markdown" which could be been used, namely CommonMark. Everything said in the rest of this answer applies if "Markdown" is understood specifically to mean "CommonMark".

Markdown permits inline links, but Gemini deliberately eschews these in an attempt to replicate the clarity of layout and ease of navigation which Gopher has proven arises naturally from a "link lines" system (see question 4.4.1).

Markdown permits inline images, but Gemini deliberate eschews these both in the interests of user autonomy and user privacy and in an attempt to replicate the lack of distraction, focus on substance over style and lack of advertising which Gopher has proven arises naturally from a text-centric space (see question 4.4.3).

Finally, but perhaps most convincingly, Markdown is in fact fundamentally tied to the concept of HTML (and allows the inclusion of arbitrary raw HTML, so it's in no way a simple, clean subset of HTML even if it is most often used as one). All of those Markdown libraries available for all major languages and platforms which would supposedly make it easy to implement a Gemini client if Markdown were the protocol's native content type do not actually do anything for the client author beyond transforming a format which is relatively pleasant to view in raw form (Markdown) into a more complex format which definitely isn't (HTML). If you were writing a simple client for a unix terminal emulator and wanted to use ANSI escape codes to render headings as bold or underlined text, transforming Markdown to HTML using a library does not actually get you closer to this goal. All it would do is require you to then parse the HTML to detect <h1>, <h2> and <h3> elements to emit the ANSI codes. You'd be better off just trying to handle the raw Markdown yourself without using any libraries, and that's less straightforward than trying to handle raw text/gemini yourself.

Of course, it is possible to serve Markdown over Gemini. The inclusion of a text/markdown Media type in the response header will allow clients to unambiguously recognise it, and nothing prohibits a client author from supporting both text/gemini and text/markdown. In fact, some Gemini clients do support Markdown. In principle, nothing could stop Markdown supplanting text/gemini as the most common item type in Geminispace and clients which support Markdown being used much more widely than clients which don't. In actuality, after more than four years, Markdown is less commonly served via Gemini than JSON or HTML.

4.5 Questions about cryptography in Gemini

4.5.1 How can you say Gemini is simple if it uses TLS?

Some people are upset that the TLS requirement means they need to use a TLS library to write Gemini code, whereas e.g. Gopher allows them full control by writing everything from scratch themselves.

Of course, even a "from scratch" Gopher client actually depends crucially on thousands of lines of complicated code written by other people in order to provide a functioning IP stack, DNS resolver and filesystem. Using a TLS library to provide a trustworthy implementation of cryptography is little different.

Gemini also turns TLS client certificates - very rarely seen on the web - into a first-class citizen with in-band signalling of their requirement. This allows restricting access to Gemini resources to certain parties, or voluntarily establishing "sessions" with server-side applications, without having to pass around cookies, passwords, authentication tokens or anything else you may be used to. It's much closer to SSH's notion of "authorized keys" and is, in fact, a much simpler approach to user authentication.

4.5.2 Why don't you care about retrocomputing support?

Gopher is so simple that computers from the 80s or 90s can easily implement the protocol, and for some people this is one of the great virtues of Gopher. The TLS requirement of Gemini limits it to more modern machines.

Old machines are awesome, and keeping them running, online and useful for as long as possible is an awesome thing to do. But it also makes no sense for the vast majority of internet users to sacrifice any and all privacy protection to facilitate this. Remember, though, that Gemini does not aim to replace Gopher, so the retro-compatible internet is not directly endangered by it. In fact, people serving content via Gopher right now are strongly encouraged to start also serving that same content via Gemini simultaneously. Retrocomputing fans can continue to access the content via Gopher, while modern computer users who wish to can switch to Gemini and reap some benefits.

And, hey, it's not like Gemini is a strictly retro-no-go-zone. Your ZX Spectrum may not be able to handle TLS, but there is in fact a functioning Gemini client for the Commodore Amiga.

AmiGemini is a Gemini+Spartan+Gopher browser for the Commodore Amiga

In fact, you can use any Gopher-capable retrocomputer to access Geminispace if you run Cosmarmot on any Gemini-capable machine on the same network:

Cosmarmot, a proxy server that translates from gemini servers to gopher clients

4.5.3 Why use TLS for crypto instead of something more modern like the Noise protocol?

TLS is certainly not without its shortcomings, but:

    There are bindings to TLS libraries available for almost every programming language under the sun
    Many developers are already at least partially familiar with TLS and therefore don't need to learn anything new to implement Gemini
    Most users are already trusting TLS to secure their web browsing and email, and therefore don't need to decide whether or not they want to trust some unfamiliar technology to start using Gemini
    TLS is a deeply entrenched industry standard, whose definition and implementations will both continue to be scrutinised and improved by security experts for the foreseeable future, and that work will happen for reasons entirely unrelated to Gemini - it makes a lot of sense for a small project to "freeride" like this.

4.5.4 Why bother with crypto at all? Nobody is making credit card purchases on Gemini. It's all just public content.

The 90s called, they would like their attitudes toward encryption back!

If Gemini were a plaintext protocol like Gopher, it would be trivial for your ISP, or, when you are out and about using public WiFi networks to access the net, for whoever runs your favourite cafe or your local public library or some random airport or hotel to:

    Read everything that you read (and maybe sell that information)
    Censor anything you try to read
    Insert adverts into anything you read
    Insert malware into software you download

This is not paranoia. All of these things have actually happened in the past. Back when the web was mostly unencrypted, there were multiple cases of commercial ISPs accepting money from advertisers to insert adverts into other people's websites, without either the ISP's customers or the website author's consenting or even knowing it was happening. This really happened! Only cryptography prevents this kind of tampering being widespread today. Again, it's not paranoid to think network providers will do this, it's naive to think that they won't. Trusting the internet is for chumps.

If you're using a public WiFi network which is itself unencrypted, which is not uncommon, then the first ability above, to read everything that you read, would apply not only to the people running the hotspot, but to everybody else sitting in the same cafe. Even if you are only reading perfectly legal public information (like browsing a Gemini interface to Wikipedia), it's nobody's business but your own if you want to read about politics, or religion, or sexual health, or anything else. In a big, bustling, anonymous city, this might not be a big deal. In small towns, where opinions are narrow and rumours travel fast, it's not remotely unreasonable to be uncomfortable literally broadcasting your online reading habits.

It might seem crazy to worry about things like this when Gemini is such a small and obscure technology, but refusing to consider them dooms it in advance to remaining smaller and more obscure than it otherwise might become.

It's true that just requiring TLS is not a silver bullet that makes everything above impossible (e.g. the hostname of the servers you visit is currently still leaked via the SNI headers, and traffic analysis might help to narrow down which specific resources you are requesting), but it substantially raises the bar.

4.5.5 Okay, but why use TLS in a weird way, without Certificate Authorities?

The Certificate Authority system is by no means without shortcomings and failures with regard to security. By now these are quite widely documented and best practices for the web are moving toward layering additional mechanisms on top in attempt to mitigate these problems (CAA, DANE, HSTS, HPKP, etc). But actually, early objections in the Gemini community to embracing the Certificate Authority system for TLS were more ideological than security minded. Gemini's designers and early adopters came overwhelmingly from Gopherspace and public access unix systems, both places where the ideals of a non-commercial, decentralised and egalitarian internet are taken very seriously.

On the web, just six certificate authorities account for about 90% of all secured websites. With the exception of the non-profit Let's Encrypt (discussed below), the rest of these CAs are all large commercial companies operated for profit and headquartered in the United States; the CA system is one where "trust" is viewed as a commodity to be bought and sold. The next most common category of CA after for-profit companies are CAs which can be considered to be directly or indirectly owned and operated by national governments, including some governments with less than stellar human rights records.

Let's Encrypt make CA-signed TLS certificates available to anybody free of charge, which is a wonderful thing and has taken the commercial nature of the CA system out of the spotlight compared to earlier times, but Let's Encrypt is free to use, not free to run. It's operated by the Internet Security Research Group, who as a non-profit depend on donations to keep the ACME servers running. The Chrome project (by Google) are a Diamond sponsor, and Meta (owner of Facebook) are a Platinum sponsor. Google and Meta are surveillance companies, and the money they donate to support Let's Encrypt is acquired through precisely the kind of practices that a lot of people use Gemini in an attempt to escape from. This isn't meant as an attack on Let's Encrypt, and it'd be hypocritical if it were, as the web mirror of the Project Gemini capsule uses Let's Encrypt certificates. We're just pointing out that for people who really hate surveillance capitalism and dream of a decentralised and non-commercial internet, it's hard to get warm fuzzies about the CA system even from Let's Encrypt.

TOFU represents an entirely self-sufficient approach to certificate validation, which doesn't rely on any infrastructure beyond the client and server which are talking to each other, and has no additional costs to either party on top of that conversation.

4.5.6 But TOFU isn't secure!

Any statement that "X is secure" or "X is insecure" without a lot of additional context is necessarily a gross simplification. All of security is economics. Attacks have costs, risks and probabilities of success, and attackers stand to receive potential rewards. Defences have costs and probabilities of success of their own, and defenders stand to incur potential losses. All any security mechanism can do is push these interrelated factors around, to disincentivise attackers and reduce risks of defenders. Something is "secure" within the framework of a particular threat model when these factors are rationally assessed to be well balanced.

TOFU is weak against active attackers launching targeted MITM attacks against individual users' connections to particular hosts. In a context that involves rich people using the internet to do their banking or shopping, like the web, that's a fatal weakness. But the first-class application of Gemini is to allow people to explore a large electronic public library on their own terms. In that context, there's no incentive for active, targeted attacks. There are, however, incentives for cheap, automated bulk surveillance and opportunistic eavesdropping.

A grounded threat model for Gemini involves ISPs and public WiFi operators who sell information on their users' reading habits for their own profit (legal without consent in the US since 2017) or who are compelled by their government to report people reading certain things (like foreign news sources, pro-democracy texts, banned religious texts, information on reproductive rights, etc.), as well as random creeps who like to passively eavesdrop on unsecured WiFi traffic. TLS+TOFU is 100% effective against the latter. It's not perfect against the former, but in today's highly mobile computing environment it's better than you might think. You can visit a dozen capsules on your home internet connection, then take your laptop, tablet or phone to your favourite cafe and visit the same capsules on their free WiFi, and then repeat this at your local public library with their free WiFi, all on the same day, for the cost of a latte and a bus ticket. If any of those three internet connections are launching bulk MITM attacks on all TLS traffic, you'll soon know about it. Of course not every Geminaut will do this, and certainly not regularly, but it only takes one to do it and spread the word, with the ISP involved potentially incurring reputational damage and losing customers. Compared to a plaintext protocol like Gopher where bulk surveillance is undetectable and therefore plausibly deniable, TLS+TOFU raises the risk of practicing bulk surveillance, which acts to disincentivise it, and raises the awareness of it when it still happens.

Of course, nothing whatsoever prohibits very privacy conscious Geminauts from adding additional certificate validation layers on top of TOFU. There are already proof-of-concept implementations of using the Tor network to validate new certificates from multiple network perspectives. If DNSSEC ever takes off, DANE can add an additional layer too.

5. Contributing to the Gemini project

5.1 I like the sound of the Gemini project, how can I help?

5.1.1 Help fill Geminispace with content

Easily the most important contribution you can make to the success of Gemini is to add some content to Geminispace! The more interesting and exciting stuff people find in Geminispace, the more likely they are to want to keep using Gemini and eventually add content of their own. See question 2.5 above for details on how to get your content into Geminispace. A lot of people wish there was less computer related content in Geminispace. If you feel like you can add some more variety to the space, go for it!

If producing original written content isn't your thing but you'd still like to help populate Geminispace, you could find some Creative Commons or similarly permissively licensed content to rehost. Don't republish a bunch of stuff just because it's CC, though. Try to find something which you actually think is interesting or entertaining or otherwise worthwhile, and try to pick something which adapts well to Gemini's technical limitations. The Wikipedia list of major CC works may provide a helpful starting point for ideas:

Wikipedia's List of major Creative Commons licensed works

5.1.2 Offer Gemini hosting to people who can't self-host

If you have the necessary technical skills, you can make a major contribution to the growth of Geminispace by providing a hosting service which people can use to publish content. This can be as simple as setting up sftp-only user accounts on a VPS. Offering hosting doesn't necessarily need to be a big commitment. You can use the cheapest VPS services on offer to very comfortably host a dozen or so users. A large number of hosts each serving the content of a relatively small number of users is a much more robust and sustainable ecosystem than a small number of servers each hosting hundreds or thousands of users!

More specifically, you could set up a hosting service which explicitly aims to fill a particular niche, by hosting content on a particular subject, or content in a particular language, or content written by a particular group of people. With a catchy name and an integrated aggregator for hosted content, such a service could easily become a valuable community hub.

More hosting options for people without system administration skills would certainly be welcome. This might take form of more services like those listed in section 2.5.1 with easy interfaces. Or it might take the form of more traditional hosting technologies like (S)FTP or git but with high quality documentation aimed at helping people to learn these tools, coupled with a volunteer help community.

You don't necessarily need to provide something like a traditional hosting service where each user builds their own capsule from scratch. You could set up a capsule designed to host a particular kind of content, say reviews of video games, or films, or albums, or maybe recipes, or home improvement advice, or fun games you can play with a standard deck of cards, or whatever. In addition to possibly writing some of that content yourself, you tell Geminispace at large that people can email you submissions. If you get submissions and you think they're good, you upload them to the capsule, attributing the original author however they'd like to. You can impose your own standards, be they high or low, for originality and quality of the content. This still functions like hosting. It helps fill Geminispace with content, and requires no technical skills on behalf of contributors other than being able to send an email.

5.1.3 Help to organise Geminispace

Geminispace is constantly growing. It's decentralised, which is a good thing, but because of that it's disorganised, which isn't necessarily. There are search engines (see 2.2.3) and aggregators (see 2.2.1), but there is still plenty of room for improvement and innovation in making it easier for people to find content of interest.

In the earlier days of Geminispace there were some categorised directories (see 2.2.2). Usually these were projects run by a single person or small group, and attempted to organise the entirety of Geminispace. Unsurprisingly, that's very hard to keep up long term, and a lot of these directories have gone offline or stopped being updated.

There hasn't been much yet in the way of attempts by larger groups to maintain directories of specific subsets of Geminispace. This approach would result in a substantially lighter workload and might allow more fine-grained categorisation. Directories could include content at the level of individual pages, rather than entire capsules (which are very rarely exclusively dedicated to a single topic, anyway). If such directories provided subscribable pages or Atom feeds of newly added content, the content submitted to separate directories on distinct but somewhat similar or related topics could be aggregated into larger directories organised by higher level thematic concepts. Starting up some projects along these lines could be a worthwhile experiment.

5.1.4 Write some software

Gemini already has a surprising number of client and server implementations in existence. That's not to say more aren't welcome, and if this is something you'd really like to do, you should feel absolutely free! But if you really want to make a contribution that will help the project to grow and thrive, and you'd like to do it by writing code, writing tools, applications and platforms might be a better bet.

A powerful tool for expanding Geminispace could be a single piece of software which simultaneously provides a Gemini server and a way for multiple users to easily manage the content provided by said server, e.g. via an interactive web interface or by sending emails full of content; Something like the Gemlog Blue and Flounder services (see question 2.5.1 again), but packaged up and documented in such a way that it's easy for people to deploy and customise their own multiuser sites, much like e.g. a Mastodon instance.

5.2 How do I contribute to the official Gemini site and documentation?

All the documentation hosted at gemini.circumlunar.space, including the FAQ you're reading now, lives in a single git repository, which has read-only access open to the public. You can clone the repo as follows:

    git clone git://gemini.circumlunar.space/gemini-site 

Then, make your suggested changes to the relevant files (the structure of the URLs mirrors the structure of the repository exactly, so e.g. gemini://gemini.circumlunar.space/docs/faq.gmi lives at docs/faq.gmi in the repo). Commit your changes with meaningful commit messages (make sure to set your name and email address so people can see who did your work!), with one commit per conceptual change. You then have two options to send your work upstream.

If you have git's send-email command configured (see below for a link to a tutorial), you can email patches containing your commits to <solderpunk _at_ posteo _dot_ net> with a single command. Otherwise, you can simply run:

    git format-patch origin 

to create a set of patch files, which you can manually attach to an email using your ordinary mail client of choice.

A friendly tutorial on configuring git send-email

Please note that if you update the FAQ, it is sufficient to update only the faq.gmi file. The separate files for the individual FAQ sections can be automatically updated by Solderpunk using a script when your patch is merged.

5.3 I'd like to translate some Gemini documentation into my native language, how can I do that?

Thank you! Volunteering to translate documentation is a wonderful way to help the project.

To do so, first clone the git repository as described in question 4.2 above. Change into the `doc` directory of the repository, and create a new subdirectory with your language's two letter ISO 639-1 code, e.g. Finnish translations should live in `doc/fi/`, Japanese translations in `doc/jp/`, etc. You can find a complete list of codes at Wikipedia, linked below. If you are translating into a region-specific variant of a language, you can use RFC4646-style codes instead, e.g. pt-PT or pt-BR for the Portuguese as spoken in Portugal or Brazil, respectively.

List of language codes at Wikipedia

For each English file which lives in `doc` which you want to translate, create a corresponding file in your language's subdirectory. It's okay to change the file name as part of the translation, e.g. the German translation of `doc/specification.gmi` might be called `doc/spezifikation.gmi`. You can translate as many or as few of the files in `doc` as you have time and energy for. Don't be shy about submitting partial translations! Once somebody else who speaks your language sees your effort, they might provide some or all of the remaining work. Having some content translated is better than none.

Once you're done, copy across the `doc/index.gmi` file and modify it to match your translated filenames and document titles, and remove links for any of the original documents which you haven't translated yet.

Finally, update `doc/translations.gmi` to include a link to your new subdirectory.

Commit your translations to the repository and send Solderpunk the patch as described in question 4.2 above.

6. Gemini-adjacent technologies and cultures

6.1 What are the Titan, Spartan and Mercury protocols?

These are, in some sense, "spinoffs" from Gemini, created by people active in the Gemini community during the earliest stages of its development, who wanted to explore taking the protocol in a slightly different direction, or to add more capabilities. None of them are an official part of the Gemini project, but some Gemini clients also support some of these additional protocols, and some people are active in both communities.

6.1.2 Titan

Titan is an add-on for Gemini clients and servers, created by Alex Schroeder, to support uploading data. It was designed with the goal of making it possible to build wikis in Geminispace (and Alex has done precisely this!). Titan is named after Titan II GLV rockets used the Gemini spacecraft in the original Project Gemini. Learn more at the link below:

The Titan Specification

6.1.3 Spartan

Spartan is a protocol strongly inspired by Gemini but is substantially more, well, spartan! It was created by mozz (of Astrobotany fame!). If Gemini "sits between Gopher and the web", then perhaps it's fair to say Spartan sits between Gopher and Gemini. Like Gopher, there's no TLS or UTF-8, but like Gemini there are MIME types, virtual hosting, and some capacity for redirects. Then again, Spartan supports clients uploading to servers, so in some ways it goes beyond both Gopher and Gemini. The overarching goals of Spartan are to be simple, familiar, fun and inspiring!

Learn more at the official Spartan Gemini capsule

6.1.4 Mercury

Mercury was an entirely hypothetical alternative to Gemini, substantially simpler, with Solderpunk sketched out in a gemlog post purely to illustrate something which could exist in principle, not with the intent that anybody actually implement it, but for it to act as a "philosophical navigation aid", to help make sure the general consensus in the community was that Gemini was not becoming overly capable and overly complicated. Mercury was supposed to be something that Gemini could be mindfully steered either toward or away from. The majority preference at the time seemed to be "away from", and the idea was never really developed further. Despite Mercury not being "an actual thing" (there's no official gopherhole/capsule/website, no leader, etc.), some people have actually implemented in software nevertheless! You're a less likely to bump into references to Mercury in the wild than Titan or Spartan, but it could happen.

The original sketch of the Mercury protocol

6.2 What is the relationship between Project Gemini and Circumlunar Space?

Circumlunar Space is another project by Gemini project leader Solderpunk. It began a little more than a year before Gemini, as a simple free Gopherspace provider which quickly morphed into a public access unix system, which later expanded into an experimental "pubnix confederation" of multiple servers.

These days all the Circumlunar Space pubnix servers offer Gemini hosting in addition to Gopher hosting. However, the two projects are essentially unrelated and are handled entirely independently of one another. The fact that the official internet presence of Project Gemini is at a host within the circumlunar.space domain is mostly a historical accident. The host was setup quickly in the very early days of the project when it was not expected to grow to anything like its current size, and registering a separate domain for it did not seem warranted.

6.3 What is the "small internet"?

"The small internet", also affectionately known as the "smolnet", is an online counter-cultural movement which has a lot of currency in the Gemini community. The term has no official, precise definition and it is not always used consistently. Often it is used simply as a shorthand term to refer to Geminispace and Gopherspace together. More properly, it refers to internet technology that embraces at least some of:

    Simple technologies and simple tools
    Careful production of thoughtful content at a comfortable pace, rather than a frantic stream of reactive "takes"
    Small, human-scale communities rather than global public spaces
    Self hosting or community hosting, rather than corporate monopoly silos
    Reply posts and private email discussions, rather than low quality, low effort "social" interactions like "likes", "boosts" and comments
    Serendipitous discovery of interesting people and content through random exploration, rather than searching for what you know or think you want
    An effort to exorcise the internet of "FOMO"
    A healthier balance between online and offline time

Of course, the above is only a rough outline of a fuzzy concept without a precise meaning and not everybody will agree fully with every dot point above, but this should provide the gist of it.

As mentioned, the two common uses of the term are not entirely consistent; it's certainly possible to use web technologies to build spaces which abide very closely by the smolnet philosophy as sketched above, and it's possible to use Gemini to build spaces which fly in the face of it. But it's not a terrible conflation, either; the small internet philosophy is a nearly invisible minority stance on "the big internet", whereas it is fairly mainstream on Gemini and Gopher.

Nevertheless, the term itself and certainly the ideology behind it both predate Gemini. You don't necessarily need to embrace the "smol" philosophy to find Gemini useful or enjoyable, but if you spend a lot of time in Geminispace or talk to a lot of people about Gemini, you are very likely to bump into the term and find yourself talking to a lot of people for whom this philosophy is almost the entire appeal of the project and the community. It's part of the "local culture", if you like. Even if it's not entirely your thing, being aware of the basic idea and having an open-minded, respectful attitude toward it will go a long, long way toward making your interactions with the community smoother and making the protocol itself seem less like a straitjacket.

6.4 What is permacomputing?

The nascent Permacomputing movement seeks to apply ideas from permaculture to the subject of computing and society's relationship to them. A core concern is the environmental impact of computing, stemming from both the large and ever-growing energy demands of consumer computing devices and the datacenters and other internet infrastructure used to supply them with content, and the burgeoning piles of hazardous, recycling-resistant e-waste produced by non-repairable computing hardware with rapid, largely artificial, cycles of obsolescence.

The "permacomputing" label was coined about one year after the Gemini project was started, without any immediate connection or mutual awareness between the two. However, many Geminauts and other small internet enthusiasts (see 6.3) were very receptive to permacomputing ideas upon encountering them, and many in the permacomputing community have embraced the small internet.

Just like the small internet philosophy, you certainly don't need to embrace the permacomputing to find Gemini useful or enjoyable, but if you spend a lot of time in Geminispace you'll likely run into the concept, so it might help to have some awareness going in.

7. Responses and rebuttals to common criticisms of Gemini

7.1 I don't like Gemini and at all and I'd rather keep using the web, it's really not as bad as you make it out to be.

Have fun!

7.2 I agree that the web has serious shortcomings, but I think a new protocol like Gemini is entirely the wrong solution.

That's okay, we don't mind.

7.3 Really, Gemini doesn't even have feature X? Doesn't that make it totally useless?

Many people loudly dismiss Gemini as being so radically minimalist as to be useless, often a few minutes after first learning it exists and without making any good faith effort to actually use it. That's a shame.

It's true that Gemini isn't capable of doing everything the modern web can - that's kind of the point. But "less useful" is not the same thing as "useless" (and "less capable" isn't even necessarily the same thing as "less useful"). If a predominantly text-based internet that didn't spy on you all the time or actively try to distract you from what you want to be doing was genuinely useless, then the internet would never have taken off in the first place, because for years and years that's the only kind of internet there was. If Gemini were genuinely useless, it would go without saying that Gopher, which is a similar technology but which has even fewer features, would be even more useless. Instead, not only was Gopher successful in its day, it is probably enjoying more popularity today than it has at any other time this century. Clearly at least some people find it useful for at least some things. Maybe you are not one of them. That's okay! It doesn't mean you're a bad person. But it doesn't mean Gemini is a bad technology, either. The internet is plenty big enough for multiple protocols and for different people with different needs and priorities to use different tools for different purposes. Gemini has never claimed to be a "one size fits all" technology and doesn't aspire to be one.

If you are imagining that Gemini was designed by sitting down with a long list of all the features and capabilities of the modern web and asking one by one whether each should be kept or thrown out, and answering "thrown out" in 99% of cases, then certainly that seems heavy handed and extreme and you might wonder "gee, couldn't we have kept something like the best 25% or 10% of the web, instead of just the best 1%?". But that's not how it happened. The real process was much closer to starting with what's in Gopher and asking "what very small number of additional things can we add to make real, substantial improvements without causing too much collateral damage?". Most of the people asking this question had been using Gopher, mostly happily, for many years. Most of them missed things like URLs and UTF-8 a lot more than they missed, say, inline images. Nobody was really concerned by the prospect of Gemini ending up being too limited. After all, it was guaranteed to be *less* limited than their familiar point of reference! We were a lot more concerned about going too far.

Of course, most people discovering Gemini for the first time don't have this point of reference. Most of them have never heard of Gopher, let alone used it for years. If all you've ever known is the modern web or smartphone apps, then Gemini can certainly seem overwhelmingly spartan, and it might be hard to imagine giving up inline links, inline images, CSS, etc. Maybe in the end you won't want to give those things up, which is fine, but you'll never know for sure whether you can live without something if you don't at least try giving it up for a while. It doesn't cost you anything to try! Maybe you'll find it refreshing once you get past the initial awkwardness. A lot of people do, even people who go in doubting that they will.

At the end of the day, the simple truth is that the expressive power of a Gemini document is often entirely adequate to reproduce a great many newspaper columns or magazine articles, scientific journal articles, novels, biographies, interviews, poetry books, recipe books, diaries, etc. Nobody would claim with a straight face that those things are useless.

7.4 Gemini is so close to perfection, it just needs one more little thing...

There are a lot of people who totally "get" Gemini, who hate all the web misfeatures that it tries to free them from, who think it is totally worthwhile to sacrifice some functionality to attain and keep that freedom, and certainly don't think the result is too limited to be of real value. They just think that it's one teeny tiny extra feature short of absolute perfection, surely it's okay if we just add that one more little thing to the spec?

The problem is that each one of these people has a different idea of what the one missing piece of the puzzle is! And while one person thinks a particular feature is the last thing we need to add to create perfection, another person thinks that same feature is awful and would completely ruin Gemini forever. If one or two of these features were added, there would be no substantial net change in community satisfaction; if all of them were added, then everybody would find something to be upset about. Meanwhile, the spec would get longer and longer and clients would have to be updated again and again, all without an obvious payoff.

It would be different if one of these features would obviously solve a really important, concrete problem. But these sorts of requests have been coming in for years and years, and over those same years Geminispace has continued to grow and diversify and win adherents despite none of these "missing" features being added. This makes it hard to take seriously the notion that any of them is genuinely a fatal flaw.

It feels petty and mean to say "no" to polite requests for simple, reasonable seeming features from enthusiastic fans of the project over and over again. It really does. It's not fun. But a line has to be drawn somewhere, even if it's ultimately arbitrary, otherwise the expansion continues forever.

7.5 This whole thing reeks of amateurism!

That's because Gemini is an amateur project!

Not in the sense that it's low quality or that the people behind it aren't proud of it or trying to make it as good as they can. But the whole thing was launched in a small and obscure internet community, on the basis of enthusiasm and passion for niche ideas about what the internet can be, and powered by rough consensus and running code without the expectation that it would ever be adopted by people for whom the underlying values and assumptions weren't obvious and axiomatic. The level of interest and adoption has exceeded anybody's wildest expectations and everybody was caught by surprise. We tried our best to roll with it while staying true to the original spirit and vision. It wasn't easy!

But Gemini certainly isn't and certainly won't ever be the result of a small group of veteran internet engineers sitting down with an explicit list of design criteria and a precisely formulated objective function whose value was carefully maximised over a series of all day in-person meetings in front of whiteboards, resulting in a production grade protocol which can effortlessly handle all the needs of millions of users, while making verifiably mathematically optimal trade-offs between competing interests, maintaining all the while a sense of beautiful intellectual elegance.

It's not that we hate the idea of professionalism, but in 2019 the very notion that there might be anywhere near enough demand to justify an approach like the above to a technology that deliberately constrained its scope to exclude most of what people have come to expect from the internet would have seemed a laughable fantasy. A lot of people also would likely have felt that the protocol getting complicated enough that a process like the above would really pay off would have been a clear sign that it had become too complicated. People would have been quoting C. A. R. Hoare and Antoine de Saint-Exupér all day long.

If there's a group of people who really think Project Gemini had some great ideas or ambitions but really missed the mark, and that they can begin with a clean slate, aim a little higher and produce something clearly better, which will cure ten times as many woes for a hundred times as many people, then they are sincerely and genuinely welcome to give it a try, no hard feelings! But there's not much enthusiasm in the existing Gemini community for trying to disruptively change course at this point in time and make big changes to either the protocol or its management structure in the name of professionalism. We don't think what we have is perfect, by any means, but it is clearly working well enough to support a larger and more vibrant community than we ever hoped to attract. We'll continue to buff out the rough edges, but we're pretty content with our little amateur world.

7.6 There's nothing but tech talk amongst tech nerds in Geminispace

There's a degree of truth in this complaint, but the extent of the problem is generally overstated. There are in fact plenty of non-technical people in Geminispace writing about non-technical things. The perception that things are otherwise comes from the fact that many of the quickest and easiest ways to find large quantities of recent content in Geminispace reveals a skewed perspective. Lots of the biggest and most popular aggregators, for example, are big and popular because they've been around for a long time. That means they aggregate content from a lot of early adopters of Geminispace, and the early adopter demographics are, unsurprisingly, "skewed techy".

Aside from encouraging more people to write about non-tech subjects (and writing it yourself is more help than complaining!), the obvious solutions are for people to rely less on big public aggregators and curate their own reading experience by subscribing to the capsules of people who write about things they want to read about and don't write about things they don't. It also wouldn't be difficult for somebody to set up an aggregator which used some simple keyword detection in the titles of posts to filter out the vast majority of tech content.

7.7 Forcing people to install a Gemini client instead of letting them use their familiar web browser is too high a barrier to entry for non-technical users

This claim is very strange in two regards.

First, it seems to pre-suppose that web browsers are some kind of universal computer interface where all new technologies work by default unless their creators deliberately design them not to, but that's not true at all. Browsers are no different to any other piece of software. They can only speak the network protocols and open the file formats they are designed to speak and open. You can't use Chrome or Firefox to browse Geminispace for exactly the same reason you can't use Microsoft Excel to listen to MP3 files or use Adobe Photoshop to play Minecraft. They are tools for different jobs.

Of course, nothing at all would stop Chrome or Firefox from adding Gemini support. Until relatively recently it went without saying that web browsers also spoke FTP, and Firefox even spoke Gopher well into this century, so this would hardly be without precedent. But the ball is squarely in their court, not ours. Don't hold your breath...

Second, the idea that installing a specific piece of software to access a specific network is somehow beyond the average computer user's ability or comprehension is an odd one in the present day. The "poster child" non-technical user in 202x accesses the internet almost exclusively via a smartphone and/or a tablet. That's an approach to computing which is entirely dominated by the idea of installing single purpose applications for each thing you want to do. If you want to use Twitter on your phone, you install the Twitter app. If you want to use Skype on your phone, you install the Skype app. Well, if you want to use Gemini on your phone, you need to install a Gemini app. It's hard to see that as an insurmountable barrier.

7.8 It's too hard to publish stuff in Geminispace

There are more than a few providers of Geminispace hosting where the publication experience almost exactly mirrors that of publishing a website in the 90s or early 00s; you create your files on your own computer with the text editor of your choice and then use (S)FTP to upload them to a server using some account credentials. While the early web is by no means some kind of gold standard of ease of use and accessibility, it's also an empirical fact that an awful lot of people did, in fact, figure it out. Not just hardcore geeks, either. Geocities was definitely not filled exclusively with sites put up by professional programmers and system administrators who just used their sites to talk about the nitty gritty technical details of how they made their sites. That's quite a modern affliction.

Publishing to the web got easier over time as more and more people got interested in doing it. Programs like Microsoft FrontPage and Netscape Composer helped people create HTML files in a WYSIWYG manner, and programs like FileZilla helped people upload those files. None of these programs existed when HTTP or HTML were first specified, and these programs were not written by the people involved in specifying HTTP or HTML. They appeared only years later, once there was sufficient demand from enough people who wanted them. The fact that similar tools for Gemini haven't existed since the very beginning of the project cannot be taken to mean that they can't or won't exist.

Gemini is still a pretty young project in the grand scheme of things. The current ecosystem does assume an above average level of computer literacy, but that's a natural consequence of the fact that a lot of the current userbase discovered the project when it went viral on networks populated by computer geeks. But the userbase is still expanding and is still diversifying in this regard, and that diversification is being fuelled in part by some of the attempts which Geminauts have already made to make posting easier (see 2.5.1). That diversification will increase demand for easier tooling. This feedback process is still ongoing and it's grossly premature to assume that Gemini has reached anything like its peak ease of use. On the contrary, we've only just lightly scratched the surface of possibilities. It's true that Gemini's lack of anything resembling a POST request means it will never get to the point of being able to offer a user experience like, say, Wordpress. But that doesn't necessarily mean usability will peak somewhere too difficult for most people who want to publish in Geminispace to be able to that.

7.9 Why not just use a subset of HTTP and HTML?

Many people are confused as to why it's worth creating a new protocol to address perceived problems with optional, non-essential features of the web. Just because websites *can* track users and run CPU-hogging Javsacript and pull in useless multi-megabyte header images or even larger autoplaying videos, doesn't mean they *have* to. Why not just build non-evil websites using the existing technology?

Of course, this is possible. "The Gemini experience" is roughly equivalent to HTTP where the only request method is "GET", the only request header is "Host" and the only response header is "Content-type", plus HTML where the only tags are <p>, <pre>, <a>, <h1> through <h3>, <ul> and <li> and <blockquote> - and the https://gemini.circumlunar.space website offers pretty much exactly this experience. Clearly we know that it can be done.

The problem is that deciding upon a strictly limited subset of HTTP and HTML, slapping a label on it and calling it a day would do almost nothing to create a clearly demarcated space where people can go to consume *only* that kind of content in *only* that kind of way. It's impossible to know in advance whether what's on the other side of a https:// URL will be within the subset or outside it. It's very tedious to verify that a website claiming to use only the subset actually does, as many of the features we want to avoid are invisible (but not harmless!) to the user. It's difficult or even impossible to deactivate support for all the unwanted features in mainstream browsers, so if somebody breaks the rules you'll pay the consequences. Writing a dumbed down web browser which gracefully ignores all the unwanted features is much harder than writing a Gemini client from scratch. Even if you did it, you'd have a very difficult time discovering the minuscule fraction of websites it could render.

Alternative, simple-by-design protocols like Gopher and Gemini create alternative, simple-by-design spaces with obvious boundaries and hard restrictions. You know for sure when you enter Geminispace, and you can know for sure and in advance when following a certain link will cause you leave it. While you're there, you know for sure and in advance that everybody else there is playing by the same rules. You can relax and get on with your browsing, and follow links to sites you've never heard of before, which just popped up yesterday, and be confident that they won't try to track you or serve you garbage because they *can't*. You can do all this with a client you wrote yourself, so you *know* you can trust it. It's a very different, much more liberating and much more empowering experience than trying to carve out a tiny, invisible sub-sub-sub-sub-space of the web. It's like riding a bike through a park instead driving a tank through a minefield. You should try it!

7.10 Why bother at all, it's a waste of time, you'll be lucky if even 1% of the public ever wants to use it.

We would indeed be phenomenally lucky! We do not realistically expect to achieve even 1% adoption. We persevere nevertheless. This really shouldn't be surprising, or confusing, or seem pathetic. "Success at any cost" is a terrible way to run just about any project, but especially one which is supposed to *mean* something. Life is absolutely full of things which some people find useful, or interesting, or rewarding, or uplifting, or just plain fun, which most other people don't see the appeal of. Chances are good that you or somebody you care about really enjoys one or more of these things! Would you tell a birdwatcher they are wasting their time because their neighbours and co-workers are never going to get excited about birds? Would you belittle somebody for writing a pen-and-paper letter to their friend instead of having a video call, just because it makes them both happy?

Because Gemini is still best known and most widely discussed within computer geek circles, chances are excellent that many of the people levelling this criticism at Gemini have at some point in their own past really enjoyed installing an obscure operating system or learning an unusual programming language that the vast majority of their computer using peers wouldn't see the appeal of. Small, opinionated technical projects that go against the grain of mainstream computing are not at all new, or unusual, or bad. Many of them have persisted for decades, perpetuating loyal, enthusiastic userbases despite never becoming household names or making their founders rich and famous.

Normally other geeks feel kind of warm and fuzzy about these projects, especially the ones perceived to be "fighting the good fight", even if they don't actually use them much themselves. Nobody tells the passionate volunteers behind them to give up and stop wasting their time, cut their hair, install Windows and learn how to write scalable, agile Node.js apps for the Real Enterprise World, not in polite company at least. That'd be crass, and would get you downvoted, or whatever, by the wise geeks who know well that computers have utility and value beyond their vulgar commercial applications.

Apparently this well-established norm doesn't apply, though, when the weird, quixotic geeks have sufficiently crazy and outlandish ideas. You know, truly bizarre notions, like that the highly successful five thousand year old technologies of reading and writing actually constitute a minimum viable product in and of themselves; that software monopolies are bad, that surveillance capitalism and attention economics are even worse, and it makes all the sense in the world to just stop using the monopoly technologies that enable them for any tasks which can be successfully completed using technologies that don't, and to build those technologies ourselves; or that internet users should actually have a degree of autonomy in deciding what kind of content they consume, when and how, rather than being forced to just hand totally unfettered access to their eyes and ears over to an unbounded number of unknown-in-advance random third parties every single time they click on a link. Those people clearly ought to be ridiculed.
Contenido proxy de gemini://gemini.circumlunar.space/docs/faq.gmi
