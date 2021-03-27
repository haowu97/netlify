# Latex杂记

## 1. 公式

### 1.1 公式环境

Markdown中通过`$$`可引入Latex公式的编辑环境()，以下用法也能在该环境中实现

a. 行内公式：`$公式内容$`

b. 行间公式

```latex
$$
	%公式内容
$$
```

c. 带编号公式

编号随文章equation环境公式个数自动变化

```latex
\begin{equation}
  公式内容
\end{equation}
```

注：Markdown中equation环境可以用`\\`实现换行，而Latex则不行

d. 公式引用

```latex
\usepackage{hyperref}%开头导入依赖包
\begin{equation}\label{公式标签}
  公式内容
\end{equation}

\autoref{公式标签}%正文引用处
```

注：Markdown中不能使用

e. 多行公式

- 多行公式共用一个编号

```latex
\usepackage{amsmath}%开头导入依赖包
\begin{equation}
	\begin{split}
公式内容 \\
公示内容...
	\end{split}
\end{equation}
```

- align环境，每行公式单独编号

```latex
\begin{align}
	公式内容 \\
	公示内容...
\end{align}
```

- align*与align功能相同，但不编号

```latex
\begin{align*}
	公式内容 \\
	公示内容...
\end{align*}
```

- aligned环境，必须依赖于已经构建好的公式环境，例如`$$`、equation等，常用于构建多列公式

```latex
$$
\begin{aligned}
	%公式内容 \\
	%公示内容...
\end{aligned}
$$
```

注：

- 多行公式中可以在每行`&`对齐；
- Markdown中可以直接使用amsmath包的功能；
- Typora中可以直接用`\\`输入多行公式，但其他平台不允许，建议添加多行公式环境。

f. 分段函数

```latex
\usepackage{amsmath}%开头导入依赖包
\begin{equation}
	Y(x)=
	\begin{cases}
	0&, \text{if $x<0$}\\
	x+1&, \text{if $x>0$}\\
	1&, \text{otherwise.}
	\end{cases}
\end{equation}
```

### 1.2 常用符号

1.2.1关系运算符

|           | 输入            | 输出      |
| --------- | --------------- | --------- |
| 大于等于  | `\ge`或者`\geq` | $\ge$     |
| 小于等于  | `\le`或者`\leq` | $\le$     |
| 相似/服从 | `\sim`          | $\sim$    |
| 约等于    | `\approx`       | $\approx$ |
|           |                 |           |

数学运算符

|      | 输入     | 输出       |
| ---- | -------- | ---------- |
| 导数 | `f'(x)`  | $f'(x)$    |
| 极限 | `\lim x` | $ \lim x $ |
|      |          |            |

箭头

|            | 输入                      | 输出                  |
| ---------- | ------------------------- | --------------------- |
| 右箭头     | `\to`                     | $\to$                 |
| 推导出     | `\implies`or`\Rightarrow` | $ \Rightarrow $       |
| 被推导出   | `\impliedby`              | $\impliedby$          |
| 不推导出   | `\nRightarrow`            | $\nRightarrow$        |
| 等价于     | `\iff`                    | $\iff$                |
| 箭头加文字 | `\underrightarrow{p}`     | $\underrightarrow{p}$ |
|            |                           |                       |
|            |                           |                       |



|        | 输入            | 输出            |
| ------ | --------------- | --------------- |
| 下划线 | `\underline{x}` | $\underline{x}$ |
|        |                 |                 |
|        |                 |                 |



### 1.3 公式内部字体大小设置

在Mrakdown中通过以下方式可以调整公式部分字体大小

```latex
{\small a} x+1
```

而Latex中要更麻烦一些

```Latex
{\tiny a} x+1
\begin{equation}
	\text{{\Large $a$}}x+1
\end{equation}
```

常用的字号调整符

| 符号          | 效果                     |
| ------------- | ------------------------ |
| `\tiny`       | $\tiny smallest$         |
| `\scriptsize` | $\scriptsize very small$ |
| `\small`      | $\small small$           |
| `\normalsize` | $\normalsize normall$    |
| `\large`      | $\large large$           |
| `\Large`      | $\Large Large$           |
| `\LARGE`      | $\LARGE LARGE$           |
| `\huge`       | $\huge huge$             |
| `\Huge`       | $\Huge Huge$             |

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200417151823.jpg)

### 1.4 字体

|              | 符号              | 效果                |
| ------------ | ----------------- | ------------------- |
| 加粗         | `\mathbf`或`\bf`  | $ \bf{bf} $         |
| 黑板报粗体   | `\mathbb`或`\Bbb` | $\Bbb{Bbb}$         |
| 粗体希腊字母 | `\boldsymbol`     | $\boldsymbol{bold}$ |
| 手写体/花体  | `\mathcal`        | $\mathcal{MATHCAL}$ |

### 1.5 文字相对位置

|              | 符号         | 效果                        |
| ------------ | ------------ | --------------------------- |
| 上加文字     | `\overset`   | $ \overset{0.96}{9.89} $    |
| 下加文字     | `\underset`  | $ \underset{0.96}{9.89} $   |
| 上加文字     | `\stackrel`  | $\stackrel{p}{\rightarrow}$ |
| 上加括号文字 | `\overbrace` | $\overbrace{kkk}^{sss}$     |
|              |              |                             |

公式人工添加编号

```
$$ 
a = b \tag{1.1} 
$$
```



## 	2. 表格

添加居中表格

```latex
\begin{table}[h]
  \centering
	\begin{tabular}{lll}
	……
	\end{tabular}
\end{table}
```

详细参见

1. Tex用户主页http://www.tug.org/
2. Texi英文社区https://tex.stackexchange.com/
3. Alex工作室https://www.latexstudio.net/
4. [武汉大学黄正华老师的中文Latex安装与使用](http://aff.whu.edu.cn/huangzh/中文Latex安装与使用.pdf)
5. [北京大学李东风老师的Latex排版心得](https://www.math.pku.edu.cn/teachers/lidf/docs/textrick/tricks.pdf)
6. 《 Latex入门》刘海洋著
7. 《 Alex2e完全学习手册》胡伟著