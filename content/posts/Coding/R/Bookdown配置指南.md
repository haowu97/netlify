

Bookdown可以将一系列的`.Rmd` 文档连在一起然后输出一个分章节的完整文件，或者输出一个长文档(支持输出PDF、Gitbook、EPUB、Word 文档等格式)，与此同时还带来了诸如交叉引用等更多的功能。


## Bookdown安装与运行

- 在R控制台中运行`install.packages("bookdown")`即可完成安装。
- 下载下方的`Bookdown`压缩包(配置好的`Bookdown`模板)，解压至任一文件夹，该文件将作为主要的工作环境。

此处插入附件

- 打开`main.Rproj`文件进入`Rstudio`的项目界面，`Ctrl+O`打开`Content.rmd`

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200820225500.png)

- 将自己翻译的**正文部分**粘贴至`Content.rmd`文件
    - 统一将章名作为一级标题，小节名作为二级标题
    - 去掉原`rmd`文件的Yaml头(即文章开头---内的配置信息)
    - 完成后的`Content.rmd`如下图所示

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821080658.png)

注：可以在文章前面统一添加代码块设置，阻止报错等无关信息的显示；其中`collapse = TRUE`表示，将代码运行结果与源代码合并到单个代码块中输出，这样可以使内容更加紧凑，生成的图片‘到处跑’的情况更少发生；设置默认图片大小为页面宽度的80%，并且居中显示；`fig.show = "hold"`表示保留所有绘图，并将其输出到代码块的末尾；`fig.showtext=TRUE`使表格中的中文文字问题能够正常显示。更多代码块选项参考https://yihui.org/knitr/options/。

```markdown
​```{r setup, include=FALSE}
knitr::opts_chunk$set(
	echo = TRUE,
	message = FALSE,
	warning = FALSE,
	collapse = TRUE,
	out.width = "80%",
	fig.align='center',
	fig.show = "hold",
	fig.showtext=TRUE
)
​```
```

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821174323.png)

- 此时在R控制台输入以下命令，即可完成编译工作，想要实时预览自己的文件效果也可以用该命令

```R
bookdown::render_book('index.Rmd', 'bookdown::pdf_book')
```

- 编译好的文件位于`Bookdown`文件夹下的`_book`文件夹中：

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821081039.png)

## 脚注与参考文献

英文原文中，存在尾注与参考文献两种注释方式(分别对应文末的`Notes`与`Reference`章节)，并在正文中有对应的引用，且两种引用方式属于不同的编号体系，我们也需要分别做不同的处理：

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821131159.png)

### 脚注

脚注的处理方式为

```Markdown
正文内容...被注释内容[^1]

[^1]:脚注内容

正文内容...被注释内容[^2]

[^2]:脚注内容

正文内容...被注释内容[^T]

[^T]:脚注内容
```

正文内容(左)与显示效果(右)如下图所示

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821084542.png)

注：

- 脚注的标签可任意设置，只要前后统一即可，例如

```Markdown
正文内容...被注释内容[^ft1]

[^ft1]:脚注内容
```

- 不同脚注的标签不能重复，否则引用会发生错误
- 若脚注需要换行，可以采用`latex`语法

```latex
正文\footnote{第一行

第二行}
正文
```

### 参考文献

#### 文献信息导入

Rmarkdown 可以使用多种格式的参考文献库文件，比较常用的像`.bib` 或`.bibtex` 文件。简单地理解，这种文件就是把文献信息分解为各个诸如`title`、`author` 等字段存储起来，方便编译文档时将各个字段按所需格式组合的一种“数据库”。我们在百度学术上找到一篇文章，然后点击引用，再点击BibTex 按钮，即可下载一篇文献的.bib 信息：

![](https://cdn.sspai.com/2019/04/14/aab7ac15faf12063e3e650acb6aef706.jpeg?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1)

打开的网页会显示如下信息：

```
@article{赵俊华2017面向能源系统的数据科学,
  title={面向能源系统的数据科学:理论、技术与展望},
  author={赵俊华 and 董朝阳 and 文福拴 and 薛禹胜},
  journal={电力系统自动化},
  volume={41},
  number={4},
  pages={1-11},
  year={2017},
}
```

这就是关于一篇文章的信息了。

下面将其保存在`.bib` 格式的纯文本文件中：

- 以记事本方式打开`myref.bib`文件
- 将文章信息粘贴至`myref.bib`文件中，然后保存并关闭该文件即可

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821091251.png)

该文章就可以供我们接下来使用。当参考文献变多时，可以继续在后面粘贴信息；当然更高效的方法是先把文献导入Endnote、Papers、Zotero 等文献管理软件，然后一次性导出包含所有文献信息的`.bib` 文件。

#### 插入参考文献

万事具备，现在可以在文章中引用参考文献了。在正文中直接插入如下格式即可：

```
[@赵俊华2017面向能源系统的数据科学]
```

在`@` 符号后写上`.bib` 中该文献部分**大括号中第一行的字符**作为标识符，编译时即可找到这篇文献的信息。如果你觉得它太长了，删去后面的一些字也无妨，但不要和其他文献的标识重复。

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821130513.png)

如果有的文中不想引用，但需要在末尾的参考文献列表中列出的文献。这时需要在`index.Rmd`头部加入一个`nocite` 参数，并列出只需要在文末列表中出现的文献标识符。否则如果不做任何操作，即使文献信息被加入到`.bib` 文件之中，它也不会出现在文中的任何地方。(目前该方法好像不支持`pdf_book`格式，不过大家要是有没在正文引用的文献，还是先通过这种方式加上吧~)

```yaml
nocite: | 
  @item1, @item2
```

## 交叉引用

以下方法支持图表自动编号，以及在正文中引用图表，请大家统一按照以下方式插入图表：

### 图引用

#### 本地图片

首先将本地图片保存到`Figs`文件夹中，为了方便后续管理，以`章节名-图片序号`的方式命名，如第二章第一张图片为`2-1.png`。

引用采用以下语法：

```R
​```{r figureLable, echo=FALSE, out.width = "80%", fig.align='center' ,fig.cap='R 控制台'}
knitr::include_graphics("Figs/fig2.1.png")
​```

引用上图\@ref(fig:figureLable) 
```

其中`figureLable`是图片标签，可以唯一标识图片，正文引用时也是引用的该标签；`echo = FALSE`使该段代码不被显示；`out.width = 80%`表示占页面长度的80%；`fig.align`控制图片位置；`fig.cap`后面跟的是正文中显示的标题。

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821130713.png)

#### R绘制的图片

语法与本地图片引用类似：

```R
​```{r fig2, out.width = "80%", fig.align='center' ,fig.cap='散点图'}
x <- c(1,2,3.2,4,3,2.1,9,19)
plot(x) # 散点图
​```

引用上图\@ref(fig:fig2) 
```

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821130614.png)

R语言绘制的图表输出PDF，可能存在中文文字不显示的问题，解决方法如下：

1. 首先可以使用前文提到的`fig.showtext=TRUE` 设置；
2. 有时即使使用了`fig.showtext=TRUE`，由于图片宽度不够，仍然可能不显示中文，此时可以适当加长图表的宽度，如设置`out.width = "90%"`

##### R同时绘制多图

有时R多图必须在同一个代码块中绘制，则可以使用以下方法(目前该方法还不支持在正文中引用)：

```R
​```{r fig13, fig.show = 'asis', out.width = "80%", fig.align='center' ,fig.cap='带指标的股票价格图',fig.cap = '重新绘制的带指标的股票价格图'}
library(TTR)
library(quantmod)
AAPL <- getSymbols("AAPL", auto.assign=FALSE)
head(AAPL)
chartSeries(AAPL, subset='2010::2010-04', 
  theme = chartTheme('white'),
  TA = "addVo(); addBBands()")
# reChart()函数可以用来更新原始的图表，而不需要指定完整的参数集:
reChart(subset='2009-01-01::2009-03-03')
​```
```

### 表引用

#### 自制表格

自制表格的代码使用的是`Markdown`语法：

```
Table: (\#tab:simple-table) A simple table in Markdown.

| 运算符 | 描述                                        |
| ------ | ------------------------------------------- |
| :      | 冒号运算符。 它为向量按顺序创建一系列数字。 |
| %in%   | 此运算符用于标识元素是否属于向量。          |
| %*%    | 此运算符用于将矩阵与其转置相乘。            |

如表 \@ref(tab:simple-table) 展示了......
```

为了能够交叉引用Markdown表，该表必须具有以下形式的带标签的标题`Table: (\#tab:label) Caption here`，必须带有前缀`tab:`。

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821130659.png)

#### R产生的数据表

语法如下：

```R
​```{r label}
knitr::kable(iris[1:5, ], caption = 'A caption')
​```

如表 \@ref(tab:label) 展示了......
```

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200821130652.png)

### 公式引用

公式的引用采用Latex语法

```Latex
\begin{equation} 
  f\left(k\right) = \binom{n}{k} p^k\left(1-p\right)^{n-k}
  (\#eq:binom)
\end{equation}

然后在文中使用\@ref(eq:binom) 引用即可。
```

## 参考资料

[R语言教程 李东风](https://www.math.pku.edu.cn/teachers/lidf/docs/Rbook/html/_Rbook/index.html)

[Rmarkdown官方文档](https://bookdown.org/yihui/rmarkdown/)

[Bookdown官方文档](https://bookdown.org/yihui/bookdown/)

[Rmarkdown-cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/)

[用Rmarkdown 写论文——解决参考文献与交叉引用](https://sspai.com/post/53998)

[Bibtex格式说明](https://blog.csdn.net/kmsj0x00/article/details/85318057)