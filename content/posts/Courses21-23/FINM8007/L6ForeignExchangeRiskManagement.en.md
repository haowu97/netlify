---
title: "Lecture 6 Foreign Exchange Risk Management"
date: 2022-08-13T12:10:08+08:00
draft: false

description: ""
upd: ""

tags: []
categories: ['FINM8007']
output: word_document
---

Learning Objectives:

- To consider the **risks** associated with international trade and investment
- To distinguish between the **three major foreign exchange exposures**
- To analyze the **measurement and management** of foreign exchange exposures
- To explain a range of **risk management techniques** for transaction exposure

<!--more-->



Risks in International Trade and Investment

- Foreign exchange risk
- Political/ Transfer risk
- Credit risk
- Transport risk

**Foreign exchange exposure** is a measure of the potential for a firm’s profitability, net cash flow and market value to change because of **unexpected changes in exchange rates**.

**Categories** of Foreign Exchange Exposure

- Transaction Exposure
- Operating/ Economic exposure
- Translation/ Accounting Exposure

## 1. Transaction Exposure

The potential for a **change in the value of outstanding foreign exchange payments and receipts** due to **exchange rate changes prior to settlement**. Transactions can be of either a current or capital nature.

**Examples**:

- Import of goods on credit with prices quoted in foreign currency.
- Receipt of dividends from off-shore subsidiaries

### 1.1 Measurement of Transaction Exposure

Measuring the transaction exposure of a firm requires calculation of the **net amount of future payments/revenues in each foreign currency**.

Determine the overall risk associated with this exposure. This can involve assessment of currency variability based on standard deviations and currency correlations.

### 1.2 Management of Transaction Exposure

Companies can manage transaction exposure by:

- Remaining unhedged
- Using contractual hedges
  - Money market hedge
  - Forward exchange contract
  - Option contract

~~Comparison of Strategies~~

- ~~How do the different strategies perform?~~
  - ~~Remain unhedged~~
  - ~~Forward exchange contract~~
  - ~~Money market hedge~~
  - ~~Foreign currency option~~
- ~~Is cost of hedging the only factor to consider?~~
- ~~Choice depends on:~~
  1. ~~Cost outcome~~
  2. ~~Exchange rate expectations~~
  3. ~~Company risk profile~~
  4. ~~Management required~~

~~Why Hedge?~~

- ~~Traders trade - that is what they do best - they are not currency speculators~~
- ~~Reduction in risk of future cash flows improves the planning capability of the firm~~
- ~~Where the cost of hedging is not excessive normal business prudence would suggest hedging~~
- ~~Hedging costs must be factored into the cost of the deal~~
- ~~If the profitability of the deal is doubtful after hedging costs are factored in - perhaps the deal is not worthwhile?~~

#### 1.2.1 Unhedged Strategy

**Advantages**:

- Can take advantage of favorable exchange rate movements
- Saving in costs associated with contractual risk management techniques

**Disadvantages**:

- Losses associated with unfavorable exchange rate movements
- Loss of planning capability

#### 1.2.2 Forward Exchange Contracts

Hedging transaction exposure by a forward contract is achieved by selling or buying foreign currency receivables or payables forward.

- **For account receivable**: Lock the price today to sell foreign currency in the future by taking a short position in a forward contract.
- **For account payable**: Lock the price today to buy foreign currency in the future by taking a long position in a forward contract.

Foreign currency payment is priced at the forward rate when the contract is written.

Cash flows take place at the future date.

Subsequent movements in the exchange rate will not affect the contract, i.e., foreign exchange risk is eliminated.

**Advantages**:

- Eliminates risk of unfavorable exchange rate movements
- Known payment/ receipt from Day 1

**Disadvantages**:

- Cannot benefit from favorable exchange rate movements

#### 1.2.3 Money Market Hedge

Money market hedge is achieved by borrowing or lending the present value of foreign currency receivables or payables, thereby creating offsetting foreign currency positions.

**For receivables**:

|                                      | **Time 0**                                                                                                                                         |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Borrow foreign currency              | $+PV(FX) = \frac{FX}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}$                                                                           |
| Transfer loan into domestic currency | $+S^{\text{DC/FX}} \times \frac{FX}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}$                                                            |
| Invest domestic currency             | $-  S^{\text{DC/FX}} \times \frac{FX}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}$                                                          |
|                                      | **Time T**                                                                                                                                         |
| Pay the loan with the receivable     | $-FX$                                                                                                                                              |
| **Receive the investment**           | $+  FX \times S^{\text{DC/FX}} \times \frac{\left(1+i^{\text{DC}} \times \frac{n}{360}\right)}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}$ |

**For payables**:

|                                     | **Time 0**                                                                                                                                         |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Borrow domestic currency            | $+\frac{FX}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}  \times S^{\text{DC/FX}}$                                                           |
| Transfer loan into foreign currency | $+\frac{FX}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}$                                                                                    |
| Invest foreign currency             | $-\frac{FX}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}$                                                                                    |
|                                     | **Time T**                                                                                                                                         |
| Pay the payable with the investment | $-FX$                                                                                                                                              |
| **Cost of the loan **               | $+  FX \times S^{\text{DC/FX}} \times \frac{\left(1+i^{\text{DC}} \times \frac{n}{360}\right)}{\left(1+i^{\text{FX}} \times \frac{n}{360}\right)}$ |

Recall **interest rate parity**:

$$
F_{n}^{\text{DC/FX}}=S^{\text{DC/FX}} \times \frac{\left[1+\left(i^{\text{DC}} \times \frac{n}{360}\right)\right]}{\left[1+\left(i^{\text{FX}} \times \frac{n}{360}\right)\right]}
$$

**If the interest rate parity is holding, forward contract and money market hedge are equivalent.**

**Advantages**:

- Eliminates risk of unfavorable exchange rate movements

**Disadvantages**:

- Cannot benefit from favorable exchange rate movements
- Credit risk associated with forex investment
- Need to raise funds on Day 1 rather than when bill is due

#### 1.2.4 Foreign currency options

An option conveys the right, but not the obligation, to buy/sell a currency.

- **Call option**: Right to purchase a foreign currency.
- **Put option**: Right to sell a foreign currency.

Price of option = Premium (e.g. 0.5% of contract value)

**Strike/exercise price** (Pe): price at which option can be exercised.

Option does not lock in the exchange rate → more flexible.

Option pricing

- Sellers/Writers of options carry all the risk
- Option price/premium is set to cover the possible cost of option being exercised.
- Option value = intrinsic value + time value

Intrinsic Value of Option

- Comparison of Strike Price (Pe) with Current Market Price (Pc)
- If Pc is “more favorable” than Pe, the option is out-of-the-money → zero intrinsic value
- If Pc is “less favorable” than Pe, the option is “in the-money” → positive intrinsic value

**For receivable**: Enter a put option on the foreign currency.

- If the foreign currency depreciates, option allow the company to sell foreign currency at exercise price. 
- If currency appreciates, the firm can choose not to exercise the option, which means sets a floor for the company receive.

**For payable**: Enter a call option on the foreign currency.

- If the foreign currency appreciates, option give the firm right to buy the foreign currency at exercise price.
- If the foreign currency depreciates, the company won't exercise the option, which sets a ceiling for the domestic currency payment.

**Advantages**:

- Can take advantage of favorable exchange rate movements while protected from unfavorable changes

**Disadvantages**:

- Premium to be paid up-front
- More complex than a forward contract

**Example**:

An Australian importer of recorded music has a payment of £200,000 to make in 90 days. Relevant market information:

| Spot rate:                | £/ AUD 0.4090-0.4100 |
| ------------------------- | -------------------- |
| 90 day forward rate:      | £/ AUD 0.4110-0.4120 |
| 90 day AUD interest rate: | 6.0% p.a.            |
| 90 day £ interest rate:   | 8.0% p.a.            |
| Call option strike rate:  | £/ AUD 0.4120        |
| Option premium:           | 0.5%                 |

What is the foreign exchange risk?

- Risk of £ appreciating before payment is due.

What can the Australian importer (company) do in response to the foreign exchange risk?

- Company may choose to remain unhedged
  - Take on risk of £ appreciating
- If they choose to hedge, they may use:
  - the forward market
  - the spot and money markets
  - the options market

**1）Remain unhedged**

Creates transaction risk since £ may **appreciate** against the AUD over the 90 day period:

- If spot in 90 days is £/ AUD 0.4 - goods will cost $500,000

However, £ may **depreciate** so company would be better off:

- If spot in 90 days is £/ AUD 0.43 - goods will cost only $465,116.28

But this amount is uncertain.

**2）Hedge in the forward market**

Australian importer of recorded music with payment of £200,000 due in 90 days

- Buy £200,000 forward at £0.4110
- Known import payment of AUD 486,618.00 (£200,000/ 0.4110) to be paid in 90 days
- **Cost of forward cover** = (0.4090 – 0.4110)/ 0.4110 x 360/ 90 = -1.95% p.a.
- £ trading at a discount in the forward market

Spot rate prevailing at maturity is irrelevant except in terms of opportunity cost/benefit. For example:

- If £ appreciates to £ 0.40
  - Spot payment would be AUD 500,000
  - AUD 13,382 ( 500,000 - 200,000/ 0.4110 ) benefit from forward cover
- If £ depreciates to £ 0.42
  - Spot payment would be AUD 476,190.4
  - Would have been AUD 10,427.53 ( 200,000/ 0.4110 - 476,190.4 ) better off unhedged

**3）Hedge in the money market**

Hedge by matching the expected import payment with a foreign currency asset.

- Need to **create a £200,000 asset** to mature on Day 90
- Therefore, borrow AUD’s, convert to £’s on the spot market and invest for 90 days
- When £ investment matures use proceeds to pay import bill
- On Day 90 also repay AUD loan – this AUD payment is **the cost of the money market hedge**

To calculate how many AUD’s to borrow:

1. First find the PV of £200,000: PV = £200,000/[1 + (r x n/360)] = £200,000/[1 + 0.08 x 90/360)] = £196,078.43
2. To buy £196,078.43 spot at £/AUD0.409 need to borrow AUD 479,409.37 today
3. Cost of repaying AUD 479,409.37 in 90 days at the borrowing cost of 6% p.a.: **Cost on Day 90** = AUD 479,409.37 x 1.015 = AUD 486,600.51

| Actions           | Day 1                                        | Day 90                                                          |
| ----------------- | -------------------------------------------- | --------------------------------------------------------------- |
| Import market     | Write contract                               | Pay £ 200,000 import bill using proceeds of sterling investment |
| AUD Money market  | Borrow AUD 479,409.37 at 6% p.a. for 90 days | Repay AUD loan, Cost = AUD 486,600.51                           |
| Spot Forex Market | Sell AUD/ buy £196,078.43                    |                                                                 |
| £ Money Market    | Invest £196,078.43 at 8% p.a. for 90 days    | £ investment matures generating £ 200,000                       |

**4）Hedge in the options market**

Premium has to be paid today= £200,000 x 0.005 / 0.4090 = AUD2,444.99

Value of premium in 90 days = 2,444.99 x 1.015 = AUD2,481.66

The option guarantees a maximum cost on Day 90 of:

1. Import payment = £200,000/ £0.412 = AUD 485,436.89
2. Option premium = AUD 2,481.66
3. **Cost = Import payment + Option premium** = AUD 487,918.56

At date of expiry:

- If £ appreciates e.g. AUD1 = £0.40
- Cost of AUD 500,000 on spot market
- Option will be exercised.
- It is **in-the-money** since Pe gives a lower cost than Pc

At date of expiry:

- If £ depreciates e.g. AUD1 = £0.43
- Cost of AUD 465,116.28 on spot market (plus premium)
- Option will be allowed to lapse.
- It is **out-of-the-money** since Pe gives a higher cost than Pc

Interpretation of graph:

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208150920328.png)

- Break even rate = £200,000/AUD487,918.56 = £0.4099
- Loss beyond the strike rate compared with the no hedge position = premium
  - Option not used as spot rate is more favorable
- Profit below breakeven rate compared with the no hedge position
  - Option used as strike rate is more favorable

Comparison of Strategies

- Remain unhedged: Day 90 cost uncertain
- Forward exchange contract: Day 90 cost = AUD 486,618.00
- Money market hedge: Day 90 cost = AUD 486,600.51
- Foreign currency option: Day 90 maximum cost = AUD 487,918.56, but potential for cost to be lower

---

**Practice** (Semester 1 -- Review Question, 2021) Question 6: Assume that the domestic currency is the Australian dollar (AUD). BHP-Billiton (an **Australian-based multinational**) has a **Canadian subsidiary** (Anglo Potash Limited), which pays a dividend to the parent company (based in Australia) each year. *A dividend of 25 million Canadian dollars (CAD) has been declared now and will be paid to BHP-Billiton 90 days later.* BHP-Billiton is trying to decide how to manage the foreign exchange risk associated with the dividend. The currently available data are given below: 

| Spot rates (CAD per AUD)           | CAD/AUD 0.9428 – 0.9431 |
| ---------------------------------- | ----------------------- |
| 90-day forward rates (CAD per AUD) | CAD/AUD 0.9471 – 0.9478 |
| 90-day CAD interest rate           | 8.0% per annum (p.a.)   |
| 90-day AUD interest rate           | 6.0% p.a.               |

Based on the data, explain and calculate how BHP-Billiton could use a **forward exchange contract and a money market hedge** to hedge the foreign exchange risk. Explain your answers clearly and completely. Give your final answers in AUD.

**Solution**:

**Forward market**: BHP-Billiton can lock in the account receivable at the forward rate of CAD/AUD 0.9478. This guarantees revenue of AUD (25 million/0.9478) = AUD 26,376,872.76 90 days later.

**Money market hedge**: This technique matches the account receivable with an account payable. BHP-Billiton Limited would borrow CAD today and repay the loan in 90 days with the CAD 25 million revenue.

Present Value (PV) of CAD 25 million = CAD 25 million/(1 + {0.08 x 90/360}) = CAD (25 million/1.02)

Sell CAD (25 million/1.02) spot at CAD/AUD 0.9431 = AUD 25 million/(1.02 x 0.9431) = AUD (25 million/0.961962)

These funds are now available to the company and therefore can be valued at the company’s opportunity cost of capital (6.0% p.a.). The value of these funds in 90 days is:

Future Value (FV) of the funds = AUD (25 million/0.961962) x {1 + (0.06 x 90/360)} = AUD 26,378,380.85

This amount represents the AUD value of the CAD 25 million revenue in 90 days’ time.

---

**Practice** (Semester 1 -- Review Question, 2021) Question 7: AIC Mines Limited (an **Australian-based multinational corporation**) has a **Canadian subsidiary** (Intrepid Mines Limited), which pays a dividend to the parent company (based in Australia) each year. *A dividend of 10 million Canadian dollars (CAD) has been declared now and will be paid to AIC Mines Limited 120 days later.* If AIC Mines Limited wants to hedge against the uncertainty associated with the dividend and lock in the Australian dollar (AUD) value of the dividend, explain and show clearly and completely with the data below how AIC Mines Limited can use the **option hedge**: 

| Spot rate (CAD per AUD)     | CAD/AUD 0.9251        |
| --------------------------- | --------------------- |
| 120-day option strike price | CAD/AUD 0.9600        |
| 120-day option premium      | 2%                    |
| 120-day CAD interest rate   | 4.5% per annum (p.a.) |
| 120-day AUD interest rate   | 3.3% p.a.             |

**Solution**:

Buy a put option on the CAD at the strike rate of CAD/AUD 0.9600

Cost of option (**option premium**) is currently AUD 10 million x 0.02 ÷ 0.9251 = AUD 200,000/0.9251

If AIC Mines Limited exercises the option:

Minimum revenue (note that CAD 10 million is an account receivable/asset) 120 days later

= AUD [10 million/0.9600 – FV of option premium]

= AUD [10 million/0.9600 – 200,000/0.9251 x (1 + 0.033 x 120/360)]

= AUD 10,198,095.70

However, there is potential for the revenue to be higher if AUD depreciates (CAD appreciates).

---

**Practice** (SQ8): ABC Equipment Company (an **Australian-based company**) manufactures and sells outdoor playground equipment throughout the world. On August 1st, it **sold** a small playground complex to the City of Nagasaki in Japan at a price of Japanese Yen (JPY) 2 million, with payment due in 90 days. The company obtains the following quotes in the market:

| Spot rate (JPY per Australian Dollar (AUD)) | JPY/AUD 85          |
| ------------------------------------------- | ------------------- |
| 90-day forward rate                         | JPY/AUD 83.75       |
| Option strike rate                          | JPY/AUD 86          |
| Option premium                              | 1%                  |
| 90-day JPY interest rates                   | 2% per annum (p.a.) |
| 90-day AUD interest rate                    | 8% p.a.             |

What are the different ways to lock in the AUD value of JPY 2 million? Show calculations and explain **the advantages and disadvantages of each way**. Which do you recommend, and why?

**Solution**:

1. Forward hedge: guarantees revenue of **AUD 23,880.60 (2,000,000/83.75)** 90 days later.
2. Money market hedge: This technique matches the account receivable with an account payable. ABC would borrow JPY today and repay the loan in 90 days with the JPY 2M revenue. The funds in JPY are converted to AUD funds, which are now available to the company and therefore can be valued at the company’s opportunity cost of capital (8% p.a.). The value of these AUD funds in 90 days is **AUD 23,880.60 (2,000,000/(1 + 0.02 x 90/360) /85 x (1 + 0.08 x 90/360))**. This amount represents the AUD value of the JPY 2M revenue in 90 days’ time.
3. Option hedge: If ABC exercises the option: Minimum revenue (note that JPY 2M is an account receivable/asset) 90 days later = **AUD 23,015.81 (2,000,000/86 - 2,000,000 x 0.01 / 85 x (1 + 0.08 x 90/360))**. However, there is potential for the revenue to be higher if AUD depreciates (JPY appreciates).

Evaluate the alternative ways on the basis of risk, revenue, exchange rate expectations and management involved in each of the hedging techniques.

Note: for detailed explanations of the advantages and disadvantages of each way, refer to the lecture slides.

---

**Practice** (Semester 1 -- Review Question, 2021) Question 8 Part B: Answer both parts [i] and [ii].

[i] Discuss and compare hedging transaction exposure using the **forward contract vs. money market** instruments. When do the alternative hedging approaches produce the same result?

[ii] Discuss and compare the costs of hedging via **the forward contract and the options contract**. What are the advantages of a currency options contract as a hedging tool compared with the forward contract?

**Solution**:

[i] Answer: Hedging transaction exposure by a forward contract is achieved by selling or buying foreign currency receivables or payables forward. On the other hand, money market hedge is achieved by borrowing or lending the present value of foreign currency receivables or payables, thereby creating offsetting foreign currency positions. If the **interest rate parity** is holding, the two hedging methods are equivalent.

[ii] Answer: There is no up-front cost of hedging by forward contracts. In the case of options hedging, however, hedgers should pay the **premiums** for the contracts up-front. The cost of forward hedging, however, may be realized ex post when the hedger **regrets** his/her hedging decision. 

Answer: The main advantage of using options contracts for hedging is that the hedger can decide whether to exercise options upon observing the realized future exchange rate. Options thus provide a hedge against **ex post regret** that forward hedger might have to suffer. In the case of options, hedgers can **eliminate the downside risk** while retaining the upside potential.

---

**Practice** (Semester 1 -- Final, 2021) Question 1 Part B: Woodside Petroleum (an **Australian-based multinational corporation**) has a **Canadian subsidiary** (Woodside Office Calgary), which either pays a dividend to the parent company or receives cash payments from the parent company each year.

The currently available data about the spot, forward, money, and options markets involving the Canadian dollar (CAD) and Australian dollar (AUD) are given below:

| Spot rates (CAD per AUD)                        | CAD/AUD 0.9452 – 0.9570      |
| ----------------------------------------------- | ---------------------------- |
| 90-day forward points                           | 20 – 23                      |
| 90-day CAD interest rates                       | 3.5% - 4.0% per annum (p.a.) |
| 90-day AUD interest rates                       | 2.5% - 3.0% p.a.             |
| 90-day AUD put option strike rate (AUD per CAD) | AUD/CAD 1.0869               |
| 90-day AUD put option premium                   | 1%                           |
| 90-day CAD put option strike rate               | AUD/CAD 1.0417               |
| 90-day CAD put option premium                   | 2%                           |

Based on the data, answer both parts [i] and [ii] below. Parts [i] and [ii] are independent of each other. **[80 marks/ 150marks]**

[i] *Suppose Woodside Office Calgary declares a dividend of CAD 3 million, which will be paid to Woodside Petroleum 90 days later*. Woodside Petroleum (based in Australia) is trying to decide how to manage the foreign exchange exposure associated with the dividend. Explain and calculate the various strategies to manage the foreign exchange exposure associated with the dividend. Explain your answers clearly and completely. Give your final answers in AUD.

[ii] *Suppose the parent company Woodside Petroleum needs to pay Woodside Calgary Office CAD 6 million 90 days later*. Discuss the various strategies to lock in the AUD cost of this payment. Which strategy do you think would be better for Woodside Petroleum? Explain your answers clearly and completely. Give your final answers in AUD.

**Practice** (PRACTICE QUESTIONS SET FIVE) Question 1: AT&T (a US based multinational) has a known cash payment of 50 million Swiss francs to be made to a Swiss supplier in 100 days. The company wishes to lock in the US dollar price of this payment today. Explain fully the procedure the company will use to obtain the best outcome assuming the currently available data:

| Spot rate                  | CHF/USD1.25   |
| -------------------------- | ------------- |
| 100-day forward rate       | CHF/USD1.2325 |
| 100-day USD interest rates | 7.0-9.0% p.a. |
| 100-day CHF interest rates | 4.0-6.0% p.a. |
| 100-day option strike rate | CHF/USD1.235  |
| Option premium             | 1%            |

Note: in money markets, two interest rates exist: a lending rate and a borrowing rate.

## 2. Operating/Economic exposure

Measures the change in the present value of the firm resulting from **changes in future operating cash flows** caused by unexpected exchange rate movements.

- It assesses the impact of exchange rate changes both on the firm’s operations and on the firm’s **competitive position**
- Can impact on firms that have no foreign currency positions

**Examples**:

- “Hills Industries reported a 22% jump in profit for the year to June. The company’s success was partly in moving production of its cheaper products to overseas factories”
- “When Woolworths outlaid A＄2.5 bn for Foodland’s NZ supermarkets last November, the NZ$ was trading at its highest level against the A＄ for 4 years. Since then the NZ＄ has slumped 14% against the A＄”

### 2.1 Measurement of Operating Exposure

Measuring the operating exposure of a firm requires forecasting and analyzing all the firm’s **future transaction exposures** together with the future exposure of all the firm’s competitors and potential competitors.

### 2.2 Management of Operating Exposure

- Low-cost production sites
- Flexible sourcing
- Market diversification
- Product differentiation
- Financial hedging

## 3. Translation/Accounting Exposure

Arises when a company has **assets and/or liabilities in any currency other than its accounting currency**.

**Translation (or restatement) of the various accounts** denominated in the foreign currency leads to a new accounting measurement of the domestic currency value of the foreign investment.

**Examples**: “When Woolworths outlaid A＄2.5 bn for Foodland’s NZ supermarkets last November, the NZ$ was trading at its highest level against the A＄ for 4 years. Since then the NZ＄ has slumped 14% against the A＄”

### 3.1 Measurement of Translation Exposure

Translation exposure is dependent on:

- The size and nature of foreign operations
  - integrated foreign entity
  - self-sustaining foreign entity
- The location of foreign operations
  - high inflation environment?
  - volatile exchange rate?
- Accounting methods used
  - The current rate method
  - The temporal method

### 3.2 Management of Translation Exposure

Majority of companies do not hedge translation exposure. If they do, can use:

- Currency swaps
- Balance sheet hedge

