---
layout: docs
title: Third-party plugin
group: docs-volantis-latest
order: 310
short_title: 3-10 third-party plugins
sidebar: [docs-volantis-latest, toc]
disqus:
   path: /wiki/volantis/
---


## Plugin library
Volantis provides compatibility optimization for rich plug-ins. You only need to turn on and off most of the plug-ins without any settings.

```yaml blog/_config.volantis.yml
plugins:
  ################ required plugins ################
  # jquery
  jquery: https://cdn.jsdelivr.net/npm/jquery@3.5/dist/jquery.min.js
  # fontawesome
  fontawesome: https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.14/css/all.min.css

  ################ optional plugins ################

  ######## Plugins to improve loading speed:

  # Preloading
   preload:
     enable: true
     service: flying_pages # instant_page, flying_pages
     instant_page: https://cdn.jsdelivr.net/gh/volantis-x/cdn-volantis@2/js/instant_page.js
     flying_pages: https://cdn.jsdelivr.net/gh/gijo-varghese/flying-pages@2.1.2/flying-pages.min.js

   # Picture lazy loading
   # https://www.npmjs.com/package/vanilla-lazyload
   lazyload:
     enable: true
     js: https://cdn.jsdelivr.net/npm/vanilla-lazyload@17.1.0/dist/lazyload.min.js
     onlypost: false
     loadingImg: # https://cdn.jsdelivr.net/gh/volantis-x/cdn-org/placeholder/c617bfd2497fcea598e621413e315c368f8d8e.svg
     blurIn: true # blur loading effect (valid when loadingImg is empty)
  ######## Plugins to optimize the experience:

  # highlight.js
  highlightjs:
    enable: #true # Please set hexo.config.highlight.enable = false !!!
    js: https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@9.18.1/build/highlight.min.js
    css: https://cdn.jsdelivr.net/npm/highlight.js@9.18.1/styles/solarized-light.css
    # more: https://www.jsdelivr.com/package/npm/highlight.js?path=styles

  # https://scrollrevealjs.org/api/reveal.html
  scrollreveal:
    enable: #true
    js: https://cdn.jsdelivr.net/npm/scrollreveal@4.0.6/dist/scrollreveal.min.js
    distance: 32px
    duration: 800 # ms
    interval: 20 # ms
    scale: 1 # 0.1~1

  # Codeblock Copy Button
  clipboard:
    enable: true
    js: https://cdn.jsdelivr.net/npm/clipboard@2/dist/clipboard.min.js

  ######## Plugins for SEO:

  # npm i hexo-wordcount
  wordcount:
    enable: #true

  ######## Plugins for ...
  # Button Ripple Effect
  nodewaves:
    enable: #true
    css: https://cdn.jsdelivr.net/npm/node-waves@0.7.6/dist/waves.min.css
    js: https://cdn.jsdelivr.net/npm/node-waves@0.7.6/dist/waves.min.js

  # fontawesome animation
  fontawesome_animation:
    enable: #true
    css: https://cdn.jsdelivr.net/gh/l-lin/font-awesome-animation/dist/font-awesome-animation.min.css

  # Typing Effects
  comment_typing:
    enable: #true
    js: https://cdn.jsdelivr.net/gh/volantis-x/cdn-volantis@2/js/comment_typing.js

  # Slide Background
  backstretch:
    enable: #true
    js: https://cdn.jsdelivr.net/npm/jquery-backstretch@2.1.18/jquery.backstretch.min.js
    position: cover       # cover: sticky on the cover.   fixed: Fixed as background for the site.
    shuffle: true         # shuffle playlist
    duration: 10000       # Duration (ms)
    fade: 1500            # fade duration (ms) (Not more than 1500)
    images:               # For personal use only. At your own risk if used for commercial purposes !!!
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/001.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/002.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/003.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/004.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/005.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/006.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/012.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/016.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/019.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/025.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/033.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/034.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/035.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/038.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/039.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/042.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/046.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/051.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/052.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/054.jpg
      - https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper-minimalist/2020/056.jpg

  # APlayer is only available in mainland China.
  # APlayer config: https://github.com/metowolf/MetingJS
  aplayer:
    enable: #true
    js:
      - https://cdn.jsdelivr.net/npm/aplayer@1.10/dist/APlayer.min.js
      - https://cdn.jsdelivr.net/npm/meting@2.0/dist/Meting.min.js
    # Required
    server: netease   # netease, tencent, kugou, xiami, baidu
    type: playlist    # song, playlist, album, search, artist
    id: 3175833810    # song id / playlist id / album id / search keyword
    # Optional
    fixed: false      # enable fixed mode
    theme: '#1BCDFC'  # main color
    autoplay: false   # audio autoplay
    order: list       # player play order, values: 'list', 'random'
    loop: all         # player loop play, values: 'all', 'one', 'none'
    volume: 0.7       # default volume, notice that player will remember user setting, default volume will not work after user set volume themselves
    list_max_height: 320px # list max height
    list_folded: true
  pjax:
    enable: true
    timeout: 5000        # The timeout in milliseconds for the XHR requests. Set to 0 to disable the timeout.
    cacheBust: false     # When set to true, Pjax appends a timestamp  to skip the browser cache.
    animation: nprogress # nprogress, circle
    banUrl: # The blocked URL address will not enable pjax redirection, you can use window.location.pathname to get it under the console
       #-/artitalk/ # artitalk does not support pjax

  # Artitalk https://artitalk.js.org
  # Please refer to the configuration process: https://artitalk.js.org/doc.html
  # Except appID and appKEY are optional
  artitalk:
    # Set `layout: artitalk` to enable in page
    appID: ogP8qj3veMh0LFpFWMPOyF0X-MdYXbMMI # your appID
    appKEY: nHXLd3N3Jgh460t2iRQKWAtr # your appKEY
    # severurl: #leancloud binds the secure domain name, you don’t need to fill in if you use the international version
    # slanguage: # Language setting, zh is Chinese, en is English, and es is Spanish. The default is Chinese
    # per: #Display number of talks on each page
    # placeholder1: #Placeholder in the input box of the editor talk
    # placeholder2: #Customize the placeholder for the input box of the avatar url
    # lazy: #Load animation switch, 1 is on, 0 is off, the default is on
    # bgimg: #Talk about the background image url of the input box
    # color1: #Talk about background color 1 & button color 1
    # color2: #Talk about background color 2 & button color 2
    # color3: #Talk about font color
  #################################
  # Dark Mode
  darkmodejs:
    enable: #true
```



## Slide background
```yaml blog/_config.volantis.yml
plugins:
  ...
  backstretch:
    enable: true
    js: https://cdn.jsdelivr.net/npm/jquery-backstretch@2.1.18/jquery.backstretch.min.js
    position: cover # cover: sticky on the cover. fixed: Fixed as background for the site.
    duration: 20000 # Duration (ms)
    fade: 1500 # fade duration (ms) (Not more than 1500)
    images: # For personal use only. At your own risk if used for commercial purposes !!!
      -https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg
      ...
```
The display position of the slideshow background image can be selected to be pasted on the cover and slide along with the cover, or fixed as the background image of the webpage.

## highlight.js
```yaml blog/_config.volantis.yml
plugins:
  ...
  highlightjs:
    js: https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@9.18.1/build/highlight.min.js
    css: https://cdn.jsdelivr.net/npm/highlight.js@9.18.1/styles/solarized-light.css
```
If you need to use highlight.js for syntax highlighting, please set `highlight.enable` in the site configuration file to `false`, otherwise the plugin will not be loaded. You can choose your favorite theme among the <u>94</u> [Syntax Highlighting Themes](https://www.jsdelivr.com/package/npm/highlight.js?path=styles), and then replace the above Css link.

{% note warning, if you use highlight.js, please make sure you do not use the official hexo codeblock tag, otherwise an error will be reported. %}
{% note bug red, after testing, using highlight.js, some code in the container may still be rendered or even report errors. %}

## APlayer Music Player
```yaml blog/_config.volantis.yml
plugins:
  ...
  aplayer:
    enable: true
    js:
      -https://cdn.jsdelivr.net/npm/aplayer@1.10/dist/APlayer.min.js
      -https://cdn.jsdelivr.net/npm/meting@2.0/dist/Meting.min.js
    # Required
    server: netease # netease, tencent, kugou, xiami, baidu
    type: playlist # song, playlist, album, search, artist
    id: 3175833810 # song id / playlist id / album id / search keyword
    # Optional
    fixed: false # enable fixed mode
    theme:'#1BCDFC' # main color
    autoplay: false # audio autoplay
    order: list # player play order, values:'list','random'
    loop: all # player loop play, values:'all','one','none'
    volume: 0.7 # default volume, notice that player will remember user setting, default volume will not work after user set volume themselves
    list_max_height: 340px # list max height
    list_folded: true
```

{% note warning, APlayer player can only be used in mainland China. Related documents: [APlayer](https://aplayer.js.org/) | [MetingJS](https://github.com/metowolf/MetingJS) %}

## Artitalk
```yaml blog/_config.volantis.yml
plugins:
  ...
  # Artitalk https://artitalk.js.org
  # Please refer to the configuration process: https://artitalk.js.org/doc.html
  # Except appID and appKEY are optional
  Artitalk:
    enable: false # true is turned on, false is turned off
    appID: ogP8qj3veMh0LFpFWMPOyF0X-MdYXbMMI # your appID
    appKEY: nHXLd3N3Jgh460t2iRQKWAtr # your appKEY
    # severurl: #leancloud binds the secure domain name, you don’t need to fill in if you use the international version
    # slanguage: # Language setting, zh is Chinese, en is English, and es is Spanish. The default is Chinese
    # per: #Display number of talks on each page
    # placeholder1: #Placeholder in the input box of the editor talk
    # placeholder2: #Customize the placeholder for the input box of the avatar url
    # lazy: #Load animation switch, 1 is on, 0 is off, the default is on
    # bgimg: #Talk about the background image url of the input box
    # color1: #Talk about background color 1 & button color 1
    # color2: #Talk about background color 2 & button color 2
    # color3: #Talk about font color
```