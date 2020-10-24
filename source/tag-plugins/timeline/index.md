---
layout: docs
group: docs-volantis-latest
order: 518
short_title: false
title:'tag-plugins: timeline'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md was last updated in version <u>3.0</u>
{% timeline title (optional) %}

{% timenode time node (title) %}

Text content

{% endtimenode %}

{% timenode time node (title) %}

Text content

{% endtimenode %}

{% endtimeline %}
```

## Demo effect

{% timeline %}

{% timenode 2020-07-24 [2.6.6 -> 3.0](https://github.com/volantis-x/hexo-theme-volantis/releases) %}

1. If there is a `hexo-lazyload-image` plugin, you need to delete and reinstall the latest version, set `lazyload.isSPA: true`.
2. The 2.x version of css and js are not applicable to the 3.x version. If you use ʻuse_cdn: true`, you need to delete them.
3. The fancybox tag of the 2.x version was renamed to gallery in the 3.x version.
4. In the 2.x version, the top `top: true` is changed to `pin: true`, and it is also applicable to the page of `layout: page`.
5. If you use the `hexo-offline` plug-in, it is recommended to uninstall it. The pjax service is enabled by default in version 3.0.

{% endtimenode %}

{% timenode 2020-05-15 [2.6.3 -> 2.6.6](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.6) %}

No additional processing is required.

{% endtimenode %}

{% timenode 2020-04-20 [2.6.2 -> 2.6.3](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.3) %}

1. Search globally for `seotitle` and replace with `seo_title`.
2. The index rule of the group component has changed. In the article using the group component, the component name corresponding to `group: group_name` must be `group_name`.
2. The list name of the group component first displays the article's `short_title` followed by `title`.

{% endtimenode %}

{% endtimeline %}

## Source code of the above example

```md example:
{% timeline %}

{% timenode 2020-07-24 [2.6.6 -> 3.0](https://github.com/volantis-x/hexo-theme-volantis/releases) %}

1. If there is a `hexo-lazyload-image` plugin, you need to delete and reinstall the latest version, set `lazyload.isSPA: true`.
2. The 2.x version of css and js are not applicable to the 3.x version. If you use ʻuse_cdn: true`, you need to delete them.
3. The 2.x version of the fancybox label was renamed to gallery in the 3.x version.
4. In the 2.x version, the top `top: true` is changed to `pin: true`, and it is also applicable to the page of `layout: page`.
5. If the `hexo-offline` plug-in is used, it is recommended to uninstall it. The pjax service is enabled by default in version 3.0.

{% endtimenode %}

{% timenode 2020-05-15 [2.6.3 -> 2.6.6](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.6) %}

No additional processing is required.

{% endtimenode %}

{% timenode 2020-04-20 [2.6.2 -> 2.6.3](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.3) %}

1. Search globally for `seotitle` and replace with `seo_title`.
2. The indexing rules of the group component have changed. In articles using the group component, the component name corresponding to `group: group_name` must be `group_name`.
2. The list name of the group component first displays the `short_title` of the article followed by `title`.

{% endtimenode %}

{% endtimeline %}
```