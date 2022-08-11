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

# 1. Forward Exchange Quotes

A **forward rate**is an exchange rate quoted today for settlement at some future date.

- The forward exchange agreement states the rate of exchange at which a foreign currency will be bought or sold forward at *a specific date in the future (typically 30, 60, 90, 180, 270 or 360 days)*

The forward rate is calculated by adjusting the current spot rate by a **forward margin** (in points)

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


# Forward Margin

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


# Interest Rate Parity (IRP)

The foreign exchange market is in equilibrium when deposits of all currencies offer the same expected rate of return, which is called **interest rate parity**.

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