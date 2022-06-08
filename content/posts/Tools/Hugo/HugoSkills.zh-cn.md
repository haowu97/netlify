---
title: "Hugo使用技巧总结"
date: 2021-02-18T17:57:18+08:00
draft: false

description: "Hugo使用中的奇技淫巧，更高效地用Hugo搭建自己地BLog。"
upd: "Hugo使用中的奇技淫巧，更高效地用Hugo搭建自己地BLog。"

tags: ['Blog', 'Hugo']
categories: ["Hugo博客搭建"]
---

<!--more-->

## 1. 博文配置信息

博文的Yaml配置信息参考如下：

```yaml
title: ""
date: 2021-08-06T21:17:53+08:00
draft: false

description: ""
upd: ""

tags: []
categories: []
```

### 1.1 默认博文格式

可以在`根目录\archetypes\default.md`设置默认文件格式，然后可以使用以下命令生成的新博文：

```powershell
hugo new post/test.md
```

生成的新博文与默认格式一致，这样就不需要每次都自己重新写一遍Yaml配置信息。

### 1.2 给博文添加标签和分类

方法一

```toml
categories:
  - documentation
```

方法二

```
tags: ["Blog", "Hugo"]
categories: ["Hugo博客搭建"]
```

其中，引号可以省略。

## 2. 在网页标签栏添加分类链接

在`config.toml`中添加

```
  [[languages.zh-cn.menu.main]]
    identifier = "documentation"
    pre = ""
    post = ""
    name = "文档"
    url = "/categories/documentation/"
    title = ""
    weight = 4
```

其中，`identifier`为分类名称，`name`是分类链接的名称。

然后在`content\categories\分类名`文件夹下添加相应`_index.md`文件即可。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210218180936.png)



## 3. 文件存储与访问

Hugo中可以存放文件的文件夹有`assets`和`static`:

1. 其中`assets`中的文件需要在正文中饮用后方可生成有效链接，详细参考[官方assets说明](https://gohugo.io/hugo-pipes/introduction/#asset-directory)
2. `static`下的文件可以直接使用链接的形式访问，例如路径为`static/Latex/Beamer/beamer_tutorial_2015.pdf`的文件，可以在`baseURL.Latex/Beamer/beamer_tutorial_2015.pdf`链接中访问到，详细参见[官方static说明](https://gohugo.io/content-management/static-files/)

## 0. 其他

`2021-02-18T17:57:18+08:00`中的`+8:00`表示太平洋标准时间

Yaml中的weight参数可以用来设置首页的展示优先级。

