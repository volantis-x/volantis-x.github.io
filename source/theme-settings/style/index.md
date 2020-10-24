---
layout: docs
title: Custom theme appearance
group: docs-volantis-latest
order: 302
short_title: 3-2 Custom theme appearance
sidebar: [docs-volantis-latest, toc]
disqus:
  path: /wiki/volantis/
---

## Maximum layout width

```yaml blog/_config.volantis.yml
custom_css:
  ...
  max_width: 1080px # Sum of body width and sidebar width
```

The maximum width of the content presented on the web page, that is, the sum of the width of the body and sidebar.

## Anti-aliasing

```yaml blog/_config.volantis.yml
custom_css:
  ...
  font_smoothing: true # font-smoothing for webkit
```

## Custom cursor style

```yaml blog/_config.volantis.yml
custom_css:
  ...
  cursor:
    enable: true
    text: https://cdn.jsdelivr.net/gh/inkss/common@master/cursor/text.png
    pointer: https://cdn.jsdelivr.net/gh/inkss/common@master/cursor/pointer.png
    default: https://cdn.jsdelivr.net/gh/inkss/common@master/cursor/left_ptr.png
    not-allowed: https://cdn.jsdelivr.net/gh/inkss/common@master/cursor/circle.png
    zoom-out: https://cdn.jsdelivr.net/gh/inkss/common@master/cursor/zoom-out.png
    zoom-in: https://cdn.jsdelivr.net/gh/inkss/common@master/cursor/zoom-in.png
    grab: https://cdn.jsdelivr.net/gh/inkss/common@master/cursor/openhand.png
```


## Navigation bar style

You can set the height of the navigation bar and visual effects. The currently available visual effects are:
-**shadow**: Card shadow.
-**floatable**: When the mouse moves into the container, it will appear to float.
-**blur**: The background blur effect (frosted glass), displayed as opaque when the browser does not support it.

```yaml blog/_config.volantis.yml
custom_css:
  ...
  navbar:
    height: 64px
    effect: [shadow, blur] # [shadow, floatable, blur]
```

## Scroll bar style

```yaml blog/_config.volantis.yml
custom_css:
  ...
  scrollbar:
    size: 4px
    border: 2px
    color:'#2196f3'
    hover:'#ff5722'
```

## Sidebar style

The visual effects parameters are the same as above. It is worth noting that the card's `floatable` effect and `blur` effect conflict.
```yaml blog/_config.volantis.yml
custom_css:
  ...
  sidebar:
    effect: [shadow] # [shadow, floatable, blur]
```

## Body area style

The visual effects parameters are the same as above. It is worth noting that the card's `floatable` effect and `blur` effect conflict. You can set the display language name of the code block in `language: true`. `text_align` can set the text alignment direction of h1/h2/h3/h4/p.
```yaml blog/_config.volantis.yml
custom_css:
  ...
  body:
    effect: [shadow] # [shadow, floatable, blur]
    highlight:
      language: true # show language of codeblock
      copy_btn: true
    text_align: # left, right, justify, center
      h1: left
      h2: left
      h3: left
      h4: left
      p: justify
    note: # style for default note: {% note text %}
      icon:'\f054'
      color:''
```

## Layout spacing

You can set several heading layout spacing h2/h3/h4, paragraph spacing line, and paragraph spacing inline within blocks.
```yaml blog/_config.volantis.yml
custom_css:
  ...
  gap:
    h2: 48px # Spacing above H2 (only px unit)
    h3: 32px # Spacing above H3 (only px unit)
    h4: 16px # Spacing above H4 (only px unit)
    paragraph: 1rem # Paragraph spacing between paragraphs
    row: .5rem # Paragraph spacing between other elements
```

## Custom font

You can customize the body and code fonts.
```yaml blog/_config.volantis.yml
custom_css:
  ...
  fontfamily:
    logofont:
      fontfamily:'"Varela Round", "PingFang SC", "Microsoft YaHei", Helvetica, Arial'
      name:'Varela Round'
      url: https://cdn.jsdelivr.net/gh/volantis-x/cdn-fonts/VarelaRound/VarelaRound-Regular.ttf
      weight: normal
      style: normal
    bodyfont:
      fontfamily:'UbuntuMono, "PingFang SC", "Microsoft YaHei", Helvetica, Arial'
      name:'UbuntuMono'
      url: https://cdn.jsdelivr.net/gh/volantis-x/cdn-fonts/UbuntuMono/UbuntuMono-Regular.ttf
      weight: normal
      style: normal
    codefont:
      fontfamily:'Menlo, Monaco'
      name:'Monaco'
      url: https://cdn.jsdelivr.net/gh/volantis-x/cdn-fonts/Monaco/Monaco.ttf
      weight: normal
      style: normal
```
## Custom color

```yaml blog/_config.volantis.yml
color_scheme:
  # ------------
  # Universal color
  common:
    # Theme color
    theme:'#44D7B6'
    # Link color
    link:'#2196f3'
    # Button color
    button:'#44D7B6'
    # The color when the mouse is placed on the interactive element
    hover:'#ff5722'
    # The color of the text inside the theme color block
    inner:'#fff'
    # The background color of the text in the selected area
    selection:'alpha(#2196f3, 0.2)'
  # ------------
  # Bright theme (default)
  light:
    # Website background color
    site_bg:'#f4f4f4'
    # Text on website background
    site_inner:'#fff'
    # Site footer text
    site_footer:'#666'

    # Card background color
    card:'#fff'
    # Normal text on the card
    text:'#444'

    # Block and code block background color
    block:'#f6f6f6'
    # The background color when the code block is highlighted
    codeblock:'#FFF7EA'
    # Inline code color
    inlinecode:'#D56D28'

    # Article section
    h1:'#444'
    h2:'#444'
    h3:'#444'
    h4:'#444'
    h5:'#444'
    h6:'#444'
    p:'#444'

    # List text
    list:'#666'
    # List the text when hover
    list_hl:'mix($color-theme, #000, 80)'
    # Supporting text
    meta:'#888'
  # ------------
  # Dark theme
  dark:
    # Website background color
    site_bg:'#222'
    # Text on website background
    site_inner:'#eee'
    # Site footer text
    site_footer:'#aaa'
    # Card background color
    card:'#444'
    # Normal text on the card
    text:'#eee'

    # Block and code block background color
    block:'#3a3a3a'
    # The background color when the code block is highlighted
    codeblock:'#343a3c'
    # Inline code color
    inlinecode:'#D56D28'

    # Article section
    h1:'#eee'
    h2:'#eee'
    h3:'#ddd'
    h4:'#ddd'
    h5:'#ddd'
    h6:'#ddd'
    p:'#bbb'

    # List text
    list:'#aaa'
    # List the text when hover
    list_hl:'mix($color-theme, #fff, 80)'
    # Supporting text
    meta:'#888'
    # Night picture brightness
    brightness: 70%
```

## Customize the right-click menu

```yaml blog/_config.volantis.yml
rightmenu:
  enable: true
  # hr: dividing line, music: music controller
  layout: [home, help, examples, contributors, hr, source_docs, source_theme, hr, print, hr, music]
  # Optional function item
  print:
    name: print page
    icon: fa fa-print
    onclick: document.execCommand('print')
  # The format of the custom menu is as follows
  help:
    name: FAQ
    icon: fa fa-question
    url: https://volantis.js.org/faqs/
  examples:
    name: sample blog
    icon: fa fa-rss
    url: https://volantis.js.org/examples/
  contributors:
    name: Join the community
    icon: fa fa-fan fa-spin
    url: https://volantis.js.org/contributors/
  source_docs:
    name: source code of this site
    icon: fa fa-code-branch
    url: https://github.com/volantis-x/volantis-docs/
  source_theme:
    name: theme source code
    icon: fa fa-code-branch
    url: https://github.com/volantis-x/hexo-theme-volantis/
```