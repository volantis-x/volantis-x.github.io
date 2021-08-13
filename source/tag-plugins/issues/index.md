---
layout: docs
group: docs-volantis-latest
order: 551
short_title: false
title:'tag-plugins: issues'
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

```md was last updated in version <u>4.0</u>
{% issues type | api=url | group=key:value1,value2(optional) %}
```

## Types of

According to different requirements, the content of issues will be parsed into different HTML tags. The currently supported types are:

-**timeline**: parsed into timeline tags, the title of the issue corresponds to the time of the timeline, and the content of the issue corresponds to the content of the timeline.
-**sites**: parsed into sites tag, need JSON code block:
  ```json
  {
      "title": "",
      "screenshot": "",
      "url": "",
      "avatar": "",
      "description": "",
      "keywords": ""
  }
  ```

## API

Pass a URL that can be transferred, for example:
```
api=https://gitee.com/api/v5/repos/xaoxuu/friends/issues?sort=updated&state=open&page=1&per_page=100&labels=active
api=https://api.github.com/repos/xaoxuu/friends/issues?sort=updated&state=open&page=1&per_page=100&labels=active
```

## Group

The issues of the site type are not grouped by default. If you need to group, you can specify the grouping basis "key", and the grouping whitelist "value1" "value2", etc., for example:

```
group=version:v4,v3,v2
```

The function of this parameter is to filter out the data that contains `"version": "v4"` or `"version": "v3"` or `"version": "v2"` in JSON and display them in groups.


## Example

### timeline

```
{% issues timeline | api=https://gitee.com/api/v5/repos/xaoxuu/timeline/issues?state=open&creator=xaoxuu&sort=created&direction=desc&page=1&per_page=100 %}
```


Corresponding warehouse link:

{% link Gitee: xaoxuu/timeline, https://gitee.com/xaoxuu/timeline/issues %}


### Friends chain

```
{% issues sites | api=https://gitee.com/api/v5/repos/xaoxuu/friends/issues?sort=updated&state=open&page=1&per_page=100&labels=active %}
{% issues sites | api=https://api.github.com/repos/xaoxuu/friends/issues?sort=updated&state=open&page=1&per_page=100&labels=active %}
```

The `labels=active` parameter in the above example can control the default issue not to be displayed, and it will only be displayed after the ʻactive` label is added after the self-review. The warehouse link corresponding to the above example:

{% link GitHub: xaoxuu/friends, https://github.com/xaoxuu/friends/issues %}

### Group

This is the data of the "Sample Blog" page of the theme's official website:

```
{% issues sites | api=https://api.github.com/repos/volantis-x/examples/issues?sort=updated&state=open&page=1&per_page=100 | group=version:版本：^4.0,版本：^3.0,版本：^2.0 %}
```

The warehouse link corresponding to the above example:

{% link GitHub: volantis-x/examples, https://github.com/volantis-x/examples/issues %}