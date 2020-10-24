---
layout: docs
group: docs-volantis-latest
order: 517
short_title: false
title:'tag-plugins: radio'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md was last updated in <u>2.6</u> version
{% checkbox style parameter (optional), text (support simple md) %}
```

## Demo effect

{% radio plain text test %}
{% radio checked, supports simple [markdown](https://guides.github.com/features/mastering-markdown/) syntax %}
{% radio red, support custom color %}
{% radio green, green %}
{% radio yellow, yellow %}
{% radio cyan, cyan %}
{% radio blue, blue %}

## Source code of the above example

```md example:
{% radio plain text test %}
{% radio checked, supports simple [markdown](https://guides.github.com/features/mastering-markdown/) syntax %}
{% radio red, support custom color %}
{% radio green, green %}
{% radio yellow, yellow %}
{% radio cyan, cyan %}
{% radio blue, blue %}
```

## Supportable parameters

### colour

```
red, yellow, green, cyan, blue
```

### Selected state

```
checked
```