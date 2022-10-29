---
title: "Special Topic2 Forward Premium Anomaly"
date: 2022-10-19T08:29:13+08:00
draft: false

description: ""
upd: "Foreign exchange rate expectations: survey and synthesis"

tags: []
categories: ['FINM8007']
output: word_document
---

**Foreign exchange rate expectations: survey and synthesis**

Journal of Economic Surveys 22 (2008) 140-165

Ron Jongen, Willem Verschoor and Christian Wolff

## Key points

**Prominent issues**:

- Forward premium puzzle*
- Forecast performance*
- Expectations formation in financial markets
- Heterogeneity of expectations
- Market microstructure
- Time-varying risk premiums

<!--more-->

**Forward premium puzzle**: $s_{t+k} \neq f_{t, t+k}$

- “Anomaly” is another word for “puzzle”
- Also called forward discount anomaly/puzzle
- Forward premium with respect to one currency = forward discount in the other currency
- **Irrational expectations and time-varying risk premiums** could explain this anomaly/puzzle

Forward rate as an unbiased estimate for future spot rates*

- Role of time-varying risk premiums
- Unrealistic assumption of rational expectations?

Forecasting exchange rates: could individual market participants outperform a random walk model?*

Time variation in the risk premium: fundamentals-based models or time-series models?

Market microstructure and the role of heterogeneous expectations.

Different sections

- Forward premium puzzle (Section 2)*
- Modelling risk premiums (Section 3)
- Foreign exchange forecast performance (Section 4)*
- Market microstructure and heterogeneity (Section 5)
- Noise trading, chartism and the role of fundamentals (Section 6)

## Forward premium puzzle (Section 2)

Sometimes also referred to as “forward discount puzzle”, “forward discount anomaly”, or “forward premium anomaly”

Unlike what the theoretical forward rate equation suggests, the forward premium puzzle refers to the phenomenon in which **the forward exchange rate did not seem to forecast the future spot exchange rate**. It means that **the forward exchange rate does not seem to be an unbiased predictor of the future spot exchange rate**.

In other words, empirical evidence suggests that we do not consistently witness the theoretical relation between the forward and spot exchange rates

- If foreign exchange markets were efficient, all arbitrage opportunities should be eliminated.
- Recall the example of covered interest arbitrage based on the forward and spot exchange rates.

If the theoretical relationship between the forward and spot exchange rates hold, forward rate should be an unbiased predictor of the spot rate (“**unbiasedness assumption**”)

Jongen et al. (2008): “In particular, the efficient market hypothesis encompasses the joint hypothesis that **expectations are formed rationally** and that market participants are **risk neutral** with respect to domestic or foreign assets.”

- Note the implicit assumption that domestic and foreign assets are perfect substitutes in this statement.
- **Rational expectations**: market participants taking into consideration all the information available and making “rational” forecasts

Regression equation in empirical analysis

$$
s_{t+k}-s_{t}=\alpha_{1}+\beta_{1}\left(f_{t, t+k}-s_{t}\right)+\varepsilon_{t+k}
$$

- Null hypothesis (H0) of unbiasedness:

$$
\mathrm{H}_{0}: \alpha=0 \text{ and } \beta=1
$$

**Rejection of unbiasedness hypothesis**: Hodrick (1987) and Engel (1996).

To find explanations for the failure of the forward discount unbiasedness hypothesis: 

$$
f_{t, t+k}-s_{t}=\left(E_{t}\left[s_{t+k}\right]-s_{t}\right)+r p_{t}^{k}
$$

- Risk premium: $r p_{t}^{k} \equiv f_{t, t+k}-E_{t}\left[s_{t+k}\right]$
- This premium is like a reward for the extra risk of holding foreign currency.
- Domestic and foreign assets **NO LONGER perfect substitutes**.

Mathematically, rejection of unbiasedness hypothesis can be decomposed as:

- biases in expectations (**no rational expectations**?)
- a **risk premium** (so, domestic and foreign assets are NOT perfect substitutes)

### Risk Premium

Empirical test:

$$
s_{t, t+k}^{e}-s=\alpha_{2}+\beta_{2}\left(f_{t, t+k}-s_{t}\right)+\varepsilon_{t}
$$

$s_{t, t+k}^{e}$ : survey-based data; proxy for market expectation of future spot rate $E_{t}\left[s_{t+k}\right]$.

So null hypothesis of perfect substitutability (no risk premium):

$$
\mathrm{H}_{0}: \alpha_2 =0 \text{ and } \beta_2=1
$$

Empirical researchers (such as Frankel and Froot (1987) etc.) **reject the null hypothesis**.

### Rational Expectations

What about rational expectations? For expectations to be rational, four conditions need to be met (Pesaran (1987)):

- **Unbiased forecasts (expected rate of depreciation = actual rate of depreciation)**;
- **Survey-based forecast errors orthogonal to (independent from/unrelated to) variables from the information set available to agents.**
- Forecast errors exhibit “limited” serial correlation.
- Efficient expectations

Focus on unbiased forecasts and orthogonality (independence) of survey-based forecast errors

#### Unbiased Forecasts

Empirical test of unbiased forecasts:

$$
s_{t+k}-s_{t}=\alpha_{3}+\beta_{3}\left(s_{t, t+k}^{e}-s_{t}\right)+\varepsilon_{t+k}
$$

Null hypothesis (H0) of unbiasedness:

$$
\mathrm{H}_{0}: \alpha_3 =0 \text{ and } \beta_3 =1
$$

Empirical researchers reject the hypothesis of unbiased forecasts: Blake et al. (1986) etc.

But **biases in forecasts and expectations does NOT imply irrational expectations**.

- Expected rate of depreciation may be a biased estimate of the actual rate, but it does not mean the rational expectations hypothesis has failed
- The assumption of **homogeneous expectations**, as made so far, may not hold.

#### Orthogonality

Empirical researchers rejected forecast error orthogonality (independence/unrelatedness): Dominguez (1986) etc.

Maybe rational expectations hypothesis does NOT hold?

- Extrapolative expectations?

$$
s_{t, t+k}^{e}-s_{t}=\alpha_{6}+\beta_{6}\left(s_{t}-s_{t-l}\right)+\varepsilon_{\mathrm{t}}
$$

- Adaptive expectations?

$$
s_{t, t+k}^{e}-s_{t}=\alpha_{7}+\beta_{7}\left(s_{t}-s_{t-k, t}^{e}\right)+\varepsilon_{t}
$$

- Regressive expectations?

Existence of the forward premium puzzle (or the
failure of the forward discount unbiasedness):

- Irrational expectations (rejection of rational expectations)
- Time-variation in risk premiums

## Time-varying risk premiums (Section 3)


Fundamentals-based models:

- Macroeconomic fundamentals (portfolio balance model): Frankel (1982)
- General equilibrium asset-pricing model: Lucas (1982)

Time-series models

- Autoregressive Moving-Average (ARMA) models (Cavaglia et al. 1994)
-  GARCH (Generalized Autoregressive Conditional Heteroskedasticity) models (Nieuwland et al. (1998) etc.)

**Macroeconomic fundamentals (portfolio balance model): Frankel (1982)**

- **A higher level of variability** of the spot exchange rate will increase the uncertainty of the returns on assets that are denominated in the domestic currency, which in its turn will increase the risk premium.
- In addition, an increase in **the proportion of domestic-currency-denominated assets relative to assets in the foreign currency** will increase the risk premium.

$$
f_{t, t+k}-E_{t}\left[s_{t+k}\right]=\gamma_{0}+\gamma_{1} V_{t}+\gamma_{2} V_{t} \varphi_{t}+\varepsilon_{t}
$$

- where $V_{t}$ is a proxy for the volatility of the spot exchange rate, and $\varphi_{t}$ is the value of domestic assets in an investor's portfolio as a proportion of total wealth.

**General equilibrium asset-pricing model: Lucas (1982)**

- Relates risk premium to **several macroeconomic variables** (fiscal and monetary variables; domestic and foreign government expenditures)

$$
f_{t, t+k}-E_{t}\left[s_{t+k}\right]=\delta_{0}+\delta_{1}\left(E_{t}\left[X_{t+k}\right]\right)+\delta_{2} \operatorname{var}\left(X_{t+k}\right)+\varepsilon_{t}
$$

- where $X$ is a vector of fiscal and monetary variables and $\operatorname{var}(X)$ proxies the volatility of these variables through their variance and covariance terms.

Time-series models: 

- These time-series models are not based on economic
fundamentals;
Success from time-series models is quite mixed.

Although most models based on fundamentals have difficulties in finding the right variables to analyse, simple time-series models have been quite successful in modelling the risk premiums for most currencies.

## Forex Forecast performance (Section 4)

**Several methodologies**:

- Root mean squared error (RMSE): MacDonald and Marsh (1994, 1996)
- Simple profit-based trading rules: Elliott and Ito (1999)
- **Benchmark** - Random walk model: Meese (1990), Meese and Rogoff (1983), and Wolff (1987, 2000)

**Empirical findings**:

- Random walk model seems to dominate!
- Survey-based forecasts: forecast errors from survey data do not seem to be significantly smaller than random walk
- No sustained accuracy of other forecast models

Forecasting seems difficult! Implications for forecast unbiasedness? Market efficiency and forward premium puzzle?

## Heterogeneous expectations (Section 5)

Microstructure of foreign exchange market and heterogeneity of beliefs of market participants:

- Beliefs/expectations are heterogeneous: models based on **one representative agent** too simplistic.
- Models based on aggregate expectations unrealistic.

**Heterogeneous beliefs**:

- **Informational asymmetry** (rigid transmission of public information): Kurz and Motolese (2001)
- **Different beliefs** about economic variables (market participants do not know the structural relations of the economy): Kurz (1994)
- Ito (1990): **individual effects** (private information) contributing to heterogeneity

## Noise trading, chartism and role of fundamentals (Section 6)

Different beliefs about the future due to presence of various types of market participants (who could have the same information set):

- Fundamentalists
- Chartists
- Portfolio managers
- See Frankel and Froot (1986, 1988) etc.

Empirical findings:

- Frankel and Froot (1986): “chartists are simply people who think only in terms of the short-run horizon, whereas fundamentalists think long term.”
- change in forecasting methodologies (chartist techniques for short forecast horizon).
- Microstructure anomaly of excessive trading volume (noise trader model): De Long et al. (1990)

## Conclusion

- Irrationality of market participants and time-varying risk premiums.
- Why time-varying term premiums exist and how to model premiums.
- Performance of market participants and random walk model in forecasting exchange rates
- Market microstructure and heterogeneity in beliefs/expectations: can they explain anomalies?
- Different market players (noise traders, chartists, fundamentalists)

## PRACTICE QUESTIONS

**Practice** (PRACTICE QUESTIONS FOR SPECIAL TOPICS) According to the article entitled “Foreign exchange rate expectations: survey and synthesis” by Jongen et al. (2008), explain and discuss the concept of the forward premium puzzle and the factors contributing to its existence.

**Solution**: As suggested by Jongen et al. (2008), the forward premium puzzle refers to the phenomenon that the forward exchange rate does not seem to be an unbiased predictor of the future spot exchange rate. This puzzling phenomenon seems to defy the expectation that the forward and spot rates should be intimately related according to the interest parity condition at market equilibrium. More specifically, if markets were efficient and all arbitrage opportunities were exhausted at market equilibrium, the forward and spot rates would have a predictable relationship.

According to Jongen et al. (2008), this idea of efficiency in the forward and spot exchange rate markets incorporates two aspects: one, the forward rate is an unbiased predictor of the spot rate and expectations are formed rationally; and two, market investors are risk neutral in their preferences towards domestic and foreign assets and implicitly treat them as perfect substitutes.

As discussed in Jongen et al. (2008), the unbiasedness assumption could be violated due to the presence of a risk premium (which is mathematically defined as the difference between the forward rate and expected future spot rate) and expectational biases. In the case of the risk premium, its presence could further imply that the domestic and foreign assets are not perfect substitutes. Indeed, the literature (Frankel and Froot, 1987) provides strong empirical evidence that perfect substitutability is probably non-existent.

As for the assumption of rational expectations, which refers to the phenomenon that market participants make rational forecasts based on all the available information, Jongen et al. (2008) suggests that this assumption might not hold because of two conditions. First, forecasts could be biased and the actual change in exchange rate is not equal to the expected change in the exchange rate. Second, survey-based forecast errors are not orthogonal (or unrelated) to the existing information available to the market participants. As highlighted by Jongen et al. (2008), these conditions provide the motivation for researchers to consider alternative types of expectations, such as extrapolative and adaptive expectations.