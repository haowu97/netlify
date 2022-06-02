---
title: "经典线性回归模型"
date: 2021-03-21T21:17:53+08:00
draft: false

description: "经典线性回归模型：假设、估计量性质、检验与应用。"
upd: "经典线性回归模型：假设、估计量性质、检验与应用。"

tags: ['笔记']
categories: ['计量经济学']

---

<!--more-->

# 1. General Regression Analysis

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223329.png)

统计：计量经济学——推断统计；经济统计——描述统计。

核心逻辑$\hat{\beta} \overset{p}{\rightarrow}  \beta^ * \overset{模型正确设定}{=} \beta ^o$ 

当且仅当模型正确设定时，$\beta^*$可以被解释为边际效应

Hausman检验可以用来检验设否正确设定

当假定$u$服从正太分布时，$E(xu)=0$与$E(u|X)=0$等价

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223348.png)
$$
\operatorname{MSE}_{T}(\theta)=\operatorname{Var}_{\theta}(T)+\left[B_{T}(\theta)\right]^{2}
$$

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223530.png)

### 1.1 回归本质在估计$E(Y|X) $

在经典回归模型中，我们希望用解释变量(regressand)$X$的函数$g(X)$来预测被解释变量(regressor)$Y$。此时需要一个标准来测度$g(X)$与$Y$的接近程度，**均方误(mean squared error, MSE)准则**最常被使用，MSE是预测误差（预测值$g(X)$与目标$Y$之差）的平方的期望，表达式如下
$$
\operatorname{MSE}(g)=E[Y-g(X)]^{2} = \int\int[y-g(x)]^2f_{XY}(x,y)\mathrm{d} x\mathrm{d} y
$$

其中，$f_{XY}(x,y)$是变量$X$和$Y$的联合概率分布。

显然，MSE越小，$g(X)$对$Y$的预测能力越强。因此现在的问题转换为，**求解使MSE最小的函数$g(·)$**，注意到MSE是函数$g(·)$的函数。

事实上，**条件均值$E(Y|X)$就是使MSE最小的函数$g_0(X)$**，可以用求微分和方差分解两种方法证明（证明见文末附录）。

需要注意的是，条件均值$E(Y|X)$是$X$而非$Y$的函数。

MSE是衡量$g(X)$对$Y$的预测能力的准则之一，但非唯一准则。例如，平均绝对误差(mean absolute error, MAE)，

$$
\operatorname{MAE}(g)=E|Y-g(X)|
$$

此时，**使MAE最小的函数$g(X)$是条件中位数**，分位数回归采用的正是该准则。

相比MAE，MSE具有连续可导的优良性质。

令**回归等式**$Y=E(Y | X)+\varepsilon$，其中$\varepsilon$被称为回归扰动项，则有
$$
\begin{aligned} E(\varepsilon | X) &=E\{[Y-E(Y | X)] | X\} 
\\ &=E(Y | X)-E\left[g_{o}(X) | X\right] 
\\ &=E(Y | X)-g_{o}(X) 
\\ &=0 \end{aligned}
$$

**$E(\varepsilon|X) = 0$意味着$\varepsilon$不包含可用于预测$Y$的期望值的任何有关$X$的信息。换句话说，可用于预测$Y$的所有$X$的信息被包含在$E(Y|X)$中**。

进一步，
$$
E(\varepsilon)= E[E(\varepsilon | X)]=0
$$
$\varepsilon$与$X$正交
$$
\begin{aligned}
E(X \varepsilon) &=E[X E(\varepsilon | X)] \\
&=E(X \cdot 0) \\
&=0
\end{aligned}
$$
事实上 ，$E[\varepsilon h(X)]=0$ (对于任一的可测函数$h(·)$)与$E(\varepsilon |X)=0$等价。这说明即使用非线性的模型，也无法改进预测效果。

#### 附录

**引理：重复期望法则**(Law of Iterated Expectations, LIE)，对给定可测函数$G(X,Y)$，假设期望$E[G(X,Y)]$存在，则

$$
E[G(X, Y)]=E\{E[G(X, Y) | X]\}
$$

证明：仅考虑$\left(Y,X^{\prime}\right)^{\prime}$是连续随机向量的情形，有

$$
\begin{aligned} E[G(X, Y)] &=\iint_{-\infty}^{\infty} G(x, y) f_{X Y}(x, y) \mathrm{d} x \mathrm{d} y \\ &=\iint_{-\infty}^{\infty} G(x, y) f_{Y | X}(y | x) f_{X}(x) \mathrm{d} x \mathrm{d} y \\ &=\int\left[\int_{-\infty}^{\infty} G(x, y) f_{Y | X}(y | x) \mathrm{d} y\right] f_{X}(x) \mathrm{d} x \\ &=\int E[G(X, Y) | X=x] f_{X}(x) \mathrm{d} x \\ &=E\{E[G(X, Y) | X]\} \end{aligned}
$$

If $J$ contains more information than $I$, similarly, we have
$$
E(Y|I) = E[E(Y|J)|I]
$$

**定理**：条件均值$E(Y|X)$是下列问题的最优解
$$
\begin{aligned} E(Y | X) &=\arg \min _{g \in \mathbb{F}} M S E(g) \\ &=\arg \min _{g \in \mathbb{F}} E[Y-g(X)]^{2} \end{aligned}
$$

其中$\mathbb{F}$是所有可测和平方可积函数的集合，即

$$
\mathbb{F}=\left\{g: \mathbb{R}^{k+1} \rightarrow \mathbb{R} | \int g^{2}(x) f_{X}(x) \mathrm{d} x<\infty\right\}
$$

**法一**：方差分解

令$g_{0}(X) = E(Y | X)$，则

$$
\begin{aligned} \operatorname{MSE}(g) &=E\left[Y-g_{0}(X)+g_{0}(X)-g(X)\right]^{2} \\ &=E\left[Y-g_{0}(X)\right]^{2}+E\left[g_{0}(X)-g(X)\right]^{2}+2 E\left\{\left[Y-g_{0}(X)\right]\left[g_{0}(X)-g(X)\right]\right\}  \end{aligned}
$$

根据重复期望法则

$$
\begin{aligned} E\left\{\left[Y-g_{0}(X)\right]\left[g_{0}(X)-g(X)\right]\right\}
&=E\left\{E\left(\left[Y-g_{0}(X)\right]\left[g_{0}(X)-g(X)\right]|X\right)\right\}
\\ &=E\left\{\left[g_{0}(X)-g(X)\right]E\left(\left[Y-g_{0}(X)\right]|X\right)\right\}
\\ &=E\left\{\left[g_{0}(X)-g(X)\right][E(Y|X)-g_{0}(X)]\right\}
\\ &=E\left\{\left[g_{0}(X)-g(X)\right]·0\right\}
\\ &=0
 \end{aligned}
$$

$$
\implies MSE(g) =E\left[Y-g_{0}(X)\right]^{2}+E\left[g_{0}(X)-g(X)\right]^{2}
$$

$$
\implies \arg \min _{g \in \mathbb{F}} M S E(g) = g_0(X) = E(Y|X)
$$

**法二**：求微分法

$$
\operatorname{MSE}(g)=E[Y-g(X)]^{2} = \int\int[y-g(x)]^2f_{XY}(x,y)\mathrm{d} x\mathrm{d} y
$$

根据一阶条件，MSE对$g(X)$的导数为0
$$
\frac{\delta MSE(g)}{\delta g(x)}=-2\int[y-g(x)] f_{XY}(x,y) \mathrm{d} y=0
$$

$$
\implies \int g(x)f_{XY}(x,y) \mathrm{d}y = \int yf_{XY}(x,y) \mathrm{d}y
$$

$$
\implies g(x)\int f_{XY}(x,y) \mathrm{d}y = \int yf_{XY}(x,y) \mathrm{d}y
$$

$$
\implies g(x) f_X(x) = \int yf_{XY}(x,y) \mathrm{d}y
$$

$$
\implies g(x)  = \int y\frac{f_{XY}(x,y)}{f_X(x)} \mathrm{d}y
$$

$$
\implies g(x)  = \int yf_{Y|X}(y|x) \mathrm{d}y=E(Y|X)
$$

### 1.2 最优线性最小二乘估计$\beta^* $

$X  =(1,X_1,\ldots,X_k )^{\prime}$

$\beta  =(\beta _0,\beta _1,\ldots,\beta_k )^{\prime}$
$$
\min _{g \in \mathbf{A}} E[Y-g(X)]^{2}=\min _{\beta \in \mathbf{R}^{k+1}} E\left(Y-X^{\prime} \beta\right)^{2}
$$

The key feature of A is that g(X) = X 0β is linear in β; not in X

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223542.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223547.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223552.png)

最优最小二乘估计量，当且仅当$E(xu)=0$(一阶条件)

why：soc Hessian matrix is positive definite provided E(XX ) is nonsingula

非奇异推出正定

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223608.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223623.png)

### 1.3 模型正确设定

模型具有经济解释意义的前提的模型正确设定$E(u|x) = 0$

模型正确设定：
$$
Y=X^{\prime} \beta+u, \beta \in \mathbb{R}^{k+1}
$$
如果存在某个参数值$\beta ^o \in  \mathbb{R}^{k+1}$，有
$$
E(Y|X) = X^{\prime} \beta^o
$$
则是对$E(Y|X)$的正确设定

若对任意$\beta  \in  \mathbb{R}^{k+1}$
$$
E(Y|X) \neq X^{\prime} \beta
$$
则模型设定错误。

如果模型正确设定，系数可以解释为期望边际效应
$$
\beta^{o}=\frac{\mathrm{d} E(Y | X)}{\mathrm{d} X}
$$
定理：如果模型正确设定$\beta^ * \overset{模型正确设定}{=} \beta ^o$ 

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223634.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223643.png)


$$
E(\epsilon|X)=0 推出  E(\epsilon X) = 0
$$
# 2. 经典线性回归模型

经典的含义是：经典回归假设

$Z_t= \{ Y_t,X^{\prime}_t \}^n_{t=1}$是容量为n的样本，其中$Y_t$是一个标量，$X_t = (1,X_{1t}, \ldots,X_{kt})^{\prime}$
$$
\begin{aligned}
\boldsymbol{Y} &=\left(Y_{1}, \cdots, Y_{n}\right)^{\prime}, n \times 1 \\
\boldsymbol{\varepsilon} &=\left(\varepsilon_{1}, \cdots, \varepsilon_{n}\right)^{\prime}, n \times 1 \\
\boldsymbol{X} &=\left(X_{1}, \cdots, X_{n}\right)^{\prime}, n \times K
\end{aligned}
$$

$$
\boldsymbol{X} = 
\begin{pmatrix} 
1 & X_{11} & \ldots & X_{k1} \\ 
1 & X_{12} & \ldots & X_{k2} \\
\vdots & \vdots & \vdots & \vdots \\
1 & X_{1n} & \ldots & X_{kn}
\end{pmatrix}
$$

**截面数据**：样本之间相互独立（空间计量打破这一假设，假定样本之间存在地理关联）

**时间序列数据**：本质区别是样本之间存在相关性

**面板数据**

## 2.1 假定

#### 假设3.1 线性

$$
Y_t=X^{\prime}_t \beta^o + \varepsilon _t, \quad t=1,\ldots,n
$$

或者等价为
$$
\boldsymbol{Y} = \boldsymbol{X}\beta ^o+ \varepsilon
$$
该假设并不保证模型正确设定，模型正确设定当且仅当$E(\varepsilon_t|X_t)=0$

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223657.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223706.png)

#### 假设3.2 严格外生性

$$
E\left(\varepsilon_{t} | \boldsymbol{X}\right)=E\left(\varepsilon_{t} | X_{1}, \cdots, X_{t}, \cdots, X_{n}\right)=0 \quad t=1, \cdots, n
$$

由重复期望法则$E(\varepsilon _t| X_t)=0$，$E(\varepsilon_t) = 0 $（小信息集=0，如果大信息集条件期望为0）

如果严格外生性成立，则
$$
E(\boldsymbol{Y}|\boldsymbol{X})=E(\boldsymbol{X}\beta^o|\boldsymbol{X})+ E(\boldsymbol{\varepsilon} | \boldsymbol{X})=\boldsymbol{X}\beta^o
$$
意味着模型被正确设定。

进一步，对任意$t,s \in \{1,\dots,n\}$
$$
\begin{aligned}
E\left(X_{s} \varepsilon_{t}\right) &=E\left[E\left(X_{s} \varepsilon_{t} | \boldsymbol{X}\right)\right] \\
&=E\left[X_{s} E\left(\varepsilon_{t} | \boldsymbol{X}\right)\right] \\
&=E\left(X_{s} \cdot 0\right) \\
&=\mathbf{0}
\end{aligned}
$$
结合$E(\varepsilon_t)=0$，有$cov(X_s,\varepsilon_t)=0$。这排除了AR模型。

该假设的提出只是为了获得有限样本分布理论，对于大样本理论不需要严格外生性假设。

#### 假设3.3 非奇异

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223716.png)

非奇异也可表述为最小特征值>0，**保证了无多重共线性**

假设(2)保无近似多重共线性

$X^{\prime}X$是对称阵，可以称为样本$X$的信息矩阵，因为它测度了$X$中的信息含量

#### 假设3.4 球形误差方差

条件同方差
$$
E(\varepsilon^2_t |\boldsymbol{X})=\sigma^2,t=1,\dots,n
$$
条件无自相关
$$
E(\varepsilon_t \varepsilon_s |\boldsymbol{X})=0,\quad t \neq s,t,s \in \{1,\dots,n\}
$$
假设3.2与3.4可以结合起来表述为
$$
E(\boldsymbol{\varepsilon} | \boldsymbol{X})=\mathbf{0}, \boldsymbol{E}\left(\boldsymbol{\varepsilon \varepsilon}^{\prime} | \boldsymbol{X}\right)=\sigma^{2} \boldsymbol{I}
$$
其中$\boldsymbol{I} \equiv \boldsymbol{I}_{n}$  是一个$\boldsymbol{n} \times \boldsymbol{n}$单位阵

#### 假设3.5 条件正态分布

$$
\boldsymbol{\varepsilon} | \boldsymbol{X} \sim N\left(\mathbf{0}, \sigma^{2} \boldsymbol{I}\right)
$$
等价于$\varepsilon_t \sim IID \quad N(0, \sigma^2)$

假设3.5可以推导出假设3.2和3.4（$E(\boldsymbol{\varepsilon} | \boldsymbol{X})=\mathbf{0}, \boldsymbol{E}\left(\boldsymbol{\varepsilon \varepsilon}^{\prime} | \boldsymbol{X}\right)=\sigma^{2} \boldsymbol{I}$），进一步
$$
f(\boldsymbol{\varepsilon} |  \boldsymbol{X})=\frac{1}{(\sqrt{2 \pi \sigma^{2}})^{n}} \exp \left(-\frac{\boldsymbol{\varepsilon}^{\prime} \boldsymbol{\varepsilon}}{2 \sigma^{2}}\right)=f(\boldsymbol{\varepsilon})
$$

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611223847.png)

可以推导出，$\boldsymbol{\varepsilon}$ 独立于 $\boldsymbol{X}$

并且正态性+$Cov(\varepsilon_t, \varepsilon_s)=0, \forall t \neq s$可推导出$\varepsilon_t$独立于$\varepsilon_s$

因此假设3.5还能推出$\varepsilon_t, t=1,2,\ldots$是IID的正态分布

综上，这是一个非常严格的假定。

## 2.2 普通最小二乘估计OLS

### 2.2.1 OLS估计量的存在性

【OLS 估计量，ordinary least squares】定义线性回归模型$Y_t = X'_t \beta + u_t$  的残差平方和(sum of squared residuals, SSR)为
$$
\begin{equation}\begin{aligned}
\operatorname{SSR}(\beta) & \equiv(\boldsymbol{Y}-\boldsymbol{X} \beta)^{\prime}(\boldsymbol{Y}-\boldsymbol{X} \beta) \\
&=\sum_{t=1}^{n}\left(Y_{t}-X_{t}^{\prime} \beta\right)^{2}
\end{aligned}\end{equation}
$$

则OLS估计量是以下最优化问题的解
$$
\begin{equation}\hat{\boldsymbol{\beta}}=\arg \min _{\boldsymbol{\beta} \in \Bbb{R}^{K}} SSR(\boldsymbol{\beta})\end{equation}
$$

【定理 2.1】在假设3.1和3.3(1)下，OLS估计量$\hat{\beta} $存在，并且
$$
\begin{equation}\begin{aligned}
\hat{\beta} &=\left(\boldsymbol{X}^{\prime} \boldsymbol{X}\right)^{-1} \boldsymbol{X}^{\prime} \boldsymbol{Y} \\
&=\left(\frac{1}{n} \sum_{t=1}^{n} X_{t} X_{t}^{\prime}\right)^{-1} \frac{1}{n} \sum_{t=1}^{n} X_{t} Y_{t}
\end{aligned}\end{equation}
$$
证明：
$$
\begin{equation}\begin{aligned}
\frac{\operatorname{d} SSR(\beta)}{\mathrm{d} \beta} &=\frac{\mathrm{d}}{\mathrm{d} \beta} \sum_{t=1}^{n}\left(Y_{t}-X_{t}^{\prime} \beta\right)^{2} \\
&=\sum_{t=1}^{n} \frac{\partial\left(Y_{t}-X_{t}^{\prime} \beta\right)^{2}}{\partial \beta} \\
&=\sum_{t=1}^{n} 2\left(Y_{t}-X_{t}^{\prime} \beta\right) \frac{\partial\left(Y_{t}-X_{t}^{\prime} \beta\right)}{\partial \beta} \\
&=-2 \sum_{t=1}^{n} X_{t}\left(Y_{t}-X_{t}^{\prime} \beta\right) \\
&=-2 \boldsymbol{X}^{\prime}(\boldsymbol{Y}-\boldsymbol{X} \beta)=\bf{0}
\end{aligned}\end{equation}
$$
结合假设3.1(1)非奇异（$\lambda_{min}(X^{\prime} X)>0$）有
$$
\begin{equation}\hat{\beta}=\left(\boldsymbol{X}^{\prime} \boldsymbol{X}\right)^{-1} \boldsymbol{X}^{\prime} \boldsymbol{Y}\end{equation}
$$
检查二阶条件，$K \times K$ Hessian矩阵
$$
\begin{aligned}
\frac{\partial^{2} S S R(\beta)}{\partial \beta \partial \beta^{\prime}} &=-2 \sum_{t=1}^{n} \frac{\partial}{\partial \beta^{\prime}}\left[\left(Y_{t}-X_{t}^{\prime} \beta\right) X_{t}\right] \\
&=2 \bf{X}^{\prime} \bf{X}
\end{aligned}
$$
根据假设3.1(1)，Hessian矩阵正定，从而$\hat{\beta}$是全局最优解。

### 2.2.2 $\hat{\beta}$与$ \beta^* $

不加证明地给出
$$
\begin{aligned}
SSR(\beta)&\stackrel{p}{\rightarrow}\operatorname{MSE}(\beta)=E[Y_t-X'_t\beta]^{2} \\
\hat{\beta}&\stackrel{p}{\rightarrow}\beta^*=
\left[E(\boldsymbol{XX'})\right]^{-1}E(\boldsymbol{XY'})
\end{aligned}
$$
联系第二章，$SSR(\beta)$与$\hat{\beta}$分别是$MSE(\beta)$与$ \beta^* $的样本类似物(sample analogs)

> Whenever you have something unknown, always replace it with sample analogs.

### 2.2.3 残差及其性质

$Y_i = X'_t\hat{\beta}$称为观测值$Y_t $的拟合值(fitted value)或预测值(predicted value)。另外，$e_t=Y_t - \hat{Y}_t$是观测值$Y_t $的估计残差(estimated residual)或预测误差(prediction error)。其中
$$
\begin{aligned}
\mathbf{e}_{t} &=Y_{t}-\hat{Y}_{t} \\
&=\left(X_{t}^{\prime} \beta^{o}+\varepsilon_{t}\right)-X_{t}^{\prime} \hat{\beta} \\
&=\varepsilon_{t}-X_{t}^{\prime}\left(\hat{\beta}-\beta^{o}\right)
\end{aligned}
$$
其中真实扰动项$ \varepsilon_t $是不可避免的，而第二项$X'_t(\hat{\beta}-\beta^o)$是估计误差：当样本容量越大(从而$\hat{\beta}$越靠近$\beta^o$)，这一项将变得越小，乃至忽略不计。

> prediction可以是对过去的预测，forecast是对将来的预测

注意到最小化问题$\min _{\boldsymbol{\beta} \in \Bbb{R}^{K}} SSR(\boldsymbol{\beta})$的一阶条件中，
$$
\boldsymbol{X}^{\prime} \boldsymbol{e}=\sum_{t=1}^{n} X_{t} e_{t}=\mathbf{0}
$$
这意味着残差向量$\boldsymbol{e}$与解释变量矩阵$\bf{X}$正交(无论模型是否正确设定)。进一步，若$\bf{X}_t$包含截距项，则$\boldsymbol{X}^{\prime} \boldsymbol{e}$意味着$\sum^n_{t=1}e^t=0$。

## 2.3 拟合优度与模型选择准则

### 2.3.1 拟合优度$ \mathcal{R}^2 $

残差波动越小，拟合优度越高

通过$\boldsymbol{Y}=\hat{\boldsymbol{Y}}+\boldsymbol{e}$，
$$
\begin{aligned}
\boldsymbol{Y}^{\prime} \boldsymbol{Y}&=(\hat{\boldsymbol{Y}}+\boldsymbol{e})'(\hat{\boldsymbol{Y}}+\boldsymbol{e}) \\
&=\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}+\boldsymbol{e}^{\prime} \boldsymbol{e}+2 \hat{\boldsymbol{Y}}^{\prime} \boldsymbol{e} \\
&= \hat{\boldsymbol{Y}}\boldsymbol{\hat{Y}}+\boldsymbol{e}^{\prime} \boldsymbol{e}
\end{aligned}
$$
其中
$$
\hat{\boldsymbol{Y}}^{\prime} \boldsymbol{e}=(\boldsymbol{X}\hat{\beta})^{\prime}\boldsymbol{e}=\hat{\beta}^{\prime}\boldsymbol{X}^{\prime}\boldsymbol{e}=\hat{\beta}^\prime\boldsymbol{0}=0
$$
因此
$$
\frac{\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}}{\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}}=\frac{\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}}{\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}}-\frac{\boldsymbol{e}^{\prime} \boldsymbol{e}}{\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}}=1-\frac{\boldsymbol{e}^{\prime} \boldsymbol{e}}{\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}}
$$
【非中心化$\mathcal{R}^{2}$】 非中心化多元相关系数平方$ R^2 $(uncentered squared multi-correlation coefficient)定义为
$$
\mathcal{R}_{\mathrm{uc}}^{2}=\frac{\hat{\boldsymbol{Y}}^{\prime} \hat{\boldsymbol{Y}}}{\boldsymbol{Y}^{\prime} \boldsymbol{Y}}=1-\frac{\boldsymbol{e}^{\prime} \boldsymbol{e}}{\boldsymbol{Y}^{\prime} \boldsymbol{Y}}
$$
$\mathcal{R}_{\mathrm{uc}}^{2}$的含义是因变量$ \{Y_t\}$ 的样本二次型变动可以被预测值$\{\hat{Y}_t\}$的样本二次型变动所预测的比例。根据定义，总有$0 \le \mathcal{R}_{\mathrm{uc}}^{2} \le1$。

下面定义一个相近的指标， 称为中心化多元相关系数平方 (centered squared multi-correlation coefficiet)，通常简称为$ \mathcal{R}^2 $。

【中心化$ \mathcal{R}^2 $或决定系数(Coefficient of Determination)】决定系数定义为
$$
\mathcal{R}^2  \equiv 1-\frac{\sum_{t-1}^{n} e_{t}^{2}}{\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}}
$$
其中 $\bar{Y}=n^{-1} \sum_{t=1}^{n} Y_{t}$是样本均值。

当$X_{t}$包含截距项即$X_{0t}=1$时，可进行如下正交分解	
$$
\begin{aligned}
\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2} &=\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}+Y_{t}-\hat{Y}_{t}\right)^{2} \\
&=\sum_{t=1}^{n}\left(\hat{Y}_{t}-Y\right)^{2}+\sum_{t=1}^{n} e_{t}^{2}+2 \sum_{t=1}^{n}\left(\hat{Y}_{t}-Y\right) e_{t} \\
&=\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right)^{2}+\sum_{t=1}^{n} e_{t}^{2}
\end{aligned}
$$
其中交差项
$$
\begin{aligned}
\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right) e_{t} &=\sum_{t=1}^{n} \hat{Y}_{t} e_{t}-\bar{Y} \sum_{t=1}^{n} e_{t} \\
&=\hat{\beta}^{\prime} \sum_{t=1}^{n} X_{t} e_{t}-\bar{Y} \sum_{t=1}^{n} e_{t} \\
&=\hat{\beta}^{\prime}\left(\mathrm{X}^{\prime} e\right)-\bar{Y} \sum_{t=1}^{n} e_{t} \\
&=\hat{\beta}^{\prime} \cdot \boldsymbol{0}-\bar{Y} \cdot 0 \\
&=0
\end{aligned}
$$
这里使用了OLS估计的一阶条件，即$\boldsymbol{X}^{\prime} \boldsymbol{e}=0$ 和 $\sum_{t=1}^{n} e_{t}=0$。从而
$$
\begin{aligned}
\mathcal{R}^{2} & \equiv 1-\frac{e^{\prime} e}{\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}} \\
&=\frac{\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}-\sum_{t=1}^{n} e_{t}^{2}}{\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}} \\
&=\frac{\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right)^{2}}{\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}}
\end{aligned}
$$
并且有
$$
0 \le \mathcal{R}^2 \le 1
$$
反之，若$ X_t $不包含截距项，则
$$
\begin{aligned}
\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2} &=\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right)^{2}+\sum_{t=1}^{n} e_{t}^{2}+2 \sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right) e_{t} \\
& \neq \sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right)^{2}+\sum_{t=1}^{n} e_{t}^{2}
\end{aligned}
$$
在这种情况下，$\mathcal{R}^2 $可能为负值。因为交叉项$2 \sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right) e_{t}$可能为负值。

【定理 2.2】当$ X_t $包含截距项时，$\mathcal{R}^2$是$\{\hat{Y}_t\}$与$\{Y_i\}$的样本方差的比值。

证明：

$\{\hat{Y}_t\}$的样本均值为
$$
\begin{aligned}
\bar{\hat{Y}}&=\frac{1}{n} \sum_{t=1}^{n} \hat{Y}_{t}\\
&=\frac{1}{n} \sum_{i=1}^{n}\left(Y_{t}-e_{t}\right)\\
&=\bar{Y}-\frac{1}{n} \sum_{i=1}^{n} e_{t}\\
&=\bar{Y}
\end{aligned}
$$
其中$\sum_{t=1}^{n} e_{t}=0$要求$ X_t $包含截距项。从而
$$
\begin{aligned}
\mathcal{R}^{2} &=\frac{\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right)^{2}}{\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}}\\
&=\frac{\frac{1}{n-1}\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{\hat{Y}}\right)^{2}}{\frac{1}{n-1}\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}}\\
&=\frac{S^2_{\hat{Y}}}{S^2_Y}
\end{aligned}
$$
此时，中心化$\mathcal{R}^2 $和非中心化$ \mathcal{R}_{\mathrm{uc}}^{2} $有相似的解释，即$\mathcal{R}^2 $测度$ \{Y_i\} $的样本方差中被预测值$\{\hat{Y}_t\}$的样本方差所预测的比例。



【定理 2.3】当$ X_t $包含截距项时，中心化$\mathcal{R}^2$是$\{Y_t\}$和$\{\hat{Y_t}\}$之间相关系数的平方
$$
\mathcal{R}^2=\hat{\rho}^2_{Y\hat{Y}}
$$
证明：

应用前文所证交叉项$\sum_{t=1}^{n}\left(\hat{Y}_{t}-\bar{Y}\right) e_{t}=0$，有
$$
\begin{aligned}
cov(Y_t, \hat{Y_t})
&=\frac{1}{n-1}\sum^n_{t=1}(\hat{Y}_{t}-\bar{Y})({Y}_{t}-\bar{Y})\\
&=\frac{1}{n-1}\sum^n_{t=1}(\hat{Y}_{t}-\bar{Y})({Y}_{t}-\hat{Y_t}+\hat{Y_t}-\bar{Y})\\
&=\frac{1}{n-1}\left[\sum^n_{t=1}(\hat{Y}_{t}-\bar{Y})({Y}_{t}-\hat{Y_t})+\sum^n_{t=1}(\hat{Y}_{t}-\bar{Y})^2\right]\\
&=\frac{1}{n-1}\sum^n_{t=1}(\hat{Y}_{t}-\bar{Y})^2=S^2_{\hat{Y}}
\end{aligned}
$$
结合定理2.2
$$
\begin{aligned}
\hat{\rho}^2_{Y\hat{Y}}
&=\frac{cov^2(Y_t, \hat{Y_t})}{S^2_{\hat{Y}}S^2_{Y}}\\
&=\frac{[S^2_{\hat{Y}}]^2}{S^2_{\hat{Y}}S^2_{Y}}\\
&=\frac{S^2_{\hat{Y}}}{S^2_Y}\\
&=\mathcal{R}^2
\end{aligned}
$$
向量的形式

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224220.png)

利用$M^0$矩阵证明

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224243.png)

i，I都是单位向量

由于拟合值 $\hat{Y}_{t}=X_{t}^{\prime} \hat{\beta}=\hat{\beta}_{0}+\sum_{j=1}^{k} \hat{\beta}_{j} X_{j t}$是$\left\{X_{j t}\right\}_{j=1}^{k}$的线性组合，$ \mathcal{R} $可视为$Y_{t}$ 与 $\left\{X_{j t}\right\}_{j=1}^{k},$之间的多元样本相关系数。因此$R^{2}$被称为多元相关系数平方(squared multi-correlation coefficient)。

这说明$ \mathcal{R}^2 $测度了因变量$Y_t$与解释变量$X_t$之间的线性关联程度，是一种相关关系，而非因果关系。当$E(Y_t|X_t)$是$X_t$的非线性函数时，用$ \mathcal{R}^2 $来测度非线性回归模型的拟合优度是不合适的。

事实上对任何给定的随机样本$\left\{Y_{t}, X_{t}^{\prime}\right\}^n_{t=1}$，$\mathcal{R}^{2}$是解释变量数目的非减函数。

【定理 2.4】假设 $\left\{Y_{t}, X_{1 t}, \ldots, X_{(k+q) t}\right\}^{n}_{t=1}$是容量为$n$的随机样本，$\mathcal{R}^2_1$是下列线性回归模型的中心化拟合优度
$$
Y_{t}=X_{t}^{\prime} \beta+u_{t}
$$
其中$X_{t}=\left(1, X_{1 t}, \ldots, X_{k t}\right)^{\prime}$，$\beta$是$K \times 1$ 未知参数向量，$R_{2}^{2}$ 是下面扩展的线性回归模型的中心化拟合优度
$$
Y_{t}=\tilde{X}_{t}^{\prime} \gamma+v_{t}
$$
其中$\tilde{X}_{t}=\left(1, X_{1 t}, \ldots, X_{k t}, X_{(k+1) t}, \ldots, X_{(k+q) t}\right)^{\prime}$， $\gamma$ 是$(K+q) \times 1$未知参数向量。则
$$
R_{2}^{2} \geq R_{1}^{2}
$$
证明：根据定义有
$$
\begin{aligned}
R_{1}^{2} &=1-\frac{e^{\prime} e}{\sum_{t=1}^{n}\left(Y_{t}-\bar{Y}\right)^{2}} \\
R_{2}^{2} &=1-\frac{\hat{e}^{\prime} \tilde{e}}{\sum_{t=1}^{n}\left(Y_{t}-Y\right)^{2}}
\end{aligned}
$$
其中$\boldsymbol{e} $是$\boldsymbol{Y}$对$\boldsymbol{X} $回归的残差向量, $\boldsymbol{\tilde{e}} $是$\boldsymbol{Y}$对$\boldsymbol{\tilde{X}} $回归的残差向量。

只需要证明$\tilde{e}^{\prime} \tilde{e} \leq e^{\prime} e .$即可。OLS估计量$\hat{\gamma}=\left(\tilde{\boldsymbol{X}}^{\prime} \tilde{\boldsymbol{X}}\right)^{-1} \tilde{\boldsymbol{X}}^{\prime} \boldsymbol{Y}$ 是使扩展模型$Y_{t}=\tilde{X}_{t}^{\prime} \gamma+v_{t}$的$S S R(\gamma)$最小化的最优解，有
$$
\tilde{e}^{\prime} \tilde{e}=\sum_{t=1}^{n}\left(Y_{t}-\tilde{X}_{t}^{\prime} \hat{\gamma}\right)^{2} \leq \sum_{t=1}^{n}\left(Y_{t}-\tilde{X}_{t}^{\prime} \gamma\right)^{2} \text { for all } \gamma \in \mathbb{R}^{K+q}
$$
令
$$
\gamma=\left(\hat{\beta}^{\prime}, \boldsymbol{0}^{\prime}\right)^{\prime}
$$
其中$\hat{\beta}=\left(\mathrm{X}^{\prime} \mathrm{X}\right)^{-1} \mathrm{X}^{\prime} Y$是$Y_{t}=X_{t}^{\prime} \beta+u_{t}$的OLS估计量。则有
$$
\begin{aligned}
\tilde{e}^{\prime} \tilde{e} & \leq \sum_{t=1}^{n}\left(Y_{t}-\sum_{j=0}^{k} \hat{\beta}_{j} X_{j t}-\sum_{j=k+1}^{k+q} 0 \cdot X_{j t}\right)^{2} \\
&=\sum_{t=1}^{n}\left(Y_{t}-X_{t}^{\prime} \hat{\beta}\right)^{2} \\
&=e^{\prime} e
\end{aligned}
$$
因此$R_{1}^{2} \leq R_{2}^{2} $。

 定理2.4表明：首先，$ \mathcal{R}^2 $可用于解释变量数目相等的线性回归模型的比较，但它不适用于比较不同解释变量数目的线性回归模型，因为模型的解释变量越多$ \mathcal{R}^2 $会越大，即使新增加的解释变量对因变量没有真正的解释力，$ \mathcal{R}^2 $也会增加。其次$ \mathcal{R}^2 $也不是正确模型设定的判断标准。$ \mathcal{R}^2 $高并不意味着模型设定正确，同 样，正确的模型设定也并不意味着高的$ \mathcal{R}^2 $。事实上，给定解释变量$X_t$，$ \mathcal{R}^2 $值的大小与线性回归模型的信噪比(signal to noise ratio) 有关。



调整$R^2$,

分子是残差的样本方差！

$R^2$在时序数据中往往较高（滞后项对当前项解释力较强），故意义不大；截面数据中有一定参考价值，大于0.3是较好的模型。

### 2.3.2 AIC&BIC

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224256.png)

## 2.4 OLS估计量的统计性质

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224305.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224317.png) 

幂等矩阵的特征值只能是1或者0

M是残差的操作符e=MY = M$\epsilon$

(2)是$ \epsilon $的线性组合

(4)正太分布随鸡变量$ \epsilon $的二次型服从卡方分布(SSR)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224327.png)

(2)当$\tau = (1,0,\ldots,0)'$，则$\tau'var(\hat{\beta}|X)\tau=var(\hat{\beta_0})$

$MSE(\hat{\beta}_0|X)=var(\hat{\beta}_0|X)+Bias^2(\hat{\beta})\rightarrow 0$, as $n \rightarrow \infty$

(3)+联合正态分布退出独立，用于推导假设检验的有限分布

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224335.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224345.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224353.png)

定理3.5 (4)(5)对于构建假设检验(t检验)有重要意义

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224358.png)

定理3.5(4)证明的一步

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224409.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224426.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224426.png)

直观理解是方差最小

高斯定理：严格外生性，球形方差，OLS是最优线性无偏估计量(BLUE)

## 2.5 OLS估计量的抽样分布

引入假定3.5

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224459.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224512.png)

## 2.6 残差方差估计量的分布

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224448.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224744.png)

## 2.7 假设检验

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224752.png)

J>K可能会产生奇异矩阵

基本思想

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224758.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224809.png)

### 2.7.1 J=1

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224816.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224828.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224836.png)

检验标准

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224845.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224852.png)

### 2.7.2 J>1

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224901.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224909.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224915.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224926.png)

更加常用的方法：本质上是LM检验

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224932.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224938.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224945.png)

Wald Test

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611224951.png)

## 2.8 重要应用

### 2.8.1 检验所有解释变量的联合显著性

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611225000.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611225009.png)

e.g. 检验有效市场：任一系数不为零，则市场不是有效市场

### 2.8.3 检验遗漏变量

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611225019.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611225027.png)

e.g. 格兰杰因果检验：预测力非因果性

Chow Test

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200611225036.png)

## 2.9 广义最小二乘估计GLS



