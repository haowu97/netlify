---
title: "Marp"
date: 2022-10-11T17:00:13+08:00
draft: true

description: ""
upd: ""

tags: []
categories: []
---

<!--more-->

通过编辑器右上角的 Marp 图标按钮就可以调出 Export slide deck... 命令并导出幻灯片了。 Marp 插件目前支持导出 HTML 和 PDF 格式，另外可以将首页导出为 PNG 或 JPEG 格式的图片。

Marp 预览功能和 Markdown Preview Enhanced 冲突，因此需要关闭 Markdown Preview Enhanced 插件，否则无法预览。

Marp 默认只提供三种主题，分别为 default、gaia 和 uncover。

无序列表语法 * 被保留为放映幻灯片时会按元素依次显示列表内容，- 与 + 可同时显示所有内容；类似的，有序列表语法 1) 被保留为依次显示列表元素，1. 为同时显示所有元素。

## 常用指令

除了页面分割符---，如果文章结构比较清晰，我们还可以使用全局指令 headingDivider 分隔幻灯片页面。换句话说，就是 headingDivider 通过识别 Markdown 文档的标题来实现幻灯片分页。

当前页面不显示页码：

```
<!-- _paginate: false -->
```

`<!-- fit -->` 用于自动调整标题（一级标题）大小，以适应幻灯片大小。

## Reference

- [用 Marp 基于 markdown 制作幻灯片](https://caizhiyuan.gitee.io/categories/skills/20200730-marp.html)
- [用Markdown制作幻灯片-五分钟学会Marp（上篇）](https://www.lianxh.cn/news/97fccdca2d7a5.html)
- [用Markdown制作幻灯片-五分钟学会Marp（下篇）](https://www.lianxh.cn/news/521900220dd33.html)
- [Marp：用 Markdown「写」PPT 的新选择](https://sspai.com/post/55718)
- [一种用markdown写PPT的方法，再也不用费劲排版了](https://zhuanlan.zhihu.com/p/149521766)
- [Marp：用 Markdown 写 PPT 成为可能](https://juejin.cn/post/7018443193146408973)
- [Marp 官方文档](https://marpit.marp.app/)
- [Markdown-LaTeX：经管人的VSCode配置大全](https://mp.weixin.qq.com/s/NDcsUCGeUapw5OhB7lTabg)