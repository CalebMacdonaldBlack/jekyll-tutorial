---
layout: post
title: Step 1
description: Getting Started
show_tile: true
---

Getting started with Jekyll is super simple. In this step we're going to get the required tools configured and create the default Jekyll site. From here we'll get this serving from our computer and then admire our new site from a browser.

## Prerequisites

Jekyll requires your system to have a few tools to get started with building your first Jekyll website.

### Ruby

The core Jekyll functionality uses Ruby to build your website. **You'll need Ruby 2.2.5 or higher installed to use Jekyll.** You can check if Ruby is installed, or if your Ruby version is compatible by running the following on a command line:
```
ruby -v
```

Find information on installing or updating your Ruby installation on the [official Ruby website](https://www.ruby-lang.org/en/documentation/installation). Windows users are recommended to install using the RubyInstaller distribution.

### Bundler

Bundler is a convenient tool for installing sets of Ruby modules and packages, called 'Gems'. Bundler will prevent you having to individually install many dependencies and can be installed using the Ruby Gem installer once Ruby is installed on your system.

You can easily install bundler by running this from your command line:
```
gem install bundler
```

## Installing Jekyll

Jekyll has a command line utility containing all the tools you'll need to get a basic Jekyll site setup and running. We're going to install that tool using the `gem` utility by running the following on the command line:

```
gem install jekyll
```

## Starting our first Jekyll site

Now our command line utility is installed we can generate a simple Jekyll website with some default content using this tool.

Using your command line navigate to an appropriate directory and run the following command to create a new folder called `myfirstsite` containing our new Jekyll site.

```
jekyll new myfirstsite
```

Lets jump into the directory this has created so we can start working with our new website.

```
cd myfirstsite
```

## Lets see it in action!

We'll take a look around the content this command has generated in a second, but for the moment lets just test everything works.

We can now use the Jekyll command line utility to build and serve our website from our computer.

```
jekyll serve
```

This command will take a few seconds to generate your website and setup a temporary webserver on your computer so you can preview it. By default this will be a sample website that Jekyll has configured for us. But its important to check that everything is working at this point before we proceed.

The command will output something like this:

```
Configuration file: /Users/tjd/src/myfirstsite/_config.yml
Configuration file: /Users/tjd/src/myfirstsite/_config.yml
            Source: /Users/tjd/src/myfirstsite
       Destination: /Users/tjd/src/myfirstsite/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.393 seconds.
 Auto-regeneration: enabled for '/Users/tjd/src/myfirstsite'
Configuration file: /Users/tjd/src/myfirstsite/_config.yml
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
  ```

Most of this we won't care about for the moment, instead, simply note the *Server address* field. This shows us that our server is running on 127.0.0.1:4000 (our local address, on port 4000).

Copy and paste this URL into your browser, or click [this link](http://127.0.0.1:4000) to open your new website in your browser.

## Our new website

We can now explore our new website. It has a simple home page, an about page and a blog post. We'll look at how these are generated in the next step!

![Our sample website](/assets/images/step1/website-preview.png)
