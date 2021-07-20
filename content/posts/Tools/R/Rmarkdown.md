---
title: "Rmarkdown配置与使用指南"
date: 2021-07-051T11:07:06+08:00
lastmod: 2021-07-06T16:07:06+08:00
draft: false

description: ""
upd: "R语言的编辑神器"

tags: ['R']
categories: []
---

如果需要插入一段 r 代码，可用如下形式：

```
​```{r}
1 + 1
​```
```

插入可运行的行内代码，例如文档里写入：

```
1 + 1 = `r 1 + 1`
```

你会在输出文档中直接得到“1 + 1 = 2”。

比较常用参数的包括 `echo` 设置是否在文档中包含代码块，`eval` 设置代码是否运行，`results` 设置运行结果的输出形式，`message` 和 `warning` 设置是否打印 message 和 warning 信息等等。你会看到每个代码块的右上角有一个用来设置常用属性的图形按钮，你也可以在这里设置属性。以下面的代码为例：

```
​```{r example label, echo = FALSE, warning = FALSE}
# coding
​```
```

这里设置了代码块的名称为 example label，然后使代码块不包括在文档中，同时不输出警告信息。

此之外，还有针对图片输出格式等等的更多细节属性设置，详细的参数可以参见[帮助文档](https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf)。如果你想设置全局的代码块属性，可以在文档开头加入如下代码：

```
​```{r setup}
knitr::opts_chunk$set()
​```
```

显而易见，该命令就是设置代码块选项的。在括号中填写需要更改的参数即可，语法与在每个代码块中设置属性时相同。到此为止，你已经可以顺利地在文档中插入可运行的代码，并且设置每个代码块的属性了。

### Initial

[Rmarkdown输出中文pdf解决方案](https://www.bioinfo-scrounger.com/archives/619/)

- 外部`Latex`（必要）
- Package: `devtool`（用来下载其他包）、`rmarkdown`（必要）、`rticle`（方案一）
- YAML中使用`xeCJK`（方案二）

```yaml
---
title: "中文"
CJKmainfont: Microsoft YaHei
output:
  pdf_document:
    includes:
      header-includes:
        - \usepackage{xeCJK}
    keep_tex: yes
    latex_engine: xelatex
---
```

## YAML示例

```yaml
---
title: "实证资产定价理论新进展"
author:
  - 石川（川总写量化）
  - llanglli（因子动物园）
  - 刀疤连（CQR）
abstract:
  近年来，实证资产定价理论发展呈现出千帆竞技、百舸争流的局面。本文梳理其中的重要成果。
output:
  rticles::ctex:
    latex_engine: xelatex
    fig_caption: yes
    number_sections: no
    toc: yes
    keep_tex: no
  html_document:
    theme: journal
    toc: yes
    toc_depth: '2'
documentclass: ctexart
geometry: "left=2.5cm,right=2cm,top=3cm,bottom=2.5cm"
colorlinks: yes
---
```

