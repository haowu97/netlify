---
title: "Explaining Exchange Rates: An Asset Approach"
date: 2021-07-31T21:17:53+08:00
lastmod: 2021-08-01T21:17:53+08:00
draft: false

description: ""
upd: "Interest rate parity"

tags: ['Notes']
categories: ['International Finance']

math: true
---

## The Demand for Foreign Currency Assets

*Factors* that influence the return on assets determine the demand for those assets.

**(Nominal) Rate of return**: the percentage change in value that an asset offers during a time period.

- The annual return for ＄100 savings deposit with an interest rate of 2% is ＄100 x 1.02 = ＄102, so that the rate of return = (＄102 – ＄100)/＄100 = 2%.

**Real rate of return**: inflation-adjusted rate of return, 

- which represents the additional amount of goods & services that can be purchased with earnings from the asset.
- The real rate of return for the above savings deposit when inflation is 1.5% is 2% – 1.5% = 0.5%. After accounting for the rise in the prices of goods and services, the asset can purchase 0.5% more goods and services after 1 year.
- if prices are fixed, the inflation rate is 0% and (nominal) rates of return = real rates of return.

Besides the rates of return, two other important factors that influence the demand of deposit/currency:

1. **Risk** of holding assets also influences decisions about whether to buy them.
2. **Liquidity** of an asset, or ease of using the asset to buy goods and services, also influences the willingness to buy assets.

But for now, *assume that risk and liquidity of currency deposits in foreign exchange markets are essentially the same*, regardless of their currency denomination. 

We therefore say that *investors are primarily concerned about the rates of return on currency deposits*. 

Rates of return that investors expect to earn are determined by 

1. *interest rates* that the assets will earn
2. *expectations* about appreciation or depreciation

A currency deposit’s **interest rate** is the amount of a currency that an individual or institution can earn by lending a unit of the currency for, say, a year.

The *rate of return for a deposit in domestic currency* is the interest rate that the deposit earns. 

To compare the *rate of return on a deposit in domestic currency with one in foreign currency*, consider

1. the interest rate for the foreign currency deposit
2. the expected rate of appreciation or depreciation of the foreign currency relative to the domestic currency.

### Exchange Rates and Asset Returns

Suppose also that the dollar interest rate is 10% per year while the euro interest rate is 5% per year. This means a deposit of ＄1.00 pays ＄1.10 after a year while a deposit of €1 pays €1.05 after a year. Which of these deposits offers the higher return?

The answer can be found in **five steps**.

1. Use today’s dollar/euro exchange rate to figure out the dollar price of a euro deposit of, say, € 1. If the exchange rate today is ＄1.10 per euro, the dollar price of a € 1 deposit is just ＄1.10.
2. Use the euro interest rate to find the amount of euros you will have a year from now if you purchase a €1 deposit today. You know that the interest rate on euro deposits is 5% per year. So at the end of a year, your € 1 deposit will be worth € 1.05. 
3. Use the exchange rate you expect to prevail a year from today to calculate the expected dollar value of the euro amount determined in Step 2. Since you expect the dollar to depreciate against the euro over the coming year so that the exchange rate 12 months from today is ＄1.165 per euro, you expect the dollar value of your euro deposit after a year to be ＄1.165 per euro * € 1.05 = ＄1.223.
4. Now that you know the dollar price of a € 1 deposit today (＄1.10) and can forecast its value in a year (＄​1.223), you can calculate the expected *dollar* rate of return on a euro deposit as (1.223 - 1.10)/1.10 = 0.11, or 11 percent per year.
5. Since the dollar rate of return on dollar deposits (the dollar interest rate) is only 10 percent per year, you expect to do better by holding your wealth in the form of euro deposits. 
    1. Despite the fact that the dollar interest rate exceeds the euro interest rate by 5% per year, 
    2. the euro’s expected appreciation against the dollar gives euro holders a prospective capital gain that is large enough to make euro deposits the higher-yield asset.

If you compute the **expected dollar return on euro deposits** using the exact five-step method we described before introducing the simple rule, you'll find that it actually equals

$$
\left(1+R_{\euro}\right)\left(E_{\$ / \euro}^{e} / E_{\$ / \euro}\right)-1
$$

This exact formula can be rewritten, however, as

$$
R_{\epsilon}+\left(E_{\$ / \epsilon}^{e}-E_{\$ / \epsilon}\right) / E_{\$ / \epsilon}+R_{\epsilon} \times\left(E_{\$ / \epsilon}^{e}-E_{\$ / \epsilon}\right) / E_{\$ / \epsilon}
$$

As is usually the case, the product $R_{\epsilon} \times\left(E_{\$ / \epsilon}^{e}-E_{\$ / \epsilon}\right) / E_{\$ / \epsilon}$​​ is a small number.

We simplify the analysis (or formula) by saying that the dollar rate of return on euro deposits approximately equals 

1. the interest rate on euro deposits
2. plus the expected rate of appreciation of euro against dollar (or the rate of depreciation of the dollar against the euro)

$$
R_{\epsilon}+\left(E_{\$ / \epsilon}^{e}-E_{\$ / \epsilon}\right) / E_{\$ / \epsilon}
$$

## Equilibrium in the Foreign Exchange Market

### Interest Rate Parity

The foreign exchange market is in *equilibrium* when deposits of all currencies offer the same expected rate of return, which is called**(uncovered) interest parity**.

- Interest parity implies that deposits in all currencies are equally desirable assets.
- Interest parity implies that *arbitrage* in the foreign exchange market is not possible.

Interest parity says:

$$
R_{\$}=R_{\epsilon}+\left(E_{\$ / \epsilon}^{e}-E_{\$ / \epsilon}\right) / E_{\$ / \epsilon}
$$

Why should this condition hold? Suppose it didn't.

- Suppose $R_{\$}>R_{\epsilon}+\left(E_{s / \epsilon}^{e}-E_{\$ / \epsilon}\right) / E_{\$ / \epsilon}$
- Then no investor would want to hold euro deposits, driving down the demand and price of euros.
- Then all investors would want to hold dollar deposits, driving up the demand and price of dollars.
- The dollar would appreciate and the euro would depreciate, increasing the right side until equality was achieved (for a given $ \left.E_{\$ / \epsilon}^{e}\right) $ :

### The Equilibrium Exchange Rate

Depreciation of the domestic currency today lowers the expected rate of return on foreign currency deposits. Why?

- When the domestic currency depreciates, the initial cost of investing in foreign currency deposits increases, thereby lowering the expected rate of return of foreign currency deposits.

Appreciation of the domestic currency today raises the expected return of deposits on foreign currency deposits. Why?

- When the domestic currency appreciates, the initial cost of investing in foreign currency deposits decreases, thereby raising the expected rate of return of foreign currency deposits.

Figure: The Relation Between the Current Dollar/Euro Exchange Rate and the Expected Dollar Return on Euro Deposits

- Given $E_{\$ / \epsilon}^{e}=1.05$​ and $R_{\epsilon}=0.05$​, an appreciation of the dollar against the euro raises the expected return on euro deposits, measured in terms of dollars.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803094646.png)

Figure: Determination of the Equilibrium Dollar/Euro Exchange Rate

- Equilibrium in the foreign exchange market is at point 1, where the expected dollar returns on dollar and euro deposits are equal.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803095151.png)

## Interest Rates, Expectations, and Equilibrium

### The effects of changing interest rates

An increase in the interest rate paid on deposits denominated in a particular currency will increase the rate of return on those deposits. This leads to an appreciation of the currency.

- Higher interest rates on dollar-denominated assets cause the dollar to appreciate.
- Higher interest rates on euro-denominated assets cause the dollar to depreciate.

Figure: Effect of a Rise in the Dollar Interest Rate

- A rise in the interest rate offered by dollar deposits from $ R_{\$}^{1} $ to $ R_{\$}^{2} $ causes the dollar to appreciate from $ E_{\$^{\prime} \epsilon}^{1}( $ point 1$ ) $ to $ E_{\$ / \epsilon}^{2}( $ point 2$ ) $.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803095520.png)

Figure: Effect of a Rise in the Euro Interest Rate

- A rise in the interest rate paid by euro deposits causes the dollar to depreciate from $ E_{\$ / \euro}^{1} $​ (point 1) to $ E_{\$ / \euro}^{2}$​(point 2). (This figure also describes the effect of a rise in the expected future $\$ / \euro$​ exchange rate.)

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210803095700.png)

### The effects of changing Expectations

If people expect the euro to appreciate in the future, then the expected rate of return on euros therefore increases (for given interest rates).

- An **expected appreciation** of a currency leads to an **actual appreciation today** (but not necessarily to the full degree) 
- An **expected depreciation** of a currency leads to an **actual depreciation today** (but not necessarily to the full degree)