---
layout: docs
group: docs-volantis-latest
order: 514
short_title: false
title:'tag-plugins: note'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

NoteBlock is an enhanced version of Blockquote, with icons displayed on the left and colors can be customized. Note is a simple way of writing NoteBlock.

```md was last updated in version <u>2.3</u>
{% note style parameter, text content %}
```

## Demo effect

### Classic usage

{% note, you can set the default style in the configuration file to provide the most convenient way to write a simple sentence. %}
{% note quote, note quote is suitable for quoting a paragraph %}
{% note info, note info default theme color, suitable for neutral information %}
{% note warning, note warning default yellow, suitable for warning information %}
{% note danger, note error/danger default red, suitable for dangerous information %}
{% note success, note done/success default green, information suitable for correct operation %}

### More icons

These are the default styles, you can add colors manually:

{% note radiation, note radiation default style %}
{% note radiation yellow, note radiation yellow can add color %}
{% note bug red, note bug red indicate some failures that still exist %}
{% note link green, note link green can place some links %}
{% note paperclip blue, note paperclip blue place some attachment links %}
{% note todo, note todo to-do items %}
{% note guide clear, note guide clear can add a section of guide %}
{% note download, note download can place download link %}
{% note message gray, note message gray A piece of message %}
{% note up, note up can explain how to update %}
{% note undo light, note undo light can explain how to cancel or roll back %}

## Source code of the above example

```md example:
### Classic usage

{% note, you can set the default style in the configuration file to provide the most convenient way to write a simple sentence. %}
{% note quote, note quote is suitable for quoting a paragraph %}
{% note info, note info default theme color, suitable for neutral information %}
{% note warning, note warning default yellow, suitable for warning information %}
{% note danger, note error/danger default red, suitable for dangerous information %}
{% note success, note done/success default green, information suitable for correct operation %}

### More icons

These are the default styles, you can add colors manually:

{% note radiation, note radiation default style %}
{% note radiation yellow, note radiation yellow can add color %}
{% note bug red, note bug red indicate some failures that still exist %}
{% note link green, note link green can place some links %}
{% note paperclip blue, note paperclip blue place some attachment links %}
{% note todo, note todo todo %}
{% note guide clear, note guide clear can add a section of guide %}
{% note download, note download can place download link %}
{% note message gray, note message gray A piece of message %}
{% note up, note up can explain how to update %}
{% note undo light, note undo light can explain how to cancel or roll back %}
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