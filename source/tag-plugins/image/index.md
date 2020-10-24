---
layout: docs
group: docs-volantis-latest
order: 542
short_title: false
title:'tag-plugins: image'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

The Image tag is a tag for a single picture application scenario, supporting picture description text and specified width.

```md This plugin was last updated in version <u>4.0</u>
{% image link, width=width (optional), height=height (optional), alt=description (optional), bg=placeholder color (optional) %}
```

## Demo effect

Add description:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, alt=The way back to the dormitory after class every day, there is no story. %}

Specify width:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, width=300px %}

Specify the width and add a description:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, width=300px, alt=The way back to the dormitory after class every day, there is no story. %}

Set the background color of the placeholder:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, width=414px, bg=#224855, alt=Optimize the look and feel of browsing in different widths %}



## Source code of the above example

```md example:
Add description:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, alt=The way back to the dormitory after class every day, there is no story. %}

Specify width:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, width=400px %}

Specify the width and add a description:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, width=400px, alt=The way back to the dormitory after class every day, there is no story. %}

Set the placeholder background color:

{% image https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg, width=400px, bg=#1D0C04, alt=Optimize the look and feel of browsing with different widths %}
```

## Supportable parameters


### Picture width and height

```md example:
width=300px, height=32px
```

### image description

```md example:
alt=picture description
```

### Placeholder background color

```md example:
bg=#f2f2f2
```