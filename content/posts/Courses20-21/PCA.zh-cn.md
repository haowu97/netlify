---
title: "PCA"
date: 2021-08-20T21:17:53+08:00
draft: true

description: ""
upd: ""

tags: []
categories: []
---

<!--more-->

**降维**：用少数几个变量代替原有的数目庞大的变量，把重复的信息合并起来，降低现有变量的维度，又不会丢失掉重要信息。

经典降维方法：

- 主成分分析 (Principal component analysis, PCA) ：构造“综合指标”， 以将原始数据最大程度地区分开
- 因子分析 (Factor analysis)：用一个变量（公因子）代替原始高度相关的变量

线性判别分析(LDA)是寻求最大化两个或多个群体之间距离的线性组合

主成分分析(PCA)中，我们只有一个群体，目标是找到一个能使 这个群体中个体差异达到最大的变量线性组合

## 总体主成分分析

主成分分析的目标是找到一组**互不相关**的变量$Z_1,\ldots, Z_p$，称为主成分。每一个主成分都是$Y_1,\ldots,Y_p$的**线性组合**，即：
$$
\begin{aligned} Z_{1} &=\mathbf{a}_{1}^{\prime} \mathbf{y}=a_{11} Y_{1}+a_{12} Y_{2}+\ldots+a_{1 p} Y_{p} \\ Z_{2} &=\mathbf{a}_{2}^{\prime} \mathbf{y}=a_{21} Y_{1}+a_{22} Y_{2}+\ldots+a_{2 p} Y_{p} \\ & \vdots \\ Z_{p} &=\mathbf{a}_{p}^{\prime} \mathbf{y}=a_{p 1} Y_{1}+a_{p 2} Y_{2}+\ldots+a_{p p} Y_{p} \end{aligned}
$$
并将主成分按照**方差贡献度（重要性）从大到小排列**。

其中，原始变量为 $\mathbf{y}=\left(Y_{1}, \dots, Y_{p}\right)^{\prime}$，其协方差矩阵为$ \Sigma $ 。则$Z_1,\ldots,Z_P$的方差与协方差为
$$
\operatorname{var}\left(Z_{j}\right)=\mathbf{a}_{j}^{\prime} \mathbf{\Sigma} \mathbf{a}_{j}, \operatorname{cov}\left(Z_{j}, Z_{k}\right)=\mathbf{a}_{j}^{\prime} \mathbf{\Sigma} \mathbf{a}_{k}, j, k=1, \ldots, p
$$
### 一般求解思路

按照方差贡献度从大到小依次求解：

第一主成分$$Z_1 = a_1^{\prime}y$$：
$$
\max_{a_1} \; var(a^{\prime}_1y), 
\\s.t.\; a^{\prime}_1a_1 = 1
$$
或者
$$
\max_{a_1} \; \frac {var(a_1^{\prime}y)} {a_1^{\prime}a_1}
$$
向量$a_1$的模越大，$Z_1$的方差越大，因此需要将其控制为1。

第二主成分$$Z_2 = a_2^{\prime}y$$：
$$
\max_{a_2} \; var(a^{\prime}_2y), 
\\s.t.\; a^{\prime}_2a_2 = 1,\;cov(a_1^{\prime}y, a_2^{\prime}y)=0
$$
……

第$j$主成分$$Z_j = a_j^{\prime}y$$：
$$
\max_{a_j} \; var(a^{\prime}_jy), \\s.t.\; a^{\prime}_ja_j = 1,\;cov(a_k^{\prime}y, a_j^{\prime}y)=0,\;k=1,2,\ldots,j-1
$$
……

第$p$主成分$$Z_p = a_p^{\prime}y$$：
$$
\min_{a_p} \; var(a^{\prime}_py)
$$
**定理**：记$$\left(\lambda_{1}, \mathbf{e}_{1}\right), \ldots,\left(\lambda_{p}, \mathbf{e}_{p}\right)$$为协方差矩阵$\Sigma$的特征值-特征向量对，其中$\lambda_{1} \geq \ldots \geq \lambda_{p} \geq 0$，则变量$Y_{1}, \ldots, Y_{p}$的第 j 个主成分为：
$$
Z_{j}=\mathbf{e}_{j}^{\prime} \mathbf{y}=e_{j 1} Y_{1}+e_{j 2} Y_{2}+\ldots+e_{j p} Y_{p},\; j=1, \ldots, p
$$
其中
$$
\begin{array}{l}{\operatorname{var}\left(Z_{j}\right)=\mathbf{e}_{j}^{\prime} \mathbf{\Sigma} \mathbf{e}_{j}=\lambda_{j}} \\ {\operatorname{cov}\left(Z_{j}, Z_{k}\right)=\mathbf{e}_{j}^{\prime} \mathbf{\Sigma} \mathbf{e}_{k}=0}\end{array}
$$
进一步
$$
\sum_{j=1}^{p} \operatorname{var}\left(Z_{j}\right)=\sum_{j=1}^{p} \operatorname{var}\left(Y_{j}\right)
$$
第$j$个主成分贡献的方差，占总体方差的比例可表示如下：
$$
\frac {var(Z_j)} {\sum_{j=1}^p var(Z_j)}=\frac{\lambda_{j}}{\sum_{j=1}^{p} \lambda_{j}}
$$

### 基于标准化变量的求解

如果变量 $$\mathbf{y}=\left(Y_{1}, \dots, Y_{p}\right)^{\prime}$$的数值（由于度量单位不同等原因）差距过大，直接由协方差矩阵 生成的主成分会由方差大的变量主导。

对每个原始变量$Y_j$进行标准化之后再进行主成分分析可以解决上述问题：
$$
W_{j}=\left(Y_{j}-\mu_{j}\right) / \sqrt{\sigma_{j j}} \quad j=1, \ldots, p
$$
令$$\mathbf{w}=\left(W_{1}, \ldots, W_{p}\right)^{\prime}, \mathbf{D}_{s}=\operatorname{diag}(\sqrt{\sigma_{11}}, \ldots, \sqrt{\sigma_{p p}})$$，则
$$
\mathbf{w}=\mathbf{D}_{s}^{-1}(\mathbf{y}-\boldsymbol{\mu})
$$
此时$\operatorname{cov}(\mathbf{w})=\mathbf{P}$，即$y$的相关系数矩阵，因此对$W_1, W_2, \ldots, W_p$进行主成分分析，**等价于基于原始变量$Y_1,Y_2,\ldots,Y_3$的相关系数矩阵进行主成分分析**。

基于相关系数矩阵$P$的主成分分析不受度量单位影响。$P$与$$\Sigma$$的特征值、特征向量是不同的，因此两组主成分的数值和方向都是不同的，两者并不能通过简单变换互相得到。如果变量数值差异很大，推荐进行标准化来获得一个较平衡的数据集。

