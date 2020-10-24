---
layout: docs
group: docs-volantis-latest
order: 546
short_title: false
title:'tag-plugins: frame'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

This is a label that can put pictures or videos into the device frame, which can be used to display screenshots and screen recordings more elegantly.

```md This plugin was last updated in version <u>4.0</u>
{% frame frame name | img=picture link | alt=picture description (optional) | part=top/bottom (optional) %}
{% frame frame name | video=video link | part=top/bottom (optional) %}
```

<br>

{% frame iphone11 | img=https://gitee.com/xaoxuu/cdn-assets/raw/master/wiki/prohud/toast-loading@2x.jpg | video=https://gitee.com/xaoxuu/cdn -assets/raw/master/wiki/prohud/toast-loading@2x.mov | part=top %}

```
{% frame iphone11 | img=https://gitee.com/xaoxuu/cdn-assets/raw/master/wiki/prohud/toast-loading@2x.jpg | video=https://gitee.com/xaoxuu/cdn -assets/raw/master/wiki/prohud/toast-loading@2x.mov | part=top %}
```

In this example, both ʻimg` and `video` appear at the same time, then it is a video with a cover, and the video cover will be displayed before the video is loaded.

## Device Framework

Currently supported are:

```
iphone11
```

If you have the following other equipment frame diagrams (svg), welcome PR compatibility.

```
android, ipad, macbook, watch
```

## Tailoring

Set `part=top` or `part=bottom` to display the upper or lower part, otherwise the complete frame and the pictures/videos in it will be displayed.