---
layout: docs
title: Select comment system
group: docs-volantis-latest
order: 308
short_title: 3-8 Select comment system
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

The currently supported comment systems are: Valine, MiniValine, Disqus, Gitalk, Vssue, Livere, Isso, Hashover

```yaml blog/_config.volantis.yml
comments:
  title: <i class='fas fa-comments'></i> Comments
  subtitle:
  service: valine # valine, minivaline, disqus, gitalk, vssue, livere, isso, hashover
```

{% tabs comments-1, 1 %}

<!-- tab Valine -->

<i class='fas fa-comment-dots fa-fw'></i> A fast, concise and efficient no back-end comment system
<i class='fas fa-globe fa-fw'></i> [https://valine.js.org](https://valine.js.org)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: valine
  ...
  valine:
    appId: # your appId
    appKey: # your appKey
    js: https://cdn.jsdelivr.net/npm/valine@1.4/dist/Valine.min.js
    ... See the source code for optional configuration items
```

Among them, `placeholder` supports setting in front-matter.

```yaml front-matter
---
valine:
  placeholder: What do you think of xxx?
---
```

You can also share a comment box for multiple pages by setting `valine.path`.

```yaml front-matter
---
valine:
  path: /wiki/volantis/
---
```

<!-- endtab -->

<!-- tab MiniValine -->

<i class='fas fa-comment-dots fa-fw'></i> A fast, concise and efficient no back-end comment system
<i class='fas fa-globe fa-fw'></i> [https://github.com/MiniValine/MiniValine/](https://github.com/MiniValine/MiniValine/)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: minivaline
  ...
  minivaline:
    appId: # Your leancloud application appid
    appKey: # Your leancloud application appkey
    ... See source code for optional configuration items
```

<!-- endtab -->

<!-- tab Vssue -->

<i class='fas fa-comment-dots fa-fw'></i> Vue-driven, Issue-based comment plugin
<i class='fas fa-globe fa-fw'></i> [https://vssue.js.org/zh/](https://vssue.js.org/zh/)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: vssue
  ...
  vssue:
    owner:
    repo:
    clientId:
    clientSecret:
```

<!-- endtab -->

<!-- tab Gitalk -->

<i class='fas fa-comment-dots fa-fw'></i> A modern comment component based on Github Issue and Preact.
<i class='fas fa-globe fa-fw'></i> [https://gitalk.github.io/](https://gitalk.github.io/)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: gitalk
  ...
  gitalk:
    clientID:
    clientSecret:
    repo:
    owner:
    admin: # []
```

The method of obtaining clientID and clientSecret can be searched for the tutorial by yourself, here is only a brief description of the steps:
1. Click GitHub -> Settings `https://github.com/settings/profile`
2. Click Developer settings `https://github.com/settings/developers`
3. Click New OAuth App `https://github.com/settings/applications/new`
4. Fill in the information:
**Application name** Fill in whatever you want, mine is: `xaoxuu.com`
**Homepage URL** and **Authorization callback URL** both write your URL, mine is: `https://xaoxuu.com`

**You can share a comment box on multiple pages by setting gitalk.id. **

```yaml front-matter
---
gitalk:
  id: /wiki/volantis/
---
```

<!-- endtab -->

<!-- tab Disqus -->

<i class='fas fa-comment-dots fa-fw'></i> Disqus-The #1 way to build an audience on your website.
<i class='fas fa-globe fa-fw'></i> [https://disqus.com/](https://disqus.com/)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: disqus
  ...
  disqus:
    shortname:
```

<!-- endtab -->

<!-- tab Livere -->

<i class='fas fa-comment-dots fa-fw'></i> Communication makes better world.
<i class='fas fa-globe fa-fw'></i> [https://www.livere.com/](https://www.livere.com/)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: livere
  ...
  livere:
    uid: #Your livere's uid
```

Check your uid here: `https://livere.com/insight/myCode`, find the following code in [Code Management -> General Website], where the content in `data-uid` is yours` livere_uid`.

```html
<!-- Labilee City version installation code -->
<div id="lv-container" data-id="city" data-uid="Your livere’s uid">
...
```

<!-- endtab -->

<!-- tab Isso -->

<i class='fas fa-comment-dots fa-fw'></i> A commenting server similar to Disqus.
<i class='fas fa-globe fa-fw'></i> [https://posativ.org/isso/](https://posativ.org/isso/)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: isso
  ...
  isso:
    url: https://example.com/[path/)
    src: https://example.com/[path/)js/embed.min.js
```

<!-- endtab -->

<!-- tab Hashover -->


<i class='fas fa-comment-dots fa-fw'></i> A free and open source PHP comment system designed to allow completely anonymous comments and easy theming.
<i class='fas fa-globe fa-fw'></i> [https://www.barkdull.org/software/hashover](https://www.barkdull.org/software/hashover)

```yaml blog/_config.volantis.yml
comments:
  ...
  service: hashover
  ...
  hashover:
    src: https://example.com/[path/)comments.php
```

<!-- endtab -->

<!-- tab ... -->


```plain blog/themes/volantis/layout/_third-party/comments/comment system name/layout.ejs
Write layout code here
```

```plain blog/themes/volantis/layout/_third-party/comments/comment system name/script.ejs
Here to write the code to load js
```

{% btn large center, contains more comment systems, https://github.com/volantis-x/, fas fa-plus %}

<!-- endtab -->

{% endtabs %}