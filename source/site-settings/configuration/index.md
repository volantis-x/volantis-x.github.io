---
layout: docs
group: docs-volantis-latest
order: 201
title: Modify site configuration file
short_title: 2-1 Modify site configuration file
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

The `_config.yml` file in the blog root directory is usually responsible for site-related configuration and third-party npm plugin-related configuration.

## Site title

```yaml blog/_config.yml
# Site title
title: my blog
```

## Website icon


{% tabs favicon, 2 %}

<!-- tab simple way -->

```yaml blog/_config.yml
# Website icons, more sizes and other icons, please use the import method to batch import
favicon: https://cdn.jsdelivr.net/gh/xaoxuu/assets@master/favicon/favicon.ico
```

<!-- endtab -->

<!-- Tab fully customizable -->

```yaml blog/_config.yml
import:
  meta:
    -<meta name="msapplication-TileColor" content="#ffffff">
    -<meta name="msapplication-config" content="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/browserconfig.xml">
    -<meta name="theme-color" content="#ffffff">
  link:
    -<link rel="apple-touch-icon" sizes="180x180" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/apple-touch-icon. png">
    -<link rel="icon" type="image/png" sizes="32x32" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/favicon-32x32 .png">
    -<link rel="icon" type="image/png" sizes="16x16" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/favicon-16x16 .png">
    -<link rel="manifest" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/site.webmanifest">
    -<link rel="mask-icon" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/safari-pinned-tab.svg" color="#5bbad5 ">
    -<link rel="shortcut icon" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/favicon.ico">
```

<!-- endtab -->

{% endtabs %}


## Multi-language settings

```yaml blog/_config.yml
language:
  -zh-CN
  -en
  -zh-HK
  -zh-TW
```

Corresponding translation file path: `themes/volantis/languages/`

## Use Import to import external files

Volantis users can add various tags to head and body without modifying the theme file. `meta` and `link` correspond to the `<meta>` and `<link>` tags in the head. `script` can import js code at the end of body.

```yaml blog/_config.yml
import:
  meta:
    -<meta name="msapplication-TileColor" content="#ffffff">
    -<meta name="msapplication-config" content="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/browserconfig.xml">
    -<meta name="theme-color" content="#ffffff">
  link:
    -<link rel="apple-touch-icon" sizes="180x180" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/apple-touch-icon. png">
    -<link rel="icon" type="image/png" sizes="32x32" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/favicon-32x32 .png">
    -<link rel="icon" type="image/png" sizes="16x16" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/favicon-16x16 .png">
    -<link rel="manifest" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/site.webmanifest">
    -<link rel="mask-icon" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/safari-pinned-tab.svg" color="#5bbad5 ">
    -<link rel="shortcut icon" href="https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/blog/favicon/favicon.ico">
  script:
    -<script></script>
```

## More

{% link Hexo official document #Configuration, https://hexo.io/docs/configuration %}