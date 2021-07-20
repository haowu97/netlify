---
title: "Pandoc使用指南"
date: 2021-06-25T16:55:26+08:00
lastmod: 2021-06-26T16:55:26+08:00
draft: false

description: ""
upd: "文本文件格式转换神器！"

tags: ['笔记']
categories: ['实用软件']
---

## 简介

Pandoc用于Markdown、Latex、docx、HTML等文本文件格式互相转换，通过CMD命令可以快速实现。

- [官方文档](https://pandoc.org/index.html)

- [Github项目地址](https://github.com/jgm/pandoc)


## 具体用法

### 下载与安装

官方使用Github下载，速度较慢，可以用网盘老版本替代；

- [网盘下载地址](https://pan.baidu.com/s/13-ccE4sY9IMAvJmAp1tzHw)(2.9.2.1-windows-x86_64) 提取码：36gy

安装直接按照流程来即可，更改安装路径在高级选项中调整。

### 使用方法

打开cmd，首先定位到文件所在位置

```powershell
d:
cd D:\Workfiles\XMU\Course\AdvEconometric2\HomeWork\HW1
```

然后按照以下语法转换文件

```powershell
pandoc HW1.tex -f latex -t markdown -s -o HW1.md
```

文件名`HW1.tex`是pandoc要转换的文件。`-f latex -t markdown`表示将latex格式文件转化为markdown格式。`-s`选项表示创建一个“独立”文件，其中包含页眉和页脚，而不仅仅是文章内容。然后`-o HW1.md`表示输出的文件名为HW1.md。

| -s/--standalone | Produce   output with an appropriate header and footer |
| --------------- | ------------------------------------------------------ |
| **-f/--from**   | Specify input format                                   |
| **-t/--to**     | Specify output format                                  |

