---
title: "用 VSCode 写 Markdown"
date: 2022-07-28T10:54:24+08:00
draft: false

description: "当 Windows 端 Typora 开始收费，VSCode 成为了我的最佳 Markdown 编辑器。"
upd: "当 Windows 端 Typora 开始收费，VSCode 成为了我的最佳 Markdown 编辑器。"

tags: ['Markdown', 'VSCode']
categories: []
---

<!--more-->

VScode 写 Markdown的**插件推荐**：
- `Markdown All in One`：提升 Markdown 书写体验——补全等；
- `Markdown Preview Enhanced`：Markdown实时预览；
- `Code Spell Checker`: 英文拼写检查。

## Markdown预览

方法一：`Ctrl + Shift + V`，在当前窗口打开预览窗口。

方法二：`Ctrl + K  V`，在侧边栏打开预览窗口（更常用）。

1. 先按Ctrl + K
2. 松开Ctrl，再按V

## Markdown导出

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
参考：
- [markdown preview enhanced文档（简体中文版）](https://www.bookstack.cn/read/mpe/zh-cn-pandoc-word.md)

## 常用快捷键

### Markdown快捷键

| 功能         | 快捷键             |
| ------------ | ------------------ |
| 插入行内公式 | `Ctrl + M`         |
| 插入行间公式 | `Ctrl + M` x 2     |
| 标题级数增加 | `Ctrl + Shift + ]` |
| 标题级数减少 | `Ctrl + Shift + [` |
| 表格格式化   | `Alt + Shift + F`  |

### VSCode快捷键

![](https://code.visualstudio.com/assets/docs/getstarted/tips-and-tricks/KeyboardReferenceSheet.png)

官方教程：
- [Visual Studio 中的键盘快捷方式](https://docs.microsoft.com/zh-cn/visualstudio/ide/default-keyboard-shortcuts-in-visual-studio?view=vs-2022)
- [Visual Studio Code Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)


| 功能            | 快捷键       |
| --------------- | ------------ |
| 切换文档        | `Ctrl + Tab` |
| 显示/隐藏侧边栏 | `Ctrl + B`   |

## 表格编辑

方法一：直接编辑表格，然后使用`Alt + Shift + F` 快捷键将表格格式化。

方法二：把word，excel里面的表格直接粘贴到网页[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)中，然后生成对应的整齐的Markdown表格。

## Markdown 写作规范

各级标题的用途和书写要求：

```
.
└── 一级标题（文章标题）
    ├── 二级标题（文章内容的大框架）
    │   ├── 三级标题（多个方面阐述二级标题）
    │   ├── 三级标题
    │   └── 三级标题
    │       ├── 四级标题（谨慎使用四级标题，尽量避免出现，保持层级的简单，防止出现过于复杂的章节）
    │       └── 四级标题
    ├── 二级标题
    │   ├── 段落一（避免孤立编号，即同级标题只有一个。假如二级标题下只有一个三级标题，则省略，改用段落）
    │   ├── 段落二
    │   └── 段落三
    └── 二级标题
```


其他：

- [Markdown 写作规范](https://keatonlao.gitee.io/a-study-note-for-markdown/document-style/)

参考资料：

- [教你Markdown+VSCODE实现最完美流畅写作体验_bilibili](https://www.bilibili.com/video/BV1si4y1472o)
- [如果使用VSCODE来写作Markdown](https://www.limfx.pro/ReadArticle/57/yi-zhong-xie-zuo-de-xin-fang-fa)
- [Markdown-LaTeX：经管人的VSCode配置大全_连享会](https://mp.weixin.qq.com/s/NDcsUCGeUapw5OhB7lTabg)


