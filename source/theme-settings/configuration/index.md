---
layout: docs
group: docs-volantis-latest
order: 301
title: Create a theme configuration file
short_title: 3-1 Create theme profile
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

The `_config.yml` file in the theme directory is usually responsible for theme-related configuration. We strongly recommend that you use a replacement theme configuration file to prevent your configuration from being lost. So how to use instead of theme configuration files?

{% timeline %}

{% timenode Step 1/2: Create configuration file %}

Create a new file next to the `_config.yml` file in the blog root directory: `_config.volantis.yml`, the configuration information in this file has priority over the configuration files in the theme folder.


{% endtimenode %}

{% timenode Step 2/2: Overwrite custom configuration %}

When you need to modify something, such as the navigation bar menu, then you need to find the relevant content in the theme configuration file and copy it into the configuration file you created:

```yaml blog/_config.volantis.yml
navbar:
  visiable: auto # always, auto
  logo: # choose [img] or [icon + title]
    img: https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/Logo-NavBar@3x.png
    icon:
    title:
  menu:
    -name: blog
      icon: fas fa-rss
      url: /
```

{% noteblock idea yellow %}
**hint**
For themes installed using "`npm i hexo-theme-volantis`", the theme configuration file is in "`blog/node_modules/hexo-theme-volantis/_config.yml`"
The theme installed in the traditional way, the theme configuration file is in "`blog/themes/volantis/_config.yml`"
{% endnoteblock %}

{% endtimenode %}

{% endtimeline %}