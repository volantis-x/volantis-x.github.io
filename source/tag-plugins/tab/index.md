---
layout: docs
group: docs-volantis-latest
order: 531
short_title: false
title:'tag-plugins: tab'
sidebar: [docs-volantis-latest, toc]
disqus:
   path: /wiki/volantis/
---

This plugin is ported from [NexT #tabs](https://theme-next.org/docs/tag-plugins/tabs)

```md was last updated to version <u>2.1</u>
{% tabs unique ID in the page %}
<!-- tab column 1 -->
content
<!-- endtab -->
<!-- tab column 2 -->
content
<!-- endtab -->
{% endtabs %}
```

## Demo effect

{% tabs tab-id %}

<!-- tab column 1 -->

. . .

<!-- endtab -->

<!-- tab column 2 -->

! ! !

<!-- endtab -->

{% endtabs %}

## Source code of the above example

```md example:
{% tabs tab-id %}

<!-- tab column 1 -->

. . .

<!-- endtab -->

<!-- tab column 2 -->

! ! !

<!-- endtab -->

{% endtabs %}
```