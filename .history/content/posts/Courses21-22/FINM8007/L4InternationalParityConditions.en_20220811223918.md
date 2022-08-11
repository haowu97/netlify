---
title: "Lecture 4 International Parity Conditions"
date: 2022-08-09T13:54:04+08:00
draft: false

description: ""
upd: ""

tags: []
categories: ['FINM8007']
---

Learning Objectives

- To explain the derivation of forward exchange rates and the size of **forward premiums and discounts**
- To examine the connection between international **money markets** and the foreign exchange market
- To discuss the concept of **interest rate parity** and its influence in the foreign exchange market

<!--more-->

## 1. Forward Exchange Quotes

A **forward rate** is an exchange rate quoted today for settlement at some future date.

- The forward exchange agreement states the rate of exchange at which a foreign currency will be bought or sold forward at *a specific date in the future (typically 30, 60, 90, 180, 270 or 360 days)*

The forward rate is calculated by adjusting the current spot rate by a **forward points**

$$
\text{forward rate} = \text{spot rate} \pm \text{forward points}
$$

Example:

| Spot rate USD/AUD            | 0.6695 – 0.6700  |
| ---------------------------- | ---------------- |
| 3 month forward points       | -0.0040 – 0.0038 |
| 3 month forward rate USD/AUD | 0.6655 – 0.6662  |

1. bank buys AUD/sells USD three months forward at USD 0.6655 per AUD1, and
2. bank sells AUD/buys USD three months forward at USD 0.6662 per AUD1

## 2. Forward Margin

Forward margin is either a **discount or a premium** over the spot rate.

The **forward margin** (FM) can be quoted in points or in annual percentage terms. To convert **points** to **annual percentages** use the following formulas:

- For indirect quotes:

$$ 
\text{FM}=\left[\frac{\text { Spot }}{\text { Forward }}-1 \right] \times \frac{360}{\text { days }} \times 100\%
$$

- For direct quotes:

$$ 
\text{FM}=\left[\frac{\text { Forward }}{\text { Spot }}-1 \right] \times \frac{360}{\text { days }} \times 100\%
$$

Example:

| Spot rate USD/AUD            | 0.6695 – 0.6700  |
| ---------------------------- | ---------------- |
| 3 month forward points       | -0.0040 – 0.0038 |
| 3 month forward rate USD/AUD | 0.6655 – 0.6662  |

The **forward margin on the US\$ (bank sell US\$)** in per cent per annum terms would be:

$$
\text{FM}= \frac{0.6695-0.6655}{0.6655} \times \frac{360}{90} \times 100\% = +2.4 \% 
$$

The positive sign indicates that the bank sells the US\$ forward at a premium of 2.4\% p.a. 
- it takes 2.4\% more A\$’s to get a US$ at the 90-day forward rate.

**Practice** (Semester 1 -- Review Question, 2021) Part D [ii]: Assume that the **domestic currency is the Australian dollar (AUD)**. Explain clearly how you would compute the forward margin associated with an n-day US dollar (USD) forward contract. Assume that 0 < n ≤ 360, the spot rate is S AUD per USD (AUD/USD), the forward rate is F AUD/USD and these rates are strictly positive. Quote your forward margin in annual percentage terms.

**Answer**:

(Direct quote) Forward margin (in annual percentage terms) = (F/S – 1) x (360/n) x 100.

**Practice** (Semester 1 -- Mid, 2021): Part A [ii] Assume that you are a currency trader of forward exchange contracts in Germany. You observe the following spot and forward quotes for the United States dollar (USD) against the Euro (EUR):

| Spot rate (USD per EUR)             | USD/EUR 1.1760 |
| ----------------------------------- | -------------- |
| 1-month forward rate (USD per EUR)  | USD/EUR 1.1904 |
| 9-month forward rate (USD per EUR)  | USD/EUR 1.1927 |
| 12-month forward rate (USD per EUR) | USD/EUR 1.1977 |

What are the **forward premiums or discounts** on the EUR? Explain and show your working clearly and completely. Give your final answers in annual percentage terms. [10 marks/ 50 marks]

**Solution**:

1-month forward premium on EUR = (1.1904/1.1760 – 1) x 360/30 x 100 % = 14.69387755 % = 14.69%

9-month forward premium on EUR = (1.1927/1.1760 -1) x 360/270 x 100 % = 1.893424036 % = 1.89%

12-month forward premium on EUR = (1.1977/1.1760 – 1) x 100% = 1.845238095 % = 1.85 %

**Practice** (Semester 1 -- Previous Final, 2021) Part A [ii] Assume that you are a currency trader of forward exchange contracts in **France**. You observe the following spot and forward quotes for the United States dollar (USD) against the Euro (EUR):

| Spot rate (USD per EUR)             | USD/EUR 1.1760 |
| ----------------------------------- | -------------- |
| 3-month forward rate (USD per EUR)  | USD/EUR 1.1804 |
| 6-month forward rate (USD per EUR)  | USD/EUR 1.1827 |
| 12-month forward rate (USD per EUR) | USD/EUR 1.1877 |

What are the **forward premiums or discounts** on the EUR? Explain and show your working clearly and completely. Give your final answers in annual percentage terms.

**Solution**:

3-month forward premium on EUR = (1.1804/1.1760 – 1) x 360/90 x 100 % = 1.49659864 % = 1.50%

6-month forward premium on EUR = (1.1827/1.1760 -1) x 360/180 x 100 % = 1.139455782 % = 1.14%

12-month forward premium on EUR = (1.1877/1.1760 – 1) x 100% = 0.994897959 % = 0.99 %

---

**Practice** (Semester 1 -- Mid, 2021): Part B Assume that you trade forward contracts involving the United States dollar (USD) against the Australian dollar (AUD) in Australia. The forward margins on the AUD are available in the table below. What are the **forward premiums or discounts on the USD**? Explain and show your working clearly and completely. Give your final answers in annual percentage terms. [20 marks/ 50 marks]

| Length of forward contract | **Forward margin on AUD** per annum |
| -------------------------- | ----------------------------------- |
| 30-day contract            | -22%                                |
| 60-day contract            | -7%                                 |
| 180-day contract           | 9%                                  |
| 270-day contract           | 12%                                 |

**Solution**:

Let, Forward rate = F(USD/AUD), Spot rate = S(USD/AUD).

30-day forward contract: (F/S -1) x 12 = -0.22 → F/S = 11.78/12

30-day forward premium on the USD = (S/F -1) x 12 = (12/11.78 – 1) x 12 = 2.64/11.78 = 22.41086587 % = 22.41 %

60-day forward contract: (F/S-1) x 6 = -0.07 → F/S = 5.93/6

60-day forward premium on the USD = (S/F - 1) x 6 = (6/5.93 – 1) x 6 = 0.42/5.93 = 7.082630691 % = 7.08 %

180-day forward contract: (F/S-1) x 2 = 0.09 → F/S = 1.045

180-day forward margin on the USD = (S/F – 1) x 2 = (1/1.045 -1) x 2 = -0.09/1.045 = - 8.612440191 % = - 8.61% (discount)

270-day forward contract: (F/S – 1) x 360/270 = 0.12 → F/S = 1.09

270-day forward margin on the USD = (S/F -1) x 360/270 = (1/1.09 -1) x 360/270 = -32.4/294.3 = -11.00917431% = -11.01% (discount)

**Practice** (Semester 1 -- Previous Final, 2021) Part B: Assume that you trade forward contracts involving the United States dollar (USD) against the Australian dollar (AUD) in Australia. The forward margins on the AUD are available in the table below. What are the forward premiums or discounts on the USD? Explain and show your working clearly and completely. Give your final answers in annual percentage terms.

| Length of forward contract | Forward margin on AUD per annum |
| -------------------------- | ------------------------------- |
| 30-day contract            | -18%                            |
| 90-day contract            | -5%                             |
| 120-day contract           | 9%                              |
| 180-day contract           | 12%                             |

**Solution**:

Let, Forward rate = F(USD/AUD), Spot rate = S(USD/AUD)

30-day forward contract: (F/S -1) x 12 = -0.18 → F/S = 0.985

30-day forward premium on the USD = (S/F -1) x 12 = (1/0.985 – 1) x 12 = 0.18/0.985 = 18.27411168 % = 18.27 %

90-day forward contract: (F/S-1) x 4 = -0.05 → F/S = 0.9875

90-day forward premium on the USD = (S/F - 1) x 4 = (1/0.9875 – 1) x 4 = 0.05/0.9875 = 5.063291139 % = 5.06 %

120-day forward contract: (F/S-1) x 3 = 0.09 → F/S = 1.03

120-day forward margin on the USD = (S/F – 1) x 3 = (1/1.03 -1) x 3= -0.09/1.03 = - 8.737864078 % = - 8.74% (discount)

180-day forward contract: (F/S – 1) x 2 = 0.12 → F/S = 1.06

180-day forward margin on the USD = (S/F -1) x 2 = (1/1.06 -1) x 2 = -0.12/1.06 = -11.32075472% = -11.32% (discount)


## 3. Interest Rate Parity (IRP)

The foreign exchange market is in equilibrium when deposits of all currencies offer the same rate of return, which is called **interest rate parity**.

$$
1+\left(i^{\$} \times \frac{n}{360}\right) = \left[1+\left(i^{\text{FX}} \times \frac{n}{360}\right)\right] \times \frac{S^{\text{FX/\$}}}{F_{n}^{\text{FX/\$}}}
$$

To calculate the forward rate

- *Banks are continually re-setting forward rates* as spot rates and interest rates change.
- The correct forward rate for a foreign currency (FX) against the dollar for a period of $ n $ days is:

$$
F_{n}^{\text{FX/\$}}=S^{\text{FX/\$}} \times \frac{\left[1+\left(i^{\text{FX}} \times \frac{n}{360}\right)\right]}{\left[1+\left(i^{\$} \times \frac{n}{360}\right)\right]}
$$

**Interest rate parity** exists when the forward discount or premium is equal to, but opposite sign to, the difference in the national interest rates for securities of similar risk and maturity (ignoring transaction costs)

$$
\begin{aligned}
i^{\$} &= i^{\text{FX}} + \text{Forward Magin}
\\
-(i^{\text{FX}} - i^{\$}) & =   \text{Forward Magin} 
\\
&=  \left[\frac{S^{\text{FX/\$}}}{F_{n}^{\text{FX/\$}}}-1 \right] \times \frac{360}{\text { days }} \\
&=  \left[\frac{F^{\text{\$/FX}}}{S_{n}^{\text{\$/FX}}}-1 \right] \times \frac{360}{\text { days }}
\end{aligned}
$$

Interest rate parity theory provides the linkage between foreign exchange markets and international money markets

---

Size of the forward margin is determined by the **interest rate differential** between the two countries.

Banks set the forward margin to equalize the **covered borrowing costs** and **investment returns** across countries
- If not an arbitrage opportunity exists


Forward premium reflects lower interest rates
- For the country with lower interest rates (USA), their currency is at a premium in the forward market
- It is more expensive to buy the USD through a forward contract today than through a spot contract today
- This is to counteract the advantage of borrowing the USD at low interest rates

**Practice** (Semester 1 -- Review Question, 2021) Part D [i]: What is meant by “interest rate parity”? Explain clearly. If the spot rate for US dollars (USD) against the Australian dollar (AUD) is USD/AUD 0.95 and 30-day interest rates are 2.0 per cent per annum in the USA and 7.25 per cent per annum in Australia, what 30-day forward rate would interest rate parity dictate? Give your final answer in terms of how many US cents per AUD. Assume that Australia is the domestic country.

**Solution**:

**Interest rate parity** means that the cost of borrowing (return from investing) off-shore after covering the exchange rate risk equals the cost of borrowing (return from investing) on the domestic market.

Forward rate = USD/AUD 0.95 x (1 + 0.02 x 30/360) / (1 + 0.0725 x 30/360) = USD/AUD 0.94586871.

94.59 US cents per AUD.

**Practice** (SQ6): Refer to the slide with the heading “To calculate the forward rate” in your lecture slides titled “The forward market and international parity conditions”. **Prove that the formula on that slide is correct by using the usual assumption of no arbitrage (“All arbitrage opportunities are exhausted”)**. For the sake of consistency with the notation on that slide, assume that the domestic currency (DC) is the Australian dollar ($) and the foreign currency (FC) is denoted as “FX”.

Show your working clearly by using both direct and indirect quotes.

**Solution**:

![](img/L4InternationalParityConditions.en_2022-08-09-18-34-04.png)

![](img/L4InternationalParityConditions.en_2022-08-09-18-35-08.png)