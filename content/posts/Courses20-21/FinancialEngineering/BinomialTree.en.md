---
title: "Binomial Trees and Option Pricing"
date: 2021-03-08T16:07:06+08:00
lastmod: 2021-03-09T16:07:06+08:00
draft: false

description: ""
upd: ""

tags: ['Notes']
categories: ['Financial Engineering']
---

## Introduction

### Option

Underlying asset: $ S $ , Stock price, foreign rate etc.

Payoff: $ \xi $ 

- European call option: $ \xi=(S-K)^{+} $
- European put option: $ \xi=(K-S)^{+} $

Parties:

- Buyer: long position of the derivative, not necessarily the underling asset. 
- Seller: short position of the derivative, not necessarily the underling asset. 

Markets: Exchange-traded, and Over-the-market, OTC

### Problem and solution

Problem: Fair value of a European option.

Methods: Mathematical model for the underlying asset price.

- Using Binomial tree: (Cox, Ross & Rubinstein 1979, CRR)
- Predicting the distribution of the underlying asset price
- Approach: No-arbitrage Principle

Approach comes before the mathematical models.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210308163133.png)

## Financial market model: one-period binomial tree

Time: now $ \left(t_{0}=0\right) $ and next $ \left(t_{1}=1\right) $ 

Assets:

- Risk-free asset (e.g. bank account, Treasury bonds) and risk-free rate, denoted by $ B $ and $ r>0 $ (per unit time), such that :

$$
B_{1}=e^{r t \Delta} B_{0}, \quad \text { where } t_{\Delta}=t_{1}-t_{0}
$$

- Risky asset (e.g. stocks, foreign rates), denoted by $ S $. Assume that $ S_{0}=s $ is a constant, and $ S_{1} $ is a random variable.
- uncertainty: $ (\Omega, \mathcal{F}, \mathbb{P}) $

$$
\Omega:=\{H, T\}, \quad \omega \in \Omega, \quad \mathcal{F}=\{\{\emptyset\},\{\Omega\},\{H\},\{T\}\}, \mathbb{P}(\{H\})=  1-\mathbb{P}(\{T\})=p<1
$$
- Derivative: European call option. 
    - $ V_{0}, $ value at $ t=0 $ 
    - payoff at $t_{1}=1, V_{1}:=\left(S_{1}-K\right)^{+}=\max \left\{S_{1}-K, 0\right\}$.

Problem: calculate $ V_{0} ! $

Company C sells a European call option to Company A, and promises that Company A can buy 100 t wheat at K \$ t if the wheat price is higher than K \$t. How much should Company A pay for such an option?

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210308182613.png)

Assumptions

- Frictionless market
    - no enter cost
    - no tax
    - no transaction cost
    - no position limit
    - small agent
- No-arbitrage Market
- any unit of underlying asset
- 4 one-price rule

No-arbitrage market: arbitrage trading strategy

- begins with no money
- has zero probability of losing money
- has positive probability of making profit

$ \Delta $ -hedging strategy: The associated portfolio, the so-called hedging portfolio, can cover the final risk. Find $\Delta$ to make portfolio riskless:

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210308221757.png)

Substituting $ S_{1}(H)=u S_{0} $ and $ S_{1}(T)=d S_{0} $ into the equations
$$
\left\{\begin{array}{l}
e^{r t_{\Delta}}\left(V_{0}-\Delta_{0} S_{0}\right)=V_{1}(H)-\Delta_{0} S_{1}(H) \\
e^{r t_{\Delta}}\left(V_{0}-\Delta_{0} S_{0}\right)=V_{1}(T)-\Delta_{0} S_{1}(T)
\end{array}\right.
$$
we have the **no-arbitrage price**
$$
\left\{\begin{array}{l}
V_{0}=e^{-r t_{\Delta}}\left[\hat{p} V_{1}(H)+(1-\hat{p}) V_{1}(T)\right]:=e^{-r t_{\Delta}} \hat{E}\left[V_{1}\right] \\
\Delta_{0}=\frac{V_{1}(H)-V_{1}(T)}{S_{1}(H)-S_{1}(T)}
\end{array}\right.
$$
in terms of **risk-neutral probability**, where
$$
\hat{p}=\frac{e^{r t_{\Delta}}-d}{u-d}, \quad 0<d<e^{r t_{\Delta}}<u
$$

**Risk-neutral world**: no risk premium, discounted at risk-free rate
$$
S_{0}=e^{-r t_{\Delta}}\left[\hat{p} S_{1}(H)+(1-\hat{p}) S_{1}(T)\right]
$$
- One-way to calculate risk-neutral probability in binomial tree setting.
- Different from the continuous-time setting.

No-arbitrage & Risk-neutral

- The no-arbitrage analysis focuses on the random states, rather than the probability of these states.
- It implies that the investor does not have to take risk into account if perfect hedge is allowed.
- The investor actually is risk-neutral in this setting, requiring no risk premium.
- In complete market (perfect hedge), risk-neutral probability is unique, vise versa.
- Option pricing in incomplete market is much difficult.提前执行

$ C=\left[p . C_{u}+(1-p) \cdot C_{d}\right] \times e^{-r T / N} \quad $ where $ \quad p=\frac{e^{r T / N}-d}{u-d} $

## Multi-period Binomial tree

Derivative: European options

Problem: Fair value of European options.

Methods: Mathematical model for the underlying asset price.

- multiperiod Binomial tree
- predicting the distribution of the underlying asset
price

Approach: No-arbitrage Principle

Consider European call option $ \left(r=0.01, K=21, e^{r} \approx 1.01\right) $

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210310103218.png)
$$
\left\{\begin{array}{rlr}p & =\frac{e^{t t} \Delta-d}{u-d} \approx 0.55 & (\mathrm{RN}) \\ V_{1}(H) & =e^{-r}\left[p V_{2}(H H)+(1-p) V_{2}(H T)\right]=1.748232 & (\mathrm{H}) \\ V_{1}(T) & =e^{-r}\left[p V_{2}(T H)+(1-p) V_{2}(T T)\right]=0 & (\mathrm{~T}) \\ V_{0} & =e^{-r}\left[p V_{1}(H)+(1-p) V_{1}(T)\right] \\ & =e^{-2 r}\left[p^{2} V_{2}(H H)+2 p(1-p) V_{2}(H T)+(1-p)^{2} V_{2}(T T)\right] & \\ & =0.94 & (\text { price }) \end{array}\right.
$$

$$
 V_{0}=e^{-2 r}\left[p^{2} V_{2}(H H)+2 p(1-p) V_{2}(H T)+(1-p)^{2} V_{2}(T T)\right] 
$$

Continuous counterpart
$$
V_{0}=e^{-r n t_{\Delta}}\left[\sum_{j=0}^{n}\left(\begin{array}{c}n \\ j\end{array}\right) p^{j}(1-p)^{n-j} V_{n}\left(H^{j} T^{n-j}\right)\right]
$$
![image-20210308222340510](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210308222340510.png)

Asset price: binomial tree to Geometric Brownian motion!

Theorem (**Replication in the multi-period binomial model**): Consider $ N $ -period binomial asset pricing model, with $ 0<d< $ $ e^{r t_{\Delta}}<u $ and with $ \hat{p}=\frac{e^{r t_{\Delta}-d}}{u-d} . $ Let $ V_{N} $ be a random variable (payoff of a derivative at time $ N $ ) depending on the first $ N $ coin tosses $ \omega_{1} \omega_{2} \ldots \omega_{N} . $ Define recursively in time the sequence of random variables $ V_{N-1}, \ldots, V_{0} $ by
$$
V_{n}\left(\omega_{1} \ldots \omega_{n}\right)=e^{-r t_{\Delta}}\left[\hat{p} V_{n+1}\left(\omega_{1} \ldots \omega_{n} H\right)+(1-\hat{p}) V_{n+1}\left(\omega_{1} \ldots \omega_{n} T\right)\right]
$$
Then define $ \Delta_{n}\left(\omega_{1} \ldots \omega_{n}\right)=\frac{V_{n+1}\left(\omega_{1} \ldots \omega_{n} H\right)-V_{n+1}\left(\omega_{1} \ldots \omega_{n} T\right)}{S_{n+1}\left(\omega_{1} \ldots \omega_{n} H\right)-S_{n+1}\left(\omega_{1} \ldots \omega_{n} T\right)} $. If setting
$ X_{0}=V_{0}, $ we will have
$$
X_{T}\left(\omega_{1} \ldots \omega_{N}\right)=V_{T}\left(\omega_{1} \ldots \omega_{N}\right), \quad \forall \omega_{i}
$$
where $ X_{n+1}=\left(X_{n}-\Delta_{n} S_{n}\right) e^{r t_{\Delta}}+\Delta_{n} S_{n+1} $ and $ n \in\{0, \ldots, N\} $

Example: 

$ t=0:\left(V_{0}, \Delta_{0}\right) $
$ t_{1}=1: X_{1}=\left(V_{0}-\Delta_{0} S_{0}\right) e^{r t_{\Delta}}+\Delta_{0} S_{1} $
$$
\left\{\begin{array}{ll}X_{1}(H)=\left(V_{0}-\Delta_{0} S_{0}\right) e^{r t_{\Delta}}+\Delta_{0} S_{1}(H) & (\mathrm{H}) \\ X_{1}(T)=\left(V_{0}-\Delta_{0} S_{0}\right) e^{r t_{\Delta}}+\Delta_{0} S_{1}(T) & (\mathrm{T})\end{array}\right.
$$
$ t_{2}=2: V_{2}=\left(X_{1}-\Delta_{1} S_{1}\right) e^{r t_{\Delta}}+\Delta_{1} S_{2} $
$$
\left\{\begin{array}{ll}V_{2}(H H)=\left(X_{1}(H)-\Delta_{1}(H) S_{1}(H)\right) e^{r t_{\Delta}}+\Delta_{1}(H) S_{2}(H H) & (\mathrm{HH}) \\ V_{2}(H T)=\left(X_{1}(H)-\Delta_{1}(H) S_{1}(H)\right) e^{r t_{\Delta}}+\Delta_{1}(H) S_{2}(H T) & (\mathrm{HT}) \\ V_{2}(T H)=\left(X_{1}(T)-\Delta_{1}(T) S_{1}(T)\right) e^{r t_{\Delta}}+\Delta_{1}(T) S_{2}(T H) & (\mathrm{TH}) \\ V_{2}(T T)=\left(X_{1}(T)-\Delta_{1}(T) S_{1}(T)\right) e^{r t_{\Delta}}+\Delta_{1}(T) S_{2}(T T) & (\mathrm{T} \mathrm{T})\end{array}\right.
$$

## American options pricing

exercise at any time period $ n \in\{1, \ldots, N\} $

- no cheaper than the European counterpart

- useless for a call on no-dividend assets.

optimal exercise date: optimal stopping time

intrinsic value $ f\left(S_{n}\right): $ payoff for immediate exercise

option price $ V_{n}\left(S_{n}\right) \geq f\left(S_{n}\right) $
$$
\begin{aligned}
&V_{n}(s)=\max \left\{f(s), e^{-r t_{\Delta}}\left[\hat{p} V_{n+1}(s H)+(1-\hat{p}) V_{n+1}(s T)\right]\right\} \\
&\Delta_{n}(s)=\frac{V_{n+1}(s H)-V_{n+1}(s T)}{S_{n+1}(s H)-S_{n+1}(s T)} 
\end{aligned}
$$
![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210310113711.png)

## Matching volatility with u, d

In practice, the key point in binomial tree model is to choose u, d and P, in order to make asset price satisfy geometric Brownian motion. Namely, we have the basic model assumption:
$$
d S_{t}=(r-q) s_{t} d t+\sigma s_{t} d W_{t}
$$
i.e., $ \frac{\Delta S_t}{S_0} \sim N(e^{(r-q) \Delta t}, \sigma^2 \Delta t)$. Where q is dividend yield.

And
$$
d \ln(S_{t})=(r-q-\frac{1}{2}\sigma^2) d t+\sigma d W_{t}
$$
i.e., $ \Delta \ln(S_t) = \ln(\frac{S_t}{S_0}) \sim N((r-q-\frac{1}{2}\sigma^2)\Delta t, \sigma^2 \Delta t)$.

To satisfy this assumption, we only need the mean and variance is the same as the normal distribution. Thus we have two equations with three parameters, which means that we have many solutions. Different models come from these solutions.

### CRR tree

In traditional CRR model, risk-neutral probability is as before
$$
p=\frac{e^{r t_{\Delta}}-d}{u-d}, \quad 0<d<e^{r t_{\Delta}}<u\hat{p}=\frac{e^{r t_{\Delta}}-d}{u-d}, \quad 0<d<e^{r t_{\Delta}}<u
$$

Then, we derive u and d

Volatility $ \sigma \sqrt{\Delta t}: $ the standard deviation of its return in a short period of time $ \Delta t $.
$$
p(u-1)^{2}+(1-p)(d-1)^{2}-[p(u-1)+(1-p)(d-1)]^{2}=\sigma^{2} \Delta t
$$
with risk neutral probability:
$$
e^{r \Delta t}(u+d)-u d-e^{2 r \Delta t}=\sigma^{2} \Delta t
$$
By using series expansion of $ e^{x} $,
$$
u=e^{\sigma \sqrt{\Delta t}} \text { and } d=e^{-\sigma \sqrt{\Delta t}}
$$

We can verify that,
$$
Var\left[\ln(\frac{S_t}{S_0})\right] = \frac{1}{2}(\ln u-\ln d)=\sigma \sqrt{\Delta t}
$$
and
$$
\begin{aligned} 
& p=\frac{e^{r \Delta t}-d}{u-d} \\ 
\Rightarrow & p u-p d=e^{(r-q) \Delta t}-d \\ 
\Rightarrow & E[\frac{\Delta S_t}{S_0}] = p u+(1-p) d=e^{(r-q) \Delta t} 
\end{aligned}
$$
The price of the underlying asset in the CRR model fluctuates around the initial starting value.

### JR tree

Risk-neutral probability $\hat{p}= 0.5$,
$$
\ln u=\left(r-q-\frac{1}{2} \sigma^{2}\right) \delta t+\sigma \sqrt{\Delta t} \\
\ln d=\left(r-q-\frac{1}{2} \sigma^{2}\right) \delta_{t}-\sigma \sqrt{\Delta t}
$$
We can verify that, under binomial distribution
$$
\begin{aligned}
E\left[\ln(\frac{S_t}{S_0})\right] &= \frac{1}{2}\left(\ln \frac{u S_0}{S_0} + \ln \frac{d S_0}{S_0} \right) =  \frac{1}{2}\left(\ln u + \ln d \right) = (r-q-\frac{1}{2}\sigma^2) \Delta t \\
Var\left[\ln(\frac{S_t}{S_0})\right]  &= \frac{1}{2}\left(\ln \frac{u S_0}{S_0} - \ln \frac{d S_0}{S_0} \right) =  \frac{1}{2}\left(\ln u - \ln d \right) = \sigma^2 \Delta t
\end{aligned}
$$

### LR tree

$$
\left\{\begin{array}{l}u=b p^{\prime} / p ; \quad b=\exp \left\{(r-q) \Delta t\right\} \\ d=b\left(1-p^{\prime}\right) /(1-p) \\ p^{\prime}=h^{-1}\left(d_{1}\right), p=h^{-1}\left(d_{2}\right)\end{array}\right.
$$

where
$$
\begin{aligned} 
h^{-1}(z) &=\frac{1}{2}+\frac{\operatorname{sign} \left(d_{1}\right)}{2} \cdot \sqrt{1-\exp \left[-\left(\frac{z}{n+\frac{1}{3}+\frac{0.1}{n+1}}\right)^{2}\left(n+\frac{1}{6}\right)\right]} \\  d_{1}&=\frac{\log \left(\frac{S}{K}\right)+\left(r+\frac{1}{2} \sigma^{2}\right) T}{\sigma \sqrt{T}} \\
 d_{2}&=\frac{\log \left(\frac{S}{K}\right)+\left(r-\frac{1}{2} \sigma^{2}\right) T}{\sigma \sqrt{T}} 
\end{aligned}
$$
Note that the LR model is only suitable for the case where the step is odd, otherwise the price won't converge.

We can also verify that,
$$
 E[\frac{\Delta S_t}{S_0}] = b =e^{(r-q) \Delta t}
$$
In the above model, LR model has the highest pricing efficiency, i.e is can converge to the price of the BS model with fewer iterations. It takes about 10 times, while the CRR and JR model requires 80 times or more.

The center price of the underlying asset price of the LR model will approach the exercise price K.

## Further reading

- Cox, J. C., Ross, S. A., & Rubinstein, M. (1979). Option pricing: A simplified approach. Journal of financial Economics, 7(3), 229–263.
- Hansen, L. P. (2014). Nobel Lecture: Uncertainty Outside and Inside Economic Models. Journal of Political Economy, 122(5), 945–987.
- Hull, J. C. (2015). Options, Futures and Other Derivatives. Boston: Prentice Hall, 9th edition.
- Neftci, S. (2008). Principles of Financial Engineering. Amasterdam: Academic Press Advanced Finance, 2nd edition.
- Shreve, S. E. (2004). Stochastic Calculus for Finance I: The Binomial Asset Pricing Model. New York: Springe-Verlag.