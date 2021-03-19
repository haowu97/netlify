---
title: "Liquidity Management"
date: 2021-03-17T21:17:53+08:00
lastmod: 2021-03-18T21:17:53+08:00
draft: false

description: ""
upd: "Many CFOs consider decisions about corporate liquidity to be among the most important decisions they make; to a large extent, they view their job as being able to find a way to fund investments proposed by the CEO"

tags: ['Notes']
categories: ['Corporate Finance']

math: true
---

Keynes(1936)General Theory

- If financial markets work as well as we typically assume they do, firms' liquidity decisions would be irrelevant (MM)
- If financial markets contain frictions, liquidity decisions are important

## Cash Balances Over Time

Cash Balances of Large Corporations have increased over time

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210316230211.png)

Source Almeida, Campello, Cunha and Weisbach( 2013)

Explanations for the increase in cash

- Cash ratios increase because **firms' cash flows become riskier**
- In addition, firms change: They hold fewer inventories and receivables and are **increasingly R\&D intensive**
- Aside: Whenever there is a time trend in firms' behavior, one usually has to distinguish the hypothesis that "the **nature** of firms change over time" from "the **behavior** of a given firm changes”

**Thinking: Is the cash ratio a leading variable in the business cycle?**

Average cash ratios by firm size quintile from 1980 to 2006

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316235205.png)

Average cash ratios by idiosyncratic risk

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316235329.png)

Average cash ratios by R\&D

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316235345.png)

Much of the cash is held abroad

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210316235403.png)

With the increasing number of multinational companies, multinational companies tend to keep more cash in different countries due to **cross-border capital flow taxes**.

## Payout Versus Retention of Cash

In perfect capital markets, once a firm has taken all positive NPV investments, it is indifferent between saving excess cash and paying it out(MM (1961) Payout Irrelevance)

- If a firm has already taken all positive-NPV projects, any additional projects it takes on are zero or negative-NPV investments
- Rather than waste excess cash on negative-NPV projects, a firm can use the cash to purchase financial assets
- In perfect capital markets, buying and selling securities is a zero-NPV transaction, so it should not affect firm value
- Thus, with perfect capital markets, the retention versus payout decision is irrelevant

With market imperfections, there is a tradeoff: Retaining cash can reduce the costs of raising capital in the future, but it can also increase taxes and agency costs

### The traditional explanations for retaining cash (besides taxes)

The transaction costs motive: Keynes' (1936)

- A firm short of liquid assets has to raise funds in the capital markets, liquidate existing assets, reduce dividends and investment, renegotiate existing financial contracts, or some combination of these actions.
- The fixed costs of accessing outside markets induce the firm to raise funds infrequently, and to use cash and liquid asset holdings as a buffer.
- As a result, for a given amount of net debt, there is an optimal amount of cash, and cash is not simply negative debt.

The precautionary motive, generated form information costs in the form of:

- **Adverse selection** in financial markets: Information asymmetries make it harder to raise outside funds (Pecking order Myers and Majluf, 1984 )
- **Managerial agency costs** associated with the use of debt: High leverage firms find it difficult and expensive to raise additional funds (asset substitution/ overinvestment problem (Jensen and Meckling (1976), and underinvestment problem Myers (1977))

Agency costs of managerial discretion over the use of cash. Managers may hold cash to pursue their own objectives at shareholder expense
- Management may hold excess cash simply because it is risk averse. More entrenched management would therefore be more likely to hold excess cash because it can avoid market discipline.
- Management may accumulate cash to have more flexibility to pursue its own objectives, like in Jensen's FCF hypothesis

The financing hierarchy theory (pecking order theory)

- Interpret cash as equity (accumulated internal CF) 
- Allow for adverse selection in financial markets
- Equity is first and last as a source: internal and external 
- There is no optimal amount of cash precisely because there is no optimum level of debt

All four explanations to some extent rely on the idea that external finance is costly, because of:
- Transaction costs 
- Asymmetric information
- External Monitoring

If you account for corporate taxes as the cost of holding cash, the first three theories suggest a trade off and a target cash holdings, while the last does not.

### Do firms have target cash levels?

The first step in investigating whether firms have target cash levels is to examine whether cash holdings revert to the mean

Basic Strategy: see if cash is mean reverting

Advanced strategy: define target and see if cash changes depend on relative position with respect to target in previous year

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210316202509.png)

Opler, Pinkowitz, Stulz, and Williamson (1999)

If there is an optimal cash ratio, then the beta will be close to -1. Finally, the coefficient is larger than -1.

Imperfect adjustment might be consistent with a "pecking order theory" of cash

Alternatively, it might still be consistent with a "trade-off theory" of cash, under which firms have an optimal cash level, if firms do rebalance their cash holdings albeit infrequently, due to adjustment costs.

## Cash flow sensitivity of cash

Almeida, Campello, and Weisbach (2004) 

**Cash flow sensitivity of cash**: the fraction of incremental cash flows(profit) that is retained by the firm as additional cash.

Financial constrained: have difficulty in raise money, but not necessarily close to bankruptcy, e.g. start-ups firms.

- If $ \rho<\rho_{o} $ a firm is unconstrained in the sense that it can finance the shock ex-post. However, there is still dilution of original investors 
- If $ \rho>\rho_{o} $ a firm is constrained in the sense that it cannot finance the shock ex-post Financial constraints are measured by the wedge between expected payoff and pledgeable income, $ \rho-\rho_{o} $. 

Confusing concept：

- Financial constraints: the capital that firm can access, which is the boundary of financial constrained.
- Financial distressed: have too many debt and  close to bankruptcy.

If external financing is costly:

- Unconstrained firms ( $\rho_O >\rho$ ) invest at the first-best level, so incremental cash flows do not have any real effects on the firm’s investments
- Financially constrained firms ($\rho_O <\rho$) will choose to allocate additional 
    cash flows to increase their investments both today and in the future, so 
    cash holdings to finance future incremental investment should increase 
    with their cash flows.

Notice that an increase in A will only lead to an increase in cash for unconstrained firms (when $ \rho>\rho_{o} $ ).

Use  the following regression strategy to estimate cash flow sensitivity of cash

$$
\Delta \text{Cash Holdings} = \alpha+\beta \Delta \text{Cash Inflow}
$$

Use payout ratio to identify whether it's a financial constrained firm.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210319101727.png)

This provide support to the idea that the cost of external finance plays a big part in cash management.

Consequently, the fraction of cash retained by a firm from incremental cash flows reflects management’s own view as to whether the firm is likely to face financial constraints in the future. Thus cash flow sensitivity of cash can measure financial constraints to some extent.

## Holding Cash Versus Building Debt Capacity

Acharya, Almeida, and Campello (2007)

Can the firm save liquidity by borrowing less at date 0 and holding debt 
capacity for date 1?

- By issuing debt today the firm transfers value from future states with high cash flows to the present. 
- By subsequently hoarding cash, the firm channels funds into all future states, including those in which cash flows and debt values are low. 

In other words, issuing risky debt and keeping the proceeds in the cash account is equivalent to transferring resources from future states with high cash flows into future states with low cash flows

On the flip side, saving/building debt capacity over time is equivalent to transferring resources into future states with high cash flows. **But debt capacity does not hedge against low cash flow states**.

**Cash is not equivalent to negative debt because for a constrained firm cash offers hedging against future low cash flow states while debt does not**.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210318193548.png)

So cash is a way of transferring funds from good to bad states of the world.

The optimal financial policy in this context is to transfer financing capacity from state $ \lambda $ (where it is plentiful and less valuable) to state $ 1-\lambda( $ where it is scarce and valuable).

This goal can be accomplished by increasing the amount of dateo borrowing, and using the excess liquidity in state $ 1-\lambda $ to make (long-term) debt payments.

Cash savings thus allow the firm to transfer financing capacity from good to bad states of the world.

Clearly, any asset that makes payments to the firm in state $ \lambda $ will perform a similar role

### Hedging through derivatives

Suppose that the firm has access to a derivative that makes state contingent payments by $ y_{\lambda} $ and $ y_{1-\lambda} $

If the firm can buy an unlimited amount of exposure to the derivative, for a given investment $I$ it can set
$$
y_{\lambda}=\left(\rho-\rho_{0}\right) I
$$
For which it makes in state $ \lambda $ a payment of $ y_{\lambda} $.

### The tradeoff between investing and hedging

In practice finding such a derivative is very difficult. And hedging requires collateral so 100% hedging is hardly ever possible (Rampini, Sufi, Vishwanathan (2012)).

Collateral constraints link the availability of financing and risk management. More specifically, if firms must have sufficient collateral to cover both future payments to financiers and future payments to hedging counterparties, there is a trade-off between financing and risk management.

This tradeoff implies that when firms’ current net worth is sufficiently low, the financing needs for investment override the hedging concerns.

Firms pledge as much as possible to finance investment, or be forced to downsize less, leaving no room for risk management.