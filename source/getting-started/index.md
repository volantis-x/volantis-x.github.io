---
layout: docs
seo_title: A feature-rich and highly modular Hexo blog theme. Supports complex systems such as multi-person collaboration and wiki documents, and supports a large number of tag plugins.
short_title: 1-1 Installation and version update
group: docs-volantis-latest
order: 1
sidebar: [docs-volantis-latest, toc]
description: Volantis is a feature-rich and highly modular Hexo blog theme. Thanks to its powerful modularity, you can easily build a minimalist style blog, or you can build a large-scale comprehensive blog with multi-person collaboration and document modules based on the official website.
---

<p>
{% span logo center large, Volantis %}
{% span center small logo, A Wonderful Theme for Hexo %}
</p>
<br>

**[Volantis](https://volantis.js.org) is a feature-rich and highly modular Hexo blog theme. Thanks to its powerful modularity, you can easily build a minimalist style blog, or you can build a large-scale comprehensive blog with multi-person collaboration and document modules based on the official website.**

{% link example blog, https://volantis.js.org/examples/ %}

All Volantis users can create their own [**Issue**](https://github.com/volantis-x/examples/issues/) according to the format to add their blog to the sample blog page of the official website.

## Ready to work


{% tabs prepare, 1 %}

<!-- tab ability conditions -->

Self-built blog requires certain relevant knowledge. Before you start, please {% u must%} make sure you can use the [markdown](https://www.runoob.com/markdown/md-tutorial.html) grammar, simple to master My git knowledge, and most importantly, know how to seek solutions when encountering difficulties:

1. Scroll through and search documents
2. Search whether there is a solution in issues
3. Create a new issue and follow the requirements to describe the problem you encountered in detail

If you haven’t used Hexo before, don’t worry, you can read through the [Hexo](https://hexo.io/zh-cn/docs/) Chinese document. If you want to use it handily, it’s best to refer to the open source project provided by the team. The source code to build:

[Demo source code](https://github.com/volantis-x/demo) ｜ [Official website source code](https://github.com/volantis-x/volantis-x.github.io)

<!-- endtab -->

<!-- tab environment configuration conditions -->

If you are updating from an old version or migrating with other themes, please make sure that the environment version is not too low, otherwise compatibility problems will occur.

```yaml
Hexo: 4.2 ~ 5.x
hexo-cli: 3.1 ~ 4.x
node.js: 12.16 ~ latest # LTS version is recommended
npm: 6.13 ~ latest
```

<!-- endtab -->

{% endtabs %}


## Quick experience

If you already have the environment configuration conditions, you can enter the following line of code in the terminal, and you can try the experience after a while:

```bash
git clone https://github.com/volantis-x/demo.git && cd demo && npm i && hexo s
```


## Download and install

{% tabs install, 1 %}

<!-- tab new blog installation -->

{% timenode Step 1/2: Modify the site configuration file %}

Find and modify in the `blog/_config.yml` file:

```
theme: volantis
```

{% endtimenode %}

{% timenode Step 2/2: Download themes %}

Type in the terminal:

```
npm i hexo-theme-volantis
```

{% endtimenode %}

{% folding, if you are a Mac user, you can use scripts to complete the entire process %}

Open the terminal in the blog path, download, install and apply the theme:

```
curl -s https://volantis.js.org/start | bash
```

This command will automatically detect and install the required environment, initialize the blog, then download, install and apply the theme.
Detailed usage of the script: [#hexo.sh](https://xaoxuu.com/wiki/hexo.sh/)

{% endfolding %}

<!-- endtab -->

<!-- tab migration from other themes -->

{% timenode Step 1/3: Modify the site configuration file %}

Find and modify in the `blog/_config.yml` file:

```
theme: volantis
```

{% endtimenode %}

{% timenode Step 2/3: Download theme %}

If you have already upgraded to `Hexo 5.0.2` and above, you can directly use the `npm` command to install:

```
npm i hexo-theme-volantis
```

For the old version, you need to download the theme source code to the `themes/` folder:

```
git clone https://github.com/volantis-x/hexo-theme-volantis themes/volantis
```

If you cannot access GitHub, you can use the domestic mirror source:

```
git clone https://e.coding.net/volantis-x/p/hexo-theme-volantis.git themes/volantis
```

{% endtimenode %}

{% timenode Step 3/3: Check and install dependencies %}

Install Hexo search dependencies:

```
npm i hexo-generator-search hexo-generator-json-content
```

Install the Stylus renderer:

```
npm i hexo-renderer-stylus
```

{% endtimenode %}

<!-- endtab -->

{% endtabs %}



## new version update

Please refer to {% btn, update log, https://github.com/volantis-x/hexo-theme-volantis/releases %} to update, the following are the things to note after the update:

{% timeline %}

{% timenode 2020-09-26 [3.0.0 -> 4.0.0](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/4.0.0) %}

{% u The configuration file of 4.0.0 has changed a lot. It is strongly recommended not to change the old configuration file. %}

1. The configuration items in the original data file are no longer supported, please set in the configuration file.
2. The theme configuration file has been redesigned and needs to be reconfigured "completely".
3. Friends chain uses data files and supports issues tags to realize dynamic self-help friends chain.
4. The original meta custom layout now only supports top_meta and bottom_meta inside the article.
5. The layout of the article list page can only be customized within a limited range.
6. The sidebar component now only supports the sidebar position; there is a dedicated component at the end of the article.
7. If the lazy loading plugin is installed, you need to uninstall it and use the lazy loading built into the theme (which conflicts with the plugin).
8. If you want to close the comments, you need to change it to `comments: false`.
9. If you want to hide the meta tag at the top or bottom of the article, you need to set `top_meta: false` or `bottom_meta: false`.
10. If you need to hide the title and the meta tag at the top at the same time, you can also change `title: xxx` to `seo_title: xxx`.
11. The information of multiple authors is defined using a data file. You only need to write ʻauthor: xxx` in the article instead of repeating the author's information.
12. Now only the pictures with the gallery tag support zooming.
13. The friend link page `layout: links` is changed to `layout: friends`.

{% endtimenode %}

{% endtimeline %}

## agreement

This theme adopts the [MIT Open Source License Agreement](https://cdn.jsdelivr.net/gh/theme-volantis/hexo-theme-volantis/LICENSE), which is free forever and unlimited use.

{% noteblock quote theme %}
**MIT Open Source License Agreement**

The authorized person has the right to use, copy, modify, merge, publish, distribute, sublicense and sell the software and copies of the software.
The licensee can modify the license terms as appropriate according to the needs of the program.
The software and all copies of the software must include a copyright notice and a license notice.
{% endnoteblock %}


## Configuration and use

{% link Configuration and use, /wiki/volantis/site-settings/configuration/, https://cdn.jsdelivr.net/gh/volantis-x/cdn-org@1.1/icon/2439351-arrows/005-arrows .svg %}
