---
seo_title: Sample blog
cover: true
sidebar: []

---

<center>
{% span large yellow, Sample %}
{% span large green, Blog %}
</center>
<br>

## Team member's blog

{% sitegroup %}
{% site xaoxuu, url=https://xaoxuu.com, screenshot=https://image.thum.io/get/width/1024/crop/768/https://xaoxuu.com/, avatar=https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png, description=简约风格 %}
{% site inkss, url=https://inkss.cn, screenshot=https://image.thum.io/get/width/1024/crop/768/https://inkss.cn/, avatar=https://cdn.jsdelivr.net/gh/inkss/common@master/static/web/avatar.jpg, description=这不是一段关于这个网站的描述文字啊喂 %}
{% site MHuiG, url=https://blog.mhuig.top, screenshot=https://image.thum.io/get/width/1024/crop/768/https://blog.mhuig.top////, avatar=https://cdn.jsdelivr.net/gh/MHuiG/imgbed@master/data/p.png, description=字文述描的站网个这于关段一是这 %}
{% site Colsrch, url=https://colsrch.cn, screenshot=https://image.thum.io/get/width/1024/crop/768/https://colsrch.cn/, avatar=https://cdn.jsdelivr.net/gh/Colsrch/images/Colsrch/avatar.jpg, description=愿多年以后，我可以酌一杯清酒，烂醉如泥，梦中回到我们的曾经。 %}
{% site Linhk1606, url=https://linhk1606.github.io, screenshot=https://image.thum.io/get/width/1024/crop/768/https://linhk1606.github.io/, avatar=https://i.loli.net/2020/02/09/PN7I5RJfFtA93r2.png, description=这是一段关于这个网站的描述文字 %}
{% endsitegroup %}


<br>

{% issues sites | api=https://api.github.com/repos/volantis-x/examples/issues?sort=updated&state=open&page=1&per_page=100 | group=version:版本：^4.0,版本：^3.0,版本：^2.0 %}
<br>


<!-- more -->

<br><br>

{% timeline how to add your own blog link %}

{% timenode Step 1: Create a new [Issue](https://github.com/volantis-x/examples/issues/) Fill in and submit according to the format %}

```json
{
     "title": "",
     "description": "",
     "screenshot": "",
     "url": "",
     "avatar": "",
     "version": "版本：^4.0"
}
```

In order to improve the image loading speed, it is recommended to optimize the image size:
1. Open [compressed image](https://www.yasuotu.com/) to upload your own screenshot, adjust the height of the image to `360px` and download it.
2. Upload the compressed picture to [去不图床](https://7bu.top/) and use the picture link as the screenshot link.

{% endtimenode %}

{% timenode Step 2: Refresh %}

Come back and refresh to take effect.

{% endtimenode %}

{% endtimeline %}

{% p h2, how to update my blog link %}

- If the issue is created by yourself, you can modify it yourself.
- If it was created by the administrator, please create a new one by yourself, and then ask the administrator to delete the old one.