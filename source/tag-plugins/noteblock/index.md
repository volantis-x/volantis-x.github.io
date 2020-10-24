---
layout: docs
group: docs-volantis-latest
order: 515
short_title: false
title:'tag-plugins: noteblock'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

NoteBlock is an enhanced version of Blockquote, with icons displayed on the left and colors can be customized. Note is a simple way of writing NoteBlock.

```md was last updated in version <u>4.0</u>
{% noteblock style parameter (optional), title (optional) %}
Text paragraph
{% endnoteblock %}
```

## Demo effect

Some complicated structures can be placed in the block, and nesting is supported.

{% noteblock, title (optional) %}

Windows 10 is not designed for everyone, but for everyone

{% noteblock done %}
Nested test: Please sit down and relax, I'm doing everything for you...
{% endnoteblock %}

{% folding yellow, Folding test: Click to see more %}

{% note warning, don't say we haven't warned you %}
{% noteblock bug red %}
We all have troubles
{% endnoteblock %}

{% endfolding %}
{% endnoteblock %}

## Source code of the above example

```md example:
{% noteblock, title (optional) %}

Windows 10 is not designed for everyone, but for everyone

{% noteblock done %}
Nested test: Please sit down and relax, I'm helping you with everything...
{% endnoteblock %}

{% folding yellow, Folding test: click to see more %}

{% note warning, don't say we haven't warned you %}
{% noteblock bug red %}
We all have troubles
{% endnoteblock %}

{% endfolding %}
{% endnoteblock %}
```

## Supportable parameters

The position of style parameters can be written with icons and colors. Multiple style parameters are separated by spaces.

### icon

```md color
quote, info, warning, done/success, error/danger
```

```md gray, color can also be specified
radiation, bug, idea, link, paperclip, todo, message, guide, download, up, undo
```

### colour

```md specify color
clear, light, gray, red, yellow, green, cyan, blue
```