---
date: 2018-11-06T15:23:00+13:00
title: On your markdown, hypertext, now!
subtitle: How to make a free disaster proof static blog for 2018 and beyond
---

I'll [start with the why](/developing-behaviours-by-starting-with-why).

```gherkin
    # language: en
    Feature: Free and minimal static blog
      In order to have a long-lasting blog
      As a blogger,
      I want a system that is portable

      Scenario: Blog host goes down
        Given a backup copy of my blog's content
         When my old blog host becomes unviable
         Then I can rehost my blog and content somewhere else
```

Bit of background, I've been blogging on and off since I was a teenager maybe 10 odd years ago.
As a kid, spending money on hosting and domain names was something I avoided like the plague, and keeping things *free* is still something I'm obsessed with.

A problem I faced was keeping my blog content safe from blogging platforms going down, becoming obsolete, or getting sucked in to very corporate locked-in platforms.
I have only a faint idea on where my first [Windows Live Spaces](https://en.m.wikipedia.org/wiki/Windows_Live_Spaces) posts are, stored in some proprietary format I may never unlock.
The backups from my golden [b2evolution](https://en.m.wikipedia.org/wiki/B2evolution) years (late 2000s to early 2010s) are likewise stuck in some mysql database which is marginally 'better'.

Around 2014 after graduating from my degree (while travelling in Chile actually) I restarted blogging using [Ghost](https://en.m.wikipedia.org/wiki/Ghost_(blogging_platform)), the beta version.
It was a bridge connecting me from the old school PHP based Content Management Systems I've used before to something akin to 'modern' JAMstack.

But when Ghost 1.0 got released, I didn't bother migrating to the new API.
Technically the posts were stored in JSON and I *could* parse it if I wanted to.
Read: still a lot of effort to go on a trip down memory lane.

Really, it all seemed too much to maintain.
Yes I *could* pay, and have someone manage the hosting, upgrades, backup and whatnot.

But stubborn ol' me thought the world must have gotten better than that.
It's 2018 already for goodness sake!
Was it too much just to have a few kilobytes or megabytes in the cloud to host some blog?

## **Nuclear disaster proof blog**

Ok, I'm probably exaggerating.
If you've read this far, you're probably hoping I've got a solution.

I'm not a web developer, but I do program and can follow instructions.
The blogging workflow below will not be Wordpress WYSISYG friendly, nor is it reliant on some passing Javascript framework that may or may not exist in the next 5 years.

Because I'm paranoid, there should be **two** and at least **two** ways to do any part of the pipeline below.

![Writing text, Text to hypertext, Publishing](https://yuml.me/diagram/scruffy/class/[Writing-text]->[Text-to-hypertext],[Text-to-hypertext]->[Publishing])

So what do we use?

## Static plaintext

One word - plain-text.

I'm not chucking my words into some database no matter how open source it is.
Nor am I going to put it into JSON, YAML, or some other FOUR letter acronym format.

Each post should **standalone** as one file.
As a minimum, the blog folder will have an index page and a folder for all the individual posts.

- \_posts/
  - hello-world.md
  - post-two.md
- index.md

I write my posts in [markdown](https://en.wikipedia.org/wiki/Markdown) and although there's a hundred flavours out there, I can probably still open up a .md file in ten years and read it.
If I had written my posts ten years ago in markdown, I would still be able to read it.
Period.
You could use some other markup language (LaTeX anyone?) if you fancy, but I highly recommend markdown.

To store all the metadata of a post (e.g. date, title, tags, etc), I put it into a short YAML frontmatter like so:

```yaml
---
date: 2018-10-31T12:00:00+12:00
title: Hello World
---
```

This follows the [Jekyll frontmatter](https://jekyllrb.com/docs/front-matter/) convention.
But we won't be using Jekyll (gasp!), though it *is* a popular static site generator.
I feel like there's too much boilerplate, [too many folders](https://jekyllrb.com/docs/structure/) for css files, plugins and whatnot.

The same can be said of most other [static site generators](https://www.staticgen.com/).
Everyone has an opinion on what's better, faster, trendier.
Popularity means nothing if we're going for longevity, remember Geocities?
Instead, we're going for something opinionatedly unopinionated.

## Text to Hypertext

The only reason we need this text-to-hypertext step is so that your blog doesn't look like some git repository.
Or, yes you could upload all your files to an FTP site and call it a day.
If that's you, skip down to the publishing/hosting part below.

Today, we're striving for minimalism, but we're not compromising on quality!

I'll jump straight to the chase and recommend no nonsense [Eleventy](https://github.com/11ty/eleventy).
Alternatively, skip ahead for Plan B - pure scripting!

### Plan A - Using Eleventy

[Install eleventy](https://www.11ty.io/docs/getting-started/) with npm in your terminal as follows:

```bash
    npm install -g @11ty/eleventy
```

Now go to the top-level directory of the blog and type this:

```bash
    eleventy
```

Eleventy will process your .md markdown files into .html, by default into a \_site folder.
Our folder should now look like:

- \_posts/
  - hello-world.md
  - post-two.md
- \_site/
  - hello-world/index.html
  - post-two/index.html
  - index.html
- index.md

And that's all there is, seriously!
Okay maybe [read the docs](https://www.11ty.io/docs/) or add some [plugins](https://www.11ty.io/docs/plugins/) if you want more configuration jazz.
Otherwise, take your `_site` folder host it somewhere (see next section).

### Plan B - Using pandoc

Credits to [@gypsydave5](https://dev.to/gypsydave5/write-and-deploy-a-super-fast-web-site-in-30-seconds-with-no-framework-4lab) for coming up with this!

If you haven't got swiss-army knife pandoc, [install it](https://pandoc.org/installing).

```bash
    sudo apt-get install pandoc #linux
    brew install pandoc         #mac
    choco install pandoc        #windows
```

I'm using Linux as my system, so next I would fire up my bash shell and type in this command:

```bash
    for POST in _posts/*.md; do pandoc --to=html5 --output=_site/$(basename ${POST%.md}).html --standalone $POST; done
```

This is basically a for-loop that converts every `.md` markdown file in the `_posts` folder to a standalone `.html` file.

The caveat with this method compared to (a properly configured) eleventy is that it **will** look horrible.
There's no CSS styling, so you'll get something that's akin to a 90s era webpage.

Luckily pandoc does allow you to set a [`--css`](https://pandoc.org/MANUAL.html#options-affecting-specific-writers) file or url to make it prettier (credits to [Martin](https://devilgate.org/blog/2012/07/02/tip-using-pandoc-to-create-truly-standalone-html-files/)).
You could point to some `pretty.css` file you made, or cheat like me below and chuck in a CDN hosted css.

```bash
    for POST in _posts/*.md; do pandoc --to=html5 --css https://cdn.rawgit.com/yegor256/tacit/gh-pages/tacit-css-1.3.1.min.css --output=_site/$(basename ${POST%.md}).html --standalone $POST; done
```

I used [tacit css](https://github.com/yegor256/tacit) above, which is a class-less CSS framework.
That means I'm not bothering with opinionated class names that goes with using some front-end framework like Bootstrap or newer players out there.
Simply write proper HTML5 (whatever proper means) and it will do the trick, at least until HTML6 comes out.

You might need to tweak this `pandoc` method further to get it to look as nice as `eleventy`.
There's probably a million ways to do this step so I'll leave that to your imagination.
Share it in a comment if you have another one-liner script that does it!

Now, let's jump straight into the scary part - publishing.

## Publishing/Hosting

So you've written your blog post (in markdown), you've converted it into nice hypertext (html), now it's time to put it up somewhere!
Again, I'm aiming for free.
That doesn't mean it can't be easy.

So far I've been through more dodgy free hosting providers than I can count.
What I dislike is a free lunch that I'll get a stomachache from later.

I'm of the opinion that publishing in itself is a scary thing, especially for new writers.
But the last thing you want is to have a blog post written up and having it stuck on your computer staring back at you an only you.
The word deserves your opinion, trust me.

You need to push it out into the world with a click of your fingers!
While you stress out on what the world will think of your post, do you really want to think about how hosting/ssl-certs/domain-names/database-configurations works?
No!

But hey, we're using static files now (<1MB in size), not some behemoth database!
No database means no funky configuration.
With static files, shouldn't there simply be a way to upload my files and get a URL link?

It's 2018, what do we have out there?

I'm going to show you the [Zeit Now](https://zeit.co/now) way for its Zen-like simplicity.
Alternatively, skip ahead for Plan B - P2P hosting!

### Plan A - Zeit Now

[Install now-cli](https://zeit.co/download#now-cli) with npm in your terminal as follows:

```bash
    npm install -g now
```

Now go to the top-level directory of the blog and type this:

```bash
    now _site
```

Type 'y' for yes to confirm.
It should take a second or three depending on how big your files are, and you'll be given a url to your blog!
Something that looks like `https://site-abcdefghij.now.sh`

Of course, you might like a nicer url, in which case you can set up an [alias](https://zeit.co/docs/features/aliases) like so:

```
    now alias https://site-abcdefghij.now.sh https://example.now.sh
```

And that's easy static hosting on Zeit Now in a nutshell.
You can even alias it to your own [custom domain](https://zeit.co/docs/features/aliases#custom-domains) if you've got the cash.
I'll also give a shout out to [Netlify Drop](https://app.netlify.com/drop) as an alternative hosting provider, just zip up your `_site` folder and  drag-and-drop it to the website!

Congrats, you've made it!
Read on though if you'd like to know another way ;)

### Plan B - P2P Dat

Credits to [this guide](https://beakerbrowser.com/docs/guides/publish-a-peer-to-peer-website).

[Install dat](https://github.com/datproject/dat) with npm in your terminal as follows:

```bash
    npm install -g dat
```

Now go to the top-level directory of the blog and type this to share the files in your `_site` folder:

```bash
    dat _site
```

It should take a second or three depending on how big your files are, and you'll be given a url to your blog!
Something that looks like `dat://abcdefghijklmnopqrstuvwxyz1234567890abcdefghijklmnopqrstuvwxyz12`.

Wait, what's `dat://`?
That's the P2P protocol part, you need a special browser like [BeakerBrowser](https://beakerbrowser.com) to open it.
That may be okay for you, or you might prefer a standard `https://` url.

Enter [hashbase](https://hashbase.io).
Hashbase wraps around your dat and gives a nicer url like `https://example.hashbase.io`.
For example, you can also access the Beaker Browser website at [https://beakerbrowser-com.hashbase.io](https://beakerbrowser-com.hashbase.io).

Hashbase acts as a super peer that hosts your files so you don't have to leave your computer switched on...
So sign up for it, or be a host yourself by forking their [Github repo](https://github.com/beakerbrowser/hashbase).

I've always wanted to go the self-hosting route, and this is probably the closest I've gotten so far.
Maybe *someday* I'll get a raspberry pi mini-server set up, but this will do for now.

## Caveat lector

I can't predict what will happen to the future.
Like I've mentioned in the beginning, I've blogged on and off for ten years or so.
What seems like a good idea back then isn't quite so now.
There is an element of hindsight bias in this post you need to be aware of.

This $0 plain text -> hypertext converter -> publishing/hosting pipeline assumes the following:

1. That plain text editors will continue to exist (and can open my markdown files).
Maybe UTF-8 won't be valid anymore?
Perhaps my favourite Atom editor will become obsolete?!!

2. That I'll be able to convert markdown to html in the future.
Will Eleventy still work in ten years time?
What will I do if pandoc goes away too?!!

3. That the hosting services I use and recommend now will remain free.
What if Zeit Now/Github Pages/Netlify/Hashbase starts charging for use?
Can the dat protocol actually continue into the future?!!

The enlightened ones may notice a potential Plan C baked into each step.
Can't I edit plain text with any editor?
Why, isn't it possible to convert markdown to html with some Python scripting?
Surely there will be another hosting provider that will do it for free?

Let me point out though, that the weakest link in the picture might be yourself.

> You are version controlling your blog posts right?

Git is awesome, I didn't mention it in the guide above but it's there in the background, silently making sure my history is intact.

There are also little details I left out from this guide such as navigation links, making an archive page, etc.
So for good measure, all my static blog templates are hosted on Github [here](https://github.com/weiji14/letsjustwander).
It is as ridiculously barebones as I can make it, and you're free to copy or build off the design.

Sure, there are definitely cons with using this free static blog system.
Some people don't think second level domain names are professional (but I can live with that).
It also takes some extra effort to get interactive stuff on the page like video embeds.

But hey, there's no javascript being served!
That means there's no popup ads (can be a good or bad thing).
My site also loads [blazingly fast](https://testmysite.io/5be0e11dfdd72a0d10c43e7a/letsjustwander.now.sh) in milliseconds.

The thing that bugs me most is having all my hard work disappear from the web in a few months or years, and having to migrate to somewhere else, usually during some inconvenient time.
This portable design aims to make that eventual migration as painless as possible.

For now, this is probably the best I can come up with.

```bash
    echo 'Hello World' > index.md  #write
    eleventy                       #convert
    now _site                      #publish
```

And there you have it, a free static blog guide for 2018 and beyond.
