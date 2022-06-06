---
title: "Hedging"
date: 2021-03-09T16:07:06+08:00
draft: true

description: ""
upd: ""

tags: ['Notes']
categories: ['Financial Engineering']
---

<!--more-->

$$
\mathrm{h}=\sigma_{\Delta \mathrm{S} \Delta \mathrm{f}} / \sigma_{\Delta \mathrm{f}}^{2}=\operatorname{cov}(\Delta \mathrm{S}, \Delta \mathrm{f}) / \operatorname{var}(\Delta \mathrm{f})
$$

For forwards we put:

$$
N_{f}=-\Delta S / \Delta f \times \frac{\text { Size of spot position }}{\text { Size of } 1 \text { futures contract }}
$$

For futures, with daily settlement, we do as above, or we may want to adjust as the futures price changes:

$$
N_{f}=-\Delta S / \Delta f \times \frac{\text { Dollar value of spot position }}{\text { Dollar value of } 1 \text { futures contract }}
$$
For a stock index is
$$
\mathrm{N}_{\mathrm{f}}=-\left(\frac{\beta_{\mathrm{s}}}{\beta_{\mathrm{f}}}\right)\left(\frac{\mathrm{S}}{\mathrm{f}}\right)
$$
Changing portfolio beta

If you want to hedge completely (reduce $ \beta $ to 0 ) then:
$$
\mathrm{N}_{\mathrm{f}}=-\left(\frac{\beta_{\mathrm{S}}}{\beta_{\mathrm{f}}}\right)\left(\frac{\mathrm{S}}{\mathrm{f}}\right)
$$
If you want to reduce from $ \beta_{\mathrm{s}} $ to a target $ \beta_{\mathrm{T}} $ then:
$$
\mathrm{N}_{\mathrm{f}}=\left(\frac{\beta_{\mathrm{T}}-\beta_{\mathrm{S}}}{\beta_{\mathrm{f}}}\right)\left(\frac{\mathrm{S}}{\mathrm{f}}\right)
$$
Therefore the hedge ratio for bond is
$$
N_{f}^{\star}=-\left(\frac{D_{B}}{D_{f}}\right)\left(\frac{B}{f}\right)
$$
![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20220606210413.png)
