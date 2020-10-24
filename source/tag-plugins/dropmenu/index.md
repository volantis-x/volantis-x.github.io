---
layout: docs
group: docs-volantis-latest
order: 525
short_title: false
title:'tag-plugins: dropmenu'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

{% note warning, the label of this page will be refactored soon %}



## Drop-down menu

Please upgrade your Volantis to version <u>3.0</u> and above.

{% tabs menu, 3 %}

<!-- tab syntax format -->

{% p subtitle, container %}

```md
{% menu prefix (can be omitted), title, suffix (can be omitted) %}
Menu content
{% endmenu %}
```

{% p subtitle, menu content %}

Menu Item

```md
{% menuitem text, link, icon %}
```

Dividing line

```md
{% menuitem hr %}
```

Submenu

```md
{% submenu Nested menu, icon %}
Menu content
{% endsubmenu %}
```

<!-- endtab -->

<!-- Tab example writing -->

{% p subtitle, example 1 %}

```md
{% menu drop-down menu %}
{% menuitem theme source code, https://github.com/volantis-x/hexo-theme-volantis/, fas fa-file-code %}
{% menuitem update log, https://github.com/volantis-x/hexo-theme-volantis/releases/, fas fa-clipboard-list %}
{% menuitem hr %}
{% submenu Have questions? , fas fa-question-circle %}
{% menuitem see FAQ, /faqs/ %}
{% menuitem see the source code of this site, https://github.com/volantis-x/volantis-docs/ %}
{% menuitem raise an Issue, https://github.com/volantis-x/hexo-theme-volantis/issues/ %}
{% endsubmenu %}
{% endmenu %}
```

{% p subtitle, example 2 %}

```md
{% menu this is, drop-down menu %}
(Same as above)
{% endmenu %}
```

{% p subtitle, example 3 %}

```md
{% menu This is the example effect of the drop-down menu. %}
(Same as above)
{% endmenu %}
```

<!-- endtab -->

<!-- tab example effect -->

{% p subtitle, example 1 %}

{% menu drop-down menu %}
{% menuitem theme source code, https://github.com/volantis-x/hexo-theme-volantis/, fas fa-file-code %}
{% menuitem update log, https://github.com/volantis-x/hexo-theme-volantis/releases/, fas fa-clipboard-list %}
{% menuitem hr %}
{% submenu Have questions? , fas fa-question-circle %}
{% menuitem see FAQ, /faqs/ %}
{% menuitem see the source code of this site, https://github.com/volantis-x/volantis-docs/ %}
{% menuitem raise an Issue, https://github.com/volantis-x/hexo-theme-volantis/issues/ %}
{% endsubmenu %}
{% endmenu %}

{% p subtitle, example 2 %}

{% menu this is, drop-down menu %}
{% menuitem theme source code, https://github.com/volantis-x/hexo-theme-volantis/, fas fa-file-code %}
{% menuitem update log, https://github.com/volantis-x/hexo-theme-volantis/releases/, fas fa-clipboard-list %}
{% menuitem hr %}
{% submenu Have questions? , fas fa-question-circle %}
{% menuitem see FAQ, /faqs/ %}
{% menuitem see the source code of this site, https://github.com/volantis-x/volantis-docs/ %}
{% menuitem raise an Issue, https://github.com/volantis-x/hexo-theme-volantis/issues/ %}
{% endsubmenu %}
{% endmenu %}

{% p subtitle, example 3 %}

{% menu This is the example effect of the drop-down menu. %}
{% menuitem theme source code, https://github.com/volantis-x/hexo-theme-volantis/, fas fa-file-code %}
{% menuitem update log, https://github.com/volantis-x/hexo-theme-volantis/releases/, fas fa-clipboard-list %}
{% menuitem hr %}
{% submenu Have questions? , fas fa-question-circle %}
{% menuitem see FAQ, /faqs/ %}
{% menuitem see the source code of this site, https://github.com/volantis-x/volantis-docs/ %}
{% menuitem raise an Issue, https://github.com/volantis-x/hexo-theme-volantis/issues/ %}
{% endsubmenu %}
{% endmenu %}

<!-- endtab -->

{% endtabs %}