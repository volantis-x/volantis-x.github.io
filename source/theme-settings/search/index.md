---
layout: docs
title: site search
group: docs-volantis-latest
order: 309
short_title: 3-9 site search
sidebar: [docs-volantis-latest, toc]
disqus:
   path: /wiki/volantis/
---

```yaml blog/_config.volantis.yml
search:
   enable: true
   service: hexo # hexo, google, algolia, azure, baidu
   js: https://cdn.jsdelivr.net/gh/volantis-x/cdn-volantis@2.6.4/js/search.js
   google:
     apiKey:
     engineId:
   algolia:
     applicationID:
     apiKey:
     indexName:
   azure:
     serviceName:
     indexName:
     queryKey:
   baidu:
     apiId:
```
The default configuration is Hexo search, but you need to install a plug-in to use it:
```sh
npm i -S hexo-generator-search hexo-generator-json-content
```