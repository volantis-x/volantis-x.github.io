---
layout: docs
group: docs-volantis-latest
order: 532
short_title: false
title:'tag-plugins: folding'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md was last updated in version <u>2.3</u>
{% folding parameter (optional), title %}
![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)
{% endfolding %}
```

## Demo effect

{% folding View image test %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% folding cyan open, view the folding box opened by default %}

This is a folding box that is opened by default.

{% endfolding %}

{% folding green, view code test %}

```md
{% folding green, view code test %}

View code test

{% endfolding %}
```

{% endfolding %}

{% folding yellow, view list test %}

-haha
-hehe

{% endfolding %}

{% folding red, view nested tests %}

{% folding blue, view nested test 2 %}

{% folding View nested test 3 %}

hahaha <span><img src='https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/tieba/%E6%BB%91%E7%A8%BD.png' style='height :24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}

## Source code of the above example

```md example:
{% folding View image test %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% folding cyan open, view the folding box opened by default %}

This is a folding box that opens by default.

{% endfolding %}

{% folding green, view code test %}

{% endfolding %}

{% folding yellow, view list test %}

-haha
-hehe

{% endfolding %}

{% folding red, view nested tests %}

{% folding blue, view nested test 2 %}

{% folding View nested test 3 %}

hahaha <span><img src='https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/tieba/%E6%BB%91%E7%A8%BD.png' style='height :24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}
```

## Supportable parameters

The color and status can be filled in the parameter position, and multiple parameters are separated by spaces.

### colour

```
blue, cyan, green, yellow, red
```

### Status

Fill in the status with ʻopen` to represent the default open.