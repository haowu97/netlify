---
title: "Rmarkdown导出PDF以及中文解决方案"
date: 2021-07-05T11:07:06+08:00
draft: false

description: "R语言的编辑神器。"
upd: "R语言的编辑神器。"

tags: ['笔记', 'R']
categories: ['R语言使用经验']
---

<!--more-->

> Rmarkdown非常适合R语言使用者导出格式漂亮的文档，但是输出中文PDF的过程中会遇到各种麻烦的问题，本文整理了我解决该问题的经验供大家参考。

总的来说，通过Rmarkdown输出中文版pdf报告，要解决以下两个核心问题：

- 导出PDF需要配置TeX环境，以下两种方案都可以：
  - 安装TinyTex
  - 安装任一LaTeX套件（TeX Live\CTeX\MiKTex\MacTeX）
- PDF中文显示问题，下面两种方案中更推荐后者：
  - 在YAML中写入LaTeX的一些设置；
  - 使用`rticles`包中的CTeX Documents模板

下面以事件先后顺序为线索详细介绍Rmarkdown输出中文版pdf报告的解决方案。

## Rmarkdown导出PDF

首先需要解决的是创建Rmarkdown并导出PDF的问题。

安装好R语言与Rstudio之后，通过菜单栏`File >>New File >>R Markdown`可以直接在Rstudio上创建一个新的Rmarkdown文档，第一次创建会弹出对话框提示需要安装以下R包，点击Yes即可

<img src="https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210401204720.png" style="zoom: 67%;" />

再次点击菜单栏`File>> New File>> R Markdown`，弹出以下对话框点击OK后，可以成功地创建Rmarkdown文件

<img src="https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210401204735.png" alt="图1.5" style="zoom:67%;" />

但是如果要导出PDF，会出现报错`pdflatex not found`

<img src="https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210401204745.png" alt="图3" style="zoom: 80%;" /> 

根据报错需要安装相应的LaTeX环境，此处有多种方案可以选择

- 安装一个常用的TeX集成编辑环境，如TeX Live，CTeX，MiKTex，MacTeX任选其一即可，安装过程比较漫长；

- 比较简单的方式是，使用谢益辉大神的开发的`TinyTeX`包，能很好的兼容Rmarkdown，安装相对比较方便快捷，参考[TinyTeX中文文档](https://yihui.org/tinytex/cn/)，直接在Rstudio控制台输入以下命令即可：

```R
install.packages('tinytex')
tinytex::install_tinytex()
```

一台电脑上同时存在多种TeX环境会产生冲突，因此益辉大神建议安装TinyTex之前需要卸载电脑中的其他 LaTeX 套装（TeX Live 或 MiKTeX 或 MacTeX）。

考虑到后续论文写作需求，我选择了安装目前比较常用的[TeX Live](http://www.tug.org/texlive/)。经历了漫长的TeX Live安装并重新启动Rstudio之后，Rmarkdown文件就可以正常导出成PDF了，但还不能显示中文。

## PDF中文解决方案

完成上述步骤后，接下来解决中文输出的问题，有两种方案可以选择：

方案一，在原有的Rmarkdown模板基础上，在YAML中加上命令调用LateX的xeCJK包，即把原有的Rmarkdown文件头改成如下格式：

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
上述方法能够解决中文显示的问题，但是原始Rmarkdown模板是基于英文写作习惯设计，如果全篇用中文写作会很奇怪，且模板格式比较单一。

因此**强烈安利方案二**，谢益辉大神写的Rmarkdown的模板包[rticles](https://github.com/rstudio/rticles)，里面的CTeX Documents就是支持中文pdf的模板，除此之外还有适用于国际期刊的Rmarkdown模板，通过以下命令即可安装：

```R
install.packages("rticles")
```

此时再次创建新的Rmarkdown文档，会出现很多新的模板，选择`CTeX Document`即可

<img src="https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210401204752.png" style="zoom:67%;" />

此外，原有`CTeX Document`模板的页边距较大，可以在YAML中加入`geometry`选项调节页边距：

```yaml
---
title: "R语言简介"
author:
  - PurePlayer
documentclass: ctexart
geometry: "left=2.5cm,right=2cm,top=3cm,bottom=2.5cm"
output:
  rticles::ctex:
    fig_caption: yes
    number_sections: yes
    toc: yes
classoption: "hyperref,"
---
```

然后就可以导出自动生成目录、页眉、标题序号的PDF了，至此大功告成！

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210401204755.png)