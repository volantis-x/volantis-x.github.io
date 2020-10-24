---
layout: docs
group: docs-volantis-latest
order: 522
short_title: false
title:'tag-plugins: button'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

{% note warning, the label of this page will be refactored soon %}

## Basic button

Please upgrade your Volantis to version <u>2.4</u> and above.

{% tabs btn, 4 %}

<!-- tab syntax format -->

```
{% btn style parameters (optional), title, link, icon (optional) %}
```

{% note warning, optional parameters can be omitted, but the order cannot be disordered. %}

<!-- endtab -->

<!-- tab parameter list -->

{% p subtitle, style parameter %}

```
regular, large, center
```

{% p subtitle, icon %}

The one with `fa-` in the first or second parameter is recognized as an icon.


<!-- endtab -->

<!-- Tab example writing -->

```md example.md:
The {% btn button, / %} without any parameters is suitable for integration into the paragraph.

The regular button is suitable for being independent of the paragraph:

{% btn regular, sample blog, https://xaoxuu.com, fas fa-play-circle %}

The large button is more emphasized, it is recommended to use it with center:

{% btn center large, get started, https://volantis.js.org/v3/getting-started/, fas fa-download %}
```

<!-- endtab -->

<!-- tab sample effect -->

{% p subtitle, inline button %}

{% btn button, / %} without any parameters is suitable to be integrated into the paragraph.

{% p subtitle, hollow button %}

{% btn regular, sample blog, /, fas fa-rss %} {% btn regular, sample blog,, fas fa-rss %}

{% btn regular large, sample blog, /, fas fa-rss %} {% btn regular large, sample blog,, fas fa-rss %}

Centered:

{% btn center large, get started, https://volantis.js.org/v3/getting-started/, fas fa-download %}

{% p subtitle, solid button %}

{% btn solid, sample blog, /, fas fa-rss %} {% btn solid, sample blog,, fas fa-rss %}

{% btn solid large, sample blog, /, fas fa-rss %} {% btn solid large, sample blog,, fas fa-rss %}

Centered:

{% btn solid center large, get started, https://volantis.js.org/v3/getting-started/, fas fa-download %}

<!-- endtab -->

{% endtabs %}


## Rich Text Button

Please upgrade your Volantis to version <u>2.3</u> and above.

{% tabs btns, 4 %}

<!-- tab syntax format -->

```
{% btns style parameter %}
{% cell title, link, picture or icon %}
{% cell title, link, picture or icon %}
{% endbtns %}
```

<!-- endtab -->

<!-- tab parameter list -->

The style parameter position can write the picture style, layout method, multiple style parameters are separated by spaces.

{% p subtitle, rounded corner style %}

The default is square

```
rounded, circle
```


{% p subtitle, layout method %}

The default is automatic width, which is suitable for situations where there is only one or two in the field of view.

{% table %}
| Parameters | Meaning |
| :-- | :-- |
| wide | Wider buttons |
| fill | Fill the layout, automatically fill at least one line, and will wrap if there is more. |
| center | Centered, with fixed spacing between buttons. |
| around | Centered and scattered |
| grid2 | The same width is up to 2 columns, and the narrower screen will reduce the number of columns appropriately. |
| grid3 | The same width is up to 3 columns, and the narrower screen will reduce the number of columns appropriately. |
| grid4 | Up to 4 columns with equal width, narrower screen will reduce the number of columns appropriately. |
| grid5 | The same width is up to 5 columns. The narrower screen will reduce the number of columns appropriately. |
{% endtable %}

{% p subtitle, add text style %}

You can add `<b>title</b>` and `<p>description text</p>` in the container

<!-- endtab -->

<!-- Tab example writing -->

If you need to display a group of links containing avatars like "team members":

```md example.md:
{% btns circle grid5 %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% endbtns %}
```

Or buttons with icons:

```md example.md:
{% btns rounded grid5 %}
{% cell download source code, /, fas fa-download %}
{% cell view document, /, fas fa-book-open %}
{% endbtns %}
```

Circular icon + title + description + picture + grid 5 columns + center

```md example.md:
{% btns circle center grid5 %}
<a href='https://apps.apple.com/cn/app/heart-mate-pro-hrm-utility/id1463348922?ls=1'>
  <i class='fab fa-apple'></i>
  <b>Heart Rate Manager</b>
  {% p red, professional edition %}
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_pro.png'>
</a>
<a href='https://apps.apple.com/cn/app/heart-mate-lite-hrm-utility/id1475747930?ls=1'>
  <i class='fab fa-apple'></i>
  <b>Heart Rate Manager</b>
  {% p green, free version %}
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_lite.png'>
</a>
{% endbtns %}
```

<!-- endtab -->

<!-- tab example effect -->

If you need to display a group of links containing avatars like "team members":
{% btns circle grid5 %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% cell xaoxuu, https://xaoxuu.com, https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png %}
{% endbtns %}

Or buttons with icons:
{% btns rounded grid5 %}
{% cell download source code, /, fas fa-download %}
{% cell view document, /, fas fa-book-open %}
{% endbtns %}


Circular icon + title + description + picture + grid 5 columns + center
{% btns circle center grid5 %}
<a href='https://apps.apple.com/cn/app/heart-mate-pro-hrm-utility/id1463348922?ls=1'>
  <i class='fab fa-apple'></i>
  <b>Heart Rate Manager</b>
  {% p red, professional edition %}
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_pro.png'>
</a>
<a href='https://apps.apple.com/cn/app/heart-mate-lite-hrm-utility/id1475747930?ls=1'>
  <i class='fab fa-apple'></i>
  <b>Heart Rate Manager</b>
  {% p green, free version %}
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_lite.png'>
</a>
{% endbtns %}

<!-- endtab -->

{% endtabs %}