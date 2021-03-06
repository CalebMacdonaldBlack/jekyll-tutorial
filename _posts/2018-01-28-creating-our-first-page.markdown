---
layout: post
title: Step 4
description: Creating our first page
show_tile: true
permalink: step4
---

To first understand how Jekyll pages are structured, we're going to have a look at the `about.md` page. This page represents a typical page in a Jekyll site.

Lets jump into the `about.md` page and take a look at how the data is structured and formatted.

## Page Structure

Each page, and blog post conforms to the same structure. It has the *frontmatter* at the top of the document, and the rest of the content following this. We'll have a look at the *frontmatter* and *content* sections to determine what these are used for and how they are formatted.

### Frontmatter

At the top of the file you'll find several lines between two lines of dashes (`---`) This is called *frontmatter* and the content between these lines is used to help configure the page's settings. The data between these lines is also YAML and works similarly to our `_config.yml` file. Lets have a look at the properties we have here.

#### `layout`

The *layout* property determines how the page generated by Jekyll looks. Most Jekyll themes have a set of basic layouts they implement `page`, `home`, and `post`, however, theme authors can create as many or as few layouts as they wish.

Different layouts may only slightly differ, or may have completely different formats all dependent on on how the theme author has chosen to implement them . For example a `post` layout may list information like the post title, author, date published, along with a link to the next blog post at the bottom whilst a page may only show the title.

#### `title`

The *title* property determines the title of the page, not only what is shown in the Browser title bar, but also what the page may show as the title. Title is not a default frontmatter tag, but is implemented by most themes as a

#### `permalink`

The `permalink` property helps the Jekyll generator generate search-engine friendly URLS by letting you set a custom URL path this page will be available at.

#### More about frontmatter

As well as these there are other default frontmatter tags for both pages and posts. There are also some caveats to frontmatter and how it can be used. For more information check out the [official Jekyll Frontmatter documentation](https://jekyllrb.com/docs/front-matter/).

### Content

The content of a Jekyll page or post is all of the content below the frontmatter. This is formatted in a special formatting language called *markdown* (hence why these files have the `.md` or `.markdown` extension)

*Markdown* is very easy to quickly understand. With markdown you can format text, add images, links, lists, quotes, tables and headings. If you're not familiar with it you can undertake a quick tutorial to understand the basics of Markdown at [markdowntutorial.com](https://www.markdowntutorial.com).

If you're familiar with HTML you can also create pages for Jekyll in HTML (by using a `.htm`) extension. You can also mix most basic HTML tags into *markdown* content if you're trying to add more complex content.

## Creating our own page

Now we're familiar with the *About* page lets create our own page and demonstrate what we've learnt about Jekyll pages.

### Setting up the file

First lets create a file for our new page.

**Create a new file in the root directory of our jekyll site and call it `mypage.md`.**

We're going to **add some basic content to the page first**. The page needs to have a frontmatter section, but we won't set anything in it for now. Try adding some content to the page, here is some basic placeholder markdown to get you started:


```
---
---

# My test page

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

Jekyll will automatically detect the presence of this page and add it to our site. You can view it here: [http://localhost:4000/mypage/](http://localhost:4000/mypage/)

 !A basic Jekyll page without a layout](/assets/images/step3/no-layout.png)

You'll note this page looks pretty basic and doesn't have the theme applied. This is because we haven't used a layout from the theme. We'll set this up in the next section.

### Setting up our frontmatter

#### Setting a layout

First thing's first for our new page, lets get it looking pretty. In the last step we created a page without a layout. Now lets setup our frontmatter to use the `page` layout the `about.md` pager was using earlier.

*Change the frontmatter of your new page to include the `page` layout option.*

```
---
layout: page
---
```

If we now jump back to [our page](http://localhost:4000/mypage/) we can see that the default page layout we saw on the *About* page has also been applied to this page.

![A basic Jekyll page using the default page layout](/assets/images/step3/page-layout.png)

#### Setting a title

Adding a title is important as this adds a title which can be shown in a browser taskbar, is indexed by search engines and can be shown by Jekyll's automatically generated navigation.

**Add a title to the frontmatter of your page.**

```
---
layout: page
title: Test Page
---
```

This time, lets go to our [home page](http://localhost:4000). Because there is a page title to be shown, our page has automatically been included in the site's navigation, at the top tight of the page, by Jekyll. Clicking the link in the top right will now take us through to our page.

#### Setting a permalink

Finally we'll test setting the permalink of our page. This can be useful in overriding the default url of a page to something which is more search-engine or use friendly, and can help you keep your pages organised without being limited by how they must be named.

**Lets add a permalink property to our frontmatter and set it to something easy to remember. For ease lets set it to `testpage`.**

```
---
layout: page
title: Test Page
permalink: testpage
---
```

Now our [old link](http://localhost:4000/mypage/) will no longer work, but our page will be available at our new url: [http://localhost:4000/testpage/](http://localhost:4000/testpage/)

The end result should be our new page, showing our content in the theme's `page` layout with our title, a navigation link and a our custom permalink.

![Our complete page](/assets/images/step3/final.png)