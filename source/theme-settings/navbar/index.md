---
layout: docs
title: Set the website navigation bar
group: docs-volantis-latest
order: 303
short_title: 3-3 Set the website navigation bar
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

## Navigation bar configuration

The navigation bar is divided into three area settings: logo, menu, and search. If pictures are set in the logo area, icons and titles cannot be displayed. The settings of the menu area can be written in a separate file.
```yaml blog/_config.volantis.yml
navbar:
  logo: # choose [img] or [icon + title]
    img:
    icon:
    title:
  menu:
    # The following can be written in `blog/source/_data/menu.yml`
    -name: blog
      icon: fas fa-rss
      url: /
    -name: category
      icon: fas fa-folder-open
      url: categories/
    -name: label
      icon: fas fa-tags
      url: tags/
    -name: archive
      icon: fas fa-archive
      url: archives/
    -name: Friends chain
      icon: fas fa-link
      url: friends/
    -name: About
      icon: fas fa-info-circle
      url: about/
  search: search # Search bar placeholder
```

{% p subtitle, use data file %}

It is recommended to create a new file to store the configuration of the navigation bar <u>menu</u>. The path of the file is:
```
blog/source/_data/menu.yml
```
The content of the file is:
```yaml blog/source/_data/menu.yml
-name: blog
  icon: fas fa-rss
  url: /
...
```

## Menu nesting

The navigation bar menu supports nesting, the nested attribute is named `rows`, and the writing example:
```yaml blog/source/_data/menu.yml
...
-name: more
  icon: fas fa-ellipsis-v
  rows:
    -name: theme source code
      url: https://github.com/volantis-x/hexo-theme-volantis/
    -name: update log
      url: https://github.com/volantis-x/hexo-theme-volantis/releases/
    -name: hr
    -name: Have questions?
      rows:
        -name: see FAQ
          url: faqs/
        -name: see the source code of this site
          url: https://github.com/volantis-x/volantis-docs/
        -name: mention Issue
          url: https://github.com/volantis-x/hexo-theme-volantis/issues/
    -name: hr
    -name: announcements and test blog posts
      url: archives/
    -name: sample blog
      url: examples/
    -name: special thanks
      url: contributors/
```

## Dividing line

In the submenu, a new "menu" with only `name: hr` will be rendered as a dividing line.
```yaml
-name: hr
```

## Subtitle

In the submenu, a new "menu" with only `name: subtitle content` (can also have ʻicon: icon for subtitle`) will be rendered as a subtitle.
```yaml
...
-name: recent
  icon: fas fa-clock
  url: /
  rows:
    -name: popular article
      icon: fas fa-fire
    -name: Design Ideas of ProHUD Open Source Library
      url: blog/2019-08-27-prohud/
    -name: ValueX: Practical safe object type conversion library
      url: blog/2019-08-29-valuex/
    -name: Design and development of Heart Rate Manager App
      url: blog/2019-07-23-heartmate/
```