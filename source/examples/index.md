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

{% sites only:test_demo %}


## Who uses Volantis

{% sites only:examples %}

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