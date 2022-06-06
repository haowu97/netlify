---
title: "BS"
date: 2021-03-09T16:07:06+08:00
draft: true

description: ""
upd: ""

tags: ['Notes']
categories: ['Financial Engineering']
---



Prices:
$$
\begin{array}{l}
C=S . N\left(d_{1}\right)-K e^{-r T} \cdot N\left(d_{2}\right) \\
P=K e^{-r T} \cdot N\left(-d_{2}\right)-S \cdot N\left(-d_{1}\right)
\end{array}
$$
where:
$$
\begin{array}{l}
d_{1}=\frac{\ln \left(\frac{S}{K}\right)+\left(r+\frac{\sigma^{2}}{2}\right) T}{\sigma \sqrt{T}} \\
d_{2}=\frac{\ln \left(\frac{S}{K}\right)+\left(r-\frac{\sigma^{2}}{2}\right) T}{\sigma \sqrt{T}}=d_{1}-\sigma \sqrt{T}
\end{array}
$$
and $ N(x) $ is the cumulative normal distribution e.g. in Excel: norm.s.dist(x,true), or normsdist(x) or in R: pnorm(x)

Stock index pays continuous dividend rate q
$$
 c=S_{0} . e^{-q T} \cdot N\left(\boldsymbol{d}_{1}\right)-e^{-r T} K . N\left(\boldsymbol{d}_{2}\right) 
$$

$$
 d_{1}=\frac{\ln \left(\frac{S_{0} \cdot e^{-q T}}{K}\right)+\left(r+\frac{\sigma^{2}}{2}\right) T}{\sigma \sqrt{T}} 
$$

$$
 d_{1}=\frac{\ln \left(\frac{S_{0}}{K}\right)+\left(r-q+\frac{\sigma^{2}}{2}\right) T}{\sigma \sqrt{T}} 
$$

$$
 \boldsymbol{c}+\boldsymbol{K} . \boldsymbol{e}^{-r T}=\boldsymbol{p}+S_{0} \cdot e^{-q T} 
$$



Valuation of currency options

Let $ r \quad $denote the risk-free rate at home 

and $ r_{f} \quad $ denote the foreign risk-free rate then $ r_{f} \equiv q $
$$
 c=S_{0} \cdot e^{-r_{f} T} \cdot N\left(\boldsymbol{d}_{1}\right)-e^{-r T} \boldsymbol{K} . N\left(\boldsymbol{d}_{2}\right) 
$$

$$
d_{1}=\frac{\ln \left(\frac{S_{0} \cdot e^{-r_{f} T}{K}}{}\right)+\left(r+\frac{\sigma^{2}}{2}\right) T}{\sigma \sqrt{T}}
$$

$$
 \boldsymbol{d}_{1}=\frac{\ln \left(\frac{\boldsymbol{S}_{0}}{\boldsymbol{K}}\right)+\left(r-r_{f}+\frac{\sigma^{2}}{2}\right) T}{\sigma \sqrt{T}} 
$$

$$
 \boldsymbol{c}+\boldsymbol{K} . \boldsymbol{e}^{-r \boldsymbol{T}}=\boldsymbol{p}+\boldsymbol{S}_{0} \cdot e^{-r_{f} T} 
$$

Futures Options
Black Model:
$$
\begin{array}{c}
c=e^{-r T}\left(F_{0} \cdot N\left(d_{1}\right)-K \cdot N\left(d_{2}\right)\right) \\
d_{1}=\frac{\ln \left(\frac{F_{0}}{K}\right)+\left(\frac{\sigma^{2}}{2}\right) T}{\sigma \sqrt{T}}
\end{array}
$$
Put-call parity:
$$
\begin{array}{c}
c+K . e^{-r T}=p+F_{0} \cdot e^{-r T} \\
\boldsymbol{F}_{0}=\boldsymbol{K}+(\boldsymbol{c}-\boldsymbol{p}) \boldsymbol{e}^{r \boldsymbol{T}}
\end{array}
$$
This relates the c-p difference with the F-K difference.

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20211028233516296.png)

