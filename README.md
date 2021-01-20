# deepin用户手册及FAQ

**deepin用户手册文档目录上线GitHub**，该项目由Jekyll驱动！

{% include list.liquid all=true %}

## 1.项目介绍

**亲爱的深粉：（深度官方原文）**

 deepin文档目录已上线GitHub，目前包括deepin用户手册&deepin-FAQ。
 
 deepin用户手册，主要是deepin操作系统的一些使用介绍文档。目前我们已经上传了一些内容，包括系统基础支持、入门知识、基础模块功能使用介绍，大家可以了解学习，或者从这些或其他方面补充。

## 2.文档及排版要求

### 使用说明

该文档支持多层目录，目录名可为中文。每一层目录下建立一个`README.md`文档（格式要求见下方），在目录下建立你需要的`正式文档.md`(格式要求见下方)。

### README.md文档格式：

文档头部格式必须为：
```
{% raw %}

---
sort: 1
---

# 该级目录的标题

{% include list.liquid all=true %}

source: `{{ page.path }}`

这里你还可以写点你想的该目录分类的介绍。

{% endraw %}
```

参数`sort: 1`为目录或文档的排序顺序。

###正式文档格式：

```
{% raw %}

---
sort: 1
---

source: `{{ page.path }}`

# 你写的文档的标题

文档正文。。。。。。。

{% endraw %}
```
参数`sort: 1`为目录或文档的排序顺序，不使用该参数，文档较多时，显示不清楚层次。

## 3.本项目使用jekyll-rtd-theme

![CI](https://github.com/rundocs/jekyll-rtd-theme/workflows/CI/badge.svg?branch=develop)
![jsDelivr](https://data.jsdelivr.com/v1/package/gh/rundocs/jekyll-rtd-theme/badge)

### 快速部署

```yml
remote_theme: rundocs/jekyll-rtd-theme
```

You can [generate](https://github.com/rundocs/starter-slim/generate) with the same files and folders from [rundocs/starter-slim](https://github.com/rundocs/starter-slim/)

### 特色 

- Shortcodes (Toasts card, mermaid)
- Pages Plugins (emoji, gist, avatar, mentions)
- Auto generate sidebar
- [Attribute List Definitions](https://kramdown.gettalong.org/syntax.html#attribute-list-definitions) (Primer/css utilities, Font Awesome 4)
- Service worker (caches)
- SEO (404, robots.txt, sitemap.xml)
- Canonical Link (Open Graph, Twitter Card, Schema data)

## 可选参数

| name          | default value        | description       |
| ------------- | -------------------- | ----------------- |
| `title`       | repo name            |                   |
| `description` | repo description     |                   |
| `url`         | user domain or cname |                   |
| `baseurl`     | repo name            |                   |
| `lang`        | `en`                 |                   |
| `direction`   | `auto`               | `ltr` or `rtl`    |
| `highlighter` | `rouge`              | Cannot be changed |

```yml
# folders sort
readme_index:
  with_frontmatter: true

meta:
  key1: value1
  key2: value2
  .
  .
  .

google:
  gtag:
  adsense:

mathjax: # this will prased to json, default: {}

mermaid:
  custom:     # mermaid link
  initialize: # this will prased to json, default: {}

scss:   # also _includes/extra/styles.scss
script: # also _includes/extra/script.js

translate:
  # shortcodes
  danger:
  note:
  tip:
  warning:
  # 404
  not_found:
  # copyright
  revision:
  # search
  searching:
  search:
  search_docs:
  search_results:
  search_results_found: # the "#" in this translate will replaced with results size!
  search_results_not_found:

plugins:
  - jemoji
  - jekyll-avatar
  - jekyll-mentions
```

## The license

The theme is available as open source under the terms of the MIT License

The theme is inspired by [sphinx-rtd-theme](https://github.com/readthedocs/sphinx_rtd_theme) and [jekyll-rtd-theme](https://github.com/rundocs/jekyll-rtd-theme).
