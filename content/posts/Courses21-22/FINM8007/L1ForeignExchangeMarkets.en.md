---
title: "Lecture 1 Foreign Exchange Markets"
date: 2022-08-02T14:33:35+08:00
draft: false

description: ""
upd: ""

tags: []
categories: ['FINM8007']
output: word_document
---

Learning Objectives

- To examine the **functions** performed by the foreign exchange market
- To describe the roles of the main **participants** in the foreign exchange market
- To analyze how **spot rates** are quoted and interpreted
- To derive **cross rates** and the opportunity for triangular arbitrage

<!--more-->

## 1. Functions of the foreign exchange market

- Transfer **purchasing power** between countries
  
  - Trade: export and import

- Obtain or provide **credit** for international trade
  
  - Facilitate lending and borrowing, especially for Multinational
    Corporations (MNCs).

- Minimize **exposure** to exchange rate **risk**
  
  - Hedge through forwards, options

**Practice** (Semester 2 -- Mid-semester, 2019)

What are the three functions of the foreign exchange market? Explain clearly. [10 marks/ 50 marks]

## 2. Market Participants

The foreign exchange market consists of two tiers,

- the inter-bank or **wholesale** market (86%)
- the client or **retail** market (14%)

Four broad categories of participants

1. Bank and non-bank foreign exchange **dealers**
   1. Dealers act as **market makers**, willing to buy or sell
      currencies without a counterpart to unload the "inventory".
   2. Dealers profit from buying currencies at a **bid** price and
      then reselling them at an **offer or ask** price.
   3. **Bid-ask spreads** represent the liquidity.
   4. Dominated by **large international banks**.
2. **Individuals and firms**
   1. Importers, exporters, portfolio investors, Multinational
      Enterprises (MNEs), tourists and others use the foreign exchange
      market to facilitate execution of commercial or investment
      **transactions**.
   2. Some of these participants use the market to **hedge** foreign
      exchange rate risk.
3. Foreign exchange **brokers**
   1. Foreign exchange brokers are agents who *match buy and sell
      orders between dealers*.
   2. Do not set prices or carry inventories of currencies.
   3. Charge a small **commission**.
   4. Maintain instant access to hundreds of dealers worldwide via
      open lines, with separate lines for different currencies, spot
      and forward rates.
   5. Electronic broking now dominates.
4. **Central banks**
   1. Central banks use the market to acquire or spend their country's
      **official currency reserves**, as well as to influence the
      price at which their own currency trades.
   2. They may act to **support the value of their currency** because
      of their government's policies or commitments with other central
      banks.
   3. Earning a profit is not a motive.

**Practice** (Semester 1 -- Review Questions, 2021)

What is the difference between the retail or client market and the wholesale or interbank market for foreign exchange? Who are the market participants in the foreign exchange market?

## 3. Spot Quotes

~~Transactions in the Foreign Exchange Market (FEM)~~

- ~~A **spot transaction** requires almost immediate delivery of foreign currency.~~
- ~~A **forward transaction** requires delivery of foreign currency at some future date.~~
- ~~A **swap transaction** is the simultaneous purchase and sale of a given amount of foreign currency for two value dates.~~

The **spot exchange rate** is the quoted price for foreign currency to be delivered at once, or in two business days for inter-bank transactions.

A foreign exchange **quote** is a statement of willingness to **buy/bid** or **sell/offer/ask** at an announced rate.

**Direct and Indirect Quotes**

- A **direct quote** is a home currency price of a unit of a foreign currency
  - HKD 5.353/AUD is a direct quote in Hong Kong
- An **indirect quote** is a foreign currency price in a unit of the home currency
  - HKD 5.353/AUD is an indirect quote in Australia
  - AUD 0.1868/HKD is a direct quote in Australia and an indirect quote in Hong Kong.

Interpreting market quote:

$$
HKD/AUD \quad 5.0700 - 5.3530
$$

Quote shows the number of Hong Kong dollars the bank will buy and sell against one Australian dollar, i.e. the price of one AUD in terms of HKD's.

1. First currency = **quoted or terms currency** is HK dollar
2. Second currency = **unit or commodity currency** is AUD
3. **Bid price**: First number = rate at which the bank buys the unit currency (AUD) and sells the terms currency (HKD)
4. **Ask price**: Second number = rate at which the bank sells the unit currency (AUD) and buys the terms currency (HKD)

**Rip-off rule**: The bank rips the customer off by expecting the customer to pay more and giving the customer less in return.

Transaction 1: A student from Hong Kong wishes to sell HKD 25k. to cover living expenses in Australia.

Transaction 2: An Australian tourist wishes to buy HKD 25k. to cover holiday expenses in Hong Kong.

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152207985.png)

**Simplified rule**: 

- **up the bid and multiply**
- **down the ask and divide**

**EXAMPLE**: Converting currencies using spot rates

A dealer is quoting the AUD/GBP spot rate as 1.5060 - 1.5067. How would we:

1. Compute the proceeds of converting 1 million GBP.
2. Compute the proceeds of converting 1 million AUD.

**Answer**:

1. To convert 1 million GBP into AUD, we go "up the quote" (i.e.,from GBP in the denominator to AUD in the numerator). Hence,we would use the bid price of 1.5060 and multiply. 

$$
\text{1 million GBP x 1.5060 = 1,506,000 AUD}
$$

2. To convert 1 million AUD into GBP, we go "down the quote" (i.e.,from AUD in the numerator to GBP in the denominator). Hence, we would use the ask price of 1.5067 and divide.

$$
\text{1 million AUD / 1.5067 = 663,702.13 GBP}
$$

---

**Practice** (Semester 1 -- Review Questions, 2021) A Danish toy company has sold plastic blocks worth 500,000 Danish Krone (DKK) to a US distributor, who has to pay the toy company immediately in DKK. The US distributor, who has US dollars (USD), receives the following spot quote for DKK per USD (DKK/USD): DKK/USD 6.9100 - 6.9500. What is the USD cost of the plastic blocks to the US distributor? Show your working clearly.

**Solution**：

USD cost of the plastic blocks = USD 500,000/6.91 = USD 72,358.90

## 4. Cross Rates & Triangular Arbitrage

**Cross Rates**:

- The USD is the base currency for interbank dealing.
- Quotes for currencies not involving the USD are obtained by crossing with the USD
- Therefore a **cross rate** is an exchange rate that does not involve the USD.

**Cross rates with bid-ask spreads Rules**: for any currency

$$
A/B \quad Bid - Ask
$$

we have,

$$
\left(\frac{\mathrm{A}}{\mathrm{B}}\right)_{\text {bid }}=\frac{1}{\left(\frac{\mathrm{B}}{\mathrm{A}}\right)_{\mathrm{ask}}}
$$

$$
\left(\frac{\mathrm{A}}{\mathrm{C}}\right)_{\text {bid}}=\left(\frac{\mathrm{A}}{\mathrm{B}}\right)_{\text {bid}} \times\left(\frac{\mathrm{B}}{\mathrm{C}}\right)_{\text {bid}}
$$

$$
\left(\frac{\mathrm{A}}{\mathrm{C}}\right)_{\text {ask}}=\left(\frac{\mathrm{A}}{\mathrm{B}}\right)_{\text {ask}} \times\left(\frac{\mathrm{B}}{\mathrm{C}}\right)_{\text {ask}}
$$

**Whether we can make triangular arbitrage**:

**Method 1**:

$$
\left(\frac{\mathrm{A}}{\mathrm{B}}\right)_{\text {bid}} \times\left(\frac{\mathrm{B}}{\mathrm{C}}\right)_{\text {bid}} \times \left(\frac{\mathrm{C}}{\mathrm{A}}\right)_{\text {bid}} > 1 
$$

or

$$
\left(\frac{\mathrm{B}}{\mathrm{A}}\right)_{\text {bid}} \times\left(\frac{\mathrm{C}}{\mathrm{B}}\right)_{\text {bid}} \times \left(\frac{\mathrm{A}}{\mathrm{C}}\right)_{\text {bid}} > 1 
$$

**Method 2**: The implied cross rate falls outside of the real cross rate.

**Practice** (Short Quiz1)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152208982.png)

**Solution**:

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152209208.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152209431.png)

**Practice** (Semester 2 -- Mid-semester, 2019)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152210187.png)

**Solution**:

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152211568.png)

**Practice** (Semester 2 -- Mid, 2020)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152220688.png)

**Solution**:

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152213554.png)

**Practice** (Semester 1 -- Final, 2021) Consider the following bilateral spot exchange rates involving the Australian dollar (AUD), Canadian dollar (CAD), Euro (EUR), and United States dollar (USD):

- AUD per USD (AUD/USD) 1.2894-1.2981

- CAD per USD (CAD/USD) 1.1151-1.1207

- EUR per USD (EUR/USD) 0.7443-0.7592

- CAD per AUD (CAD/AUD) 0.9438-0.9545

- EUR per AUD (EUR/AUD) 0.6418-0.6460

- EUR per CAD (EUR/CAD) 0.6755-0.6810

Start with AUD 10,000. Can you identify **any positive arbitrage opportunities** with all these quotes? Assume that all the interest rates are zero. Explain and show your working clearly and completely. Give your final answers in AUD. [10 marks/ 150marks]

**Practice** (Semester 2 -- Mid, 2022) Part A: You are a trader in Sydney and currently observe the following exchange rates on the trading screen for the Australian dollar (AUD), Euro (EUR), and United States (US) dollar (USD):

| AUD per USD (AUD/USD) | 1.4531 – 1.4551 |
| --------------------- | --------------- |
| EUR per AUD (EUR/AUD) | 0.6744 – 0.6753 |
| EUR per USD (EUR/USD) | 0.9957 – 0.9961 |

Suppose that you have AUD 500,000 in your trading account and interest rates are 0. Can you identify any positive arbitrage opportunities (in AUD) by using these exchange rates? Explain and show your working clearly and completely. [20 marks/ 50 marks]

**Short Quiz 4**

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208152222304.png)