# [Let's Just Wander!](https://letsjustwander.now.sh)

A blog to jot down wanderlusting thoughts with a heck of a mindset.
Built using the [Eleventy](https://github.com/11ty/11ty.io) static site generator.

## Directory structure ([Jekyll inspired](https://jekyllrb.com/docs/structure/))

    letsjustwander/
    ├── _posts/ (contains individual blog posts written in markdown)
    │   ├── *.md (the stuff bloggers need to write!)
    ├── _site/ (hidden in git, contains static pre-generated html files)
    │   ├── name-of-a-post
    │   │   ├── index.html (pre-generated blog post)
    │   ├──index.html (pre-generated main page)
    ├──README.md (the markdown file you're reading now)
    └──index.md (the markdown file that will become the front page of the blog)


# Getting Started

How to replicate a static blog like this for the technical minded!

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
    now ls
    # Point the `https://site-<abcdefgh>.now.sh` instance to `https://letsjustwander.now.sh`
    now alias site-<abcdefgh>.now.sh letsjustwander.now.sh

## Cleanup old Zeit instances
    now ls
    now rm _site
