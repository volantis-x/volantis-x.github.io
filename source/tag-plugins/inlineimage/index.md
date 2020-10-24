---
layout: docs
group: docs-volantis-latest
order: 541
short_title: false
title:'tag-plugins: inlineimage'
sidebar: [docs-volantis-latest, toc]
disqus:
   path: /wiki/volantis/
---

Inlineimage tag is a kind of inline image tag, which can be used to insert emoticons in the middle of a paragraph.

```md This plugin was last updated in version <u>4.0</u>
{% inlineimage image link, height=height (optional) %}
```

## Demo effect

This is a passage from {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/0000.gif %}.

This is another paragraph of {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/5150.gif, height=40px %}.


## Source code of the above example

```md example:
This is a passage from {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/0000.gif %}.

This is another paragraph of {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/5150.gif, height=40px %}.
```

## Supportable parameters

### Height

```
height=20px
```