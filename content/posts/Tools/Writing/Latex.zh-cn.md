---
title: "Latex使用笔记"
date: 2021-05-21T17:38:51+08:00
lastmod: 2021-05-22T17:38:51+08:00

draft: false

description: ""
upd: "Latex速查，Beamer教程"

tags: ['笔记', 'Latex']
categories: ['实用软件']
---

[Muboard - Mathematics Chalkboard With LaTeX and Markdown Support](https://muboard.net/)

[特殊符号大全 (fhdq.net)](http://www.fhdq.net/)

## 公式

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



## 	表格

添加居中表格

```latex
\begin{table}[h]
  \centering
	\begin{tabular}{lll}
	……
	\end{tabular}
\end{table}
```





## 希腊字母

| 序号 | 大写 | 小写 |          国际音标[推荐]           |  英文   |    汉字注音     | Latex命令                   | 常用指代意义                                                 |
| :--: | :--: | :--: | :-------------------------------: | :-----: | :-------------: | --------------------------- | :----------------------------------------------------------- |
|  1   |  Α   |  α   |              /'ælfə/              |  alpha  |     阿尔法      | `\alpha`                    | 角度，系数，角加速度                                         |
|  2   |  Β   |  β   |         /'bi:tə/ /'beɪtə/         |  beta   |    贝塔/毕塔    | `\beta`                     | 磁通系数，角度，系数                                         |
|  3   |  Γ   |  γ   |              /'gæmə/              |  gamma  |    伽玛/甘玛    | `\gamma`                    | 电导系数，角度，比热容比                                     |
|  4   |  Δ   |  δ   |             /'deltə/              |  delta  |  德尔塔/岱欧塔  | `\delta`                    | 变化量，化学反应中的加热，屈光度，一元二次方程中的判别式     |
|  5   |  Ε   |  ε   |            /'epsɪlɒn/             | epsilon |    艾普西龙     | `\varepsilon` or `\epsilon` | 对数之基数，介电常数                                         |
|  6   |  Ζ   |  ζ   |             /'zi:tə/              |  zeta   |      泽塔       | `\zeta`                     | 系数，方位角，阻抗，相对黏度                                 |
|  7   |  Η   |  η   |              /'i:tə/              |   eta   |    伊塔/诶塔    | `\eta`                      | 迟滞系数，效率                                               |
|  8   |  Θ   |  θ   |             /'θi:tə/              |  theta  |      西塔       | `\theta`                    | 温度，角度                                                   |
|  9   |  Ι   |  ι   |             /aɪ'əʊtə/             |  iota   |     埃欧塔      | `\iota`                     | 微小，一点                                                   |
|  10  |  Κ   |  κ   |              /'kæpə/              |  kappa  |      堪帕       | `\kappa`                    | 介质常数，绝热指数                                           |
|  11  |  ∧   |  λ   |             /'læmdə/              | lambda  |     兰姆达      | `\lambda`                   | 波长，体积，导热系数; 强度                                   |
|  12  |  Μ   |  μ   |              /mju:/               |   mu    |      谬/穆      | `\mu`                       | 磁导系数，微，动摩擦系（因）数，流体动力黏度; 数学期望       |
|  13  |  Ν   |  ν   |              /nju:/               |   nu    |      拗/奴      | `\nu`                       | 磁阻系数，流体运动粘度,光子频率，化学计量数                  |
|  14  |  Ξ   |  ξ   | 希腊: /ksi/ 英美: /ˈzaɪ/或/ˈksaɪ/ |   xi    |     可西/赛     | `\xi`                       | 随机变量，（小）区间内的一个未知特定值                       |
|  15  |  Ο   |  ο   |     /əuˈmaikrən/ /ˈɑmɪˌkrɑn/      | omicron | 欧 (阿~) 米可荣 | `\omicron`                  | 高阶无穷小函数                                               |
|  16  |  ∏   |  π   |               /paɪ/               |   pi    |       派        | `\pi`                       | 圆周率，π(n)表示不大于n的质数个数                            |
|  17  |  Ρ   |  ρ   |               /rəʊ/               |   rho   |      柔/若      | `\rho`                      | 电阻系数，柱坐标和极坐标中的极径，密度                       |
|  18  |  ∑   |  σ   |             /'sɪɡmə/              |  sigma  |     西格玛      | `\sigma`                    | 总和，表面密度，跨导，正应力; 标准差                         |
|  19  |  Τ   |  τ   |            /tɔ:/ /taʊ/            |   tau   |      套/驼      | `\tau`                      | 时间常数，切应力，2π（两倍圆周率）                           |
|  20  |  Υ   |  υ   |       /ˈipsilon/ /ˈʌpsɨlɒn/       | upsilon | 宇 (阿~) 普西龙 | `\upsilon`                  | 位移                                                         |
|  21  |  Φ   |  φ   |               /faɪ/               |   phi   |    弗爱/弗忆    | `\phi`                      | 磁通，角，透镜焦度，热流量                                   |
|  22  |  Χ   |  χ   |               /kaɪ/               |   chi   |     凯/柯义     | `chi`                       | 统计学中有卡方(χ^2)分布                                      |
|  23  |  Ψ   |  ψ   |              /psaɪ/               |   psi   |  赛/普赛/普西   | `\psi`                      | 角速，介质电通量，ψ函数                                      |
|  24  |  Ω   |  ω   |        /'əʊmɪɡə/ /oʊ'meɡə/        |  omega  |  欧米伽/欧枚嘎  | `\omega`                    | 欧姆，角速度，交流电的电角度，化学中的质量分数; 概率论：必然事件、样本空间; |

参考

1. [希腊字母表](https://xilazimu.net/)
2. [希腊字母和LaTeX命令对照表](https://www.xilazimu.net/m/articles/greek_letter_latex.html)

## Beamer

官方主题一览： https://mpetroff.net/files/beamer-theme-matrix/

Beamer教程：

1. [使用 Beamer 制作学术讲稿](https://www.wuhao.ink/Latex/Beamer/beamer_tutorial_2015.pdf)
2. [Beamer 演示学习笔记](https://www.wuhao.ink/Latex/Beamer/beamerlog-1112.pdf)

## 参考资料

1. Tex用户主页http://www.tug.org/
2. Texi英文社区https://tex.stackexchange.com/
3. Alex工作室https://www.latexstudio.net/
4. [武汉大学黄正华老师的中文Latex安装与使用](http://aff.whu.edu.cn/huangzh/中文Latex安装与使用.pdf)
5. [北京大学李东风老师的Latex排版心得](https://www.math.pku.edu.cn/teachers/lidf/docs/textrick/tricks.pdf)
6. 《 Latex入门》刘海洋著
7. 《 Alex2e完全学习手册》胡伟著