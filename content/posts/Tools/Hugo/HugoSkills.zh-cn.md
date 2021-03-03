---
title: "Hugo使用技巧"
date: 2021-02-18T17:57:18+08:00
draft: true

description: ""
upd: ""

tags: [Blog, Hugo]
categories: ["Hugo博客搭建"]
---

## 给博文添加标签和分类

方法一

```
categories:
  - documentation
```

方法二

```
tags: ["Blog", "Hugo"]
categories: ["Hugo博客搭建"]
```

其中，引号可以省略。

## 在标签栏添加分类链接

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





`2021-02-18T17:57:18+08:00`中的`+8:00`表示太平洋标准时间

