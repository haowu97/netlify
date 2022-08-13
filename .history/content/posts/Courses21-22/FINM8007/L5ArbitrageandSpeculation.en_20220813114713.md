---
title: "Lecture 5 Arbitrage and Speculation"
date: 2022-08-09T13:54:59+08:00
draft: false

description: ""
upd: ""

tags: []
categories: ['FINM8007']
output: word_document
---

Learning Objectives

- To discuss the consequences when *international parity conditions are violated*
- To analyze the process of **covered interest arbitrage**
- To examine how foreign currency **swaps** are used by investors and borrowers
- To consider the role of **speculators** in spot and forward markets

<!--more-->

## 1. Arbitrage and Speculation

Speculators and arbitrageurs **seek to profit** from trading in the market.

- They operate for their **own interest, without need or obligation** to serve clients or ensure a continuous market.
- A large proportion of speculation and arbitrage is conducted **on behalf of major banks** by dealers employed by those banks.

Arbitrage Transactions

- An arbitrageur takes advantage of opportunities for profit which arise from short-term price discrepancies between different markets
- There is no risk - buy and sell at the same time
- Arbitrage actions eliminate the price differentials

Speculative Transactions

- Speculators aim to make a profit by buying at a low price and selling at a higher price
- Entails risk since expectations may not be fulfilled
- ‘Short’ - sell before buying if expect asset price to fall
- ‘Long’ - buy prior to selling if expect asset price to rise

**Summary**:

|          | Arbitrage                                                   | Speculation                                         |
| -------- | ----------------------------------------------------------- | --------------------------------------------------- |
| Risk     | No                                                          | Yes                                                 |
| Profit   | Short-term price discrepancies in between different markets | Buying at a low price and selling at a higher price |
| Strategy | Buy and sell at the same time                               | Short or long                                       |

## 2. Foreign Currency Arbitrage

### 2.1 Covered Interest Arbitrage

Covered interest arbitrage (CIA):

- When **Interest Rate Parity** holds, the return from investing off-shore - on a covered basis - equals the return from investing on the domestic market. 
- Therefore, any funding advantage from investing where interest rates are higher is cancelled by the cost of buying forward cover.
- Because the spot and forward markets are not always in a state of equilibrium as described by IRP, the opportunity for arbitrage exists.
- The arbitrageur who recognizes this imbalance can *invest in the currency that offers the higher return on a covered basis*.

**Example**:

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208131051410.png)

Capital flow:
$$
i^{DC} = i^{\text{FC}} + \text{Forward Magin}
$$

To calculate the forward rate

$$
F_{n}^{\text{FX/\$}}=S^{\text{FX/\$}} \times \frac{\left[1+\left(i^{\text{FX}} \times \frac{n}{360}\right)\right]}{\left[1+\left(i^{\$} \times \frac{n}{360}\right)\right]}
$$

**Practice** (Semester 2 -- Mid, 2019)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208122055130.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208122058249.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208122104364.png)

**Practice** (Semester 2 -- Mid, 2020)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130902001.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130902650.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130903425.png)

**Practice** (SQ7)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130904242.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130905391.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130905737.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130906988.png)

**Practice** (Semester 1 -- Review Question, 2021) Question 3: Suppose that you are a trader in Japan and you see the following quotes on your screen:

| Spot exchange rate       | 86.85 Japanese Yen (JPY) per Australian dollar (AUD) |
| ------------------------ | ---------------------------------------------------- |
| 30-day forward rate      | 87.41 JPY per AUD                                    |
| 30-day AUD interest rate | 4% per annum (p.a.)                                  |
| 30-day JPY Interest rate | 1% p.a.                                              |

Assuming that you have JPY 1 million, can you make a profit (in JPY) with these quotes? Show your working clearly.

**Solution**:

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208130906182.png)

You can make a profit of JPY 8,969.39 from CIA in AUD.

### 2.2 Uncovered Interest Arbitrage

**Uncovered interest arbitrage (UIA)** exists when investors *borrow in currencies exhibiting relatively low interest rates and convert the proceeds into currencies which offer higher interest rates*.

The transaction is **“uncovered”** because the investor *does not sell the investment proceeds forward*, thus remaining exposed to the risk of the currency depreciating.

**Example**:

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208131016035.png)

- **Risk** is that the **NZD may depreciate** against the Yen over the 12 months.

## 3. Foreign Currency Speculation

### 3.1 Speculate in the Spot Market

**Example**:

Hans Schmidt is willing to risk his money based on his view of currencies. Assume Hans believes that the NZD will depreciate against the USD over the next month from the current spot of USD/NZD 0.55.

- Spot: NZD1 = USD 0.55
- Expected one month spot: NZD1 = USD 0.52
- USD 30 day interest rate = 1% pa
- NZD 30 day interest rate = 8% pa

Hans will go ‘short’ on NZD’s.

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208131109983.png)

### 3.2 Speculate in the Forward Market

**Example**:

Hans can also speculate using the forward market by going ‘short’ on NZD’s.

- 30 day forward: NZD1 = USD 0.5450
- Expected future spot: NZD1 = USD 0.5200

**Actions**:

1. Buy a forward contract today to sell NZD1m at USD 0.5450. Guaranteed revenue of USD545,000. No funds required today.
2. If expectation is correct, on day 30 sell USD545,000 at spot of USD0.52 generating revenue of NZD 1,048,077 on day 30 and a profit of NZD 48,077.
3. If expectation is incorrect and spot NZD is higher than USD 0.5450, will make a loss.

## 4. Foreign Exchange Swaps

An Australian company needs to borrow AUD1m. for 180 days. The company considers two alternate sources of funds:

1. Borrowing AUD1m. from an Australian bank
2. Borrowing USD’s from a US bank and swapping into AUD’s

To borrow in the USA the company will:

1. Borrow USD’s for 180 days
2. Sell the USD’s/buy AUD’s on the foreign exchange market at today’s spot rate
3. The company now has the funds it needs for 180 days
4. Cover the risk of a USD appreciation over the period of the loan by buying the USD’s on the forward market today for delivery in 180 days

| 180 day AUD interest rate | 9% p.a. |
| ------------------------- | ------- |
| 180 day USD interest rate | 3% p.a. |
| USD/AUD spot rate         | 0.5762  |
| 180 day forward margin    | -0.0130 |
| 180 day forward rate      | 0.5632  |


Cost of forward cover (margin) on USD funds

= (spot – forward) / forward x 360 / days (indirect quote of US$)

= (0.5762 - 0.5632) / 0.5632 x 360 / 180

= 4.6% p.a.

Total cost of USD funds

= USD interest rate + cost of forward cover

= 3% + 4.6% = 7.6% p.a.