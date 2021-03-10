Delta - sensitivity of (option) price to small changes in price of underlying asset

Gamma - sensitivity of (option) price to large changes in price of underlying asset

Rho - sensitivity of (option) price to interest rates

Vega - sensitivity of (option) price to volatility

Theta - time decay of portfolio value, holding everything else constant

（一）Delta（德尔塔）

Dela衡量的是期权价格变动与期权标的物价格变动之间的关系
$$
\Delta  = \frac{期权价格的变化}{期权标的物价格的变化}
$$
Dela在期权套期保值交易中有很重要的应用，被称为Dela对冲交易法。

![image-20210310171959217](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210310171959217.png)

折线为期权的内在价值，红色虚线是期权的价值，蓝色阴影部分是期权的时间价值。

Delta的性质

- Delta的取值范围在-1与1之间
- 看涨期权的 Delta 是正值，范围从0到1，期权实值程度越深，其Delta值越大，深度实值看涨期权的Delta会达到0.8以上，深度虚值看涨期权的 Delta会达到0.2以下
- 解释：由于看涨期权价格与标的物价格成正向关系，即期权价格与期权标的物价格关系曲线的斜率为正，我们说过 Delta本质上就是斜率，所以看张期权的 Delta为正。
- 注：我们这是所说的 Delta为正是指看涨期权多头，如果是看涨期权空头，则 Delta为负！