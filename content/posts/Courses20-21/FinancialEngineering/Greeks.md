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

理论上看涨期权的时间价值总为正，因此不可能提前行权。然而实际中并非如此，当期权价格低于内在价值时，大多数投资者将提前行权，详细阅读[美国期权投资者是否理性行权？](https://mp.weixin.qq.com/s/5cYLUxpaNrYZkMxFrtAsWQ)，

Delta值即红色虚线的斜率。

Delta的取值范围在-1与1之间

- 看涨期权的 Delta 是正值，范围从0到1，期权实值程度越深，其Delta值越大，深度实值看涨期权的Delta会达到0.8以上，深度虚值看涨期权的 Delta会达到0.2以下
- 解释：由于看涨期权价格与标的物价格成正向关系，即期权价格与期权标的物价格关系曲线的斜率为正，我们说过 Delta本质上就是斜率，所以看张期权的 Delta为正。
- 注：我们这是所说的 Delta为正是指看涨期权多头，如果是看涨期权空头，则 Delta为负！

深度实值期权几乎等价于持有股票

平值期权的德尔塔接近于0.5

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

Gamma: curvature
$$
\Gamma = \frac{\partial c}{\partial^2 S^2} = \frac{\partial \Delta}{\partial S} 
$$
从图形上容易得到，看涨、看跌期权的Gamma值都是正值。

通过对Put-call parity两边求两次导数，易得看涨、看跌期权的Gamma值必须相等

- 深度虚值与深度实值的Delta值随标的资产变化均不大，因此Gamma接近于0，并且随着到期日临近，Gamma越来越接近于0(红色虚线越来越接近蓝色折线)；
- 平值期权的Gamma最大，并且随着到期日临近，Gamma越来越大(红色虚线越来越接近蓝色折线)

波动率变大，红色虚线上移，平值期权的Gamma变小，深度虚值与深度实值的Gamma变大，当波动率非常大时，三者的Gamma趋同

| 看涨期权                                                     | 看跌期权                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092434.png) | ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316092532.png) |

