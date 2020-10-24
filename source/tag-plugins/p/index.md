---
layout: docs
group: docs-volantis-latest
order: 513
short_title: false
title:'tag-plugins: p'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md This plugin was last updated in version <u>2.5</u>
{% p style parameter, text content %}
```

## Demo effect

### Colored text

It is convenient to insert labels of various colors in a paragraph, including: {% p red, red%}, {% p yellow, yellow%}, {% p green, green%}, {% p cyan, cyan%}, {% p blue, blue%}, {% p gray, gray%}.

### Oversized text

The title part of the document "start" page is oversized text.

{% p center logo large, Volantis %}
{% p center small, A Wonderful Theme for Hexo %}

## Source code of the above example

```md example:
### Colored text

It is convenient to insert labels of various colors in a paragraph, including: {% p red, red%}, {% p yellow, yellow%}, {% p green, green%}, {% p cyan, cyan%}, {% p blue, blue%}, {% p gray, gray%}.

### Oversized text

The title part of the document "start" page is oversized text.

{% p center logo large, Volantis %}
{% p center small, A Wonderful Theme for Hexo %}
```

## Supportable parameters

The style parameter position can write color, size, and alignment direction, and multiple style parameters are separated by spaces.

### Font

```
logo, code
```

### colour

```
red, yellow, green, cyan, blue, gray
```

### Size

```
small, h4, h3, h2, h1, large, huge, ultra
```

### Alignment direction

```
left, center, right
```