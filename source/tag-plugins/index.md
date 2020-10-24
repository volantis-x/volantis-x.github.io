---
layout: docs
group: docs-volantis-latest
order: 501
title: Built-in tag plugin
short_title: 5-1 Built-in tag plugin (x23)
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

## Volantis dedicated label

### Text class

{% linkgroup %}
{% link inline text style, text %}
{% link inline text, span %}
{% link paragraph text, p %}
{% link quote, note %}
{% link quote block, noteblock %}
{% link check list, checkbox %}
{% link single-selection list, radio %}
{% link timeline, timeline %}
{% endlinkgroup %}

### Links, buttons, menus

{% linkgroup %}
{% link link card, link %}
{% link button, button %}
{% link GitHub card, ghcard %}
{% link website card, site %}
{% link drop-down menu, dropmenu %}
{% endlinkgroup %}


### Container Class

{% linkgroup %}
{% link column, tab %}
{% link folding box, folding %}
{% endlinkgroup %}


### Multimedia

{% linkgroup %}
{% link inline image, inlineimage %}
{% link single image, image %}
{% link album, gallery, gallery %}
{% link audio, audio %}
{% link video, video %}
{% link Picture video with frame, frame %}
{% link music player, aplayer %}
{% endlinkgroup %}

### Data collection class

{% linkgroup %}
{% link Issues API, issues %}
{% endlinkgroup %}


## Hexo General Tags

Use `<!-- more -->` in the article, then the text before `<!-- more -->` will be regarded as an abstract. Only this part of the text will appear on the homepage, and it will also appear in the main text. For details, see Hexo official documentation:

{% link Hexo official document #tag-plugins, https://hexo.io/docs/tag-plugins %}