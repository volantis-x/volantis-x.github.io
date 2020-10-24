---
layout: docs
title: page custom layout
group: docs-volantis-latest
order: 403
short_title: 4-3 page custom layout
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

## Show mini music player

The mini music player is displayed on the right side of the title. The supported fields are: `server`, `type`, ʻid`.

```yaml front-matter
---
music:
 server: netease # netease, tencent, kugou, xiami, baidu
 type: song # song, playlist, album, search, artist
 id: 16846091 # song id / playlist id / album id / search keyword
---
```

{% note play, see the actual effect: [#contributors](/contributors/) %}

## Show meta tags

The date, category, update date, tags, sharing, etc. at the top and bottom of the article are meta tags.

```yaml front-matter
---
top_meta: false
bottom_meta: false
---
```
If a page has no title, top_meta will not be displayed, like 404, about pages can be completely hidden:

```yaml front-matter
---
seo_title: About
top_meta: false
bottom_meta: false
---
```


## Thumbnails are shown on the right

```yaml front-matter
---
thumbnail: https://img.vim-cn.com/17/0c7b02722686d1527a1df807dae0794d995860.png
---
```

The thumbnail is only displayed on the article list and article page, not on the archive page.

## The icon is displayed on the right side of the title

```yaml front-matter
---
icons: [fas fa-fire red, fas fa-star green]
---
```

The icon is only displayed on the archive page and can be used to mark popular articles.

{% note info, you can set the color of the icon through red / blue / green / yellow / orange / theme / accent %}


## Do you want to show cover

If a page needs a cover, you can write it like this:
```yaml front-matter
---
cover: true
---
```


## Show sidebar

By freely setting the sidebar card to delete the redundant information of the corresponding page, increase the weight of valuable information in the page.

If a page does not require a sidebar, you can write:
```yaml front-matter
---
sidebar: []
---
```

If a certain page wants to display certain sidebars, just write:
```yaml front-matter
---
sidebar: [grid, toc, tags] # Place any sidebar widgets you want to display
---
```

## Close comment

```yaml front-matter
---
comments: false
---
```