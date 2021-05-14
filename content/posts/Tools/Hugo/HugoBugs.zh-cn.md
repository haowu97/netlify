---
title: "Hugo踩坑指南"
date: 2021-05-12T21:17:53+08:00
lastmod: 2021-05-13T21:17:53+08:00
draft: false

description: ""
upd: "Hugo Bug汇总"

tags: [Blog, Hugo]
categories: ["Hugo博客搭建"]
---

## Failed to render pages

```
ERROR 2021/04/13 22:27:28 Failed to render pages: render of "home" failed: execute of template failed: template: index.html:36:20: executing "content" at <.Render>: error calling Render: failed to execute template ["summary"] v: "D:\Workfiles\Blog\uBloggerSite\themes\uBlogger\layouts\_default\summary.html:59:29": execute of template failed: template: _default/summary.html:59:29: executing "_default/summary.html" at <partialCached "function/path.html" . .>: error calling partialCached: partial that returns a value needs a non-zero argument.
```

有两种原因都可能导致上述错误：

1. Markdown文档中有奇怪的字符组合(非常离谱的才会导致这种错误)
2. YAML头出现这种空置的引号`categories: [""]`，去掉引号即可正常显示

```yaml
---
title: "10. 理解货币"
date: 2021-04-10T12:11:59+08:00
lastmod: 2021-04-11T12:11:59+08:00
draft: false

description: ""
upd: "货币创造"

tags: ["笔记"]
categories: [""]
---
```

## Failed to get JSON resource

```
ERROR 2021/05/14 23:02:02 Failed to get JSON resource "https://api.twitter.com/1/statuses/oembed.json?id=877500564405444608&dnt=true": Get "https://api.twitter.com/1/statuses/oembed.json?id=877500564405444608&dnt=true": dial tcp 31.13.94.7:443: connectex: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.
If you feel that this should not be logged as an ERROR, you can ignore it by adding this to your site config:
ignoreErrors = ["error-remote-getjson"]
```

报错中已经给出了解决方法：`If you feel that this should not be logged as an ERROR, you can ignore it by adding this to your site config: ignoreErrors = ["error-remote-getjson"]`

即在 `config.toml` 文件中添加 `ignoreErrors = ["error-remote-getjson"]`(不需要缩进)。

参考[BUG: Failed to get JSON resource - API.instagram Bad request · Issue #205 · pacollins/hugo-future-imperfect-slim (github.com)](https://github.com/pacollins/hugo-future-imperfect-slim/issues/205)

