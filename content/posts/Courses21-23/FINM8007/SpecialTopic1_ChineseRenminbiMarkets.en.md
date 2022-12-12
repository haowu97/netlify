---
title: "Special Topic1 Chinese Renminbi Markets"
date: 2022-10-14T18:02:17+08:00
draft: false

description: ""
upd: "Chinese RMB volatility, Public Information Arrival, Price Discovery and Dynamic Correlations in the Chinese Renminbi Markets"

tags: []
categories: ['FINM8007']
output: word_document
---

## Does news matter in China’s foreign exchange market? Chinese RMB volatility and public information arrivals

**Volatility**: how stable is the return series? The sharp change indicates the large volatility

### Key points

Impact of public information flows on the volatility of the bilateral RMB-USD exchange rates in the spot, non-deliverable forward (NDF), and futures markets

- Relationship between public news sentiment and volatility of the RMB-USD exchange rate

Two-state Regime-Switching EGARCH-in-mean (**RSEGARCH-M**) model incorporating the effects of news sentiment

- Different regimes in the RMB-USD volatility

<!--more-->

### Motivation of the Research

The Chinese Renminbi (RMB)

- RMB has become an **important** currency for conducting international transactions
- Jin (2012): RMB was a **settlement currency** for cross-border trade with neighboring countries in 1980s
- China's Bilateral Currency Trade Settlement Agreements with Russia and Australia
- Top five payments currency (SWIFT, 2015)

**Challenges** to the current RMB exchange rate system and arrangements

- RMB not fully convertible due to **capital account restrictions**
- “**Managed float**” regime started from July 21 2005 (previously US dollar peg)
- RMB floated within a controlled range: ±0.3% → ±0.5% → ±1% → ±2%
- **Market-oriented reforms** of the RMB exchange rate
  - Temporary suspension of managed float in August 2008
  - Back to “managed float” in June 2010

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210182208671.png)

**Volatility Clustering**: Big changes followed by big changes.

The **rising demand for hedging** against foreign exchange risk

- The expansion of offshore RMB **non-deliverable forward** (NDF) markets (Lien et al, 2013)
- In June 2006, the RMB/USD **futures** contract was launched at the Chicago Mercantile Exchange (CME)
- Hedging against foreign exchange risk requires understanding its volatility dynamics

### Theoretical Underpinning

The idea of “Mixture of Distribution Hypothesis” (MDH)

- Originated by Clark (1973) who assert that the security price change follows a mixture of distribution, and the **volatility will be decided by the number of increment**
- Extended by Tauchen and Pitts (1983), Harris (1986,
1987), Lamoureux and Lastrapes (1990) and Andersen (1996): **the variance of returns at a given interval is proportional to the rate of information arrival on the market**

Idea of Veronesi (1999)

- **the sentiment of news plays an important role in explaining the financial return volatility, and its effect depends on the state of volatility**

Our proposition:

$$
\log \left(h_{t}\right) \propto f\left(n_{t}, Q_{\tau}\right)
$$

where $h_{t}$ is the conditional volatility of exchange rate return at time $t$, $n_{t}$ is number of relevant news arriving at the interval $[t-1, t]$ and $Q \tau$ is the sentiment of news story $\tau(\tau \in[t-1, t])$, which is a non-negative value.

### Sample and Data

Daily Return Series (ranging from 22/7/2005 to 31/12/2011)

$$
r_{t}=100 \times \log \left(S_{t} / S_{t-1}\right),
$$

#### News Data

**RavenPack News Analytics Dow Jones Edition**

- Comprehensive database covering more than 1700 types of firm-specific and macroeconomic news events.
- Automatically tracks and monitors relevant information on tens of thousands of companies, government organizations, influential people, key geographical locations, and all major currencies and traded commodities.
- The service includes analytics on more than 170,000 entities in over 100 countries, and it covers over 98 percent of the investable global market.
- Among its many benefits, RavenPack **delivers sentiment analysis** and event data that are most likely to affect financial markets and trading around the world - all in a matter of milliseconds.
- It continuously analyzes relevant information from major real-time newswires and trustworthy sources such as Dow Jones Newswires, regional editions of the Wall Street Journal and Barron's, and internet sources including financial sites, blogs, and local and regional newspapers, to **produce real-time news sentiment scores**.
- **All relevant news articles about entities are classified and quantified according to their sentiment, relevance, topic, novelty and market effect**.

**RavenPack Dow Jones News Analytics**

- A proprietary computational linguistic analysis algorithm to quantify positive and negative perceptions on facts and opinions reported in the news textual content
- **Algorithm** can be divided into two steps:
  - RavenPack builds up a **historical database** of words, phrases, combinations and other word-level definitions that have affected the target company, market or asset class;
  - The text in the specific news story is compared with the historical database, and the sentiment score is generated accordingly.
- Among all the news (sub)categories, we collect news releases from **RMB-related and USD-related subcategories separately**

Original News Data (ranging from 22/7/2005 to 31/12/2011)

- ESS: sentiment score ( $>50$ positive, $<50$ negative)
- ENS: novelty score $(0-100)$

News Variables (ranging from 22/7/2005 to 31/12/2011)
- Weighted ESS

$$
W E S S_{c, t}=\frac{1}{T} \sum_{a ll t} \frac{\left(E S S_{c, t}-50\right) E N S_{c, t}}{100}
$$

- Logarithm of Weighted Numbers of Negative or Positive News

$$
\begin{array}{c}
W N N_{c, t}=\log \left(\sum_{\text {all } \tau} \frac{I\left(E S S_{c, r}<50\right)\left|E S S_{c, r}-50\right| E N S_{c, r}}{100}\right) \\
W N P_{c, t}=\log \left(\sum_{\text {all } \tau} \frac{I\left(E S S_{c, r}>50\right)\left|E S S_{c, r}-50\right| E N S_{c, r}}{100}\right)
\end{array}
$$

### Methodology

Exponential GARCH-in-Mean (EGARCH-M) Model

$$
\begin{array}{c}
r_{t}=b_{0}+b_{\lambda} h_{t}+b_{1} WESS_t+\varepsilon_{t} \\
\varepsilon_{t}=\eta_{t} \sqrt{h_{t}} \text { where } \eta_{t} \sim t(0,1, v) \\
\log \left(h_{t}\right)=c+\alpha \frac{\varepsilon_{t-1}}{\sqrt{h_{t-1}}}+\beta \log \left(h_{t-1}\right)+\gamma\left\{\left|\frac{\varepsilon_{t-1}}{\sqrt{h_{t-1}}}\right|-E\left(\left|\frac{\varepsilon_{t-1}}{\sqrt{h_{t-1}}}\right|\right)\right\}+\lambda_{1} W N N_{t}+\lambda_{2} W N P_{t}
\end{array}
$$

#### RS-GARCH model

The reason for employing **regime-switching approach**.

Economic theory perspective

- Beine et al. (2003): central bank interventions can lead to either stabilizing or destabilizing effect in different states
- Wilfling (2009) argues that two state regime-switching approach should be used to model exchange rates
- Funke and Gronwald (2008) suggest that allowing the presence of volatility transition is needed to model exchange rate volatility

Modelling perspective

- GARCH family model is not appropriate when structural changes are present
- Lamoureux and Lastrapes (1990), Hamilton and Susmel (1994) and Klaassen (2002) argue that GARCH family model always implies a high volatility persistence, which may originate from structural changes in the variance

Markov Regime Switching EGARCH-M (RS-EGARCHM) Model

When $s_{t}=1, r_{t}=b_{1,0}+b_{1, \lambda} h_{1, t}+b_{1,1} W E S S_{t}+\varepsilon_{1, t}$

$\eta_{1, t}=\varepsilon_{1, t} / \sqrt{h_{1, t}}$ where $\eta_{1, t} \sim t\left(0,1, v_{1}\right)$

$\log \left(h_{1, t}\right)=c_{1}+\alpha_{1} \eta_{1, t-1}+\gamma_{1}\left\{\left|\eta_{1, t-1}\right|-E\left(\left|\eta_{1, t-1}\right|\right)\right\}+\beta_{1} \log \left(h_{1, t-1}\right)+\lambda_{11} W N N_{t}+\lambda_{12} W N P_{t}$

When $s_{t}=2, r_{t}=b_{2,0}+b_{2, \lambda} h_{2, t}+b_{2,1} W E S S_{t}+\varepsilon_{2, t}$

$\eta_{2, t}=\varepsilon_{2, t} / \sqrt{h_{2, t}}$ where $\eta_{2, t} \sim t\left(0,1, v_{2}\right)$

$\log \left(h_{2, t}\right)=c_{2}+\alpha_{2} \eta_{2, t-1}+\gamma_{2}\left\{\left|\eta_{2, t-1}\right|-E\left(\left|\eta_{2, t-1}\right|\right)\right\}+\beta_{2} \log \left(h_{2, t-1}\right)+\lambda_{21} W N N_{t}+\lambda_{22} W N P_{t}$

### Empirical Findings

**EGARCH-M Model**

- Consistent with MDH
  - Including either RMB or USD news are preferred by AIC and can greatly improve the log likelihood value
  - Volatility persistence reduced to some extent in most cases
- Marginal effects of news are mostly insignificant
- Effects of conditional volatility on contemporaneous returns are negatively significant for spot, short term maturity NDF and futures rate; insignificant for long term maturity NDF rates

**RS-EGARCH-M Model**

- Most models are preferred by AIC to EGARCH-M
- Including either RMB or USD news are preferred by AIC and can greatly improve the log likelihood value
- **Volatility persistence** reduced at greater level 
  - Reductions caused by RMB news are greater
  - Reductions in calm state are greater (except for spot rate)
- **Marginal effects of news** are various across different exchange rates, origin of news and states
  - Among the significant estimates, they are almost all positive, with negative news having greater estimates than positive news for all the exchange rates.
  - Effects of RMB news are generally greater
  - Effects on spot, short term maturity NDF (1 and 3 month(s)) and futures rate are greater than effects on long term maturity NDF (6, 9, and 12 months) rate
- Consistent with MDH
- Identification of states of spot rate could be related to the state of the economy and exchange rate policy
  - State structure of spot, short term maturity NDF and futures rate are similar
  - State structure of long term maturity NDF rates are similar
- Generally, the effects of conditional volatility on contemporaneous returns are insignificant.

### Conclusion

- Empirical results from Regime-Switching approach outperforms the one regime approach and are consistent with MDH and Veronesi (1999)
- News is an important factor, which both quantitatively and qualitatively affects the RMB/USD exchange volatility
- News effects on spot, NDF and futures rates are different


## Public Information Arrival, Price Discovery and Dynamic Correlations in the Chinese Renminbi Markets

### Key points

- Comprehensive analysis of the dynamics of the RMB in both the spot and NDF markets since 2005 by examining the role and significance of the RMB NDF in the price discovery process and in predicting the volatility dynamics of the RMB markets.
- Asymmetric volatility effects are significant for several NDF contract maturities and the spot-NDF correlations are significantly time-varying.
- Moreover, shocks to the volatility levels are highly persistent.
- Causality tests on the spot and NDF volatilities further suggest that the NDF markets impact the future fluctuations of the spot market, but the spot market does not have predictive power for the volatility of the NDF markets.
- Public information flows are found to have a significantly
positive impact on the spot-forward conditional correlations. These findings have important implications for market linkages and effective hedging strategies.

### Motivation of the Research

The increasingly prominent role of China in international trade

- the second largest economy worldwide in 2010

The backward financial system

- subject to many regulatory controls and not fully convertible

The Chinese currency, Yuan or Renminbi (CNY thereafter) reform

- US dollar pegging system (before 21/7/2005): fixed in a centain range
- “managed float” regime (from 21/7/2005): fully driven by the market

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202210182208743.png)

The potential of internationalizing the CNY

- Used in the settlement of cross-border trade between China and some neighboring countries

The rising demand for hedging against foreign exchange risk

- The expansion of offshore CNY non-deliverable forward (NDF) markets

### Objectives

- Comprehensive analysis of the dynamics of the RMB in both the spot and NDF in both the spot and NDF markets
- examining the role and significance of the RMB NDF in the overall **price discovery process** and in predicting the **volatility** in the spot market,
- assessing how **public information arrivals** affect the dynamic correlations between the spot and forward rates.

### Contributions

Firstly, from the perspective of price formation we show that **the RMB NDF contributes significantly towards the overall price discovery process**.

- **Price discovery**: the impounding of **new information** into the security price and comprising the efficient and timely incorporation of the information implicit in investor trading into market prices (Lehmann, 2002).
- When a security is traded in different markets, an important question is which market is more informative for fundamental valuation.
- Literature on price discovery (Hasbrouck, 1995, 2003; Tse, 1999; Baillie, Booth, Tse, & Zabotina, 2002; de Jong, 2002; Tse, Xiang, & Fung, 2006; Cabrera et al., 2009; Rosenberg & Traub, 2009; Bohl, Salm, & Schuppli, 2011) assumes that prices for an asset in different markets share a common efficient price which represents the fundamental value of the asset.
- In the long run the prices in different markets converge to the efficient price, but in the short run they might deviate from it due to trading frictions.
- Although Peng et al. (2007) and Zhang and Chan (2010) have noted that the pricing of NDFs does not appear to be tied to financial fundamentals, we show that the NDF has a dominant role in price discovery by using three different information share measures (Gonzalo & Granger, 1995; Hasbrouck, 1995; Lien & Shrestha,
2009).

Secondly, we analyze the **conditional volatility dynamics** of the spot and NDF series in a multivariate setting that incorporates asymmetric effects in volatility, time-varying conditional correlations, and leptokurtic distributions.

- Volatility is a measure of stability, which is important for international trade in the context of exchange rates. We show that the NDF market has a significant role in predicting the volatility in the spot market.

Finally, **the impact of public information flows on the correlations between the NDF and spot markets is quantified**.

- It is a well-established paradigm in finance that financial asset dynamics are affected by new information arrivals (Berry & Howe, 1994; Kalev, Liu, Pham, & Jarnecic, 2004; Fang & Peress, 2009; Ho, Shi, & Zhang, 2017).
- In particular, it is noted that foreign exchange markets are highly sensitive to macroeconomic and political news announcements (DeGennaro & Shrieves, 1997; Chen & Gau, 2010; Ho et al., 2017).
- As such, RMB market participants around the world most likely have to pay attention to the impact of news flows on dynamics of the exchange rate. The role of public information arrivals is expected to become more prominent, with increased use of the RMB. We add to the
existing literature by focusing on how public information arrivals can also affect the dynamic correlations between the spot and forward rates.

### Methodology

Vector Error Correction and Price Discovery

- VEC model (Engle and Granger, 1987)
- Granger/Gonzalo (1995) measure
- Hasbrouck (1995) information share (IS) measure
- Lien and Shrestha (2009) modified information share (MIS) measure

Multivariate GARCH: extract the conditional correlation

- DBEKK-MGARCH models
- DVECH-MGARCH models

Correlations and news

$$
\operatorname{Corr}_{x, t}=b_{0}+b_{1} \operatorname{Corr}_{x, t-1}+\lambda N e w s_{t}+\omega _{t}
$$


### Data Description

The Sources of News

- FACTIVA database
- 10 English-language US newspapers & 12 Chinese language media publications

### Empirical Findings

Cointegration, VEC and Price Discovery

- Augmented Dickey Fuller (ADF) and Phillips-Perron (PP) tests show that the spot and NDF rates are **both integrated of order one**
- **Johansen cointegration test** results indicate that the spot and NDF rates, at each term to maturity, share a **long-run equilibrium relationship with each other**.
- Thus, VEC models with lag 2 (selected by the Bayesian information criterion) are fitted for all the four groups of datasets.
-  Price discovery measures also show that the NDF markets are the
dominant contributors to the overall price formation process.
-  As illustrated by the Granger Causality tests based on the VEC model, **the lagged values of the CNY NDF series have predictive power for the current values of the spot series, but not vice**

MGARCH by Diagonal BEKK Estimations

- There is evidence that some of the NDF series exhibit significant asymmetry
- Shocks to the volatility seem persistent; this is evident from the sum of the parameters Ai and Bi, which is very close to one
- Robust by DVECH-MGARCH models
- **From the Granger Causality tests that the NDF volatility has predictive ability for the spot volatility. In contrast, the spot volatility does not seem to Granger Cause the NDF volatility**.

Correlations and Public Information Arrivals

- Public information flows have a positive impact on the conditional correlations.

### Conclusion

- The CNY NDF market has a significant role in the **price discovery** process, despite the fact that some researchers (such as Peng et al, 2007) have noted that the pricing in the NDF market is not tied to financial fundamentals.
- The Granger Causality tests in volatility suggest that past values of the NDF volatility have predictive ability for the current values of the spot volatility
- The conditional volatilities of several NDF series are substantially time-varying and asymmetric, which could indicate the presence of heterogeneous expectations in the NDF markets (Hogan and Melvin, 1994; Tse and Tsui, 1997)
- Shocks to the volatility are quite persistent
- The spot-forward correlation over time is positively related to the public information flows in the CNY markets

**Implication**

- Strengthening the linkages between the CNY spot and NDF markets
- Regulatory implications
  - Peng et al (2007): there is a need to strike a balance between development and regulation
  - Measures to improve transparency in the unregulated NDF market may be needed in future
- Correlation Hedging
  - Optimal (minimum-variance) hedge ratio is dynamic and has to be regularly adjusted by hedgers
  - Role of public information arrival to improve the hedging strategies involving the NDFs

## PRACTICE QUESTIONS

**Practice** (PRACTICE QUESTIONS FOR SPECIAL TOPICS) Discuss the relationship between the Chinese Renminbi (RMB) spot and nondeliverable forward (NDF) markets based on the findings in the article entitled “Public information arrival, price discovery, and dynamic correlations in the Chinese Renminbi markets” by Ho et al. (2018).

**Solution**: According to Ho et al. (2018), the Chinese RMB spot and NDF markets have evolved with the following key developments in the past twenty years: one, the RMB has transitioned to a managed floating system since July 2005; two, the offshore NDF market has grown rapidly since its inception in the 1990s; and three, restrictions on using the RMB have gradually eased to promote its increased use regionally and internationally. Despite these developments, RMB trading in the spot market still remains largely separate from the offshore NDF market due to capital controls.

**Nonetheless**, based on empirical analysis, Ho et al. (2018) suggest that the offshore NDF market is closely related to the spot market in the following ways: 

First, the empirical results demonstrate the significant contributions of the offshore NDF market towards the **overall price discovery** of the RMB. Based on three different information share measures (Gonzalo and Granger, 1995; Hasbrouck, 1995; Lien and Shrestha, 2009), Ho et al. (2018) observe that the NDF has a dominant role in price discovery.

Second, analysis of the conditional volatility dynamics of the spot and NDF markets in a multivariate GARCH framework indicates that the NDF market plays an important role in **forecasting the volatility in the spot market**. More specifically, Ho et al. (2018) employ Granger Causality tests to show that the NDF volatility affects the future volatility of the spot rate. In contrast, the spot rate does not predict the future volatility of the NDF rate.

Third, correlations between the spot and NDF rates display time-varying properties and **public news arrivals** seem to influence these time-varying correlations.

---

**Practice** (Semester 1 -- Final, 2021) With reference to the journal articles in **Special Topics 1 and 3**, explain and discuss in your own words **the characteristics and significance of volatility** in the Chinese and United States financial markets. The word limit of your answer is 1000 words. This word limit does NOT include the list of references. Do NOT include graphs and tables in your answer. Formulas are not necessary in your answer.

Note: your answer must contain in-text citations and references. 10 marks from your final exam marks will be deducted for not including in-text citations and a SINGLE list of references. Use the Harvardstyle of referencing. Any sentences and paragraphs that exceed the word limit will NOT be marked. For instance, if you have submitted an answer containing 1030 words, then only the first 1000 words will be marked and the last 30 words will not be marked.