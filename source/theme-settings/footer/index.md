---
layout: docs
title: Set website footer
group: docs-volantis-latest
order: 304
short_title: 3-4 set website footer
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

Through `layout`, you can freely lay out the content of website footer ʻaplayer`, `social`, `license`, ʻinfo`, `copyright`.
```yaml blog/_config.volantis.yml
site_footer:
  # layout of footer: [aplayer, social, license, info, copyright]
  layout: [aplayer, social, license, info, copyright]
  social:
    -icon: fas fa-rss
      url: atom.xml
    -icon: fas fa-envelope
      url: mailto:me@xaoxuu.com
    -icon: fab fa-github
      url: https://github.com/xaoxuu
    -icon: fas fa-headphones-alt
      url: https://music.163.com/#/user/home?id=63035382
  copyright:'[Copyright © 2017-2020 Mr. X](https://xaoxuu.com)'
  # You can add your own property here. (Support markdown, for example: br:'<br>')
  br:'<br>'
```
Among them, ʻaplayer` needs to be enabled in the plugin settings. You can add text attributes to display other text information, for example:
```yaml blog/_config.volantis.yml
site_footer:
  layout: [..., br, hello, ...]
  ...
  # You can add your own property here. (Support markdown, for example: br:'<br>')
  br:'<br>'
  hello:'[Hello World](/)'
```