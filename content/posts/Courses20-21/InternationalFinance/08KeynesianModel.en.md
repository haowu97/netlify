---
title: "Chapter8 National Income and the Trade Balance: the Keynesian Model"
date: 2021-08-05T21:17:53+08:00
draft: false

description: "Open Country Keynesian Model, IS-LM curve, Crowding-out effect."
upd: "Open Country Keynesian Model, IS-LM curve, Crowding-out effect."

tags: ['Notes']
categories: ['International Finance']
---

<!--more-->

## The Small Open Country Keynesian Model (“SMOC”)

Assumptions:

1. Fixed exchange rates
2. Constant price level
3. Keynesian consumption function
4. "Small": Any impact of the domestic economy on the rest of the world can be safely ignored.
5. Investment and government expenditures are exogenous and constant

Setting

1. $ \mathrm{Y}^{DD}=\mathrm{C}+\mathrm{I}+\mathrm{G}+\mathrm{NX} $
2. $ \mathrm{C}=\mathrm{C}_{0}+\mathrm{c} \cdot \mathrm{Y} $
3. $ \mathrm{I}=\mathrm{I}_{0} $
4. $ \mathrm{G}=\mathrm{G}_{0} $
5. $ \mathrm{X}=\mathrm{X}_{0} $
6. $ \mathrm{M}=\mathrm{M}_{0}+\mathrm{m} \cdot \mathrm{Y} $
7. $ \mathrm{Y}^{\mathrm{SY}} \quad=\mathrm{Y} $
8. $ Y^\mathrm{SY} \quad=Y^\mathrm{DD} $

Therefore, we can write aggregate demand as 

$$
Y^{\mathrm{DD}}=\mathrm{C}_{0}+\mathrm{c} \cdot \mathrm{Y}+\mathrm{I}_{0}+\mathrm{G}_{0}+\mathrm{X}_{0}-\left(\mathrm{M}_{0}+\mathrm{m} \cdot \mathrm{Y}\right)
$$

or 

$$
Y^{\mathrm{DD}}=\mathrm{C}_{0}+\mathrm{I}_{0}+\mathrm{G}_{0}+\mathrm{X}_{0}-\mathrm{M}_{0}+(\mathrm{c}-\mathrm{m}) \cdot \mathrm{Y}
$$

Using the equilibrium condition we find:

$$
\mathrm{Y}=\mathrm{Y}^{\mathrm{S} Y}=\mathrm{Y}^{\mathrm{DD}}
$$

Solving for the **equilibrium level of income**,

$$
Y = \frac{\mathrm{C}_{0}+\mathrm{I}_{0}+\mathrm{G}_{0}+\mathrm{X}_{0}-\mathrm{M}_{0}}{1-c+m}
$$

Simplified to

$$
Y = \frac{\mathrm{A}_{0}+\mathrm{X}_{0}-\mathrm{M}_{0}}{s+m}
$$

where:

- $A_0$ = Autonomous component of domestic aggregate demand
- Marginal saving propensity $s = 1 – c$​.​

Trade balance (TB):

$$
TB=NX = X_0 - (M_0 + m·Y)
$$

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803172617.png)

### Equilibrium: The “Small” Keynesian Cross

Derived by the National Savings Identity: $S - I = X - M$

$$
Y = \frac{\mathrm{A}_{0}+\mathrm{X}_{0}-\mathrm{M}_{0}}{s+m}
$$

with

$$
S - I = (Y-C_0-cY-G_0) - I_0 = sY - C_0 -G_0- I_0 = sY-A_0\\
X-M = X_0 - M_0-mY
$$

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803223609.png)

### The Fiscal Multiplier

$$
\frac{\Delta Y^{e}}{\Delta G}=\frac{1}{s+m}\\
\frac{\Delta N X}{\Delta G}=-\frac{m}{s+m}
$$

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803223916.png)

【Example】$ \Delta \mathrm{G}_{0}=\Delta \mathrm{A}_{0}=\$ 1 $ billion

Differentiate $ Y^{\neg}=\frac{A_{0}+X_{0}-M_{0}}{s+m} $ partially with respect to $ A_{0} $

$$
\quad \Delta \mathrm{Y}=\frac{1}{\mathrm{~s}+\mathrm{m}} \cdot \Delta \mathrm{A}_{0} = \mathrm{m} \cdot \$ 1 \text{ billion} 
$$

with $ s=0.3 $ and $ m=0.2 $ : $ \Delta \mathrm{Y}=\frac{1}{0.3+.02} \cdot \$ 1 $ billion $ =\frac{1}{0.5} \cdot \$ 1 $ billion, $ \Delta \mathrm{Y}=2 \cdot \$ 1 $ billion

### The Export Multiplier

$$
\frac{\Delta \mathrm{Y}^{e}}{\Delta \mathrm{X}_{0}}=\frac{1}{\mathrm{~s}+\mathrm{m}}\\
 \frac{\Delta \mathrm{NX}}{\Delta \mathrm{X}_{0}}=\frac{\mathrm{s}}{\mathrm{s}+\mathrm{m}}
$$

Proof:

$$
\Delta \mathrm{NX}=\Delta \mathrm{X}-\Delta \mathrm{M}=\Delta \mathrm{X}_{0}-\mathrm{m} \cdot \frac{1}{\mathrm{~s}+\mathrm{m}} \Delta \mathrm{X}_{0} =\left(\frac{\mathrm{s}+\mathrm{m}}{\mathrm{s}+\mathrm{m}}-\frac{\mathrm{m}}{\mathrm{s}+\mathrm{m}}\right) \Delta \mathrm{X}_{0}=\frac{\mathrm{s}}{\mathrm{s}+\mathrm{m}} \cdot \Delta \mathrm{X}_{0}
$$

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803232216.png)

### Derivation of the export multiplier

$$
\mathrm{NX}=\mathrm{X}-\mathrm{M}=\mathrm{X}_{0}-\mathrm{M}_{0}-\mathrm{m} \cdot \mathrm{Y} \\
 \Delta \mathrm{NX}=\Delta \mathrm{X}-\Delta \mathrm{M}=0-0-\mathrm{m} \cdot \Delta \mathrm{Y}
$$

since $ \Delta \mathrm{Y}=\frac{1}{\mathrm{s}+\mathrm{m}} \cdot \Delta \mathrm{G}_{0} $, we have

$$
\Delta \mathrm{NX}=-\mathrm{m} \cdot \Delta \mathrm{Y}=-\mathrm{m} \cdot \frac{1}{\mathrm{~s}+\mathrm{m}} \cdot \Delta \mathrm{G}_{0}=\frac{-\mathrm{m}}{\mathrm{s}+\mathrm{m}} \cdot \Delta \mathrm{G}_{0} 
$$

Then

$$
\frac{\Delta \mathrm{NX}}{\Delta \mathrm{G}_{0}}=\frac{-\mathrm{m}}{\mathrm{s}+\mathrm{m}}
$$

### Taxes

Disposable Income $ \left(Y^{\text {disp }}\right): $ $Y^{\text {disp }}=Y-T$

$$
C=C_{0}+c \cdot Y^{\text {disp }}=C_{0}-C \cdot(Y-T)=C_{0}+C \cdot Y-c 
$$

#### Poll Tax

With $ T=T_{0} $,

$$
Y^{\mathrm{DD}}=C_{0}+c Y-c T_{0}+I_{0}+G_{0}+X_{0}-M_{0}-m Y
$$

Equilibrium:

$$
\mathrm{Y}^{e}=\frac{\mathrm{C}_{0}+\mathrm{I}_{0}+\mathrm{G}_{0}+\mathrm{X}_{0}-\mathrm{M}_{0}-\mathrm{CT}_{0}}{\mathrm{~s}+\mathrm{m}} 
$$

#### Income Tax

With $T=tY$,

$$
Y^{\mathrm{DD}} =C_{0}+C \cdot Y-C \cdot t \cdot Y+I_{0}+G_{0}+X_{0}-M_{0}-m \cdot Y
$$

Equilibrium:

$$
Y^{e} =\frac{C_{0}+I_{0}+G_{0}+X_{0}-M_{0}}{1-c \cdot(1-t)+m}
$$

## Two Country Keynesian Model

For a Large Country: If income in the foreign country, $ Y^{*} $, increases, foreigners import more from the home country.

$$
X=\bar{X}+m^{*} Y^{*}
$$

The new formula for equilibrium income:

$$
Y=\frac{\bar{A}+\bar{X}-\bar{M}+m^{*} Y^{*}}{s+m}
$$

Similarly, the solution for equilibrium foreign income is

$$
Y^{*}=\frac{\bar{A}^{*}+\bar{M}+m Y-\bar{X}}{s^{*}+m^{*}}
$$

Equilibrium income for each country is indicated algebraically by solving the two equations simultaneously. 

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803234641.png)

FIGURE: Simultaneous Solution for Both Countries' Incomes

1. A domestic expansion shifts the domestic line up so that the new intersection occurs at $ D^{\prime} $. The increase in $ Y $ is greater than in the small-country model - which ignored the repercussion effect of higher income abroad (point $ D $ ).
2. It can also be used to illustrate the point about an adverse trend in the U.S. trade balance. The line that gives U.S. income, Y(as a function of foreign income, $Y^*$), shifts out faster than the line that gives foreign income (as a function of U.S income). At point $D^"$ it lies above the trade balance equilibrium schedule.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804001541.png)

The multiplier for a domestic expansion turns out to be

$$
\frac{\Delta Y}{\Delta A}=\frac{1}{s+m-\frac{m^{*} m}{s^{*}+m^{*}}}
$$

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803234412.png)

### Policy Analysis

*FIGURE*: Insulation Under Floating Exchange Rates

1. Panel (a) shows how domestic disturbances are "bottled up" inside the country. A fall in investment, I, has a greater effect on income under a floating rate than under a fixed rate because the currency appreciates and discourages net exports. 
2. Panel (b) shows how the country is "insulated" from foreign disturbances. A fall in foreign demand causes the domestic currency to depreciate, which stimulates net exports.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804003027.png)

|                    | Fixed Exchange Rates                              | Flexible Exchange Rates             |
| ------------------ | ------------------------------------------------- | ----------------------------------- |
| Domestic shocks    | Partially  transmitted abroad                     | Remain entirely  within the country |
| Shocks from abroad | Are partially  transferred to the domestic market | Remain completely abroad            |

Policy under CA deficit:

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804003839.png)

### External Balance or Internal Balance

*FIGURE*: Dilemma: **External Balance or Internal Balance**?

1. Panel (a) shows how the government, *using just fiscal policy*, can attain either a zero trade balance at point X or full employment at N, but not both. 
2. Panel (b) shows how the government, *using just exchange rate policy*, again can attain either one goal at B or the other at N, but not both.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804004411.png)

*FIGURE*: Policy Combinations That Give **External Balance**

*After a fiscal expansion, there must also be a devaluation if the trade balance is to be restored to its original level*. 

1. In panel (a), the axes represent the policy goals.
2. In panel (b), the axes represent the policy instruments.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804005029.png)

where

- TB means current account.
- E means exchange rate.
- G means government expenditure.

*FIGURE* Policy Combinations That Give **Internal Balance**

*After a fiscal expansion there must also be a revaluation of the currency if the level of output is to be restored to its' original level.* 

1. In panel (a), the axes represent the policy goals. 
2. In panel (b), the axes represent the policy instruments.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804005537.png)



*FIGURE*: The **Swan Diagram** of Internal and Externa Balance

- The BB schedule shows the combinations of spending, G, and the exchange rate, E, that give the desired trade balance.
- The YY schedule shows the combinations that give the desired level of output. 

Onlyby deliberately using bothindependent policy instrumentscould the government attain both policy goals at point A.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804191629.png)

## The Open Economy IS-LM Curves

### Monetary Factors

Setting:

1. $\mathrm{Y}^{DD}=\mathrm{C}+\mathrm{I}+\mathrm{G}+\mathrm{NX}$
2. $ C=C_{0}+c \cdot Y $
3. $ \mathrm{I}=\mathrm{I}_{0}-\mathrm{h} \cdot \mathrm{i} $
4. $ G=G_{0} $
5. $ \mathrm{NX}=\mathrm{NX}_{0}$
6. $ \mathrm{Y}^{\mathrm{SY}} \quad=\mathrm{Y}$
7. $Y^{SY} = Y^{DD}$

where:

1. $ \mathrm{i}= $ Interest rate 
2. $\mathrm{h}=$ Marginal efficency of investment

*FIGURE*: Effect of a Fall in the Interest Rate, i

- If monetary policy lowers the interest rate from $ i_{1} $ to $ i_{2} $, then it stimulates investment from $ I_{1} $ to $ I_{2} $. The saving-investment line shifts out, raising the level of income from $ Y_{1} $ to $ Y_{2} $. This inverse relationship between $ i $ and $ Y $ is the IS curve.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804194853.png)

### Policy Analysis

*FIGURE*: **Monetary Expansion**

- The upward-sloping LM curve gives equilibrium in the money market. An increase in the money supply shifts the LM curve out, *driving down the interest rate*, $ i $, at point $ M $, and as a result increasing income, $ Y $. The *trade balance worsens*.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804195143.png)

*FIGURE*: **Fiscal Expansion with Crowding-out of Investment**

- An increase in spending shifts the IS curve to the right by the amount of the simple Keynesian multiplier. However, the actual increase in income is somewhat less than this, at point F, because an increase in the demand for money *drives up the interest rate and crowds out investment*.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804200501.png)

*FIGURE*: **Devaluation with Crowding-out**

- A devaluation shifts the IS curve to the right by the amount of the simple Keynesian multiplier(at point L). However, the actual increase in income is somewhat less than this because *investment is crowded out at D. The trade balance improves*.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210804201000.png)
