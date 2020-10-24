---
layout: docs
title: page layout template
group: docs-volantis-latest
order: 401
short_title: 4-1 page layout template
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

## Layout template

{% table %}
| Value | Meaning |
| :----- | :---- |
| page | Independent page |
| post | Article page |
| docs | Documentation page |
| category | Category page |
| tag | Tag page |
| friends | Friends link page |
| list | List page |
{% endtable %}

## page & post & docs

These three types of pages are the same, but have the following subtle differences:

- When the post article has a title, scroll down the web page, the navigation bar will move up and out of the screen to display the article title, but page and docs will not.
- post At the end of the article, up to four modules can be displayed: "Reference", "Related Article", "Copyright Mark", and "Reward".
- At most one module of "reference" can be displayed at the end of the docs article.


Except that the archive page is automatically generated, other independent pages need to be created manually.

## Archive page

The archive page is automatically generated and has been generated during initialization. The path is as follows:

```yaml blog/_config.yml
# Directory
archive_dir: archives
```

## About page

```yaml Create file if not exists: source/about/index.md
---
layout: docs
seo_title: About
bottom_meta: false
sidebar: []
valine:
  placeholder: What do you want to tell me?
---

Write about yourself below

```

## Category page

```yaml Create file if not exists: source/categories/index.md
---
layout: category
index: true
title: All categories
---
```

## Tag page

```yaml Create file if not exists: source/tags/index.md
---
layout: tag
index: true
title: all tags
---
```

## List page

```yaml Create file if not exists: source/mylist/index.md
---
layout: list
group: mylist
index: true
---
```

The result is to filter out all articles that contain `group: mylist` in the `front-matter` section.


## Friends link page

### Create page file

```yaml Create file if not exists: source/friends/index.md
---
layout: friends # required
title: My friends # Optional, this is the title of the friend link page
---

Write the content above the friend chain here.

<!-- more -->

Here you can write text notes at the bottom of the friend chain page, such as your own friend chain specifications, examples, etc.

```

### Choose a layout

Find the following in the theme configuration file:

```yaml
pages:
  # Friends link page configuration
  friends:
    layout_scheme: traditional # simple: simple layout, traditional: traditional layout, sites: website card layout
```

Three layout schemes are currently provided:
- simple: Simple layout, only avatar and title.
- traditional: Traditional layout, the style of the old version of Volantis.
- sites: site card layout, which is the new style of website card tags added in Volantis 4.x.

### Set data source


{% tabs about, 1 %}

<!-- tab static data source -->

The data source of Friends Chain is written in the following path, if not, please create it yourself:
```
blog/source/_data/friends.yml
```
The content format is:
```yaml blog/source/_data/friends.yml
-group: # Group title
  description: # Group description
  items:
    -title: # name
      avatar: # Avatar
      url: # link
      screenshot: # Screenshot
      keywords: # Keywords
      description: # description
    -title: # name
      avatar: # Avatar
      url: # link
      screenshot: # Screenshot
      keywords: # Keywords
      description: # description
```

Different layout methods will use some fields. Generally speaking, `title`, ʻavatar` and ʻurl` are all required. These data are converted into HTML tags and inserted into the `<!-- more -->` part of the friend link page.

<!-- endtab -->

<!-- tab dynamic data source -->

Use the issues tag to get JSON data from issues to parse and generate HTML to fill in the page. The usage is as follows:

```
{% issues sites | api=https://api.github.com/repos/xaoxuu/friends/issues?sort=updated&state=open&page=1&per_page=100&labels=active %}
```

In this way, the way to add a friend chain becomes: the other party raises an Issue, reviews it by yourself, then adds the ʻactive` tag, and then refreshes the webpage to take effect. It is also very convenient to update the content of the friend chain. The creator of the issue has the right to modify and close it.

Create a new GitHub or Gitee repository and create the Issues template as follows:

```json
{
    "title": "",
    "screenshot": "",
    "url": "",
    "avatar": "",
    "description": "",
    "keywords": ""
}
```

For details on how to use the issues tag, see this article:

{% link static blog uses the Issues API to post updates, friend links, and bookmarks, https://xaoxuu.com/blog/2020-08-23-issues-api/ %}


<!-- endtab -->

{% endtabs %}

{% noteblock idea, suggest %}

- Both can be used at the same time. It is recommended to open the issues friend chain to everyone, and save it to the static friend chain if you contact yourself frequently.
- The actual speed and stability of the GitHub API is not as good as Gitee. If you pursue stability, it is recommended to use Gitee.

{% endnoteblock %}

## 404 page

```yaml Create file if not exists: source/404.md
---
cover: true
robots: noindex,nofollow
sitemap: false
seo_title: 404 Not Found
bottom_meta: false
sidebar: []
valine:
  path: /404.html
  placeholder: Please leave a message and tell me which page you want to visit is not found
---

{% p logo center huge, 404 %}
{% p center bold, sorry, the page you visited does not exist %}
{% p center small, the address may be entered incorrectly or the address has been deleted %}

```