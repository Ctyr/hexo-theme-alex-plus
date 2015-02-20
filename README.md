#ALEX-PLUS theme for Hexo

**Description:** Add more features for alex theme,include:

- use fonts hosted on aliyun OSS+CDN instead of 360 fonts(useso.com).
     
  *The fonts url 'http://i.chenhd.com/fonts', resolves to 'i.chenhd.com.w.alikunlun.com',which represent for aliyun CDN service.*

- use aliyun CDN to accelerate static files as:

  - jquery.fancybox.css
  - jquery.fancybox.js
  - jquery.fancybox.pack.js
  - jquery.min.js
  - jquery.scrollLoading.js
  - script.js

   *The url is 'http://i.chenhd.com/js/'*

- add meta language tag
  It's good for SEO to add meta language.The default language is zh-cn,you can alter it in `themes/alex-plus/layout/_partial/head.ejs`.

- alter blockquote css
  The default blockquote css is quite disgusting,so i altered the blockquote css.You can find the contract pictures in [tyr.so/hexo-optimization](http://tyr.so/hexo-optimization.html).

- add toc support
  Alter default toc(table of content) and add css for toc.You can find the contract pictures in [tyr.so/add-toc-for-hexo](http://tyr.so/add-toc-for-hexo.html).

- add duoshuo support
  The default comment system is disqus which not works well in china.So change it to duoshuo comment system.
  You have to fill in your duoshuo shortname in the alex-plus `_config.yml` section of `duoshuo_shortname`.

- add return-to-top button
  When the webpage reach to footer,the button will show up and when you click,the page will return to top.
  The button picture comes from renren.com.
  You can alter the arguments in `source/js/totop.js`

- add Baidu statistics
  If you want to use Baidu statistics,you should edit `layout\_partial\head.ejs`and remove the annotation in the lin 40 and 50.Then replace the "your-token" in line 45 to your Baidu statistics code.

 
**Attention:** If you want more information or see the effect,please visit [tyr.so](http://tyr.so)


---
**描述：** 为ALEX主题增加了更多的特性，包括：
- 使用搭建在阿里云OSS+CDN服务上的字体库来代替默认的360字体库(useso.com)。
  字体url为http://i.chenhd.com/fonts',解析到'i.chenhd.com.w.alikunlun.com',域名是阿里云昆仑架构（CDN）。
- 使用阿里云CDN加速静态文件，包括：
  jquery.fancybox.css 
  jquery.fancybox.js 
  jquery.fancybox.pack.js 
  jquery.min.js 
  jquery.scrollLoading.js 
  script.js

  url为 'http://i.chenhd.com/js/'

- 增加meta language元信息，利于SEO
  默认的语言为` zh-cn`,你可以在`themes/alex-plus/layout/_partial/head.ejs`中修改

- 修改blockquote CSS
  默认的blockquote效果是居中且字体巨大，不甚美观，故修改CSS，实现引用效果。可以访问[tyr.so/hexo-optimization](http://tyr.so/hexo-optimization.html#blockquote_CSS的修改)获取前后对比效果。

- 增加TOC支持
  默认没有开启TOC，且开启之后也不甚美观。故增加CSS支持和文章中开选择是否显示TOC.可以访问[tyr.so/add-toc-for-hexo](http://tyr.so/add-toc-for-hexo.html)获取前后对比效果。
  如果需要在文章中显示TOC，则再文章的预处理段落加上`toc: true`即可(默认为不显示)，如：
  ```
 title: 
 date: 
 tags: 
 - hexo
 categories: 
 - hexo
 permalink: hexo-optimization
 toc: true
 ---
```
- 增加多说评论的支持
  默认评论系统为disqus,现增加了对多说的支持。需要编辑主题的`_config.yml`配置文件，在最后的`duoshuo_shortname`中填入你的多说short name.

- 增加返回顶部的支持
  当网页到达底部时，会出现返回顶部按钮。可以编辑`source/js/totop.js`修改配置参数。

- 增加百度统计支持
  如果需要启用，编辑`layout\_partial\head.ejs` 去除45行和50行的注释，将45行中的'your-token'替换成你百度统计代码中相同位置出现的字符。

  **注意：** 你可以访问[tyr.so](http://tyr.so) 来获取更多信息、前后对比效果和预览。


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
