---
layout: page
title: FAQ
pid: faq
body: [article, comments]
cover: true
sidebar: []
---

Generally speaking, a brand new project using the default configuration is <green>normal</green> without failure. If it is not available or the effect is quite different from the example, you can use the official Hexo blog for unit testing to apply this topic to check whether the style is normal, and compare the `_config.yml` file to troubleshoot problems.

{% note warning yellow, Hexo official unit test project: [https://github.com/hexojs/hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test ) %}

<br>{% btn solid large center, feedback issues to developers, https://github.com/volantis-x/hexo-theme-volantis/issues/, fas fa-paper-plane %}

<!-- more -->

## How to update the theme

When using themes, try to fork the theme to your GitHub, then modify and use it. The advantage of this is that when the theme undergoes an important update, you can pull and merge the code as needed, so that your DIY theme can get BUG fixes or new features through the update.

If you don’t understand, please search for keywords yourself: <u>fork update</u>

{% noteblock idea, practical tips %}

All the configuration that needs to be written in the theme configuration file can be written in the `theme_config:` of the site configuration file, after {% u Hexo 5.0 %}, it can also be written in the file `_config.volantis.yml`, see details Hexo official documents:
{% link covers theme configuration, https://hexo.io/docs/configuration#%E8%A6%86%E7%9B%96%E4%B8%BB%E9%A2%98%E9% 85%8D%E7%BD%AE %}

You can also directly view the wording of the site configuration file in the source code of this site: [_config.volantis.yml](https://github.com/volantis-x/volantis-x.github.io/blob/master/_config.volantis.yml)

{% endnoteblock %}

## Unable to run local preview successfully

- There may be no installation dependencies. Please follow the steps on the "Start" page to install and install the required dependencies.
- If some third-party services are enabled, please check whether the installation of plug-ins is required in the documentation.
- If the error message has `lastIndex`, you can try to find `highlight` in the blog root directory configuration file and set ʻauto_detect` to `false`.


## Theme configuration modification does not take effect

Please confirm whether the document requires modification to the configuration file `blog/_config.yml` of the blog home directory or the theme configuration file `blog/_config.volantis.yml`.

## Theme style modification does not take effect

If the cdn service is enabled in the theme configuration file, then the modification of the local style will not take effect, and the cdn service needs to be disabled.

## The modification did not take effect

Requires `hexo clean` and then restarts `hexo s`

If you install the "Related Article Recommendations" plugin, you need to re-`hexo s` every time you modify the md file

## The style is messy after turning off the CDN

- Please go to the "Start" page of the document to check whether the necessary dependencies are installed.

## Search is not available

- Please go to the "Start" page of the document to check whether the necessary dependencies are installed.
- Check the root directory configuration file for conflicts with `search` fields.
- If the problem cannot be found in the above two steps, please download the sample source code for comparison.

## The search result link is incorrect

Please check whether the link in the root directory configuration file is correct, such as:

```yaml blog/_config.yml
url: https://xaoxuu.com
root: /
```

<br><br>

{% folding open, tutorials and guides %}

[Hexo official document](https://hexo.io) | [Valine official document](https://valine.js.org)

Please be sure to read the official documentation!

{% image https://cdn.jsdelivr.net/npm/alus@latest/8080.png, width=800px %}

{% endfolding %}