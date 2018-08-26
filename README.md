# [Let's Just Wander!](https://letsjustwander.now.sh)

[![P2P Blog](https://dat-badge.glitch.me/letsjustwander.hashbase.io/badge.svg)](https://letsjustwander.hashbase.io)

A blog to jot down wanderlusting thoughts with a heck of a mindset.
Built using the [Eleventy](https://github.com/11ty/11ty.io) static site generator.

## Directory structure ([Jekyll inspired](https://jekyllrb.com/docs/structure/))

```
    letsjustwander/
    ├── _includes/ (contains reusable stuff like templates)
    │   ├── base.njk (the base layout for the blog)
    ├── _posts/ (contains individual blog posts written in markdown)
    │   ├── *.md (the stuff bloggers need to write!)
    │   ├── _posts.json (standard yaml front matter headers for all posts)
    ├── _site/ (hidden in git, contains static pre-generated html files)
    │   ├── name-of-a-post
    │   │   ├── index.html (pre-generated blog post)
    │   ├──index.html (pre-generated main page)
    │   ├──about.html (pre-generated about page)
    ├── .<something>ignore (files ignored by a particular piece of software)
    ├──README.md (the markdown file you're reading now)
    ├──about.md (the markdown file that will become the about page)
    ├──dat.json (useful for people wanting to share this repo via p2p dat protocol)
    └──index.md (the markdown file that will become the front page of the blog)
```

# Getting Started

How to replicate a static blog like this for the technical minded!
Also, optional steps for those wanting to go the p2p way.

## Install [11ty](https://www.11ty.io/docs/getting-started) static site generator and [Zeit Now](https://github.com/zeit/now-cli) for static hosting
    npm install -g @11ty/eleventy
    npm install -g now

## Build html files with eleventy
    # Change directory into the blog folder
    cd letsjustwander
    # Use eleventy to build from `.` directory to `_site`
    eleventy

## Deploy into the web with Zeit Now
    # Deploy static html files in the `_site` folder
    now _site
    # Cleanup old Zeit instances (if any)
    now ls
    now rm _site
    # Point the `https://site-<abcdefgh>.now.sh` instance to `https://letsjustwander.now.sh`
    now alias site-<abcdefgh>.now.sh letsjustwander.now.sh

## (Optional) Deploy into the p2p world with Dat/Beaker Browser

Inspired by [this](https://pipette-dev-blog-jimpick.hashbase.io/post/introducing-pipette/).
Note that this may require some expertise to work, rough guidelines below.

    # Use either dat-cli or beaker browser

    # Publish using [dat](https://docs.datproject.org/publish) (**hard**)
    npm install -g dat
    cd letsjustwander
    dat create
    dat share

    # [Publish using beaker-browser](https://beakerbrowser.com/docs/tutorials/create-a-blog.html) (**easy**, but not recommended)
    # Download browser from https://beakerbrowser.com/install/ and install
    # Open browser, open new tab, click on 'New +', and then 'Import from folder'

The result should be a `dat://...` url that links to your files, accessible using dat/beakerbrowser.
If you're good, you should have a `dat.json` file in the folder, otherwise just modify the one in this repo.

Note that you'll need to keep your computer running to sync the files with the dat world.
Alternatively, use [hashbase](https://hashbase.io/) to host your files for you with a pretty url like `yourwebsite.hashbase.io`
