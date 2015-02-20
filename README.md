#ALEX-PLUS theme for Hexo

**Description:** Add more features for alex theme,include:

- use fonts hosted on aliyun OSS+CDN instead of 360 fonts(useso.com).
  *The fonts url 'http://i.chenhd.com/fonts', resolves to 'i.chenhd.com.w.alikunlun.com',which represent for aliyun CDN service.*

- use aliyun CDN to accelerate static files as:
  jquery.fancybox.css
  jquery.fancybox.js
  jquery.fancybox.pack.js
  jquery.min.js
  jquery.scrollLoading.js
  script.js

   *The url is 'http://i.chenhd.com/js/'*

- add meta language tag
  It's good for SEO to add meta language.The default language is zh-cn,you can alter it in `themes/alex-plus/layout/_partial/head.ejs`.

- alter blockquote css
  The default blockquote css is quite disgusting,so i altered the blockquote css.You can find the contract pictures in [tyr.so/hexo-optimization](http://tyr.so/hexo-optimization.html).

- add toc support
  Alter default toc(table of content) and add css for toc.You can find the contract pictures in [tyr.so/hexo-optimization](http://tyr.so/hexo-optimization.html).

- add duoshuo support
  The default comment system is disqus which not works well in china.So change it to duoshuo comment system.
  You have to fill in your duoshuo shortname in the alex-plus `_config.yml` section of `duoshuo_shortname`.

- add return-to-top button
  When the webpage reach to footer,the button will show up and when you click,the page will return to top.
  The button picture comes from renren.com.
  You can alter the arguments in `source/js/totop.js`

- add Baidu statistics
  If you want to use Baidu statistics,you should remove the annotation in the lin 40 and 50.Then replace the "your-token" in line 45 to your Baidu statistics code.

 
**Attention:** If you want more information or see the effect,please visit [tyr.so](http://tyr.so)


---
#Alex

A very simple, elegant and responsive theme for [Hexo].

![](http://ppoffice.github.io/hexo-theme-alex/gallery/preview.jpg "Preview")

- [Preview](http://ppoffice.github.io/hexo-theme-alex/)

## Installation

### Install

``` bash
$ git clone git://github.com/ppoffice/alex-hexo-theme.git themes/alex
```

**Alex requires Hexo 2.4 and above.**

### Enable

Modify `theme` setting in `_config.yml` to `Alex`.

### Update

``` bash
cd themes/Alex
git pull
```

## Configuration

``` yml
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml

# Content
excerpt_link: Read More
fancybox: true

# Sidebar
sidebar: left
widgets:
- category
- tag
- tagcloud
- archives
- recent_posts

# Miscellaneous
google_analytics:
favicon: /favicon.png
twitter:
google_plus:
```

- **menu** - Navigation menu
- **rss** - RSS link
- **excerpt_link** - "Read More" link at the bottom of excerpted articles. `false` to hide the link.
- **fancybox** - Enable [Fancybox]
- **sidebar** - Sidebar style. You can choose `left`, `right`, `bottom` or `false`.
- **widgets** - Widgets displaying in sidebar
- **google_analytics** - Google Analytics ID
- **favicon** - Favicon path
- **twitter** - Twiiter ID
- **google_plus** - Google+ ID

## Features

### Fancybox

Alex uses [Fancybox] to showcase your photos. You can use Markdown syntax or fancybox tag plugin to add your photos.

```
![img caption](img url)

{% fancybox img_url [img_thumbnail] [img_caption] %}
```

### Sidebar

You can put your sidebar in left side, right side or bottom of your site by editing `sidebar` setting.

Alex provides 5 built-in widgets:

- category
- tag
- tagcloud
- archives
- recent_posts

All of them are enabled by default. You can edit them in `widget` setting.

## Development

### Requirements

- [Grunt] 0.4+
- Hexo 2.4+

### Grunt tasks

- **default** - Download [Fancybox] and [Font Awesome].
- **fontawesome** - Only download [Font Awesome].
- **fancybox** - Only download [Fancybox].
- **clean** - Clean temporarily files and downloaded files.

[Hexo]: http://zespia.tw/hexo/
[Fancybox]: http://fancyapps.com/fancybox/
[Font Awesome]: http://fontawesome.io/
[Grunt]: http://gruntjs.com/
