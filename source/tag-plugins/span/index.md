---
layout: docs
group: docs-volantis-latest
order: 512
short_title: false
title:'tag-plugins: span'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md This plugin was last updated in version <u>2.5</u>
{% span style parameter, text content %}
```

## Demo effect

### Colored text

It is convenient to insert tags of various colors in a paragraph, including: {% span red, red%}, {% span yellow, yellow%}, {% span green, green%}, {% span cyan, cyan%}, {% span blue, blue%}, {% span gray, gray%}.

### Oversized text

The title part of the document "start" page is oversized text.

{% span center logo large, Volantis %}
{% span center small, A Wonderful Theme for Hexo %}

## Source code of the above example

```md example:
### Colored text

It is convenient to insert tags of various colors in a paragraph, including: {% span red, red%}, {% span yellow, yellow%}, {% span green, green%}, {% span cyan, cyan%}, {% span blue, blue%}, {% span gray, gray%}.

### Oversized text

The title part of the document "start" page is oversized text.

{% span center logo large, Volantis %}
{% span center small, A Wonderful Theme for Hexo %}
```

## Supportable parameters

The style parameter position can write color, size and alignment direction, and multiple style parameters are separated by spaces.

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