

Delta - sensitivity of (option) price to small changes in price of underlying asset

Gamma - sensitivity of (option) price to large changes in price of underlying asset

Rho - sensitivity of (option) price to interest rates

Vega - sensitivity of (option) price to volatility

Theta - time decay of portfolio value, holding everything else constant

## Delta（德尔塔）

Dela衡量的是期权价格变动与期权标的物价格变动之间的关系
$$
\Delta  = \frac{期权价格的变化}{期权标的物价格的变化}
$$
Dela在期权套期保值交易中有很重要的应用，被称为Dela对冲交易法。

数学上，$ Delta (c)=N (d_1)$

- $ Pr(S<K)=N(-d_2)=1-N(d_2) $:看跌期权被执行的（风险中立测度下的）概率；
- $ N(d_2)=Pr(S>K) $,即看涨期权被执行的（风险中立测度下的）概率。

看涨期权德尔塔与看跌期权德尔塔之间的关系：$ Delta (p)=Delta (c)-1=-N(-d_1) $，这个关系可以从平价公式推出。

| 看涨期权                                                     | 看跌期权                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092434.png) | ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092532.png) |

折线为期权的内在价值，红色虚线是期权的价值，蓝色阴影部分是期权的时间价值。其中，看跌期权的时间价值可能为负(e.g.当看跌期权已经实现最大收益时，图中为50，提前行权是最佳选择)。

理论上看涨期权的时间价值总为正，因此不可能提前行权。然而实际中并非如此，当期权价格低于内在价值时，大多数投资者将提前行权，详细阅读[美国期权投资者是否理性行权？](https://mp.weixin.qq.com/s/5cYLUxpaNrYZkMxFrtAsWQ)

Delta值即红色虚线的斜率。

Delta的取值范围在-1与1之间

- 看涨期权的 Delta 是正值，范围从0到1，期权实值程度越深，其Delta值越大，深度实值看涨期权的Delta会达到0.8以上，深度虚值看涨期权的 Delta会达到0.2以下
- 解释：由于看涨期权价格与标的物价格成正向关系，即期权价格与期权标的物价格关系曲线的斜率为正，我们说过 Delta本质上就是斜率，所以看张期权的 Delta为正。
- 注：我们这是所说的 Delta为正是指看涨期权多头，如果是看涨期权空头，则 Delta为负！

深度实值期权几乎等价于持有股票，因此期权交易者经常构建深度实值看涨期权以此替代现货多头头寸(多头替代)，相比于直接持有股票，需要的资金量更少，例如，公募基金经常使用该方法流出资金应对赎回需求。

平值期权的德尔塔接近于0.5

证明：

以European Call Option为例，可以证明： ATMS Call Option的Delta接近于0.5, 且与ATMS Call Option相比，ATMF(at the money forward) Call Option的Delta更接近于0.5。
$$
 \Delta_{c a l l}=N\left(d_{1}\right)=\Phi\left(\frac{\log \left(\frac{S_{0}}{K}\right)+\left(r+\frac{1}{2} \sigma^{2}\right)(T-t)}{\sigma \sqrt{T-t}}\right) 
$$
因此, 对于ATMS Call Option, 即 $ S_{0}=K, $ 
$$
 \Delta_{\text {call }}^{A T M S}=\Phi\left(\frac{\left(r+\frac{1}{2} \sigma^{2}\right)(T-t)}{\sigma \sqrt{T-t}}\right) 
$$
而对于ATMF Call Option, 即 $ K=S_{0} e^{r(T-t)}, $ 
$$
 \Delta_{\text {call }}^{A T M F}=\Phi\left(\frac{\sigma \sqrt{T-t}}{2}\right) 
$$
对于ATMF Call Option, Delta中与无风险利率相关的项进一步被消除。

对上面的等式在0处进行Taylor展开， 
$$
 \Delta_{c a l l}^{A T M F}=\Phi\left(\frac{\sigma \sqrt{T-t}}{2}\right) \approx \Phi(0)+\Phi^{\prime}(0) \frac{1}{2} \sigma \sqrt{T-t}=0.5+\frac{1}{\sqrt{2 \pi}} \frac{1}{2} \sigma \sqrt{T-t} \approx 0.5+0.1995 \sigma \sqrt{T-1} 
$$
接近于0.5。

德尔塔跟存续期的关系：

- 当到期日临近时，虚值期权的德尔塔慢慢接近0,实值期权的德尔塔趋近于1，而平值期权的德尔塔保持在0.5附近。

德尔塔与波动率的关系

- 当波动率越来越大的时候，虚值期权越来越像平值（且速度很快），德尔塔从0增长到0.5;
- 实值期权也是越来越像平值（速度较慢），德尔塔从1降低到0.5;而平值期权的价格保持线性增长，德尔塔保持在0.5左右。
- 所以当波动率增加的时候，所有期权的德尔塔都趋向于0.5附近。

练习

1.如果一个价格为3元的看涨期权其德尔塔为0.35,那么当股价上涨1元时期权价格为多少？

期权价值上涨至3+0.35*1 = 3.35

2.当股价继续下跌1元时，期权价格会回到期初的3元吗？为什么？

期权价格上涨后，Delta值变大，因此当股价继续下跌1元时，期权价格会下降至比期初更低。

## Gamma

Gamma:衡量期权Delta相对于标的资产价格的变化率，也即期权理论价值对标的资产价格的二阶导数(curvature)。
$$
\Gamma = \frac{\partial p}{\partial^2 S^2} = \frac{\partial \Delta}{\partial S}
$$
从图形上容易得到，看涨、看跌期权的Gamma值都是正值。

通过对Put-call parity两边求两次导数，易得看涨、看跌期权的Gamma值必须相等

- 深度虚值与深度实值的Delta值随标的资产变化均不大，因此Gamma接近于0，并且随着到期日临近，Gamma越来越接近于0(红色虚线越来越接近蓝色折线)；
- 平值期权的Gamma最大，并且随着到期日临近，Gamma越来越大(红色虚线越来越接近蓝色折线)

| 看涨期权                                                     | 看跌期权                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092434.png) | ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092532.png) |

看涨期权多头Gamma随资产价格变化

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318082008.png)

看涨期权多头Gamma随到期日变化

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318081912.png)

看涨期权多头Gamma随波动率变化：波动率变大，红色虚线上移，平值期权的Gamma变小，深度虚值与深度实值的Gamma变大，当波动率非常大时，三者的Gamma趋同

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318082602.png)

### 美国散户逼空Gamestock事件：Gamma squeeze

散户除了买入GME股票外，还买入大量以GME股票为标的的看涨期权(美国存在对应的个股期权)。

做市商为了提供流动性，因此大量卖出看涨期权，同时为了实现Delta对冲，做市商不断买入GME股票，推动了股价上涨。

Gamma squeeze: 随着标的股价S上涨，由于Gamma>0，Delta越来越大，Delta对冲需要购买的GME股票越来越多，进一步加速股价的上涨。

最后券商暂停散户交易。

【练习】期权交易者经常构建深度实值看涨期权以此代替现货多头头寸。假如我们买入10手行权价格为50元的看涨期权，德尔塔为1.0，现货股票价格为75元。试问：如果股票价格下跌20元，下面哪一个是正确的？

1. 期权交易将比1000股股票损失得更多；
2. 期权交易将比1000股股票损失得更少；
3. 两者都损失20000元。

注：一手期权对应100股

由于Gamma>0，因此随着价格下降Delta会减小，从而对股价下跌更不敏感，因此期权损失更少，选1。

## Theta

Theta衡量期权理论价值因为时间流逝而贬值的速度，是期权关于时间的风险度量指标
$$
Theta = \frac{\partial p}{\partial T}
$$
期权多头Theta<0，期权空头Theta>0。

Theta绝对值越大，表明期权价格的时间衰减速度越快！

随着到期日临近，期权价值都会降低，其中平值期权本身的时间价值最大(蓝色阴影部分最高)，因此贬值速度也最快，特别是在期权到期的一个月内，期权价值会迅速下降；其次是实值期权对时间变化较为敏感，最不敏感的是虚值期权。

| 看涨期权                                                     | 看跌期权                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092434.png) | ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092532.png) |

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318165503.png)

Theta关于价格的分布是非对称的，随着期权存续期的增加，这种敏感度的不对称性越大。

| T = 0.01                                                     | T = 1                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318170900.png) | ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318173855.png) |

Theta随到期日变化，实值与虚值期权Theta临近到期日都趋向于0，而平值期权Theta的绝对值越来越大。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210318170408.png)

Theta随波动率变化，波动率越大，Theta的绝对值均越来越大。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318173654.png)

【练习】估计看涨期权价格：S = 100, K = 100, T = 7, r = 0.015, 波动率 = 75%, Theta = -0.3

解：在距离期权的到期的一个月内，Theta的平均值是初始值的两倍，因此平均$\bar{Theta} = -0.6$，最后在到期时平值期权的价值变为0，因此期权价值大约为 $7 \times|-0.6| +0= 4.2$，通过BS公式计算的价格为4.18

## Vega

Vega是期权价值变动与波动率变动的比值：


$$
Vega = \frac{\partial c}{\partial \sigma}
$$
期权多头的Vega值总为正，空头则为负。

Vega随标的资产价格变化：平值期权的Vega值最大，实值/虚值程度越大Vega越小。



平值期权与波动率线性相关，即Vega为常数

$$
V = 0.4 \times S \sigma \sqrt{T} \\
Vega = 0.4 \times S \sqrt{T}
$$
注意到，这种线性关用到了拉格朗日中值定理做近似，当$\sqrt{T}$较大时，$d_1-d_2 = \sigma \sqrt{T}$较大，因此近似不准确。



Vega与波动率

波动率 很大时，虚值/实值期权的Vega都接近与平值期权，平值期权的Vega再一个狭窄的范围内波动

波动率增加，Vega变大

Vega与



隐含波动率起到了非常重要的作用

隐含波动率的预测具有非常大的现实意义

【练习】当标的物价格下跌时，市场中经常发生，看涨期权价格保持不变甚至上升的情况，如何解释？

隐含波动率上涨



同样当标的物价格下跌时，市场中经常发生，看跌期权价格保持不变甚至下降的情况，如何解释？

隐含波动率下跌

[如何看待期权价格暴涨192倍？](https://mp.weixin.qq.com/s/aAtcNXFbuzA7oX25TDUN0w)

## Rho

Rho发挥的作用较小，通常对于十年以上的交易经验者，Rho才有意义
$$
Rho = \frac{\partial V}{\partial r}
$$

## 如何解读希腊字母？

Delta中性交易：对于股票涨跌方向不感兴趣，只是看多/看空波动率。

例子，做市商在开仓后，希望立即平仓来获取价差收益，为了规避标的价格变动风险，常进行Delta中性交易。

《Dynamic Hedge》、《黑天鹅》作者的策略：一直购买深度虚值的看跌期权，大多数时候处于亏损状态，但亏损并不多，深度虚值的看跌期权不值钱；一旦发生黑天鹅事件，则股价将对暴跌，带来巨大收益

Delta hedge：成本较低

Delta-Gamma Hedge：成本更高，对于标的价格变动更不敏感

做多期权(无论时看涨或者看跌)即做多波动率