---
title: ""
date: 2021-08-06T21:17:53+08:00
draft: true

description: ""
upd: ""

tags: []
categories: []
---

<!--more-->

[利用R语言做结构方程模型分析](https://zhuanlan.zhihu.com/p/22811566)

[lavaan简明教程](https://blog.csdn.net/bababi0833/article/details/102350104?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.edu_weight&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.edu_weight)




```r
install.packages("lavaan", dependencies=TRUE)
install.packages("semPlot")
```

基本流程实现


```r
library(lavaan)
```

```
## This is lavaan 0.6-7
```

```
## lavaan is BETA software! Please report any bugs.
```

```r
data(PoliticalDemocracy)
model <- ' 
  # main regressions/主要回归方程
    dem60 ~ ind60
    dem65 ~ ind60 + dem60
    
  # latent variable definitions/定义潜变量
     ind60 =~ x1 + x2 + x3
     dem60 =~ y1 + a*y2 + b*y3 + c*y4
     dem65 =~ y5 + a*y6 + b*y7 + c*y8

  # residual correlations/方差和协方差
    y1 ~~ y5
    y2 ~~ y4 + y6
    y3 ~~ y7
    y4 ~~ y8
    y6 ~~ y8
    
    #截距项
    dem60 ~ 1
    dem65 ~ 1
'
fit <- sem(model, data = PoliticalDemocracy)
```

```
## Warning in lav_model_vcov(lavmodel = lavmodel, lavsamplestats = lavsamplestats, : lavaan WARNING:
##     The variance-covariance matrix of the estimated parameters (vcov)
##     does not appear to be positive definite! The smallest eigenvalue
##     (= 1.579160e-17) is close to zero. This may be a symptom that the
##     model is not identified.
```

```r
# summary()只适合展示结果
summary(fit, fit.measures = TRUE)
```

```
## lavaan 0.6-7 ended normally after 65 iterations
## 
##   Estimator                                         ML
##   Optimization method                           NLMINB
##   Number of free parameters                         44
##   Number of equality constraints                     3
##                                                       
##   Number of observations                            75
##                                                       
## Model Test User Model:
##                                                       
##   Test statistic                                40.179
##   Degrees of freedom                                36
##   P-value (Chi-square)                           0.290
## 
## Model Test Baseline Model:
## 
##   Test statistic                               730.654
##   Degrees of freedom                                55
##   P-value                                        0.000
## 
## User Model versus Baseline Model:
## 
##   Comparative Fit Index (CFI)                    0.994
##   Tucker-Lewis Index (TLI)                       0.991
## 
## Loglikelihood and Information Criteria:
## 
##   Loglikelihood user model (H0)              -1548.818
##   Loglikelihood unrestricted model (H1)      -1528.728
##                                                       
##   Akaike (AIC)                                3179.636
##   Bayesian (BIC)                              3274.653
##   Sample-size adjusted Bayesian (BIC)         3145.432
## 
## Root Mean Square Error of Approximation:
## 
##   RMSEA                                          0.039
##   90 Percent confidence interval - lower         0.000
##   90 Percent confidence interval - upper         0.094
##   P-value RMSEA <= 0.05                          0.574
## 
## Standardized Root Mean Square Residual:
## 
##   SRMR                                           0.052
## 
## Parameter Estimates:
## 
##   Standard errors                             Standard
##   Information                                 Expected
##   Information saturated (h1) model          Structured
## 
## Latent Variables:
##                    Estimate  Std.Err  z-value  P(>|z|)
##   ind60 =~                                            
##     x1                1.000                           
##     x2                2.180    0.138   15.751    0.000
##     x3                1.818    0.152   11.971    0.000
##   dem60 =~                                            
##     y1                1.000                           
##     y2         (a)    1.191    0.139    8.551    0.000
##     y3         (b)    1.175    0.120    9.755    0.000
##     y4         (c)    1.251    0.117   10.712    0.000
##   dem65 =~                                            
##     y5                1.000                           
##     y6         (a)    1.191    0.139    8.551    0.000
##     y7         (b)    1.175    0.120    9.755    0.000
##     y8         (c)    1.251    0.117   10.712    0.000
## 
## Regressions:
##                    Estimate  Std.Err  z-value  P(>|z|)
##   dem60 ~                                             
##     ind60             1.471    0.392    3.750    0.000
##   dem65 ~                                             
##     ind60             0.600    0.226    2.661    0.008
##     dem60             0.865    0.075   11.554    0.000
## 
## Covariances:
##                    Estimate  Std.Err  z-value  P(>|z|)
##  .y1 ~~                                               
##    .y5                0.583    0.356    1.637    0.102
##  .y2 ~~                                               
##    .y4                1.440    0.689    2.092    0.036
##    .y6                2.183    0.737    2.960    0.003
##  .y3 ~~                                               
##    .y7                0.712    0.611    1.165    0.244
##  .y4 ~~                                               
##    .y8                0.363    0.444    0.817    0.414
##  .y6 ~~                                               
##    .y8                1.372    0.577    2.378    0.017
## 
## Intercepts:
##                    Estimate  Std.Err  z-value  P(>|z|)
##    .dem60             0.000    0.238    0.000    1.000
##    .dem65             0.000    0.112    0.000    1.000
##    .x1                5.054    0.084   60.127    0.000
##    .x2                4.792    0.173   27.657    0.000
##    .x3                3.558    0.161   22.066    0.000
##    .y1                5.465    0.164   33.308    0.000
##    .y2                4.256    0.253   16.843    0.000
##    .y3                6.563    0.230   28.592    0.000
##    .y4                4.453    0.174   25.604    0.000
##    .y5                5.136    0.172   29.947    0.000
##    .y6                2.978    0.196   15.219    0.000
##    .y7                6.196    0.195   31.754    0.000
##    .y8                4.043    0.163   24.741    0.000
##     ind60             0.000                           
## 
## Variances:
##                    Estimate  Std.Err  z-value  P(>|z|)
##    .x1                0.081    0.019    4.182    0.000
##    .x2                0.120    0.070    1.729    0.084
##    .x3                0.467    0.090    5.177    0.000
##    .y1                1.855    0.433    4.279    0.000
##    .y2                7.581    1.366    5.549    0.000
##    .y3                4.956    0.956    5.182    0.000
##    .y4                3.224    0.723    4.458    0.000
##    .y5                2.313    0.479    4.831    0.000
##    .y6                4.968    0.921    5.393    0.000
##    .y7                3.560    0.710    5.018    0.000
##    .y8                3.308    0.704    4.701    0.000
##     ind60             0.449    0.087    5.175    0.000
##    .dem60             3.875    0.866    4.477    0.000
##    .dem65             0.164    0.227    0.725    0.469
```

```r
# parameterEstimates()会返回一个数据框，方便进一步的处理
parameterEstimates(fit,ci=FALSE,standardized = TRUE)
```

```
##      lhs op   rhs label   est    se      z pvalue std.lv std.all std.nox
## 1  dem60  ~ ind60       1.471 0.392  3.750  0.000  0.448   0.448   0.448
## 2  dem65  ~ ind60       0.600 0.226  2.661  0.008  0.187   0.187   0.187
## 3  dem65  ~ dem60       0.865 0.075 11.554  0.000  0.884   0.884   0.884
## 4  ind60 =~    x1       1.000 0.000     NA     NA  0.670   0.920   0.920
## 5  ind60 =~    x2       2.180 0.138 15.751  0.000  1.460   0.973   0.973
## 6  ind60 =~    x3       1.818 0.152 11.971  0.000  1.218   0.872   0.872
## 7  dem60 =~    y1       1.000 0.000     NA     NA  2.201   0.850   0.850
## 8  dem60 =~    y2     a 1.191 0.139  8.551  0.000  2.621   0.690   0.690
## 9  dem60 =~    y3     b 1.175 0.120  9.755  0.000  2.586   0.758   0.758
## 10 dem60 =~    y4     c 1.251 0.117 10.712  0.000  2.754   0.838   0.838
## 11 dem65 =~    y5       1.000 0.000     NA     NA  2.154   0.817   0.817
## 12 dem65 =~    y6     a 1.191 0.139  8.551  0.000  2.565   0.755   0.755
## 13 dem65 =~    y7     b 1.175 0.120  9.755  0.000  2.530   0.802   0.802
## 14 dem65 =~    y8     c 1.251 0.117 10.712  0.000  2.694   0.829   0.829
## 15    y1 ~~    y5       0.583 0.356  1.637  0.102  0.583   0.281   0.281
## 16    y2 ~~    y4       1.440 0.689  2.092  0.036  1.440   0.291   0.291
## 17    y2 ~~    y6       2.183 0.737  2.960  0.003  2.183   0.356   0.356
## 18    y3 ~~    y7       0.712 0.611  1.165  0.244  0.712   0.169   0.169
## 19    y4 ~~    y8       0.363 0.444  0.817  0.414  0.363   0.111   0.111
## 20    y6 ~~    y8       1.372 0.577  2.378  0.017  1.372   0.338   0.338
## 21 dem60 ~1             0.000 0.238  0.000  1.000  0.000   0.000   0.000
## 22 dem65 ~1             0.000 0.112  0.000  1.000  0.000   0.000   0.000
## 23    x1 ~~    x1       0.081 0.019  4.182  0.000  0.081   0.154   0.154
## 24    x2 ~~    x2       0.120 0.070  1.729  0.084  0.120   0.053   0.053
## 25    x3 ~~    x3       0.467 0.090  5.177  0.000  0.467   0.239   0.239
## 26    y1 ~~    y1       1.855 0.433  4.279  0.000  1.855   0.277   0.277
## 27    y2 ~~    y2       7.581 1.366  5.549  0.000  7.581   0.525   0.525
## 28    y3 ~~    y3       4.956 0.956  5.182  0.000  4.956   0.426   0.426
## 29    y4 ~~    y4       3.224 0.723  4.458  0.000  3.224   0.298   0.298
## 30    y5 ~~    y5       2.313 0.479  4.831  0.000  2.313   0.333   0.333
## 31    y6 ~~    y6       4.968 0.921  5.393  0.000  4.968   0.430   0.430
## 32    y7 ~~    y7       3.560 0.710  5.018  0.000  3.560   0.357   0.357
## 33    y8 ~~    y8       3.308 0.704  4.701  0.000  3.308   0.313   0.313
## 34 ind60 ~~ ind60       0.449 0.087  5.175  0.000  1.000   1.000   1.000
## 35 dem60 ~~ dem60       3.875 0.866  4.477  0.000  0.800   0.800   0.800
## 36 dem65 ~~ dem65       0.164 0.227  0.725  0.469  0.035   0.035   0.035
## 37    x1 ~1             5.054 0.084 60.127  0.000  5.054   6.943   6.943
## 38    x2 ~1             4.792 0.173 27.657  0.000  4.792   3.194   3.194
## 39    x3 ~1             3.558 0.161 22.066  0.000  3.558   2.548   2.548
## 40    y1 ~1             5.465 0.164 33.308  0.000  5.465   2.111   2.111
## 41    y2 ~1             4.256 0.253 16.843  0.000  4.256   1.120   1.120
## 42    y3 ~1             6.563 0.230 28.592  0.000  6.563   1.924   1.924
## 43    y4 ~1             4.453 0.174 25.604  0.000  4.453   1.354   1.354
## 44    y5 ~1             5.136 0.172 29.947  0.000  5.136   1.948   1.948
## 45    y6 ~1             2.978 0.196 15.219  0.000  2.978   0.876   0.876
## 46    y7 ~1             6.196 0.195 31.754  0.000  6.196   1.963   1.963
## 47    y8 ~1             4.043 0.163 24.741  0.000  4.043   1.244   1.244
## 48 ind60 ~1             0.000 0.000     NA     NA  0.000   0.000   0.000
```

绘制SEM图


```r
library("semPlot")
```

```
## Registered S3 methods overwritten by 'huge':
##   method    from   
##   plot.sim  BDgraph
##   print.sim BDgraph
```

```r
semPaths(fit,whatLabel = "est")
```

![](main_files/figure-docx/unnamed-chunk-3-1.png)<!-- -->



