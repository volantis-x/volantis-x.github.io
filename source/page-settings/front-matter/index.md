---
layout: docs
title: front-matter
group: docs-volantis-latest
order: 402
short_title: 4-2 front-matter
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

## front-matter

The front-matter is the area at the top of the file separated by `---`, used to specify the variables of individual files. For more information, please refer to Hexo official document: [#front-matter](https://hexo.io/zh-cn/docs/front-matter)

{% table %}
| Field | Meaning | Value Type | Default Value |
| :----------- | :------------ | :------------- | :------ |
| layout | Layout template | String |-|
| title | Page title | String |-|
| seo_title | Page title | String | page.title |
| short_title | Page title (displayed in the group list) | String | page.title |
| date | Creation time | Date | File creation time |
| updated | Update date | Date | File modification time |
| link | External article URL | String |-|
| music | Internal music controls | [Object] |-|
| robots | robots | String |-|
| keywords | Page keywords | String |-|
| description | Page description, abstract | String |-|
| cover | Whether to show the cover | Bool | true |
| top_meta | Whether to display the meta information at the top of the article or page | Bool | true |
| bottom_meta | Whether to display the meta information at the bottom of the article or page | Bool | true |
| sidebar | Page sidebar | Bool, Array | theme.layout.*.sidebar |
| body | Page body elements | Array | theme.layout.on_page.body |
| mathjax | Whether to render formulas | Bool, String | false |
| thumbnail | Thumbnail | String | false |
| icons | icons | Array | [] |
| pin | whether to top | Bool | false |
{% endtable %}

Fields unique to `layout:post`:

{% table %}
| Field | Meaning | Value Type | Default Value |
| :----------------- | :------------ | :------------- |: ------ |
| author | Article author | [Object] | config.author |
| categories | Categories | String, Array |-|
| tags | Tags | String, Array |-|
| toc | Whether to generate a directory | Bool | true |
{% endtable %}

author

{% table %}
| Field | Meaning | Value Type | Default Value |
| :----------------- | :------------ | :------------- |: ------ |
| name | Author name | String | config.author |
| avatar | Avatar | String | config.avatar |
| url | Link | String | config.url |
{% endtable %}

music

{% table %}
| Field | Must | Value Type |
| :----------------- | :------------ | :--------------- - |
| server | yes | netease, tencent, kugou, xiami, baidu |
| type | yes | song, playlist, album, search, artist |
| id | yes | song id / playlist id / album id / search keyword |
{% endtable %}

### Top article

Set the following values ​​in front-matter:
```yaml front-matter
pin: true
```

### Article classification

Multiple categories have two relationships, one is hierarchy (equivalent to folders), and the other is juxtaposition (equivalent to tags).

Multi-level classification:
```yaml front-matter
---
categories: [category A, category B]
---
```
or

```yaml front-matter
---
categories:
  -Category A
  -Category B
---
```

Parallel classification

```yaml front-matter
categories:
  -[Category A]
  -[Category B]
```

Multi-level + parallel classification

```yaml front-matter
categories:
  -[Category A, Category B]
  -[Category C, Category D]
```

### Article Summary

Insert `<!-- more -->` in the article, the previous part is the abstract.

```yml source code of an article
---
title: xxx
date: 2020-02-21
---

This is a summary

<!-- more -->

This is the text
```

{% note warning, **Note**: `<!-- more -->` There must be blank lines before and after `<!-- more -->`, otherwise it may cause display dislocation. %}

### Set article author

With support for multi-author jointly maintain a blog, so you can set up a separate authors:
```yaml front-matter
---
author:
  name: Author
  avatar: https://img.vim-cn.com/a1/d53c11fb5d4fd69529bc805d385fe818feb3f6.png
  url: https://baidu.com
---
```

## Import external articles

Using `link`, with customized article author information, you can display external articles or URLs in the article list, for example:

```yaml front-matter
---
layout: post
date: 2017-07-05
title: [转] How to build an independent blog based on Hexo
categories: [Dev, Hexo]
tags:
  -Hexo
author:
  name: xaoxuu
  avatar: https://cdn.jsdelivr.net/gh/xaoxuu/assets@master/avatar/avatar.png
  url: https://xaoxuu.com
link: https://xaoxuu.com/blog/2017-07-05-hexo-blog/
---

![](https://img.vim-cn.com/d9/a9af7dc49fc0af8ca3e6dd2450a2f7095a87db.png)

```

## Top

For any article or page, set `pin: true` to put it on the top page.

```yaml front-matter
---
pin: true
---
```

This will cause a small problem: the number of post cards on the homepage is more than the set value. If you have obsessive-compulsive disorder and want the number of each page to be the same, you can install a plug-in to achieve it, see: [#421](https://github.com/ volantis-x/hexo-theme-volantis/issues/421)

## Do not archive

Articles stored in the `_posts` folder will generally appear on the archive page. If a post does not want to appear on the archive page:

```yaml front-matter
---
archive: false
---
```