---
title: "Special Topic3 Anomalies in International Financial Markets"
date: 2022-10-25T15:37:46+08:00
draft: false

description: ""
upd: "Liquidity premium, value premium, and idiosyncratic volatility puzzle."

tags: []
categories: ['FINM8007']
output: word_document
---

## What drives the liquidity premium in the Chinese stock market?

North American Journal of Economics and Finance 54 (2020) 101088

Jiyoun An, Kin-Yip Ho, and Zhaoyong Zhang

### Background: liquidity in China

**The banking liquidity crisis and subsequent instability in the Chinese financial markets**: importance of liquidity in influencing market dynamics.

The Economist, 2013: “The impact of the sudden liquidity crunch in the overnight loans market on June 20 adversely affected the equity markets on June 24 and 25… The biggest daily loss in nearly four years”

July 2015: the China Security Regulatory Commission introduced **circuit breakers** to stabilize the situation.

China Daily, 2017: “Even though the Chinese government rectified the situation through the adoption of corrective measures subsequently, the issue of liquidity continues to weigh on the Chinese financial market”

<!--more-->

### Challenges of examining liquidity

**First challenge**: liquidity could be intimately related to other factors commonly known to influence asset pricing and return predictability in equity markets.

- Idiosyncratic volatility premium: linked to liquidity costs and biases. (Ang et al. 2009; Han and Lesmond, 2011)
- Liquidity, firm size and dividends: jointly significant in predicting returns. (Eun and Hung, 2007)
- Narayan and Zheng (2010) and Nartea et al. (2013): possible links between liquidity and other factors in the Chinese equity market.
  
Second challenge is the existence of **numerous liquidity measures**, which potentially **represent various aspects of market imperfection or embed different asset characteristics**, since these measures may use different information.

- participation costs, transactions costs, asymmetric information, imperfect competition, funding constraints, search costs

### Research questions

How are the dynamics of liquidity in the Chinese stock market linked to other driving forces of asset pricing and return predictability?

- Using a range of liquidity measures
- Decomposing the liquidity measure into several components (Hou and Loh, 2016)

### Data

Stock returns in Shanghai and Shenzhen A-share

Sample period: July 1995 ~ December 2015

Limiting our sample:

- Price, market value, book value, and return data for the subsequent three-year period should exist.
- Drop penny stocks with 3 RMB market values (too many penny stocks, thus use US 50 cents instead of USD 1)
- Drop extreme values
- CSMAR datasets are available from 1991, but we limit the sample from July 1995 to December 2015 due to lack of sufficient observations before 1995.

### Liquidity measures

Campbell, Lo, and MacKinlay (1997) define **liquidity** as “the ability to buy or sell significant quantities of a security quickly, anonymously, and with relatively little price impact.”

The bid-ask spread, trading size, and turnover are intuitive and heuristic measures.

Three monthly frequency **liquidity measures: Stocks with high values are highly illiquid**.

- AMIHUD: Amihud (2002) measure, the average ratio of the daily absolute return to the trading volume on that day

$$
\left|R D_{i, t}\right| / V O L D_{i, t}
$$

- PS: Pastor-Stambaugh measure, coefficient of a regression of a stock’s daily return in excess of the market index on the previous day’s signed volume, controlling for the previous day’s return
  - The idea is that trades in illiquid markets should generate **transitory deviations** between price and fundamental value.
- INVTO: **Inverse of turnover ratio** (the number of shares traded on a given day divided by the total number of shares outstanding)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290854502.png)

### Liquidity premium

**Fama-MacBeth (1973) cross-sectional regressions**

$$
R_{i, t+1}=a_{t}+b_{t} L I Q_{i, t}+\sum_{j=1}^{J} c_{t} X_{i, j, t}+\varepsilon_{i, t}
$$

The results indicate that **highly illiquid stocks based on AMIHUD and INVTO provide higher future returns**. It suggests that liquidity in the Chinese financial market is a critical variable in equity asset pricing.

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290855472.png)


The product of $LIQ$ and estimated coeffcient $b_t$ for each stock i at month t is the expected returns related to liquidity. The mean of the product across stocks at month t is the monthly **liquidity premium** (LP).

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290855206.png)

### Decomposition analysis


Hou and Loh (JFE 2016):

- Use decomposition analysis to quantify the marginal contributions of different explanations to asset pricing puzzles/anomalies
  - Hou and Loh (2016) applied it to the IVOL puzzle
- Method is equally applicable to examine how various asset
pricing anomalies can be explained by different variables.

Apply Hou and Loh (2016 JFE) approach to the liquidity premium puzzle

- Step 1: Cross-sectional regressions → Returns regressed against LIQUIDITY (LIQ) → LIQ coefficient
- Step 2: regress LIQ against Candidate explanation (CANDIDATE) →LIQ decomposed into 2 components

$$
L I Q_{i, t}=\phi_{t}+\delta_{t} S I Z E_{i, t}+\kappa_{i, t}
$$

- Decompose LIQ coefficient → compute fraction explained by CANDIDATE

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290857654.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290858601.png)

### Conclusion

The liquidity premium is statistically significant. 

The premium has not only remained persistent but also become more significant in recent years starting from 2011. 

- This result is in stark contrast to that in the US market, in which the premium is recently declining

**Decomposition approach**

- Amihud liquidity measure: size contributes 45–65% to the
liquidity premium.
- Turnover measure: idiosyncratic volatility accounts for at least 60% of the liquidity premium.
- Local factor (local market liquidity beta) more significant compared with the global factor.

**Implications** of these finding

- Liquidity-based strategies profitable
  - challenging to implement in practice.
- Implications for existing institutional reforms
  - Various measures to improve market efficiency (the relaxation of short-selling constraints and introduction of margin trading). 
  - **These reforms may be mostly ineffective**.


## Decomposing the value premium: The role of intangible information in the Chinese stock market

Emerging Markets Review 44 (2020) 100700

Kin-Yip Ho and Jiyoun An

### Introduction

**Value premium** (also known as the book-to-market effect), suggests that stocks with high book-to-market ratios provide higher average returns than those with low book-to-market ratios.

Two explanations:

- **Risk-based explanation**: the value premium essentially represents **compensation for systematic risk factors** in asset pricing.
- **Mispricing-based explanation**: market participants underestimate (overestimate) future earnings of firms that have high (low) book-to-market ratios.
  - **Arbitrage risk** impedes arbitrage activities and allows for the systematic mispricing
  - **Intangible information**: the component of its past return that is orthogonal to the firm's past accounting-based information (non-accounting related
information)
    - the value premium is higher in stocks with lower past intangible information (Daniel and Titman, 2006; Jiang, 2010)
    - investors overreact to stocks with high intangible information and overprice them

A unified explanation for its existence is yet to be proposed.

**Contribution**: a possible linkage between the arbitrage risk and intangible information.

**Idiosyncratic volatility**: the historical volatility of market model residuals.

- Used to measure **arbitrage risk**
- Be attributable to firm-specific news flows that extend **beyond accounting-related information**. (DeLisle et al., 2016 and Shi et al., 2016a, 2016b)

**Chinese stock market**:

- Increases in importance.
- A T + 1 trading rule and restrictions on short-selling and margin trading in the Chinese market impose **limits to arbitrage** → arbitrage risk is substantial
- High-quality accounting information about firms can be challenging to obtain → rely on non-accounting-related information more often

### Hypothesis

**Hypothesis I**. Intangible information and idiosyncratic volatility drive the value premium in the Chinese stock market.

- investors regard policy-related and **non-accounting-related information** to be more critical than accounting-related information (Wang et al., 2006)
- **arbitrage risk** could be significant in the Chinese stock market owing to the government policies on **trading restrictions** (the “T + 1” trading rule and other short-selling prohibitions)

**Hypothesis II**. The dynamics of idiosyncratic volatility is attributable in part to intangible information.

- idiosyncratic volatility can also be interpreted from the perspective of information flows (non-accounting-related information)

**Hypothesis III**. Intangible information is the main driver of the value premium from two channels:

- one, the **direct channel**, which measures the intangible information's direct impact on the value premium, and 
- two, the **indirect channel**, which measures the impact of intangible information on idiosyncratic volatility.

### Data

Stocks listed on the Shanghai and Shenzhen A-share markets from January 1995 to December 2015.

Monthly stock returns, share prices, market values, and accounting variables, such as book values

**Book-to-market ratio (BM)** is the ratio of the book value over the market value at the end of December of year t − 1.

**Intangible information (INTAN)** is estimated based on a cross-sectional regression of the past two-year log stock returns of each firm on the firms' two-year lagged log book-to-market ratio and two-year book returns.

- Tangible returns are the fitted values of the regression,
- and intangible returns (a proxy for INTAN) are the residuals

**Idiosyncratic volatility** is the standard deviation of the residuals after estimating the **Fama and French (1993) three-factor model** using the excess daily returns over the past month (for monthly frequency) or the past year (for annual frequency).

The information available in June of year t is used to predict the returns in July of t to June of t + 1: 

- BM in December of year t − 1;
- IVOL in June of year t; 
- and INTAN in December of year t − 1.

### Methodology

#### Examine the existence of the value premium

**Method 1: Sorting of returns on BM**

1. firms are ranked each year according to their BM ratio and are assigned to quintile portfolios based on their ranking
2. compare the average abnormal returns in each quintile.
3. if high BM stocks provide higher average returns, the highest BM quintile group would have higher average returns than those of the lowest group

A **drawback** of the sorting technique is that capturing the incremental roles of the factors influencing the value premium is difficult.

**Method 2: Cross-section regressions**

$$
\begin{array}{l}
R_{t+1}^{e i}=a_{t}+b_{t} B M_{i, t}+e_{t+1}^{i} \text { for each } t \\
\hat{b}=\frac{1}{T} \sum_{t=1}^{T} \widehat{b}_{t}
\end{array}
$$

When $\hat{b}$ is significantly positive, it suggests that higher $B M$ increases future abnormal returns.

**Fama–French abnormal returns** $R_{t+1}^{e i}$: residuals of the regression in which Raw returns at each firm are regressed on the Fama–French three factors.

#### Decomposition methodology

$$
\mathrm{BM}_{\mathrm{i}, \mathrm{t}}=\hat{\varphi}_{\mathrm{t}}+\hat{\delta}_{\mathrm{t}}^{1} \mathrm{INTAN}_{\mathrm{i}, \mathrm{t}}+\hat{\delta}_{\mathrm{t}}^{2} \mathrm{IVOL}_{\mathrm{i}, \mathrm{t}}+\hat{\mu}_{\mathrm{i}, \mathrm{t}}
$$

$$
\hat{\mathrm{b}}_{\mathrm{t}} \equiv \frac{\operatorname{Cov}\left[\mathrm{R}_{\mathrm{t}+1}^{\mathrm{e}}, \mathrm{BM}_{\mathrm{i}, \mathrm{t}}\right]}{\operatorname{Var}\left[\mathrm{BM}_{\mathrm{i}, \mathrm{t}}\right]}=\frac{\operatorname{Cov}\left[\mathrm{R}_{\mathrm{t}+1}^{\mathrm{e}}, \hat{\delta}_{\mathrm{t}}^{1} \mathrm{INTAN_{ \textrm {i } , \mathrm { t } } ]}\right.}{\operatorname{Var}\left[\mathrm{BM}_{\mathrm{i}, \mathrm{t}}\right]}+\frac{\operatorname{Cov}\left[\mathrm{R}_{\mathrm{t}+1}^{\mathrm{e}}, \hat{\delta}^{2}{ }_{\mathrm{t}}{\mathrm{IVOL}} \mathrm{i}, \mathrm{t}\right]}{\operatorname{Var}\left[\mathrm{BM}_{\mathrm{i}, \mathrm{t}}\right]}+\frac{\operatorname{Cov}\left[\mathrm{R}_{\mathrm{t}+1}^{\mathrm{ei}}, \hat{\varphi}_{\mathrm{t}}+\hat{\mu}_{\mathrm{i}, \mathrm{t}}\right]}{\operatorname{Var}\left[\mathrm{BM}_{\mathrm{i}, \mathrm{t}}\right]}
$$

$$
\hat{b}_{t} \equiv \hat{b}_{t}^{I N T A N}+\hat{b}_{t}^{\text {IVOL }}+\hat{b}_{t}^{R}
$$

### Empirical significance of the value premium

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290858950.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290859400.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290859156.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290957405.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290957920.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290958939.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210290959040.png)

$$
I V O L_{i, t}=\eta_{t}+\kappa_{t} I N T A N_{i, t}+\varsigma_{i, t}
$$

$$
IVOLEX_{i, t}=I V O L_{i, t}-\widehat{\kappa}_{t} INTAN_{i, t}
$$

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291002745.png)

### key findings

1. Based on portfolio sorts of abnormal returns on the BM ratio and cross-section regressions, **the significant presence of the BM effect** in the Chinese stock market can be observed.
2. The **single decomposition analysis** confirms that arbitrage risk and intangible information contribute to the value premium in the Chinese stock market. More specifically, intangible information can account for at least 50% of the value premium over different investment horizons.
3. The **multivariate decomposition analysis** indicates that compared with intangible information, idiosyncratic volatility does not significantly contribute to the value premium, which further confirms the **dominant role of intangible information**.
4.  Moreover, **INTAN also influences value effects indirectly through IVOL**. Once we fully account for the impact of INTAN on IVOL, the latter influences only less than half of the original IVOL on the BM effect.

### PRACTICE QUESTIONS

**Practice** (PRACTICE QUESTIONS FOR SPECIAL TOPICS) With reference to the article entitled “Decomposing the value premium: the role of intangible information in the Chinese stock market” by Ho and An (2020), explain and discuss **the factors contributing to the book-to-market effect in China’s stock market**.

According to Fama and French (1998, 2012), the book-to-market (BM) effect (otherwise known as the **value premium puzzle**) refers to the stylized fact that stocks with high BM ratios provide higher average returns in future compared with stocks with low BM ratios. Based on portfolio sorts of abnormal returns on the BM ratio (Table 2) and cross-section regressions (Table 3), Ho and An (2020) observe **the significant presence of the BM effect** in the Chinese stock market.

Further analysis based on Hou and Loh’s (2016) **single and multivariate decomposition analyses** in Tables 4, 5, and 7 of Ho and An (2020) suggest that **intangible information (INTAN) and arbitrage risk are two major factors** contributing to the BM effect.

**INTAN** (also known as non-accounting-related information) refers to information that is orthogonal or unrelated to past accounting-based information (Daniel and Titman, 2006; Jiang 2010). Ho and An (2020) measure INTAN by extracting the residuals from the cross-sectional regression involving the past stock returns of each firm on the firms’ lagged BM ratio and book returns. Depending on the length of investment horizons (which could range from 9 months to 2 years), INTAN is negatively correlated with BM and contributes at least 50% to the value premium in the Chinese stock market. More specifically, as shown in Table 4, for an investment horizon of 9 months, the estimated coefficient of INTAN is -0.126 (t-statistic = 4.772) in Stage 3 of the single decomposition analysis and INTAN contributes 64.8% to the value
premium.

The second factor, **arbitrage risk**, refers to the risk associated with arbitrage-related transactions; in practice, arbitrage is conducted by a smally group of traders, who could be worried about the fluctuations in their portfolio values (also called arbitrage risk). Idiosyncratic volatility (IVOL) measures the extent of arbitrage risk. Ho and An (2020) measure the IVOL by extracting the residual component from the Fama and French (1993) three-factor model involving the excess daily returns. The single decomposition results in Table 4 of Ho and An (2020) suggest that IVOL is negatively related to BM and contributes up to 49% to the value premium in China’s stock market.

Based on **multiple decomposition analysis** (Table 5), the estimated coefficient of IVOL does not appear to be significant and INTAN is the dominant contributor to the value premium in the Chinese stock market. In particular, when the investment horizon is one year, INTAN contributes about 67% to the value premium.

Further analysis of the **relationship between INTAN and IVOL** by Ho and An (2020) suggests that after considering the influence of INTAN on IVOL, IVOL does not seem to contribute substantially to the value premium. As illustrated in Table 7, the component of IVOL that excludes INTAN (**IVOLEX**) contributes about 24% to the value premium. This result could suggest that INTAN is the major driving force of the value premium in China’s stock market.

## Have we solved the idiosyncratic volatility puzzle?

Journal of Financial Economics 121 (2016) 167-194

Kewei Hou and Roger Loh

### Introduction

Ang, Hodrick, Xing, and Zhang (2006) , in a highly influential paper, document **a negative relation between idiosyncratic volatility and subsequent stock returns**.

- Puzzling because according to standard asset-pricing models (e.g. CAPM), non-systematic risk should not be priced (Fama and MacBeth, 1973)
- Or if priced, the relation should be positive (Merton, 1987; Hirshleifer, 1988). Investors with undiversified portfolios demand positive premium for holding stocks with high idiosyncratic risk.

Many papers try to explain the puzzle. But unclear which explanation is best or whether the puzzle is fully explained.

To date, there has been no comprehensive examination about which explanations best explain the puzzle.

**Hou and Loh’s (2016) contribution:** Provides a method to objectively quantify the incremental contribution of each existing reason that claims to explain the puzzle.

- Objective and agnostic approach
  - Most papers aim to remove the IVOL puzzle with their favorite key explanation. Hou and Loh (2016) treat each potential candidate explanation seriously, without favorites.
  - Most papers just aim to make the IVOL coefficient insignificant. Hou and Loh (2016) can **quantify** the fraction of the puzzle that a candidate explains.
- Hou and Loh (2016) pit existing explanations against one another
  - A common framework, standard sample, and fair horse race between explanations.
  - Existing papers usually do not consider competing explanations.
- Hou and Loh’s (2016) method can be used to evaluate any anomaly in asset-pricing.

**Candidate explanations**

1) Lottery Preference (Sections 2.2 and 3.3)
   1) Skewness (Barberis & Huang, 2008)
   2) Co-skewness (Chabi-Yo & Yang, 2009)
   3) Expected idiosyncratic skewness (Boyer, Mitton, & Vorkink, 2010)
   4) Maximum daily return (Bali, Cakici, Whitelaw, 2011)
   5) Retail-trading proportion (Han & Kumar, 2013)
2) Market Frictions (Sections 2.3 and 3.4)
   1) Return reversal effects (Fu, 2009; Huang, Liu, Rhee, & Zhang, 2009)
   2) Amihud (2002) illiquidity (Han & Lesmond, 2011)
   3) Zero-return measure (Han & Lesmond, 2011)
   4) Bid-ask spread (Han & Lesmond, 2011)
3) Others (Sections 2.4 and 3.5)
   1) Dispersion (Johnson, 2004)
   2) Average variance beta (Chen & Petkova, 2012)
   3) Standardized unexpected earnings (Wong, 2011; Jiang, Xu, & Yao, 2009)

### Decomposition methodology

Start from **Fama-MacBeth cross-sectional regressions** each month $t$ for all stocks $i$.

$$
R_{i t}=\alpha_{t}+\gamma_{t} I V O L_{i t-1}+\varepsilon_{i t}
$$

Let $Candidate$ be a candidate explanation. $Candidate_{i t-1}$ must be correlated with $I V O L_{i t-1}$ to explain the IVOL puzzle.

$$
I V O L_{i t-1}=a_{t-1}+\delta_{t-1} Candidate_{i t-1}+\mu_{i t-1}
$$

From above, we can decompose $I V O L_{i t-1}$ into 2 components, $\left(\delta_{t-1} Candidate_{i t-1}\right)$ and $\left(a_{t-1}+\mu_{i t-1}\right)$.

- First is the component of IVOL related to the candidate.
- Second is a residual component unrelated to the candidate.

The final step is to use the linearity of covariances to decompose the estimated $\gamma_{t}$ coefficient from $R_{i t}=\alpha_{t}+\gamma_{t} I V O L_{i t-1}+\varepsilon_{i t}$:

$$
\begin{aligned}
\gamma_{t}=& \frac{\operatorname{Cov}\left[R_{i t}, I V O L_{i t-1}\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]} \\
=& \frac{\operatorname{Cov}\left[R_{i t}, \quad\left(\delta_{t-1} \text { Candidate }_{i t-1}+a_{t-1}+\mu_{i t-1}\right)\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]} \\
=& \frac{\operatorname{Cov}\left[R_{i t}, \quad \delta_{t-1} \text { Candidate }_{i t-1}\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]} +\frac{\operatorname{Cov}\left[R_{i t}, \quad\left(a_{t-1}+\mu_{i t-1}\right)\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]} \\
=& \gamma_{t}^{C}+\gamma_{t}^{R}
\end{aligned}
$$

$\gamma_{t}^{C} / \gamma_{t}$ is the fraction explained by the Candidate variable.

#### Relating to the conventional approach

Conventional approach:

$$
R_{i t}=\tilde{\alpha}_{t}+\tilde{\gamma}_{t}^{R} I V O L_{i t-1}+\tilde{\gamma}_{t}^{C} C_{i t-1}+\tilde{\epsilon}_{i t}
$$

Which can be re-written as:

$$
\begin{array}{l}
R_{i t}=\tilde{\alpha}_{t}+\tilde{\gamma}_{t}^{R}\left(a_{t-1}+\mu_{i t-1}+\delta_{t-1} C_{i t-1}\right)+\tilde{\gamma}^{C} C_{i t-1}+\tilde{\epsilon}_{i t} \\
R_{i t}=\tilde{\alpha}_{t}+\tilde{\gamma}_{t}^{R}\left(a_{t-1}+\mu_{i t-1}\right)+\bar{\gamma}^{C} C_{i t-1}+\tilde{\epsilon}_{i t}
\end{array}
$$

where $\bar{\gamma}_{t}^{c}=\tilde{\gamma}_{t}^{c}+\delta_{t-1} \tilde{\gamma}_{t}^{R}$, is the coefficient when $R_{i t}$ is regressed on $C_{i t-1}$. 

Rewrite Equation:

$$
\begin{aligned}
\gamma_{t}^{c} &=\frac{\operatorname{Cov}\left[R_{i t}, \delta_{t-1} C_{i t-1}\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]} \\
&=\frac{\operatorname{Cov}\left[R_{i t}, \delta_{t-1} C_{i t-1}\right]}{\operatorname{Var}\left[\delta_{t-1} C_{i t-1}\right]} \times \frac{\operatorname{Var}\left[\delta_{t-1} C_{i t-1}\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]} \\
&=\frac{\bar{\gamma}_{t}^{C}}{\delta_{t-1}} \times \frac{\operatorname{Var}\left[\delta_{t-1} C_{i t-1}\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]} \\
&=\left(\frac{\tilde{\gamma}_{t}^{c}}{\delta_{t-1}}+\tilde{\gamma}_{t}^{R}\right) \times \frac{\operatorname{Var}\left[\delta_{t-1} C_{i t-1}\right]}{\operatorname{Var}\left[I V O L_{i t-1}\right]}
\end{aligned}
$$

Note: " $\mathrm{C}$ " denotes the candidate explanatory variable.

This suggests that $\gamma_{t}^{C}$ 

- not only depends on the fraction of the variation of idiosyncratic volatility explained by the candidate variable $\left(\frac{\operatorname{Var}\left[\delta_{t-1} \text { Candidate }_{i t-1}\right]}{\operatorname{Var}\left[N L_{i t-1}\right]}\right)$, 
- but also on the component of the candidate variable that is uncorrelated with idiosyncratic volatility but correlated with future returns as captured by $\tilde{\gamma}_{t}^{\mathrm{C}}$.

### Results

**Univariate candidates**

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291000892.png)

**Multivariate analysis**

Lottery and friction variables dominate other explanations.

Table 5

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291001908.png)

**Fig 1A: Summary of explained fraction**

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291001885.png)

- All existing explanations explain 30-55%
- Lottery-preference and market friction-based stories are the most successful.
- We can plot such pie charts because the contributions add up to 100%.
- Cannot be done with conventional approach.

### Flexibility of decomposition

- **Portfolios**: Can be applied to cross-sectional regressions on portfolios sorted by IVOL (portfolios help reduce measurement error which causes downward bias in fraction explained).
- **Non-linear specifications**: Replace continuous IVOL with a dummy variable indicating high IVOL, and/or replace candidate with dummy variable. We show non-linear specifications produce similar set of best
candidates.
- **Decompose other anomalies**: We can flip the analysis to see how much of other anomalies (e.g. Maxret, SUE) are explained by IVOL. Our method can be easily applied to other anomalies.

### Conclusion

**About the methodology**:

- Hou and Loh (2016) survey explanations for the IVOL puzzle and propose a simple methodology to quantify the success of each explanation.
- Main advantage of their approach: quantify the incremental contribution of each explanation
- Hou and Loh’s (2016) simple methodology can be used to compare competing explanations for other anomalies.

**Key findings**:

- The most promising explanations are lottery preference and market friction explanations.
- Most explanations explain <10% of the puzzle.
- Across various specifications, the residual part of the IVOL puzzle that remains unexplained by the best candidates is statistically significant.

## Public news arrivals and the idiosyncratic volatility puzzle

Journal of Empirical Finance 37 (2016) 159-172

Yanlin Shi, Wai Liu, and Kin-Yip Ho

### Introduction

**Idiosyncratic volatility puzzle**

- Modern portfolio theory asserts that, in the absence of market imperfections, rational investors should hold diversified portfolios, and therefore **idiosyncratic volatility (IVOL) or risk should not be priced**.
- In the presence of market imperfections, investors under-diversify, and such **under-diversification could lead to a positive relation between IVOL and expected stock returns** in the cross-section (Levy, 1978; Malkiel and Xu, 2002; Merton, 1987).
- recent work by **Ang et al. (2006)** documents an opposite and puzzling result; they find that **portfolios with high IVOL have abnormally low returns**.

Many studies have emerged in the past decade to address the puzzling results of Ang et al. (2006). This paper offers an **alternative explanation**.

- Studies such as Saryal (2009) and Fu (2009) point out that the puzzle is in part **caused by the method of IVOL measurement**.

### Estimation of idiosyncratic volatility (IVOL)

In his critique of Ang et al. (2006) methodology, Fu (2009) contends that **lagged IVOL** may not be appropriate to serve as proxy for **expected IVOL** because of the return reversal and the time-varying property of IVOL.

Estimate the monthly IVOL using EGARCH:

$$
\begin{array}{l}
r_{i, t}=\alpha_{i}+\beta_{i} M K T_{t}+s_{i} S M B_{t}+h_{i} H M L_{t}+\varepsilon_{i, t} \text { and } \varepsilon_{i, t} \sim N\left(0, \sigma_{i, t}^{2}\right) \\
\ln \left(\sigma_{i, t}^{2}\right)=a_{i}+\sum_{l=1}^{p} b_{i, l} \ln \left(\sigma_{i, t-1}^{2}\right)+\sum_{k=1}^{q} c_{i, k}\left\{\theta\left(\frac{\varepsilon_{i, t-k}}{\sigma_{i, t-k}}\right)+\gamma\left[\left|\frac{\varepsilon_{i, t-k}}{\sigma_{i, t-k}}\right|-(2 / \pi)^{1 / 2}\right]\right\}
\end{array}
$$

### Sample and Data

Original News Data (ranging from 1/1/2000 to 31/12/2011)

- REL: relevance score (0-100)
- ESS: essential score (>50 positive, <50 negative)
- ENS: novelty score (0-100)
- CSS: sentiment score (>50 positive, <50 negative)

Regenerate number of news articles weighted by REL:

$$
R N_{i, t}=\sum_{\text {all } \tau} \frac{R E L_{i, \tau}}{100}
$$

News variables (ranging from 1/1/2000 to 31/12/2011)

- Weighted ESS

$$
WE S S_{i, t}=\frac{1}{T} \sum_{\text {all } \tau} \frac{\left(E S S_{i, \tau}-50\right) E N S_{i, \tau}}{100}
$$

- Weighted Numbers of Negative or Positive News

$$
\begin{array}{l}
W N N_{i, t}=\sum_{\text {all } \tau} \frac{I\left(C S S_{i, \tau}<50\right)\left|C S S_{i, \tau}-50\right| R E L_{i, \tau}}{100} \\
W N P_{i, t}=\sum_{\text {all } \tau} \frac{I\left(C S S_{i, \tau}>50\right)\left|C S S_{i, \tau}-50\right| R E L_{i, \tau}}{100}
\end{array}
$$

### Empirical Results

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291003769.png)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291003275.png)

As the lagged IVOL rises, the average excess return falls.

The average excess return falls with the number of weighted negative news, while it rises with the number of weighted positive news.

Overall, Table 3’s result highlights that **the IVOL puzzle may be caused by the potential confounding effect of news**. 

- A high weighted number of bad news tends to be associated with high IVOL.
- A high weighted number of good news tends to be associated with low IVOL.

High intensity of news arrival may exacerbate the negative relation documented by Ang et al. (2006), which implies that the presence of news arrival may reduce the positive relation documented by Fu (2009).

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291004363.png)

#### Effect of idiosyncratic volatility on excess return

In the **panel regression**, we include the FF3F and WESS with the standard error clustered by firm and month–year (Petersen, 2009):

$$
r_{t}=\beta_{0}+\beta_{1} E(I V O L)_{t}+\beta_{2} W E S S_{t}+\beta_{3} M K T_{t}+\beta_{4} S M B_{t}+\beta_{5} H M L_{t}+\varepsilon_{t} 
$$

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291004070.png)

Examine the returns of portfolios based on sorting stocks into quintiles of expected IVOL, both with and without the news variables in the EGARCH estimation.

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291005314.png)

##### Robustness checks

First, we consider taking the time-series average of the slopes in cross-sectional regressions based on **the standard Fama-Macbeth methodology**.

$$
R_{t}=\beta_{0}+\beta_{1} E(I V O L) t+\beta_{2} \ln (B E / M E)+\beta_{3} \ln (M E)+\beta_{4} \ln (T U R N)+\beta_{5} \ln (\text { CVTURN })+\beta_{6} R E T(-2,-7)+\varepsilon_{t} .
$$

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291005329.png)

Divide these news items into two broad groups: 

- **earnings news**, which covers the announcement of earnings figures, dividend payout or change of dividend payment; and 
- **non-earnings news**, which covers nine categories which we believe are significant enough to affect share values, but which we restrict to those that are considered to be **value-relevant**.

Our results are even stronger after we include only value-relevant news.

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210291005765.png)

### Key Findings

While the average positive effect of expected IVOL on the expected return is substantial, the average effect is reduced by roughly 50% after the confounding effect of news is taken into consideration.

This result is robust to the inclusion of other risk factors such as information risk and liquidity risk, and different model specifications including the Fama–MacBeth model with firm-level controls and the robust panel fixed effects model.

Since not all firm-specific news releases are equally important, we focus exclusively on the value-relevant ones and find that the positive IVOL-return relation disappears as a result.