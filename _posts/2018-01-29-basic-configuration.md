---
layout: post
title: Step 3
description: Basic configuration
show_tile: true
permalink: step3
---

The `_config.yml' file we found in our root is very important to how Jekyll generates our website. When our site is generated all the settings for this are read from here. There are many things you can configure in this file including the theme (by default a theme was added during our default setup), special custom options required by plugins or modules and advanced technical options.

This file is configured in a [YAML format](http://yaml.org/start.html) and has specific requirements about its format and syntax. If you're not familiar with the YAML format, it doesn't matter, the file is very easy to edit without understanding the intricacies of the format.

## Exploring the `_config.yml` file

By opening the `_config.yml` file you'll discover a number of interesting configuration options and an explanation of how the configuration options work of these work.

In some cases configuration options provide simple pieces of global information which can be used throughout the website (eg. `title`, `email`, `twitter_username` etc.) whilst others provide the Jekyll generator useful configuration values for generating URLs (eg. `baseurl`, `url`), processing content (ie. `markdown`), any any custom themes (ie. `theme`) or ruby plugins (ie. `gems`) to load and apply to the generated site.

A full list of default configuration options can be found in the [Jekyll documentation](https://jekyllrb.com/docs/configuration/options/). Many themes or Jekyll plugins may have their own configuration options. For example, the default theme our site is using, minima, has its all its configuration settings documented in its [own readme](https://github.com/jekyll/minima).

## Changing the `_config.yml`

Inside the file you'll quickly discover the website title, description, contact email and social media custom options. We can change some of these values to demonstrate how this file is read.

**Open into the file and find the lines that say:**

```
title: Your awesome title
email: your-email@domain.com
```

**Change the title and email associated with your nw Jekyll site by modifying these**. In my example I'm going to change it as follows:

```
title: Tristan's Demo Site
email: tristan@tristandavey.com
```

### Testing your changes

Because this file is read during the site generation process our webpage won't automatically update with these new settings. To apply the settings we're going to stop the `jekyll serve` command we ran earlier and re-run it.

**Press *Ctrl*+*c* in the terminal window running your `jekyll serve` command to stop it.
Then run `jekyll serve` again.**

If you refresh your web browser you should now see you changes! Check the title bar of the browser, as well as the site name and email shown in the footer of the website.

![Web browser showing the new title and email address](/assets/images/step2/new-title.png)

#### Troubleshooting

If you have problems modifying this file when starting your server you may have an error in your configuration file. Check the the error that you are given, or consult the YAML documentation to try to find any errors.

