---
title: "The Foreign Exchange Market and Trade Elasticities"
date: 2021-08-06T21:17:53+08:00
lastmod: 2021-08-07T21:17:53+08:00
draft: false

description: ""
upd: "Marshall-Lerner-Condition, J-curve"

tags: ['Notes']
categories: ['International Finance']

math: true
---

## Marshall-Lerner Condition

### Assumptions

Consider a two-country model with no capital flows where supply of exports and imports are perfectly elastic and changes in the volume of exports and imports have no effect on prices

The volume of exports and imports vary with the exchange rate.

Under these assumptions, the quantity of domestic currency demanded is equal to the value of domestic exports, and the quantity of domestic currency supplied is equal to the value of the domestic imports.

$$
B=P_{X} Q_{X}-S P_{M}^{*} Q_{M}=X-S M
$$

where

- $ P_{x}= $ price in domestic currency of domestic exports

- $ Q_{x}= $ volume of domestic exports
- $ P_{M}= $ price in foreign currency of domestic imports
- $ Q_{M}= $ volume of domestic imports
- $ S= $ nominal exchange rate
- $ X= $ value of exports in domestic currency
- $ M= $ value of imports in foreign currency

### Differentiate

$$
\frac{\partial B}{\partial S}=\frac{\partial X}{\partial S}-S \frac{\partial M}{\partial S}-M
$$

where $ B=B(S), X=X(S) $ and $ M=M(S) $ are function of $ S $. Then divide by $ M $

$$
\frac{\partial B}{\partial S} \frac{1}{M}=\frac{\partial X}{\partial S} \frac{1}{M}-\frac{S}{M} \frac{\partial M}{\partial S}-1
$$

and in equilibrium, the trade balance is

$$
B=X-S M=0 \Longrightarrow X=S M
$$

Substitute $ S / X $ in place of $ 1 / M $, and obtain

$$
\frac{\partial B}{\partial S} \frac{S}{X}=\frac{\partial X}{\partial S} \frac{S}{X}-\frac{S}{M} \frac{\partial M}{\partial S}-1
$$

Hence, rewrite as

$$
\begin{aligned}
\frac{\partial B}{\partial S} &=\left(\frac{\partial X / X}{\partial S / S}-\frac{\partial M / M}{\partial S / S}-1\right) \frac{X}{S} \\
&=\left(\eta_{X}+\eta_{M}-1\right) \frac{X}{S}
\end{aligned}
$$

where $ \eta_{X}=\frac{\partial X / X}{\partial S / S} $ is price elasticity of demand for exports, and $ \eta_{M}=-\frac{d M / M}{d S / S} $ is the price elasticity of demand for imports. An exchange rate depreciation implies a positive effect on the trade balance when

$$
\frac{\partial B}{\partial S}>0
$$

which is equivalent to

$$
\left(\eta_{X}+\eta_{M}-1\right) \frac{X}{S}>0
$$

Since $ X / S>0 $, we obtain the **Marshall-Lerner condition**

$$
\eta_{X}+\eta_{M}>1
$$

While this condition is fulfilled in the long-run, in the short-run the sum of the elasticities turns out to be less than one. So, a domestic depreciation (devaluation) implies a deterioration of the current account in the short-term and an improvement in the long-term.

## The Foreign Exchange Market and the Reaction of the Current Account

*Figure*: Increase in Demand for Foreign Currency

When the demand for foreign currency shifts out from D to D', the result depends on the *exchange rate regime*. 

- Panel (a)/ Left panel illustrates a **floating exchange rate**: An increase in the priceof foreign currency is necessary to equilibrate the private market. 
- Panel (b)/ Right panel illustrates a **fixed exchange rate**: 
    - The central bank intervenes by supplying the excess amount demanded, out of its foreign exchange reserves
    - **Net capital outflow, BP deficits**

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803151801.jpg)



## The Effects of a Devaluation of the Dollar on Export and Import

Assumptions:

1. There are no capital flows (KA = 0): BoP = sales of the export – spending on the import.
2. Only two goods are traded, an importable good and an exportable good.
3. Domestic residents look only at the price expressed in domestic currency and foreign residents look only at the price expressed in foreign currency.
    1. $ \mathrm{M}^{\mathrm{DD}}=\mathrm{M}^{\mathrm{DD}}(\mathrm{p}[\$])=\mathrm{M}^{\mathrm{DD}}\left(\mathrm{P}_{\euro} \cdot \mathrm{e}_{\$ / \euro}\right) $​​
    2. $\mathrm{X}^{\mathrm{DD}}=\mathrm{X}^{\mathrm{DD}}(\mathrm{p}[\euro])=\mathrm{X}^{\mathrm{DD}}\left(\frac{\mathrm{P}_{\$}}{\mathrm{e}_{\$ / \euro}}\right)$​​​
4. **Supply is infinitely elastic**, that is supply is determined by demand.
5. The economy is initially in a position of balanced trade (*NX = 0*).

*Figure*: Effect of a Devaluation on Trade

1. Panel (a)/ Left panel shows how a devaluation lowers the quantity of imports. 
2. Panel(b)/ Right panel shows how the devaluation raises the quantity of exports. 
3. The effects on import spending and export revenue respectively, are shown by the areas of the shaded rectangles.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803153611.png)
$$
\text{Net supply of forrign exchange}[\epsilon]=X-M =\left(\frac{\bar{P}}{e \uparrow}\right) \downarrow \cdot X \uparrow-\bar{P}^* \cdot M \downarrow
$$
where $P^*$​​ or $\bar{P}^*$​​​ indicates the foreign price level, $P$​ or $\bar{P}$​​​ indicates the domesitic price level.

### Marshall-Lerner-Condition

**Elasticity** according to Wikipedia: The variation in demand in response to a variation in price is called price elasticity of demand. It may also be defined as the ratio of the percentage change in demand to the percentage change in price of particular commodity.
$$
|\varepsilon|=\frac{\frac{\Delta q}{q}}{\frac{\Delta p}{p}}
$$
$\varepsilon_X$ = price elasticity of demand for exports

$\varepsilon_M$ = price elasticity of demand for imports

The **Marshall-Lerner-Condition**: Given the assumptions before, the *necessary and sufficient condition for the devaluation to improve the trade balance*, or for the foreign exchange market to be stable, is the
$$
\varepsilon_{X}+\varepsilon_{M}>1
$$
=> Normal reaction of the foreign balance to exchange rate changes

If the economy is initially in a position of trade deficits (*NX < 0*), the necessary condition for a devaluation to improve the trade balance is more stringent:
$$
\varepsilon_{X}+\varepsilon_{M}\gg 1
$$
*FIGURE*: The J-curve

In the aftermath of a devaluationthe trade balance

1. worsens initiallybecause of the perverse valuationeffect, then
2. gradually improves overtime as the elasticities rise, and finally
3. surpasses its starting point when the Marshall-lerner condition is satisfied

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803162847.png)

### Elasticity Pessimism

In the *short run the Marshal Learner condition is not fullfilled* because:

1. In the 1930s exchange rates were highly volatile
2. Volumes of imports and exports are fixed by long term contracts
3. Price elasticity of supply and demand usually rises over time





![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210804050129115.png)
