---
layout: post
title: Step 6
description: Adding images and more...
show_tile: true
---

Now we've built a page and post in Jekyll we'll have a look at some more advanced tasks and some of Jekyll's cooler features.

## Images

Because Jekyll generates HTML and CSS for our website from our markdown content its not immediately obvious how we might add images and multimedia content.

### Storing our image

You can actually add images directly to your content in Markdown, but you need to provide your image file to Jekyll in a way that it understands that the image is needed by the generated website. To do that we can place this file in an `assets` folder in the root.

**Create a folder called `assets` in the root of your Jekyll site. Next create a `images` folder within this assets folder.**

We can now add images to this `assets/images` directory which will be included in your generated website. You can add other subdirectories in the `assets` folder for videos, fonts or even downloadable files.

**Add an image to your `assets/images` directory. In our example we're going to use a NASA image of the [Voyager I Spacecraft's golden record](/assets/images/goldrenrecord.jpg).

When complete your Jekyll site directory should look something like this:

 ```
├── Gemfile
├── Gemfile.lock
├── _config.yml
├── _posts
│   ├── 2018-11-14-yet-another-post.md
│   └── 2018-11-17-welcome-to-jekyll.markdown
├── _site
│     ...
├── about.md
├── assets
│   └── images
│       └── goldenrecord.jpg
├── index.md
└── mypage.md
```

### Adding our image to a page

To display our image on our Jekyll site we're going to add it to the page we created earlier.

**Open `mypage.md` and at the bottom of the page insert the following block of markdown making sure you substitute the text between the `<` and `>` characters:**

 ```
 ![<alternative text>](/assets/images/<filename>)
 ```

 In my example I've added the following to my `mypage.md` file

 ```
 ![NASA Voyager I Golden Record](/assets/images/goldenrecord.jpg)
```

Although strictly optional adding text the alternate text box between the `[` and `]` characters is recommended to provide a better experience for vision impaired users, or users who can't load the image.

### Viewing our image

Now, lets check out our `mypage.md` file in our site. If you recall we gave this page a permalink, so either navigate to the page or open [http://localhost:4000/testpage](http://localhost:4000/testpage)

You should be able to see the image rendered on the page at the bottom of your other content. If you image is large it may span the full width of the page.

![]()

## Includes

One of the advantages of Jekyll's generated nature is we can use some tricks to reduce repetition of content, making our website easier to maintain. *Includes* are a feature that allow us to create content once, and display it in multiple places.

### Creating an includes

Includes are files of content which can be compiled into other Jekyll files when they are generated. The files live in a folder called `_includes` in the root directory of the Jekyll site.

**Create a folder called `_includes` in the root of your Jekyll site.**

We'll create an includes which we can use to provide a prompt to email us.

**Create a file inside the `_includes` folder called `email.md`. Add the following content to the file:**

```
Interested in finding out more? Email us at [info@devnq.org](mailto:info@devnq.org)
```

### Using our includes

**Back in our `mypage.md`, above our image, add the following snippet of code:**

```
{{ "{% include email.md " }} %}
```

You can add this includes snippets like this as many times as you want to any file in your Jekyll project. This allows you to easily create reusable elements and content which you can place anywhere on your website.

### Viewing our includes

Refresh your tab, if it is still open, or navigate back to [http://localhost:4000/testpage](http://localhost:4000/testpage) to see how our includes has been rendered.

![]()

### Extending includes

Includes are very powerful, and can even output variables and accept parameters. You can find more information on how this operates in the [Jekyll Includes documentation](https://jekyllrb.com/docs/includes/).
