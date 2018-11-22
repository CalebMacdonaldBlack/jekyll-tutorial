---
layout: post
title: Step 2
description: A quick tour of Jekyll
show_tile: true
permalink: step2
---

Next we're going to take a quick tour of the files Jekyll has generated for us, and how that is represented in the website.

## Overview

If you open the directory you created in the last step in your file browser you should see a file structure similar to this:

```
├── Gemfile
├── Gemfile.lock
├── _config.yml
├── _posts
│   └── 2018-11-17-welcome-to-jekyll.markdown
├── _site
│   ├── about
│   │   └── index.html
│   ├── assets
│   │   └── main.css
│   ├── feed.xml
│   ├── index.html
│   └── jekyll
│       └── update
│           └── 2018
│               └── 11
│                   └── 17
│                       └── welcome-to-jekyll.html
├── about.md
└── index.md
```

Lets start exploring this structure. Open your favourite IDE or text editor and open each of the following files as we step through them.

## Gemfile, Gemfile.lock

These files store information about the Ruby dependencies Jekyll needs. You can modify these if you have special requirements that require extra Jekyll components, but for the most part you don't need to touch these files. Just ensure they are always stored with the project.

## _config.yml

`_config.yml` is our Jekyll configuration file. This contains global settings for configuring our Jekyll site and can also be used to store configuration options for optional plugins and custom themes.

## _posts

The `_posts` folder contains all of our blog posts or other journalled content. You'll note that the filenames in this folder all contain dates. This is used to assist in ordering and locating the correct article. We'll take a deeper dive into how these posts work towards the end of this workshop.

## _site

When we run commands that generate our site (like `jekyll serve`) a copy of our site in static HTML and CSS is generated into the `_site` directory. You shouldn't edit this directory, as any changes you make will be lost the next time the project is built. For this reason you also don't need to store this directory as it can be generated at any time. However, the contents of this directory are what you will want to upload to a hosting service if you choose to host your site on the internet.

You may notice the structure of this replicates many of the names and structures of the parent Jekyll project in unusual ways. This is done to provide a cleaner directory structure for the user's browser. If you're not familiar with HTML and CSS the files in this folder may look like nonsense, but this is how webpages are presented to browsers on the internet, and your browser will understand whatever Jekyll generates for you.

## about.md

`about.md` houses the content for the *About* page (http://127.0.0.1:4000/about). It is a good example of a typical page of content in a Jekyll site. We'll look at it in the next step.

## index.md

`index.md` generates the basic homepage. This has been left deliberately empty in our installation except for a few lines at the top. We'll explain what these lines do, and why this file is empty later.
