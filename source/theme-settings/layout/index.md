---
layout: docs
title: Article layout configuration
group: docs-volantis-latest
order: 306
short_title: 3-6 article layout configuration
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---


```yaml
# Article layout
article:
  # Article card layout scheme of the article list page
  preview:
    scheme: landscape # landscape
    # pin icon for post
    pin_icon: https://cdn.jsdelivr.net/gh/twitter/twemoji@13.0/assets/svg/1f4cc.svg
    # auto generate title if not exist
    auto_title: true # false, true
    # auto generate excerpt if not exist
    auto_excerpt: true # false, true
    # show split line or not
    line_style: solid # hidden, solid, dashed, dotted
    # show readmore button
    readmore: auto # auto, always
  # The layout scheme of the article card body on the article details page
  body:
    # Top of article information
    # Take from meta_library
    top_meta: [author, category, date, counter]
    # ----------------
    # Article footer component
    footer_widget:
      # ----------------
      # Reference materials, related materials, etc. (for layout: post/docs)
      references:
        title: Reference
        icon: fas fa-quote-left
        # In front-matter:
        # references:
        #-title: an article
        # url: https://
        # To display this component.
      # ----------------
      # Related articles, plug-ins need to be installed (for layout: post)
      # npm i hexo-related-popular-posts
      related_posts:
        enable: false
        title: Related articles
        icon: fas fa-bookmark
        max_count: 5
        # Set to empty to not use the article header
        placeholder_img: https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/046.jpg
      # ----------------
      # Copyright notice component (for layout: post/docs)
      copyright:
        enable: true
        permalink:'The permanent link to this article is:'
        content:
          -'The content of the blog follows the attribution-non-commercial use-share in the same way 4.0 International (CC BY-NC-SA 4.0) agreement'
          -permalink
      # ----------------
      # Reward component (for layout: post/docs)
      donate:
        enable: false
        images:
          -https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/qrcode/github@volantis.png
          -https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/qrcode/github@volantis.png
    # Information at the bottom of the article
    # Take from meta_library
    bottom_meta: [updated, tags, share]
    # meta library
    meta_library:
      # Default article author (can be overridden in front-matter)
      author:
        avatar:
        name: Please set the author of the article
        url: /
      # Article creation date
      date:
        icon: fas fa-calendar-alt
        title:'Posted on:'
        format:'ll' # Date format http://momentjs.com/docs/
      # Article update date
      updated:
        icon: fas fa-edit
        title:'Updated at:'
        format:'ll' # Date format http://momentjs.com/docs/
      # Article classification
      category:
        icon: fas fa-folder-open
      # Article view count
      counter:
        icon: fas fa-eye
        unit:'Views'
      # Number of article comments: only valine is supported
      valinecount:
        icon: fas fa-comment-dots
        desc:'' # comments
      # Article word count and reading time
      wordcount:
        icon_wordcount: fas fa-keyboard
        icon_duration: fas fa-hourglass-half
      # Article tags
      tags:
        icon: fas fa-hashtag
      # share it
      share:
        -id: qq
          img: https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/logo/128/qq.png
        -id: qzone
          img: https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/logo/128/qzone.png
        -id: weibo
          img: https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/logo/128/weibo.png
        -id: # qrcode # When id is qrcode, plug-in needs to be installed npm i hexo-helper-qrcode
          img: # https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/logo/128/wechat.png
        -id: # telegram
          img: # https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/logo/128/telegram.png

```
The values ​​of `top_meta` and `bottom_meta` are taken from the `meta_library` library.