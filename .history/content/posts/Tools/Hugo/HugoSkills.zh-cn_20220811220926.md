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

1. 其中`assets`中的文件需要在正文中引用后方可生成有效链接，详细参考[官方assets说明](https://gohugo.io/hugo-pipes/introduction/#asset-directory)
2. `static`下的文件可以直接使用链接的形式访问，例如路径为`static/Latex/Beamer/beamer_tutorial_2015.pdf`的文件，可以在`baseURL.Latex/Beamer/beamer_tutorial_2015.pdf`链接中访问到，详细参见[官方static说明](https://gohugo.io/content-management/static-files/)

## 图片插入

对于本地图片插入，可以使用相对路径。有以下两种方法：

设立 index.md 文件，方便，但是会让文件层级多一层。参考：

- [Hugo/Doks 静态网站图片插入问题](http://i.lckiss.com/?p=7455)
- [hugo-处理图片的方式](https://sqkikyo.com/post/hugo%E5%A4%84%E7%90%86%E5%9B%BE%E7%89%87%E7%9A%84%E6%96%B9%E5%BC%8F/)

## 4. Google Analytics

作用：统计站点的流量情况。

参考

- [谷歌流量分析工具Google Analytics使用方法指南教程 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/136378374)

UA可以直接使用，但是 UA 在2023年将被弃用！

- [Hugo中使用Google Analytics · 零壹軒·笔记 (qidong.name)](https://note.qidong.name/2017/07/05/google-analytics-in-hugo/)

- [How to add Google Analytics to your Hugo site | Charly3Pins](https://charly3pins.dev/blog/how-to-add-google-analytics-to-your-hugo-site/)

- [如何为网站设置UA Google Analytics（分析） - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/371973749)

- [为 Hugo 配置 Google Analytics | 长风 (immwind.com)](https://immwind.com/google-analytics-for-hugo/)

- [Hugo设置Google Analysis_WingsZeng的博客-CSDN博客](https://blog.csdn.net/weixin_42465278/article/details/117368515)

GA4 添加防范参考，目前还没有成功过：

- [Google Analytics | Hugo学习笔记 (skyao.io)](https://skyao.io/learning-hugo/docs/theme/docsy/googleanalytics.html)

- [Add Minimal Analytics (Google Analytics v4) to Hugo - tips & tricks - HUGO (gohugo.io)](https://discourse.gohugo.io/t/add-minimal-analytics-google-analytics-v4-to-hugo/39016)

## 0. 其他

`2021-02-18T17:57:18+08:00`中的`+8:00`表示太平洋标准时间

Yaml中的weight参数可以用来设置首页的展示优先级。
