---
title: "用 VSCode 写 Markdown"
date: 2022-07-28T10:54:24+08:00
draft: false

description: "当 Windows 端 Typora 开始收费，VSCode 成为了我的最佳 Markdown 编辑器。"
upd: "当 Windows 端 Typora 开始收费，VSCode 成为了我的最佳 Markdown 编辑器。"

tags: ['Markdown', 'VSCode']
categories: []
output: pdf_document
---

<!--more-->

- [Markdown预览](#markdown预览)
- [Markdown导出](#markdown导出)
- [常用快捷键](#常用快捷键)
  - [Markdown快捷键](#markdown快捷键)
  - [VSCode快捷键](#vscode快捷键)
- [表格编辑](#表格编辑)

VScode 写 Markdown的**插件推荐**：
- `Markdown All in One`：提升 Markdown 书写体验——补全等；
- `Markdown Preview Enhanced`：Markdown实时预览；
- `Code Spell Checker`: 英文拼写检查。

# Markdown预览

方法一：`Ctrl + Shift + V`，在当前窗口打开预览窗口。

方法二：`Ctrl + K  V`，在侧边栏打开预览窗口（更常用）。

1. 先按Ctrl + K
2. 松开Ctrl，再按V

# Markdown导出

在预览页面可以右键直接导出 HTML、PDF、图片等格式。

还可以借助 Pandoc 导出 docx、PDF 等格式。需要以下步骤：

1. 安装 Pandoc
2. 在 Markdown 文档的 front-matter 中声明导出文件类型，例如：

```yaml
# 导出 Word 文档
output: word_document
# 导出 PDF 文档
output: pdf_document
```



# 常用快捷键

## Markdown快捷键

| 功能         | 快捷键             |
| ------------ | ------------------ |
| 插入行内公式 | `Ctrl + M`         |
| 插入行间公式 | `Ctrl + M` x 2     |
| 标题级数增加 | `Ctrl + Shift + ]` |
| 标题级数减少 | `Ctrl + Shift + [` |
| 表格格式化   | `Alt + Shift + F`  |

## VSCode快捷键

![](https://code.visualstudio.com/assets/docs/getstarted/tips-and-tricks/KeyboardReferenceSheet.png)

官方教程：
- [Visual Studio 中的键盘快捷方式](https://docs.microsoft.com/zh-cn/visualstudio/ide/default-keyboard-shortcuts-in-visual-studio?view=vs-2022)
- [Visual Studio Code Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)


| 功能            | 快捷键       |
| --------------- | ------------ |
| 切换文档        | `Ctrl + Tab` |
| 显示/隐藏侧边栏 | `Ctrl + B`   |




# 表格编辑

方法一：直接编辑表格，然后使用`Alt + Shift + F` 快捷键将表格格式化。

方法二：把word，excel里面的表格直接粘贴到网页[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)中，然后生成对应的整齐的Markdown表格。

参考资料：
- [教你Markdown+VSCODE实现最完美流畅写作体验_bilibili](https://www.bilibili.com/video/BV1si4y1472o)
- [如果使用VSCODE来写作Markdown](https://www.limfx.pro/ReadArticle/57/yi-zhong-xie-zuo-de-xin-fang-fa)
- [Markdown-LaTeX：经管人的VSCode配置大全_连享会](https://mp.weixin.qq.com/s/NDcsUCGeUapw5OhB7lTabg)


