---
layout: docs
title: Sidebar configuration
group: docs-volantis-latest
order: 307
short_title: 3-7 sidebar configuration
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

The sidebar widget is different from the meta library: In addition to the existing widget, you can easily create your own widget and place it where you need it. In addition, you can also write widgets in separate files.

{% folding View all related configurations %}

```yaml blog/_config.volantis.yml
sidebar:
  # Home page, category, archive and other independent pages
  for_page: [blogger, category, tagcloud, qrcode]
  # layout: docs/post such article pages
  for_post: [toc]
  # Sidebar component library
  widget_library:
    # ---------------------------------------
    # blogger info widget
    blogger:
      class: blogger
      display: [desktop, mobile] # [desktop, mobile]
      avatar: https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/Logo-NavBar@3x.png
      shape: rectangle # circle, rectangle
      url: /about/
      title:
      subtitle:
      jinrishici: true # Poetry Today. You can set a string, and it will be displayed when loading fails.
      social: true
    # ---------------------------------------
    # toc widget (valid only in articles)
    toc:
      class: toc
      display: [desktop, mobile] # [desktop, mobile]
      header:
        icon: fas fa-list
        title: Contents of this article
      list_number: false
      min_depth: 2
      max_depth: 5
    # ---------------------------------------
    # category widget
    category:
      class: category
      display: [desktop] # [desktop, mobile]
      header:
        icon: fas fa-folder-open
        title: Article classification
        url: /blog/categories/
    # ---------------------------------------
    # tagcloud widget
    tagcloud:
      class: tagcloud
      display: [desktop, mobile] # [desktop, mobile]
      header:
        icon: fas fa-tags
        title: Popular tags
        url: /blog/tags/
      min_font: 14
      max_font: 24
      color: true
      start_color:'#999'
      end_color:'#555'

    # ---------------------------------------
    # qrcode widget
    donate:
      class: qrcode
      display: [desktop, mobile] # [desktop, mobile]
      height: 64px # Automatic height if not set
      images:
        -https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/qrcode/github@volantis.png
        -https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/qrcode/github@volantis.png
    # ---------------------------------------
    # webinfo widget
    webinfo:
      class: webinfo
      display: [desktop]
      header:
        icon: fas fa-award
        title: site information
      type:
        article:
          enable: true
          text:'Number of articles:'
          unit:'Article'
        runtime:
          enable: true
          data: '2020/01/01' # Fill in the site construction date
          text:'Elapsed time:'
          unit:'day'
        wordcount:
          enable: true
          text:'Total words on this site:' # Need to enable wordcount
          unit:'word'
        siteuv:
          enable: true
          text:'Number of visitors to this site:' # Need to enable busuanzi
          unit:'person'
        sitepv:
          enable: true
          text:'Total visits to this site:' # Need to enable busuanzi
          unit:'time'
        lastupd:
          enable: true
          friendlyShow: true # More friendly time display
          text:'Last activity time:'
          unit:'day'
```
{% endfolding %}

Every widget has `class` and `display`. The former represents what the widget is, and the latter represents whether the widget is displayed on what desktop and mobile platform. The sidebar widgets will be moved to the bottom of the body area, so some sidebar widgets have no meaning. It is recommended to set it to display only on the desktop.

```yaml
Widget name:
  class: widget category
  display: [Whether the widget is displayed on the desktop, and whether the widget is displayed on the mobile device]
```

## Blogger information widget
```yaml blog/_config.volantis.yml
blogger:
  class: blogger
  display: [desktop] # [desktop, mobile]
  avatar: https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png
  title:
  subtitle:
  jinrishici: true # Poetry Today. You can set a string, and it will be displayed when loading fails.
  social: true
```
Among them, if today's poem `jinrishici` is set to a string, this string will become a placeholder text and will be displayed when loading fails. If you don't need it, please set it to `jinrishici: false`. Please set the specific content of `social` in the footer of the website.

## Article directory widget
```yaml blog/_config.volantis.yml
toc:
  class: toc
  display: [desktop, mobile] # [desktop, mobile]
  header:
    icon: fas fa-list
    title: Contents of this article
  list_number: false
  min_depth: 2
  max_depth: 5
```
This widget can only be placed in the sidebar and is valid in the article. When previewing on a mobile device, the TOC button will appear on the right side of the navigation bar when you swipe your finger upwards, click to expand the TOC component. If you need to display the chapter number, please set `list_number`. `min_depth` and `max_depth` represent the header level supported by TOC, the maximum range is 2-6.

## Article classification widget
```yaml blog/_config.volantis.yml
category:
  class: category
  display: [desktop] # [desktop, mobile]
  header:
    icon: fas fa-folder-open
    title: Article classification
    url: /blog/categories/
```
This component can directly display all article categories. If you want a separate page to display, you need to create a file by yourself. The specific operation is in the "page" part of the document.

## Tag cloud widget
```yaml blog/_config.volantis.yml
tagcloud:
  class: tagcloud
  display: [desktop] # [desktop, mobile]
  header:
    icon: fas fa-tags
    title: Popular tags
    url: /blog/tags/
  min_font: 14
  max_font: 24
  color: true
  start_color:'#999'
  end_color:'#555'
```
This component can directly display the tags of all articles. If you want a separate page to display, you need to create a file by yourself. The specific operation is in the "page" part of the document.


## QR code parts
```yaml blog/_config.volantis.yml
donate:
  class: qrcode
  display: [desktop, mobile] # [desktop, mobile]
  height: 64px # Automatic height if not set
  images:
    -https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/qrcode/github@volantis.png
    -https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/qrcode/github@volantis.png
```
You can place it in the footer of the article to display rewarding pictures, or place it in the sidebar.

## Universal text widget
```yaml blog/_config.volantis.yml
repos:
  class: text
  display: [desktop] # [desktop, mobile]
  header:
    icon: fab fa-github
    title: Like it
    url: https://github.com/xaoxuu/
  content:
    -'Your likes are very important to me. If you like this theme, I hope you can give me a like to support the items below. '
    -'[<img src="https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/prohud/logo.png" height="50px">](https://github.com/ xaoxuu/ProHUD)'
    -'[<img src="https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/valuex/logo.png" height="50px">](https://github.com/ xaoxuu/ValueX)'
    -'[<img src="https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/inspire/logo.png" height="50px">](https://github.com/ xaoxuu/Inspire)'
```
You can create text widgets to display any text content.

## Universal list widget
```yaml blog/_config.volantis.yml
wiki-hexo-theme:
  class: list
  display: [desktop, mobile] # [desktop, mobile]
  header:
    icon: fas fa-chevron-left
    title: Hexo Themes
    url: /wiki/
  rows:
    -name: Volantis for Hexo
      url: /wiki/volantis/
    -name: Resume for Hexo
      url: /wiki/resume/
```
You can create a list part to display any linked list. The attributes supported by each item in the list of `rows` are: `name`, ʻurl`, ʻicon`, ʻimg`, ʻavatar`, where ʻimg` is a link to a square image and ʻavatar` is a circle Link to the shape picture.

### Group Index

The layout of this widget is inherited from the list widget and is used to display the grouped article list to which the article belongs. Please upgrade your Volantis to version <u>2.5</u> or higher.

```yaml blog/_config.volantis.yml
group-1:
  class: group
  display: [desktop, mobile] # [desktop, mobile]
  header:
    icon: fab fa-github
    title: Git
    url: /wiki/git/
```

Set in the front-matter of the article:
```yaml front-matter
group: group-1
order: 16
sidebar: [group-1, toc]
```

The "group-1" card will display all the articles with `group: group-1` in the form of a list, sorted from small to large in the order of ʻorder`.

## Universal grid widget
```yaml blog/_config.volantis.yml
feedback:
  class: grid
  display: [desktop, mobile]
  header:
    icon: fas fa-headset
    title: Contact the developer
    url: https://github.com/volantis-x/hexo-theme-volantis
  fixed: true # fixed width
  rows:
    -name: feedback BUG
      icon: fas fa-bug
      url: https://github.com/volantis-x/hexo-theme-volantis/issues/
    -name: ask for help
      icon: fas fa-question-circle
      url: https://github.com/volantis-x/hexo-theme-volantis/issues/
    -name: make a suggestion
      icon: fas fa-lightbulb
      url: https://github.com/volantis-x/hexo-theme-volantis/issues/
```
You can create a grid widget to display any list of links. By default, the grid automatically determines the width of each grid according to the text length. If the text length is different, it is recommended to set `fixed: true` to fix the width. At this time, the text in the grid with too long text will be displayed in a new line.

## Universal page widget
```yaml blog/_config.volantis.yml
test:
  class: page
  display: [desktop, mobile]
  pid: haha
  content: excerpt # excerpt, more, content
```
You can render the md content of the entire page as a small part. Just set the `pid` property in the widget and the same `pid` in the article's `front-matter`. `content` represents the content displayed by this component, optional ʻexcerpt`, `more`, and `content` correspond to the abstract of the article, the content behind the abstract, and the full text respectively.