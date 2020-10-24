---
layout: docs
group: docs-volantis-latest
order: 516
short_title: false
title:'tag-plugins: checkbox'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md was last updated in <u>2.6</u> version
{% checkbox style parameter (optional), text (support simple md) %}
```

## Demo effect

{% checkbox plain text test %}
{% checkbox checked, supports simple [markdown](https://guides.github.com/features/mastering-markdown/) syntax %}
{% checkbox red, support custom color %}
{% checkbox green checked, green + default selected %}
{% checkbox yellow checked, yellow + default selected %}
{% checkbox cyan checked, cyan + default selected %}
{% checkbox blue checked, blue + default selected %}
{% checkbox plus green checked, increase %}
{% checkbox minus yellow checked, reduce %}
{% checkbox times red checked, cross %}

## Source code of the above example

```md example:
{% checkbox plain text test %}
{% checkbox checked, supports simple [markdown](https://guides.github.com/features/mastering-markdown/) syntax %}
{% checkbox red, support custom color %}
{% checkbox green checked, green + default selected %}
{% checkbox yellow checked, yellow + default selected %}
{% checkbox cyan checked, cyan + default selected %}
{% checkbox blue checked, blue + default selected %}
{% checkbox plus green checked, increase %}
{% checkbox minus yellow checked, reduce %}
{% checkbox times red checked, cross %}
```

## Supportable parameters

### colour

```
red, yellow, green, cyan, blue
```

### Style

```
plus, minus, times
```

### Selected state

```
checked
```