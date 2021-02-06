# 1. Valuation of Risky Cash Flow

## 1.1 Inter-temporal Optimization

Static optimization is to optimally allocate spending across different goods at a point of time (e.g. maximize utility from consuming apples and bananas today subject to current budget constraint).

**Intertemporal optimization** is to optimally allocate spending over time (e.g. maximize utility from consuming apples today and next year subject to intertemporal budget constraint).

### 1.1.1 Time Dimension

#### Intertemporal utility function

For simplicity, economists typically assume **separable, discounting and concave utility function** in 2 periods
$$
u\left(C_{0}\right)+\beta u\left(C_{1}\right)
$$

where $C_{0}$ and $C_{1}$ are consumptions today and next year

- A concave utility implies convex indifference curves with slope called intertemporal marginal rate of substitution (how much to give up today for next year)
- $u$ is concave utility function which implies consumption smoothing preference.

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200520125132.png)

- $\beta<1$ is the discount factor, a measure of patience

#### Intertemporal budget constraint

Suppose
$$
\begin{aligned}
Y_{0}&=\text { income today } \\
Y_{1}&=\text { income next year }\\
S&= \text{amount saved(or borrowed if negative) today}\\
r&= \text{interest rate}
\end{aligned}
$$

Today $Y_{0} \geq C_{0}+S$.

Next year, $Y_{1}+(1+r) S \geq C_{1}$.

Thus the life-time budget constraint is
$$
Y_{0}+\frac{Y_{1}}{1+r} \geq C_{0}+\frac{C_{1}}{1+r}
$$

The present value of income must be sufficient to cover the presen value of consumption over the two periods!

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200520130204.png)

The price of consumption today relative to the price of consumption next year is given by

$$
\frac{p_{0}}{p_{1}}=1+r
$$

The slope of the intertemporal budget constraint is $-(1+r)$.

#### Optimal Allocation

At the optimum, the intertemporal marginal rate of substitution equals the slope of the budget constraint
$$
\frac{u'(C_0)}{\beta u'(C_1)}=1+r
$$

### 1.1.2 Risk Dimension 

To add/model the element of risk, let's follow Arrow-Debreu by imagining that there are two possible outcomes:

$$
\begin{aligned}
Y_{0} &=\text { income today } \\
Y_{1}^{G} &=\text { income next year under good state }
\end{aligned}
$$

$Y_{1}^{B}=$ income next year under bad state
where assumption $Y_{1}^{G}>Y_{1}^{B}$ makes good state good and $\pi=$ probability of the good state $1-\pi=$ probability of the bad state

How to represent preferences over risky alternatives?

Under uncertainty, the consumer maximizes expected utility $u\left(C_{0}\right)+\beta u\left(C_{1}\right)$ which equivalent to

$$
u\left(C_{0}\right)+\beta\left[\pi u\left(C_{1}^{G}\right)+(1-\pi) u\left(C_{1}^{B}\right)\right]
$$

We can see that concavity of the function u, which in the standard micro case represents a preference for diversity, represents a preference for smoothness in consumption over time and across states in the future–the consumer is risk averse in the sense that he does not want consumption in the bad state to be too much different from consumption in the good state.
$$
Y_0 + \underbrace{q_G Y^G_1 + q_B Y^B_1}_{\text{PV of future income}} ≥ C_0 + \underbrace{q_G C^G_1 + q_B C^B_1}_{\text{PV of future consumption}}
$$


![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522191457.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522191531.png)

Value a bond that pays its \$100 coupon at the end of each year for 3-years, and its par value of \$1,000 in 3-years You have discovered three pure discount bonds (each with a \$1,000 par value) that mature in 1, 2, and 3 years, and that are trading at \$960, \$890, and \$810 respectively	

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522191656.png)



# 2. Making Choices in Risky Situations

1 Criteria for Choice Over Risky Prospects 

State-by-state Dominance 

Mean-variance Dominance 

Sharpe Ratio 

2 Preferences and Utility Functions Preferences Preferences and Utility Functions 3 Expected Utility Functions 4 The Expected Utility Theorem Lottery Assumptions The Expected Utility Theorem 5 The Allais Paradox

### Criteria for Choice Over Risky Prospects

“**risk**” refers to uncertainty about the future cash flows provided by a financial asset.

**state-by-state dominance** over investments 1 and 2, because it **pays as much in all states and strictly more in at least one state**. Any investor who prefers more to less (nonsatiated in consumption) would always choose investment 3 above the others.

**mean-variance dominance** over investment 2, since it offers a higher expected return with lower variance.

**Mean-variance dominance neither implies nor is implied by state-by-state dominance.**

In probability theory, if a random variable X can take on n possible values, X1; X2; ... ; Xn, with probabilities p1; p2; ...; pn, then the expected value of X is E(X) = p1X1 + p2X2 + ... + pnXn the variance of X is σ 2 (X) = p1[X1 − E(X)]2 + p2[X2 − E(X)]2 + ... + pn[Xn − E(X)]2 and the standard deviation of X is σ(X) = [σ 2 (X)](1/2) .

In a mean-variance (M-V) framework, an investor's wants to maximize a function $u\left(\mu_{r}, \sigma_{P}\right)$
She likes expected return $\left(\mu_{r}\right)$ and dislikes standard deviation $\left(\sigma_{P}\right)$ Recall that portfolio $A$ is said to exhibit mean-variance dominance over portfolio B if either
$$
\frac{\mu_{A}>\mu_{B}}{\mu_{A} \geq \mu_{B}} \text { and } \sigma_{A} \leq \sigma_{B}
$$
Mean-variance dominance neither implies nor is implied by state-by-state dominance.

Mean-variance Dominance can be expressed in the form of a criterion for selecting investments of equal magnitude For investments of the same Er, choose the one with lower σ For investments of the same σ, choose the one with greatest Er

William Sharpe (US, b.1934, Nobel Prize 1990) suggested that in these circumstances, it can help to compare the two assets’ **Sharpe ratios**, defined as E(r)/σ(r).

But **using the Sharpe ratio to choose between assets means assuming that investors “weight” the mean and standard deviation equally, in the sense that a doubling of σ(r) is adequately compensated by a doubling of E(r). Investors who are more or less averse to risk will disagree.**

#### Summary

State-by-state dominance is the most robust criterion, but often cannot be applied. 

Mean-variance dominance is more widely-applicable, but can sometimes be misleading and cannot always be applied. 

The Sharpe ratio can always be applied, but requires a very specific assumption about consumer attitudes towards risk. 

We need a more careful and comprehensive approach to comparing random cash flows.

###  Preferences and Utility Functions

rational: A1完备性、A2传递性

A.3. The preference relation is assumed to be **continuous**: if an and bn are two sequences of bundles such that an → a, bn → b and an  bn for all n, then a  b.Very small changes in consumption bundles cannot lead to large changes in preferences over those bundles.

理性是效用函数存在的必要非充分条件

理性+连续是连续效用函数存在的充分条件

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522192102.png)

An **ordinal utility function** describing a consumer’s preferences over two goods can be written as u(x, y), the same preferences could be expressed as another utility function that is an increasing transformation of u: g(x, y) = f (u(x, y)). Utility functions g and u give rise to identical indifference curve mappings. 

A **cardinal utility function** that preserves preference orderings **uniquely up to positive affine transformations**. Two utility indices are related by an affine transformation, i.e. u and v satisfies a relationship of the form v(x) = au(x) + b, where a and b are constants.

### 不确定性下的效用函数：伯努利效用函数，VNM效用函数

期望效用函数

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522192135.png)

### 彩票

多结果彩票可以被看成复合彩票

因此彩票不失一般性

### 期望效用定理

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522192605.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522192806.png)

By Theorem 3.1, we already know that (C:2) and (C:3) are sucient to guarantee the existence of a utility function U over lotteries and, by (C:1a), dened both on lotteries and specic payos received with certainty as well.

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522192916.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522192941.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193103.png)

假设

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193134.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193309.png)

首先证明U(X)存在，然后证明关于概率线性

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193339.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193435.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193519.png)

The concept of a Bernoulli utility function is ordinal  （单调变换保序）

the concept of vN-M utility function is cardinal!In this sense, the vN-M utility function that represents any given preference relation is not unique.（线性变换保序）

### 独立性假设的悖论：Allais parodox

The Allais paradox suggests that **feelings about probabilities may not always be “linear**,” but linearity in the probabilities is precisely what defines vN-M utility functions.

行为金融批判：独立性（效用函数对概率不一定线性），风	险厌恶（某些初始财富，有可能变得风险偏好）

# 3. Measuring Risk and Risk Aversion

### 3.1 Measuring Risk Aversion

If U[E(W )] < E[U(W )] or the utility function is strictly convex, then the individual is a risk lover; 

If U[E(W )] = E[U(W )] or the utility function is linear, then the individual is risk neutral; 

If U[E(W )] > E[U(W )] or the utility function is strictly concave, then the individual is risk averse;

#### coeffcient of  risk aversion & Probability premium

coeffcient of absolute risk aversion 
$$
R_{A}(Y)=-\frac{u^{\prime \prime}(Y)}{u^{\prime}(Y)}
$$
coeffcient of relative risk aversion
$$
R_{R}(Y)=-\frac{Y u^{\prime \prime}(Y)}{u^{\prime}(Y)}
$$
To interpret the two measures of risk aversion, it is helpful to recall from calculus the theorem stated by Brook Taylor (England, $1685-1731$ ), regarding the approximation of a function $f$ using its derivatives: the "first-order" approximation
$$
f(x+a)=f(x)+f^{\prime}(x) a+o(a)
$$
and the "second-order" approximation
$$
f(x+a)=f(x)+f^{\prime}(x) a+\frac{1}{2} f^{\prime \prime}(x) a^{2}+o\left(a^{2}\right)
$$
![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193553.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193629.png)

注意上述等式与**概率溢价**的联系

Probability premium $\pi(w, \epsilon, u)$
$$
L=(0.5+\pi \circ w+\epsilon, 0.5-\pi \circ w-\epsilon)
$$
Find the $\pi$ to make $C E(L)=w,$ that is
$$
\begin{aligned}
& U(L)=u(w)=(0.5+\pi) u(w+\epsilon)+(0.5-\pi) u(w-\epsilon) \\
\Rightarrow \quad & \pi(w, \epsilon ; u)
\end{aligned}
$$

#### 风险溢价(Risk premium)与确定性等价

**Jensen's Inequality** Let $g$ be a concave function and $\tilde{x}$ be a random variable. Then
$$
g[E(\tilde{x})] \geq E[g(\tilde{x})]
$$
Furthermore, if $g$ is strictly concave and the probability that $\tilde{x} \neq E(\tilde{x})$ is greater than zero, the inequality is strict.

An implication of Jensen's inequality is that the maximum riskless payoff that a risk-averse investor is willing to exchange for the asset with random payoff $\tilde{Z}$, called the certainty equivalent for that asset, will always be less than $E(\tilde{Z})$

The difference between the higher expected value $E(\tilde{Z})$ and the
- smaller certainty equivalent $C E(\tilde{Z})$ can then be used to define the positive risk premium $\Pi(\tilde{Z})$ for the asset:

$$
\Pi(\tilde{Z})=E(\tilde{Z})-C E(\tilde{Z})
$$

Mathematically, the **certainty equivalent** $C E(\tilde{Z})$ and **risk premium** $\Pi(\tilde{Z})$ for an asset with random payoff $\tilde{Z}$ with expected value $E(\tilde{Z})$ are defined by
$$
E(u(Y+\tilde{Z}))=u[Y+C E(\tilde{Z})]
$$
"the expected utility from buying the asset equals the utility from getting the certainty equivalent for sure," and
$$
E(u(Y+\tilde{Z}))=u[Y+E(\tilde{Z})-\Pi(\tilde{Z})]
$$
<img src="https://upload-images.jianshu.io/upload_images/20447423-bcf46f32a2fe1c9d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240" style="zoom:50%;" />

assume for simplicity that $E(\tilde{Z})=0$ and consider a second-order Taylor approximation to $E(u(Y+\tilde{Z}))$
$$
\begin{aligned}
E(u(Y+\tilde{Z})) & \approx E[u(Y)]+E\left[u^{\prime}(Y) \tilde{Z}\right]+E\left[\frac{1}{2} u^{\prime \prime}(Y) \tilde{Z}^{2}\right] \\
&=u(Y)+u^{\prime}(Y) E(\tilde{Z})+\frac{1}{2} u^{\prime \prime}(Y) E\left[\tilde{Z}^{2}\right] \\
&=u(Y)+\frac{1}{2} \sigma_{\tilde{Z}}^{2} u^{\prime \prime}(Y)
\end{aligned}
$$
since $Y$ is not random.

Consider a first-order Taylor approximation to $u[Y+E(\tilde{Z})-\Pi(\tilde{Z})]$
$$
\begin{aligned}
u[Y+E(\tilde{Z})-\Pi(\tilde{Z})] &=u[Y-\Pi(\tilde{Z})] \\
& \approx u(Y)-u^{\prime}(Y) \Pi(\tilde{Z})
\end{aligned}
$$
Hence, with $E(\tilde{Z})=0,$ the equation defining the risk premium $E(u(Y+\tilde{z}))=u[Y+E(\tilde{Z})-\Pi(\tilde{Z})]$
$$
\begin{aligned}
E(u(Y+\tilde{Z})) & \approx u(Y)+\frac{1}{2} \sigma_{\bar{Z}}^{2} u^{\prime \prime}(Y) \\
u[Y+E(\tilde{Z})-\Pi(\tilde{Z})] & \approx u(Y)-u^{\prime}(Y) \Pi(\tilde{Z})
\end{aligned}
$$
imply
$$
\Pi(\tilde{Z}) \approx \frac{1}{2} \sigma_{\bar{Z}}^{2} R_{A}(Y)
$$
(上述证明过程经常考到)

![](https://upload-images.jianshu.io/upload_images/20447423-89b86e2a349b6249.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

under the simplifying assumption that $E(\tilde{Z})=0,$ it also applies when $E(\tilde{Z}) \neq 0,$ except that the level of income must be adjusted from $Y$ to $Y+E(\tilde{Z})$ to take into account the nonzero expected return:
$$
\Pi(\tilde{Z}) \approx \frac{1}{2} \sigma_{\tilde{Z}}^{2} R_{A}(Y+E(\tilde{Z}))
$$
当保险仅仅补偿不确定性至$E(\tilde{Z})$时，
$$
u(Y+E\tilde{Z}-Fee) \longleftrightarrow u\left(Y+E\tilde{Z}- \Pi(\tilde{Z})\right)
$$
![](https://upload-images.jianshu.io/upload_images/20447423-7e2f9df73e99c041.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/20447423-c0a7b86931ad4777.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 3.2 Stochastic Dominance

SBSD implies FSD implies SSD

#### First-order stochastic dominance

First-order stochastic dominance(FSD) Let $F_{A}(\tilde{x})$ and $F_{B}(\tilde{x})$ be two cumulative probability distributions for random payoffs in $[a, b] .$ We say that $F_{A}(\tilde{x}) F S D F_{B}(\tilde{x})$ if and only if:
$$
F_{A}(x) \leq F_{B}(x), \forall x
$$
<img src="https://upload-images.jianshu.io/upload_images/20447423-5dd3a8f69d03a175.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240" style="zoom:50%;" />

that is, $F_{2}(x) \text{ FSD } F_{1}(x),$ if and only if
$$
E\left[u\left(Z_{2}\right)\right] \geq E\left[u\left(Z_{1}\right)\right]
$$
**for any nondecreasing Bernoulli utility function** $u$

state-by-state dominance implies first-order stochastic dominance but first-order stochastic dominance does not necessarily imply state-by-state dominance. 

But **first-order stochastic dominance remains quite a strong condition**. Since an asset that displays first-order stochastic dominance over all others will be preferred by any investor with vN-M utility who prefers higher payoffs to lower payoffs, the price of **such an asset is likely to be bid up until the dominance goes away**.

#### Second-order stochastic dominance

second-order stochastic dominance(SSD) Let $F_{A}(\tilde{x})$ and $F_{B}(\tilde{x})$ be two cumulative probability distributions for random payoffs in $[a, b] .$ We say that $F_{A}(\tilde{x}) \text{ SSD } F_{B}(\tilde{x})$ if and only if for any $x:$
$$
\int_{-\infty}^{x}\left[F_{B}(t)-F_{A}(t)\right] d t \geq 0
$$
(with strict inequality for some meaningful interval of values of $t$ ).

![](https://upload-images.jianshu.io/upload_images/20447423-bb96c9eab17df45b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

that is, asset 4 displays second-order stochastic dominance over asset $3,$ if and only if
$$
E\left[u\left(Z_{4}\right)\right] \geq E\left[u\left(Z_{3}\right)\right]
$$
for any nondecreasing and concave Bernoulli utility function $u$

Second-order stochastic dominance is a weaker condition than first-order stochastic dominance, in that first-order stochastic dominance implies second-order stochastic dominance but second-order stochastic dominance does not necessarily imply first-order stochastic dominance. 

But second-order stochastic dominance remains a strong condition. Since an asset that displays **second-order stochastic dominance over all others will be preferred by any risk-averse investor with vN-M utility, the price of such an asset is likely to be bid up until the dominance goes away.**

### 3.3 Mean Preserving Spreads

It is also useful, therefore, to consider an alternative criterion that focuses entirely on the standard deviation of a random payoff, as a measure of the riskiness of the corresponding asset, holding the mean or expected value fixed.

Graphically, a mean preserving spread takes probability from the center of a distribution and shifts it to the tails.

![](https://upload-images.jianshu.io/upload_images/20447423-77796ce234acbc53.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

Mathematically, one way of producing a mean preserving spread is to take one random variable $X_{1}$ and defining a second, $X_{2}$, by adding "noise" in the form of a third, zero-mean random variable $Z$ :
$$
X_{2}=X_{1}+Z
$$
with $E(Z)=0$

Let $X_{1}$ and $X_{2}$, with $E\left(X_{1}\right)=E\left(X_{2}\right),$ be random payoffs on two assets. Then the following two statements are equivalent:
(i) $X_{2}=X_{1}+Z$ for some random variable $Z$ with $E(Z)=0$
(ii) asset 1 displays second-order stochastic dominance (SSD) over asset 2

# 4. 风险厌恶与投资决策

### 4.1 投资组合配置

风险厌恶投资者决策：风险资产与无风险资产

$$
\begin{aligned}
Y_{0}&= \text{initial wealth} \\
a&= \text{amount allocated to stocks} \\
\tilde{r}&= \text{random return on stocks}\\
r_{f} &=\text {risk - free return} \\
\tilde{Y}_{1} &=\text { final wealth} \\
\tilde{Y}_{1} &=\left(1+r_{f}\right)\left(Y_{0}-a\right)+a(1+\tilde{r}) \\
&=Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)
\end{aligned}
$$
Objective Function
The investor chooses a to maximize expected utility:
$$
\max _{a} E\left[u\left(\tilde{Y}_{1}\right)\right]=\max _{a} E u\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]
$$

The first-order condition(F.O.C.) is
$$
E\left[u^{\prime}\left[Y_{0}\left(1+r_{f}\right)+a^{*}\left(\tilde{r}-r_{f}\right)\right]\left(\tilde{r}-r_{f}\right)\right]=0
$$
Note: we are allowing the investor to sell stocks short $\left(a^{*}<0\right)$ or to buy stocks on margin $\left(a^{*}>Y_{0}\right)$ if he or she desires.
 **Theorem 5.1** If the Bernoulli utility function $u$ is increasing and concave, then
$\bullet a^{*}>0$ if and only if $E(\tilde{r})>r_{f}$
$\circ a^{*}=0$ if and only if $E(\tilde{r})=r_{f}$
$\circ a^{*}<0$ if and only if $E(\tilde{r})<r_{f}$
Thus, a risk-averse investor will always allocate at least some funds to the stock market if the expected return on stocks exceeds the risk-free rate.

定理证明

To prove the theorem, let
$$
W(a)=E\left[u^{\prime}\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]\left(\tilde{r}-r_{f}\right)\right]
$$
so that the investor's first-order condition can be written more compactly as
$$
W\left(a^{*}\right)=0
$$
it follows that
$$
W^{\prime}(a)=E\left[u^{\prime \prime}\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]\left(\tilde{r}-r_{f}\right)^{2}\right]<0
$$
since $u$ is concave. This means that $W$ is a decreasing function of
Finally, with
$$
\begin{aligned}
W(a) &=E\left[u^{\prime}\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]\left(\tilde{r}-r_{f}\right)\right] \\
W(0) &=E\left[u^{\prime}\left[Y_{0}\left(1+r_{f}\right)\right]\left(\tilde{r}-r_{f}\right)\right] \\
&=u^{\prime}\left[Y_{0}\left(1+r_{f}\right)\right] E\left(\tilde{r}-r_{f}\right) \\
&=u^{\prime}\left[Y_{0}\left(1+r_{f}\right)\right]\left[E(\tilde{r})-r_{f}\right]
\end{aligned}
$$
since $u$ is increasing, this means that $W(0)$ has the same sign as
$$
E(\tilde{r})-r_{f}
$$
We now know that:

$\bullet W(a)$ is a decreasing function
$\bullet W(0)$ has the same sign as $E(\tilde{r})-r_{f}$
$\bullet W\left(a^{*}\right)=0$
roof
$=(\tilde{r})-r_{f}>0$ implies $W(0)>0,$ and since $W$ is decreasing, $\mathcal{W}\left(a^{*}\right)=0$ implies $a^{*}>0 .$ since $W(0)$ has the same sign as
$E(\tilde{r})-r_{f}, E(\tilde{r})-r_{f}>0$

风险中性情况

Before moving on, return to the general problem
$$
\max _{a} E u\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]
$$
but assume now that the investor is risk-neutral, with
$$
u(Y)=\alpha Y+\beta
$$
and $\alpha>0,$ so that more wealth is preferred to less. The risk-neutral investor solves
$$
\begin{aligned}
& \max _{a} \in \alpha\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]+\beta \\
=& \max _{a} \alpha Y_{0}\left(1+r_{f}\right)+a\left[E(\tilde{r})-r_{f}\right]+\beta
\end{aligned}
$$
So long as $E(\tilde{r})-r_{f}>0,$ the risk-neutral investor will choose $a^{*}$ to be as large as possible, borrowing as much as he or she is allowed to in order to buy more stocks on margin.

### 4.2 风险厌恶与投资组合配置

The following result was proven by Kenneth Arrow in "The Theory of Risk Aversion," published in the 1971 volume Essays in the Theory of Risk-Bearing and reprinted in 1983 in volume 3 of the Collected Papers of Kenneth $J$. Arrow (Harvard University Press). 

#### 投资者之间比较

**Theorem 5.2*** Consider two investors, $i=1$ and $i=2,$ and suppose that for all wealth levels $Y$, $$ \begin{array}{l}R_{A}^{1}(Y)>R_{A}^{2}(Y) \\ \text { where } R_{A}^{i}(Y) \text { is investor i's coefficient of absolute risk aversion. Then } \\ a_{1}^{*}(Y)<a_{2}^{*}(Y)\end{array} $$ where $a_{i}^{*}(Y)$ is amount allocated by investor i to stocks when he or she has initial wealth $Y$.

其中绝对风险偏好也可以替换为相对风险偏好

注意到：DARA+CRRA是比较合理的风险偏好结构

#### 投资者风险投资随收入变化

ARA与投资额

**Theorem 5.4** Let $a^{*}\left(Y_{0}\right)$ be the solution to
$$
\max _{a} E u\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]
$$
If $u(Y)$ is such that
(a) $R_{A}^{\prime}(Y)<0$ then $\frac{d a^{*}\left(Y_{0}\right)}{d Y_{0}}>0$
(b) $R_{A}^{\prime}(Y)=0$ then $\frac{d a^{*}\left(Y_{0}\right)}{d Y_{0}}=0$
(c) $R_{A}^{\prime}(Y)>0$ then $\frac{d a^{*}\left(Y_{0}\right)}{d Y_{0}}<0$

RRA与投资弹性

Define the elasticity of the function $a^{*}\left(Y_{0}\right)$ as
$$
\eta=\frac{d\left(\ln a^{*}\left(Y_{0}\right)\right)}{d\left(\ln Y_{0}\right)}=\frac{Y_{0}}{a^{*}\left(Y_{0}\right)} \frac{d\left(a^{*}\left(Y_{0}\right)\right)}{d Y_{0}}
$$
The elasticity measures the percentage change in $a^{*}\left(Y_{0}\right)$ brought about by a percentage-point change in $Y_{0}$

**Theorem 5.5** Let $a^{*}\left(Y_{0}\right)$ be the solution to
$$
\max _{a} E u\left[Y_{0}\left(1+r_{f}\right)+a\left(\tilde{r}-r_{f}\right)\right]
$$
If $u(Y)$ is such that
$$
\begin{array}{l}
\text { (a) } R_{R}^{\prime}(Y)<0 \text { then } \eta>1 \\
\text { (b) } R_{R}^{\prime}(Y)=0 \text { then } \eta=1 \\
\text { (c) } R_{R}^{\prime}(Y)>0 \text { then } \eta<1
\end{array}
$$
Note that with constant relative risk aversion, $a^∗$ rises proportionally with wealth. Two additional

The theorem confirms what we know about CRRA utility: it implies that $a^{*}$ rises proportionally with $Y_{0}$. But the theorem extends the results to the cases of decreasing and increasing relative risk aversion.
Portfolios, Risk Aversion, and Wealth
With CRRA
$$
\frac{a^{*}}{Y_{0}}=K
$$
where
$$
K=\frac{\left(1+r_{f}\right)\left(\left[\pi\left(r_{G}-r_{f}\right)\right]^{1 / \gamma}-\left[(1-\pi)\left(r_{f}-r_{B}\right)\right]^{1 / \gamma}\right)}{\left(r_{G}-r_{f}\right)\left[(1-\pi)\left(r_{f}-r_{B}\right)\right]^{1 / \gamma}-\left(r_{B}-r_{f}\right)\left[\pi\left(r_{G}-r_{f}\right)\right]^{1 / \gamma}}
$$
Hence
$$
\begin{aligned}
\ln \left(a^{*}\left(Y_{0}\right)\right) &=\ln (K)+\ln \left(Y_{0}\right) \\
\eta &=\frac{d\left(\ln a^{*}\left(Y_{0}\right)\right)}{d\left(\ln Y_{0}\right)}=1
\end{aligned}
$$

### 4.3 风险厌恶与储蓄行为

Suppose there are two periods, $t=0$ and $t=1,$ and let
$Y_{0}=$ initial wealth 

$s=$ amount saved in period $\mathrm{t}=0$

$c_{0}=Y_{0}-s=$ amount consumed in period $t=0$ $\tilde{R}=1+\tilde{r}=$ random, gross return on savings $\bar{c}_{1}=s \tilde{R}=$ amount consumed in period $\mathrm{t}=1$
Suppose also that the investor has vN-M expected utility over consumption during periods $t=0$ and $t=1$ given by
$$
u\left(c_{0}\right)+\beta E\left[u\left(\tilde{c}_{1}\right)\right]=u\left(Y_{0}-s\right)+\beta E[u(s \tilde{R})]
$$
where the discount factor $\beta$ is a measure of patience
Risk Aversion and Saving Behavior
The solution to the investor's saving problem
$$
\max _{s} u\left(Y_{0}-s\right)+\beta E[u(s \tilde{R})]
$$
FOC
$$
\underbrace{u^{\prime}\left(Y_{0}-s^{*}\right)}_{MU_1}=\underbrace{\beta E\left[u^{\prime}\left(s^{*} \tilde{R}\right) \tilde{R}\right]}_{MU_2}
$$
必考

当储蓄收入$\tilde{R}$的不确定性上升时：

in the form of a mean preserving spread in the distribution of R˜ . Intuitively, one might expect there to be two offsetting effects: 

替代效应 the riskier return will make saving less attractive and thereby reduce s ∗ ; 

预防性储蓄 The riskier return might lead to “precautionary saving” in order to cushion period t = 1 consumption against the possibility of a bad output and thereby increase s ∗ .

let
$$
g(\tilde{R}) = u^{\prime}\left(s^{*} \tilde{R}\right) \tilde{R}
$$
Jensen’s inequality will imply that after a mean preserving spread the distribution of $\tilde{R}$ in this expectation will fall if g is concave and rise if g is convex.

The product and chain rules for differentiation imply
$$
\begin{aligned}
g^{\prime}(\tilde{R}) &=u^{\prime \prime}\left(s^{*} \tilde{R}\right) s^{*} \tilde{R}+u^{\prime}\left(s^{*} \tilde{R}\right) \\
g^{\prime \prime}(\tilde{R}) &=u^{\prime \prime \prime}\left(s^{*} \tilde{R}\right)\left(s^{*}\right)^{2} \tilde{R}+u^{\prime \prime}\left(s^{*} \tilde{R}\right) s^{*}+u^{\prime \prime}\left(s^{*} \tilde{R}\right) s^{*} \\
&=u^{\prime \prime \prime}\left(s^{*} \tilde{R}\right)\left(s^{*}\right)^{2} \tilde{R}+2 u^{\prime \prime}\left(s^{*} \tilde{R}\right) s^{*}
\end{aligned}
$$
implies that $g^{\prime \prime}(\tilde{R})$ has the same sign as
$$
u^{\prime \prime \prime}\left(s^{*} \tilde{R}\right) s^{*} \tilde{R}+2 u^{\prime \prime}\left(s^{*} \tilde{R}\right)
$$
To understand precautionary saving behavior, the concept of prudence is defined by Miles Kimball, “Precautionary Saving in the Small and in the Large,” Econometrica Vol.58 (January 1990): pp.53-73.

Kimball defines the coefficient of absolute prudence as
$$
P_{A}(Y)=-\frac{u^{\prime \prime \prime}(Y)}{u^{\prime \prime}(Y)}
$$
and the coefficient of relative prudence as
$$
P_{R}(Y)=-\frac{Y u^{\prime \prime \prime}(Y)}{u^{\prime \prime}(Y)}
$$
thereby extending the analogous measures of absolute and relative risk aversion.
Risk Aversion and Saving Behavior
$g^{\prime \prime}(\tilde{R})$ has the same sign as
$$
\begin{array}{l}
\qquad u^{\prime \prime \prime}\left(s^{*} \tilde{R}\right) s^{*} \tilde{R}+2 u^{\prime \prime}\left(s^{*} \tilde{R}\right) \\
r^{\prime \prime \prime}(Y) Y+2 u^{\prime \prime}(Y)=u^{\prime \prime}(Y)\left[\frac{Y u^{\prime \prime \prime}(Y)}{u^{\prime \prime}(Y)}+2\right]=u^{\prime \prime}(Y)\left[2-P_{R}(Y)\right]
\end{array}
$$
$g^{\prime \prime}(\tilde{R})$ is positive if $2<P_{R}(Y)$
$g^{\prime \prime}(\tilde{R})$ is negative if $2>P_{R}(Y)$

Kimball defines the coefficient of absolute prudence as
$$
P_{A}(Y)=-\frac{u^{\prime \prime \prime}(Y)}{u^{\prime \prime}(Y)}
$$
and the coefficient of relative prudence as
$$
P_{R}(Y)=-\frac{Y u^{\prime \prime \prime}(Y)}{u^{\prime \prime}(Y)}
$$
thereby extending the analogous measures of absolute and relative risk aversion.
Risk Aversion and Saving Behavior
$g^{\prime \prime}(\tilde{R})$ has the same sign as
$$
\begin{array}{l}
\qquad u^{\prime \prime \prime}\left(s^{*} \tilde{R}\right) s^{*} \tilde{R}+2 u^{\prime \prime}\left(s^{*} \tilde{R}\right) \\
u^{\prime \prime \prime}(Y) Y+2 u^{\prime \prime}(Y)=u^{\prime \prime}(Y)\left[\frac{Y u^{\prime \prime \prime}(Y)}{u^{\prime \prime}(Y)}+2\right]=u^{\prime \prime}(Y)\left[2-P_{R}(Y)\right]
\end{array}
$$
$g^{\prime \prime}(\tilde{R})$ is positive if $2<P_{R}(Y)$
$g^{\prime \prime}(\tilde{R})$ is negative if $2>P_{R}(Y)$

Hence, if $2<P_{R}(Y),$ then $g^{\prime \prime}(\tilde{R})>0 .$ since $g$ is convex, a mean preserving spread in the distribution of $\tilde{R}$ increases the right hand side of the optimality condition
$$
u^{\prime}\left(Y_{0}-s^{*}\right)=\beta E\left[u^{\prime}\left(s^{*} \tilde{R}\right) \tilde{R}\right]
$$
and $s^{*}$ must increase to maintain the equality. The precautionary saving effect dominates if the coefficient of relative prudence exceeds 2. 

**Kimball proves that more prudence induces more precautionary savings.** 

![](https://upload-images.jianshu.io/upload_images/20447423-6ee203ecff5907c7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### Purdence的更多说明

While the paper is famous for its link with the behavior of precautionary savings, it can be equivalently interpreted in a different way. since marginal utility (and not total utility) is the relevant concept for the analysis of decisions, it might be interesting to characterize the cost of risk through its impact on marginal (and not total) utility. Instead of computing a risk premium that keeps total utility constant, Kimball suggests the prudence premium ( $\psi$ ) that keeps marginal utility constant. Formally one has:
$$
u^{\prime}\left(x+E(\tilde{\varepsilon})-\psi^{\prime \prime}(x, \tilde{\varepsilon})\right)=E\left[u^{\prime}(x+\tilde{\varepsilon})\right]
$$
It is then easy to show that:
$$
\psi^{\prime \prime}(x, \tilde{\varepsilon}) \cong \frac{\sigma_{\bar{\ell}}^{2}}{2}\left(-\frac{u^{m}(x)}{u^{\prime \prime}(x)}\right)
$$
where $-\frac{u^{m}(x)}{u^{\prime \prime}(x)}$ is the index of absolute prudence.

### 4.4 风险厌恶与prudence (补充)

下面三者等价   ![](https://upload-images.jianshu.io/upload_images/20447423-bbbf98d49683897a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

证明

![](https://upload-images.jianshu.io/upload_images/20447423-73b6fc3424ae8c57.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193817.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200522193843.png)

