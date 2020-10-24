---
layout: docs
group: docs-volantis-latest
order: 601
title: advanced settings
short_title: 6-1 advanced settings
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

## Set up submodule

{% folding yellow open, add the theme as a submodule %}

```sh
git submodule add https://github.com/volantis-x/hexo-theme-volantis.git themes/volantis
```

{% endfolding %}

## Multiplayer collaboration

The default author information is set in the theme configuration file:

```yaml blog/themes/volantis/_config.yml
# Article layout
article:
  ...
  body:
    ...
    meta_library:
      author:
        avatar:
        name: Please set the author of the article
        url: /
```

Volantis supports multiple authors, other author information needs to be written in the data file, for example:

```yaml blog/source/_data/author.yml
Jon:
  name: Jon Snow
  avatar: https://cn.bing.com/th?id=AMMS_fc8f99fd41ebd737a71c4e13806db9a0&w=110&h=110&c=7&rs=1&qlt=80&pcl=f9f9f9&cdv=1&dpr=2&pid=16.1
  url: https://gameofthrones.fandom.com/wiki/Jon_Snow
Dany:
  name: Daenerys Targaryen
  avatar: https://tse1-mm.cn.bing.net/th?id=OIP.Yax4wLzIFbcBVUa_RsKywQHaLH&w=80&h=80&c=8&rs=1&qlt=90&dpr=2&pid=3.1&rm=2
  url: https://gameofthrones.fandom.com/wiki/Daenerys_Targaryen
```

Just add ʻauthor` to the front-matter of the article:

```md
---
title: Jon Snow | Game of Thrones Wiki | Fandom
author: Jon
---
```

## Speed ​​up the website

### Loading speed

-Reduce unnecessary js plugins, such as word count, dynamic background.

-Find and solve the slow down resources, take Chrome browser as an example:
  1. Right-click on the page and select "Check".
  2. In the right window, "Network" tab, and check "Disable cache".
  3. Refresh the web page to view resources that load slowly.
    3.1. For slow loading pictures, CDN is recommended.
    3.2. It is recommended to discard the js plugins that load slowly and do not need to.
    3.3. The js plug-in that is slow to load but must be used is recommended to download and upload to jsdelivr.

### Running speed

-When visiting a website with dynamic special effects backgrounds (such as snowflakes, particles, etc.), the phone will soon become hot and get stuck, the notebook will soon fan out and the browser prompts to close this page. If you want the website to have a good experience, please try not to install such plug-ins.



## Optimize SEO

```yaml blog/_config.volantis.yml
seo:
  # When there are no keywords in the article's front-matter, use tags as keywords.
  use_tags_as_keywords: true
  # When there is no description in the article's front-matter, use excerpt as the description.
  use_excerpt_as_description: true
  robots:
    home_first_page: index,follow
    home_other_pages: noindex,follow
    archive: noindex,follow
    category: noindex,follow
    tag: noindex,follow
    # robots can be written in front-matter
```

In front-matter, you can set `keywords`, `description`, `robots` and `seo_title`. Among them, `seo_title` is only used as the title of the webpage and has a higher priority than `title`.

-Do not use H1 headings inside articles.

-Check and delete the inaccessible links through the dead link detection tool.

-Install SEO optimization plugin:
  {% link hexo-autonofollow, https://github.com/liuzc/hexo-autonofollow %}
  {% link hexo-generator-seo-friendly-sitemap, https://github.com/ludoviclefevre/hexo-generator-seo-friendly-sitemap %}

-Don't pile up keywords on the page and don't change the path frequently.

## Use CDN

For most users who deploy blogs to GitHub, it is relatively slow to load local resources directly. You can use the CDN service provided by jsdelivr for open source projects.

For the `4.1.4+` version, the JS file uses the CDN compressed version of https://cdn.jsdelivr.net/npm/hexo-theme-volantis/source/js/ by default.

For example: `https://cdn.jsdelivr.net/npm/hexo-theme-volantis@4.1.4/source/js/app.min.js`
### How to open

```yaml blog/_config.volantis.yml
use_cdn: true
```

important:

1. Developers note that ʻuse_cdn` is set to `false`.
2. Pay attention to the version number of the CDN file:
```yaml blog/_config.volantis.yml
info:
  theme_version: '4.1.4' # This is theme's version.
```
3. Only JS files provide CDN by default.
4. About CSS file CDN:
```yaml blog/_config.volantis.yml
info:
  theme_name: Volantis # This is theme's name.
  theme_version: '4.1.4' # This is theme's version.
  theme_docs: https://volantis.js.org/ # This is theme's URL.
  theme_repo: https://github.com/volantis-x/hexo-theme-volantis
  cdn:
    js: # The default is https://cdn.jsdelivr.net/npm/hexo-theme-volantis@4.1.4/source/js/app.min.js
    css:
      first: # CDN is not provided by default. First.css is the style rendered for the first screen, and contains the style of cover navbar search.
      style: # CDN is not provided by default, and style.css is a delayed loading style.
```

{% note info, if you need to DIY the style, you can just turn off the CDN of the style file. %}

### Custom CDN

If you upload the corresponding file to your CDN server, you can change the corresponding link to your own CDN link.

## Try Terser to compress ES6

### Install compression tool

```shell
npm install -g gulp
npm install --save gulp
npm install --save gulp-html-minifier-terser
npm install --save gulp-htmlclean
npm install --save gulp-htmlmin
npm install --save gulp-minify-css
npm install gulp-terser --save-dev
```

### gulp configuration file

```js blog/gulpfile.js
var gulp = require('gulp');
var minifycss = require('gulp-minify-css');
var htmlmin = require('gulp-html-minifier-terser');
var htmlclean = require('gulp-htmlclean');
var terser = require('gulp-terser');

// Compress the css file
const minify_css = () => (
    gulp.src(['./public/**/*.css'])
        .pipe(minifycss())
        .pipe(gulp.dest('./public'))
);

// Compress html file
const minify_html = () => (
    gulp.src(['./public/**/*.html','!./public/{lib,lib/**}'])
        .pipe(htmlclean())
        .pipe(htmlmin({
            removeComments: true,
            minifyJS: true,
            minifyCSS: true,
            minifyURLs: true,
        }))
        .pipe(gulp.dest('./public'))
)

// Compress the js file
const minify_js = () => (
    gulp.src(['./public/**/*.js','!./public/**/*.min.js','!./public/{lib,lib/**}'] )
        .pipe(terser())
        .pipe(gulp.dest('./public'))
)

module.exports = {
    minify_html: minify_html,
    minify_css: minify_css,
    minify_js: minify_js
};
gulp.task('one', gulp.parallel(
    minify_html,
    minify_css,
    minify_js
))

gulp.task('default', gulp.series('one'));
```
### Run compression

```shell
gulp
```

## Install Service Worker Service

```yaml blog/_config.yml
# Global import
import:
  script:
    -<script>"serviceWorker"in navigator&&navigator.serviceWorker.register("/sw.js").then(function(n){n.onupdatefound=function(){var e=n.installing;e.onstatechange=function( ){switch(e.state){case"installed":navigator.serviceWorker.controller?console.log("Updated serviceWorker."):console.log("serviceWorker Sucess!");break;case"redundant":console .log("The installing service worker became redundant.")}}}}).catch(function(e){console.log("Error during service worker registration:",e)}); </script>
```

Create the `sw.js` file in `blog/source`.

The content is as follows:

```js
importScripts('https://cdn.jsdelivr.net/npm/workbox-cdn@5.1.3/workbox/workbox-sw.js');

workbox.setConfig({
    modulePathPrefix:'https://cdn.jsdelivr.net/npm/workbox-cdn@5.1.3/workbox/'
});

const {core, precaching, routing, strategies, expiration, cacheableResponse, backgroundSync} = workbox;
const {CacheFirst, NetworkFirst, NetworkOnly, StaleWhileRevalidate} = strategies;
const {ExpirationPlugin} = expiration;
const {CacheableResponsePlugin} = cacheableResponse;

const cacheSuffixVersion ='-000010', // The cache version number is extremely important. You must modify the cache version number when publishing web pages after modifying static files
    maxEntries = 100;

self.addEventListener('activate', (event) => {
    event.waitUntil(
        caches.keys().then((keys) => {
            return Promise.all(keys.map((key) => {
                if (!key.includes(cacheSuffixVersion)) return caches.delete(key);
            }));
        })
    );
});


core.setCacheNameDetails({
    prefix:'volantis', // extremely important, draw up a name by yourself
    suffix: cacheSuffixVersion
});

core.skipWaiting();
core.clientsClaim();
precaching.cleanupOutdatedCaches();

/*
 * Precache
 *-Static Assets
 */
precaching.precacheAndRoute( // Extremely important defines the static file to be cached for the first time
    [
        {url:'/css/first.css', revision: null },
        {url:'/css/style.css', revision: null },
        {url:'/js/app.js', revision: null },
    ],
);

/*
 * Cache File From CDN
 *
 * Method: CacheFirst
 * cacheName: static-immutable
 * cacheTime: 30d
 */

// cdn.jsdelivr.net-cors enabled
routing.registerRoute(
    /.*cdn\.jsdelivr\.net/,
    new CacheFirst({
        cacheName:'static-immutable' + cacheSuffixVersion,
        fetchOptions: {
            mode:'cors',
            credentials:'omit'
        },
        plugins: [
            new ExpirationPlugin({
                maxAgeSeconds: 30 * 24 * 60 * 60,
                purgeOnQuotaError: true
            })
        ]
    })
);

// m7.music.126.net-cors enabled
routing.registerRoute(
    /.*m7\.music\.126\.net/,
    new CacheFirst({
        cacheName:'static-immutable' + cacheSuffixVersion,
        fetchOptions: {
            mode:'cors',
            credentials:'omit'
        },
        plugins: [
            new ExpirationPlugin({
                maxAgeSeconds: 30 * 24 * 60 * 60,
                purgeOnQuotaError: true
            })
        ]
    })
);

/*
 * No Cache
 *
 * Method: networkOnly
 */
routing.registerRoute(
    /.*baidu\.com.*/,
    new NetworkOnly()
);
/*
 * Others img fonts
 * Method: staleWhileRevalidate
 */
routing.registerRoute(
    // Cache image fonts files
    /.*\.(?:png|jpg|jpeg|svg|gif|webp|ico|eot|ttf|woff|woff2|mp3)/,
    new StaleWhileRevalidate()
);

/*
 * Static Assets
 * Method: staleWhileRevalidate
 */
routing.registerRoute(
    // Cache CSS files
    /.*\.(css|js)/,
    // Use cache but update in the background ASAP
    new StaleWhileRevalidate()
);

/*
 * sw.js-Revalidate every time
 * staleWhileRevalidate
 */
routing.registerRoute(
    '/sw.js', // this file name
    new StaleWhileRevalidate()
);

/*
 * Default-Serve as it is
 * networkFirst
 */
routing.setDefaultHandler(
    new NetworkFirst({
        networkTimeoutSeconds: 3
    })
);

```

{% note info, after modifying the static file, you must modify the cached version number when publishing a web page. %}

## Install the "Related Articles" plugin

1. Install the plugin
```sh
npm i -S hexo-related-popular-posts
```

2. Custom configuration method of plug-in:
{% link hexo-related-popular-posts, https://github.com/tea3/hexo-related-popular-posts %}

If you use a header image, you can add the following settings in the site configuration file to make related articles display the correct article header image:

```yaml blog/_config.yml
popularPosts:
  eyeCatchImageAttributeName: headimg
```

{% noteblock warning up, note %}

You need to upgrade to 5.0.1 and above to support custom header images, see [#29](https://github.com/tea3/hexo-related-popular-posts/issues/29)

{% endnoteblock %}

## Analysis and Statistics

By default, the visit statistics of [Bu Suanzi](http://busuanzi.ibruce.info/) are supported. You can add Baidu statistics and Google Analytics by yourself.

### Word count and reading time

1. Install the following plugins:
```
npm i --save hexo-wordcount
```
2. Modify the configuration file and open the `wordcount` plugin
```yaml blog/_config.volantis.yml
plugins:
  ...
  # The word count of the article, the reading time, and the plug-in needs to be installed: npm i --save hexo-wordcount
  wordcount:
    enable: #true
```
3. Then modify the configuration file to write `wordcount` into the meta location that needs to be displayed:
```yaml blog/_config.volantis.yml
# Article layout
article:
  ...
  # The layout scheme of the article card body on the article details page
  body:
    # Top of article information
    # Take from meta_library
    top_meta: [..., wordcount, ...]
    ...
    # Information at the bottom of the article
    # Take from meta_library
    bottom_meta: [..., wordcount, ...]
```


### CNZZ Statistics

Please refer to this tutorial by ZYMIN:
{% link Hexo hexo+ejs+material x Add CNZZ statistical code, https://zymin.cn/arcticle/hexo+ejs+material.html %}

## More advanced gameplay

For details, please refer to this blog of [@TRHX](https://www.itrhx.com):
{% link Hexo blog topic personalization, https://www.itrhx.com/2018/08/27/A04-Hexo-blog-topic-personalization/ %}

Contains a variety of detailed tutorials such as translucent cards, adding cartoon characters, custom mouse styles, mouse special effects, firework special effects, color scrolling fonts, website running time, dynamic browser titles, and snowflakes falling special effects.

{% link theme official website #Advanced gameplay, https://volantis.js.org/categories/Advanced gameplay/ %}
