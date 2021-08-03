---
title: "Exchange Rate"
date: 2021-04-29T21:17:53+08:00
lastmod: 2021-04-30T21:17:53+08:00
draft: false

description: ""
upd: ""

tags: ['Notes']
categories: ['International Finance']

math: true
---

## Nominal exchange rate

*Exchange rates*: The price of one nation’s currency in terms of another currency. Namely, the rate at which a person can trade the currency of one country for the currency of another.

- *Base currency* per *Quote currency*, the number of Base currency needed to buy 1 Quote currency.

**Textbook notation**: 

`AUD1.5/USD` or `AUD1.5 = USD 1`

- the number of AUD needed to buy 1 USD, or number of AUD you can buy with 1USD
- you need 1.5 AUD to buy 1 USD, or you can buy 1.5AUD with 1 USD

`¥93.17/A$` or `A$0.0107/¥`: 

- How much can be exchanged for one dollar? ¥93.17/A$
- How much can be exchanged for one yen? A$0.0107/ ¥

However, **industry notation**:

- USD/AUD → number of AUD needed to buy 1USD
- … yes, it can get confusing

### Exchange Rate Quotes

- *Direct quote/ (Price quote)*: units of domestic currency per unit of foreign currency; quoting domestic currency first (in the numerator)
- *Indirect quote/ (quantity quote)*: units of foreign currency per unit of domestic currency; quoting foreign currency first (in the numerator)

$$
Indirect = \frac{1}{Direct}
$$

### Exchange Rate Changes

*Appreciation/ depreciation*: value of a currency increases/decreases in terms of another currency, driven by **market forces**, e.g. in free float systems.

*Revaluation/ devaluation*: value of a currency is changed by the **government**, e.g. in fixed rate systems

A depreciated currency is less valuable, and therefore it can buy fewer foreign-produced goods that are denominated in foreign currency.

- A Honda costs `¥2,500,000 x $0.0107/¥ = $26,750`
- Less expensive than `$30,000 at $0.0120/¥`

A depreciated currency means that imports are more expensive and domestically-produced goods and exports are less expensive. 

- **A depreciated currency lowers the price of exports relative to the price of imports** (OR: raises the price of imports relative to the price exports). 
- The reverse holds under an appreciated currency.

#### Calculating exchange rate changes

Amount of currency appreciation/depreciation = (New value - Old value) / Old value 

【Example 1】Suppose the Canadian dollar devaluate against the euro: The exchange rate goes down from $ e_{1}=0.8 \frac{E U R}{C A D} $​ to $ e_{2}=0.72 \frac{E U R}{C A D} $​.

This is a devaluation by
$$
(e_2-e_1)/e_1 = \text{-10\%}
$$
【Example 2】If the Thai baht fell 17% against the US dollar, by how much has the USD appreciated against the baht?

Let $ e_{1}=\mathrm{USD} / \mathrm{THB} $, then $ \mathrm{THB} / \mathrm{USD}=1 / e_{1} $

Change in USD/THB is
$$
\left(e_{1}-e_{0}\right) / e_{0}=-17 \% \rightarrow e_{1}=-0.17 e_{0}+e_{0}=0.83 e_{0} 
$$
Change in THB/USD is
$$
\left(1 / e_{1}-1 / e_{0}\right) /\left(1 / e_{0}\right)=\left(e_{0}-e_{1}\right) / e_{1} 
\rightarrow \left(e_{0}-0.83 e_{0}\right) / 0.83 e_{0}=0.17 e_{0} / 0.83 e_{0}=0.2048
$$
The USD appreciated $ 20.48 \% $ relative to the Thai baht

Note: Change in USD/THB $\neq$ change in THB/USD!

## Real exchange rate

The *real exchange rate* is the rate of exchange for goods and services across countries. 

- In other words, it is the **relative value/price/cost of goods and services across countries**: the rate at which a person can trade the goods and services of one country for the goods and services of another
- For example, it is the dollar price of a European group of goods and services relative to the dollar price of an American group of goods and services:

$$
q_{U S / E U}=\left(E_{\$ / €} \times P_{E U}\right) / P_{U S}
$$

**The real exchange rate is a key determinant of how much a country**
**exports and imports**.

1. A *real depreciation* of the value of U.S. products means a fall in a dollar’s purchasing power of EU products relative to a dollar’s purchasing power of U.S. products.
    1. This implies that U.S. goods become less expensive and less valuable relative to EU goods.
    2. This implies that the value of U.S. goods relative to value of EU goods falls
    3. As a result, U.S. exports rise, and U.S. imports fall, and both of these changes **raise U.S. net exports**.
2. A *real appreciation* of the value of U.S. products means a rise in a dollar’s purchasing power of EU products relative to a dollar’s purchasing power of U.S. products.
    1. This implies that U.S. goods become more expensive and more valuable relative to EU goods.
    2. This implies that the value of U.S. goods relative to value of EU goods rises. 
    3. As a result, U.S. exports fall, and U.S. imports rise, and both of these changes **reduce U.S. net exports**.

## Foreign Exchange Markets

### Characteristics of the FX Markets

The volume of FX transactions has risen significantly of the last decades:

1. In April 1989, the average total value of global foreign exchange trading was close to \$600 billion per day.
2. In 2001 the daily volume of trading was \$1.2 trillion
3. In April 2010, the daily global value of foreign exchange trading had jumped to around \$4,000 billion.
4. In April 2013, average daily turnover is a mind-numbing \$​​​5.3 trillion. In three days foreign exchange turnover is sufficient to cover world trade in a year.

The most important marktet places are London, New York, Tokio, Frankfurt and Singapore.

They are highly interconnected this allows 24h trading except on the weekends.

This integration rules out the possibility of good arbitrage opportunies.

The exchange rate quoted in financial newspapers are for large transactions of over \$1 million.

**International financial transactions have risen substantial** over the past 45 years

- Reduced costs of communication and information
- Less capital controls
- More direct foreign investments by international corporations.
- New financial instruments
- More speculation
- Cross border capital flows have outnumbered crossborder trade flows
- The dominance of the US Dollar in international transactions

### Spot and Forward Rates

**Spot exchange rates**: The rate of a foreign-exchange contract for immediate delivery.

**Forward exchange rate**: The rate fixed today that is applicable to a financial transaction that will take place in the future.

- Forward dates are typically 30, 90, 180 or 360 days in the future.

Forward and spot exchange rates, while not necessarily equal, do move closely together.

*The future market drives the spot market, especialy FX swaps.*

#### Spot Contracts

Spot exchange: a contract for immediate exchange of currencies

How it works:

1. Trader 1 calls Trader 2 and asks for a price of a currency, say GBP
2. The *bid price* is the exchange rate at which Trader 2 is willing to buy GBP
3. The *ask (or offer) price* is the exchange rate at which Trader 2 is willing to sell GBP
4. The difference (*bid-ask spread*) generates profits for Trader 2/ brokers

The **bid-ask spread** (profit margin) on currency quotations is 

- positively influenced by order costs, inventory costs, and currency risk, 
- and negatively influenced by competition, and volume.

The spread for heavily traded currencies like the $, €, RMB, £, and ¥ are low because of their liquidity.

Often the **bid-ask spread** is quoted as a percentage term:
$$
\text{Percentage spread} = [(Ask – Bid) / Ask] \times 100
$$
In price quotation: The bid rate is always lower than the ask rate

【Example】If GBP is quoted at USD 1.8419-28/GBP 

- USD1.8419/GBP is the bid rate, USD1.8428/GBP is the ask rate
- Percentage spread = [(1.8428-1.8419) / 1.8428] x 100 = 0.049%

### Vehicle Currency and Cross-Rates 

**Vehicle currency**, a currency that is actively used in many international financial transactions around the world.

- U.S. Dollar primary vehicle currency (89% of all transactions)
- transaction costs of making markets in certain currencies

Exchange rate between two currencies, based on exchange rates between each of these currencies and the vehicle currency. 

A **cross exchange rate** reflects the amount of one foreign currency per unit of another foreign currency

- e.g. if 1 EUR = 1.47 USD and 1 SFR = 0.98 USD, what should be SFR/EUR? 
    - USD/EUR = 1.47USD/EUR and USD/SFR = 0.98USD/SFR
    - SFR/EUR = (1.47USD/EUR) / (0.98USD/SFR) = 1.5 SFR/EUR

$$
\begin{align}
\frac{C N Y}{A U D}&=\frac{C N Y}{U S D} \times \frac{U S D}{A U D} \\
&=\frac{C N Y}{U S D} \times 1 / \frac{A U D}{U S D}\\
&=6.7 \times \frac{1}{1.480}=¥ 4.527 / A \$
\end{align}
$$

#### Triangular Arbitrage

In **cross exchange rate equilibrium**: 
$$
CNY/AUD = CNY/USD× USD/AUD 
$$
or
$$
CNY/USD × USD/AUD × AUD/CNY = 1
$$
**Currency arbitrage**: profiting from exchange rate inconsistencies across money centers.

**Triangular currency arbitrage**: 

- involves three currencies
- keeps cross-rates in line with exchange rates quoted relative to a third currency

**How does it work?**

1. If *CNY/USD × USD/AUD × AUD/CNY < 1*, one of the three rates must increase
    1. The *currency in denominator is too low* relative to the currency in the numerator
    2. Buy USD with CNY, buy AUD with USD, or buy CNY with AUD
2. If *CNY/USD × USD/AUD × AUD/CNY > 1*, one of the three rates must decrease
    1. The *currency in denominator is too high* relative to the currency in the numerator
    2. Sell USD for CNY, sell AUD for USD, or sell CNY for AUD

【Example】Suppose exchange rates for AUD, USD, and CNY are AUD1.60/USD, CNY4.77/AUD, and USD0.14/CNY.

AUD1.60/USD × CNY4.77/AUD × USD0.14/CNY = 1.068 > 1 

1. If you sell 1 USD for 1.60 AUD
2. Then sell 1.60 AUD for 7.632 CNY ( = 1.60 x 4.77)
3. Then sell 7.632 CNY for 1.068 USD ( = 7.632 x 0.14)
4. You have earned 1.068 USD – 1 USD = 0.068 USD, or 6.8% of your initial investment

### Forward vs. Futures

**Forward contract**: The terms of a financial transaction that will take place in the future but are fixed today

**Futures contract**: A futures contract is the same as a forward contract except that it is *standardized* with respect to volume, currency, date of delivery.

【Example】

The spot rate is: 1.1152 EUR/USD
The forward quotation is: 13.941 EUR/USD
The forward rate is then:
$$
\mathrm{e}_{\$ / \euro}^{3 \mathrm{M}}=1.1152+13.941 / 10,000=1.1165941
$$

## Central Bank Reputations and Expectations

A nation’s official monetary authority, the *central bank* uses monetary policy to achieve price stability, set interest rates, or maintain a certain currency value.

Fiat money is no longer linked to an underlying asset, so 

- central banks play a crucial role in setting the risk associated with holding a currency.
- Risk depends on central bank’s ability to maintain price stability, target values, etc.
- Investors’ expectations of central bank behavior affect exchange rates

*Central bank independence*: avoid direct control by government officials that could use monetary policy for short-term political gains at the costs of long-term economic issues

- Non-independent central bank may be forced to monetize budget deficit by printing money to finance public sector spending
- E.g. Post WWI Germany, Zimbabwe

Independent central banks tend to have

- Lower inflation rates
- Higher economic growth

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210501212454.png)

Example: New Zealand’s central bank was made independent in 1990: inflation dropped to 1.3% and cut government spending on welfare programs.

*Central Bank Interventions*: Official purchases or sales of currencies to influence local (domestic) currency.

*Unsterilized intervention*

- e.g. European Central Bank (ECB) wants to let USD/EUR depreciate → increase supply of EUR or increase demand for USD
- Buy USD in exchange for EUR (i.e. sell EUR for USD)
- However, EU money supply and therefore **inflation increases**

*Sterilized intervention*: **neutralize inflation**

- Open-market operations to keep money supply constant
- usually by buying or selling treasury securities
- e.g. ECB can reduce EUR supply by selling euro-denominated securities to public
- However, assumes public views euro-denominated securities as perfect substitutes for dollar-denominated securities, portfolio rebalancing can result in a null effect on exchange rates. 