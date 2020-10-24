---
layout: docs
group: docs-volantis-latest
order: 523
short_title: false
title:'tag-plugins: ghcard'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md was last updated in version <u>4.0</u>
{% ghcard username, other parameters (optional) %}
{% ghcard username/warehouse, other parameters (optional) %}
```

## User Information Card

| {% ghcard xaoxuu %} | {% ghcard xaoxuu, theme=vue %} |
| - | - |
| {% ghcard xaoxuu, theme=buefy %} | {% ghcard xaoxuu, theme=solarized-light %} |
| {% ghcard xaoxuu, theme=onedark %} | {% ghcard xaoxuu, theme=solarized-dark %} |
| {% ghcard xaoxuu, theme=algolia %} | {% ghcard xaoxuu, theme=calm %} |

The source code of the above example:

```md example:
| {% ghcard xaoxuu %} | {% ghcard xaoxuu, theme=vue %} |
| - | - |
| {% ghcard xaoxuu, theme=buefy %} | {% ghcard xaoxuu, theme=solarized-light %} |
| {% ghcard xaoxuu, theme=onedark %} | {% ghcard xaoxuu, theme=solarized-dark %} |
| {% ghcard xaoxuu, theme=algolia %} | {% ghcard xaoxuu, theme=calm %} |
```

## Warehouse Information Card

| {% ghcard volantis-x/hexo-theme-volantis %} | {% ghcard volantis-x/hexo-theme-volantis, theme=vue %} |
| - | - |
| {% ghcard volantis-x/hexo-theme-volantis, theme=buefy %} | {% ghcard volantis-x/hexo-theme-volantis, theme=solarized-light %} |
| {% ghcard volantis-x/hexo-theme-volantis, theme=onedark %} | {% ghcard volantis-x/hexo-theme-volantis, theme=solarized-dark %} |
| {% ghcard volantis-x/hexo-theme-volantis, theme=algolia %} | {% ghcard volantis-x/hexo-theme-volantis, theme=calm %} |

The source code of the above example:

```md example:
| {% ghcard volantis-x/hexo-theme-volantis %} | {% ghcard volantis-x/hexo-theme-volantis, theme=vue %} |
| - | - |
| {% ghcard volantis-x/hexo-theme-volantis, theme=buefy %} | {% ghcard volantis-x/hexo-theme-volantis, theme=solarized-light %} |
| {% ghcard volantis-x/hexo-theme-volantis, theme=onedark %} | {% ghcard volantis-x/hexo-theme-volantis, theme=solarized-dark %} |
| {% ghcard volantis-x/hexo-theme-volantis, theme=algolia %} | {% ghcard volantis-x/hexo-theme-volantis, theme=calm %} |
```

## More parameter options

{% link GitHub card API parameters, https://github-readme-stats.vercel.app %}