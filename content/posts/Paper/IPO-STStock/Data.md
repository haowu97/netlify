CSMAR，提供创业板/科创板的因子数据，但是3个月定存利率需要自己下载并转换为日度

 

在计算收益率时，需要区分的是“**考虑现金红利再投资**”的收益率，和“**不考虑现金红利再投资**”的收益率。“考虑现金红利再投资”的收益称为累积收益； “不考虑现金红利再投资”的收益称为持有期收益。在**计算日收益率时，两种收益率算法得出的值相同**。

 

锐思数据比较全且全面，但是不提供提供创业板/科创板的因子数据，仅提供全市场的因子数据。

 ![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/Figs/20210508095243.png)





上市公司数据：CSMAR

IPO sample is from CSMAR

CSMAR: resumes of firms' executives and directors from，政治关联度

six main levels in the Chinese bureaucracy: 

- ministry (bu), 
- department (ju), 
- division (chu), 
- section(ke), 
- staff member (keyuan), 
- and clerk (banshiyuan).

Following the literature (e.g., Haveman et al., 2017), we define an executive or director as being politically connected if she or he has served as a chief or deputy-chief at the division level or above. We then construct a dummy variable (PC) that is equal to 1 if a firm has at least one executive or director with political connection, and 0 otherwise. In addition to the dummy variable, we construct the number of political connections (PC Percent), which is the ratio of the number of politically connected executives and directors over the total number of executives and directors. Prior evidence suggests that the political connections of independent directors are irrelevant (e.g., Chen et al., 2011), so we exclude independent directors. However, none of our results are affected if we include them.

## 逆向并购数据

同花顺IFind：一般采用IFind

- 预案公告日：2006年1月1日--2021年10月11日

瑞思数据库：有

Wind：有



CSMAR：难以识别收购类型



### Going public in China: Reverse mergers versus IPOs

The financial and stock returns data of listed firms are from the China Stock Market and Accounting Research (CSMAR) Database.

All variables are winsorized at 1% level in each period.

Our initial RM sample is from the iFinD database provided by Tong Hua Shun (THS), a major financial data service company inChina. THS identifies each RM by following the CSRC definition for these transactions. Specifically, THS checks whether a proposed
business combination between a listed and an unlisted firm involves: 

1. (i) a change in the control right of the listed firm and 
2. (ii) atransaction value larger than the book value of the total assets of the listed firm before the announcement. 

If both conditions are met, the transaction is deemed to be an RM.

In some special cases, THS slightly modifies the CRSC criteria. First, if both the listed and unlisted firms are ultimately owned by the state, THS looks for a change in the controlling unit within the government. This ensures that a change in control from one branch of government to another is reflected in the RM sample. Second, THS includes deals where the transaction value is slightly less than the value of listed firms' total assets. This is the case when the listed firm makes a clear statement that the deal is an RM and is subject to CSRC regulations.

We begin with a sample of **248 RMs announced from January 2007 to December 2015**. We then manually collect financial information on each RM proposal from www.cninfo.com.cn, a CSRC-authorized website that archives documents and filings for listed firms. We **drop 68 transactions where the unlisted firms had acquired shares of the listed firm over time before the RM announcement**, because in such transactions post-listing performance is ambiguous. We also exclude **47 transactions that are either in process or had failed**. The final sample consists of 133 clean RMs.



![image-20211011173952904](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20211011173952904.png)

In our sample period, the CSRC suspended the IPO approval process three times. During a suspension, no IPOs were approved and no new IPO applications were accepted. Specifically, the three suspension periods were: (1) October 2008 to June 2009; (2) October 2012 to March 2014; and, (3) August 2015 to October 2015. For ease of reference, any calendar year that had been affected, in whole or in part, by an IPO suspension is shaded in gray.

![image-20211011174010295](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20211011174010295.png)	

### Reverse Mergers, Shell Value, and Regulation Risk in Chinese Equity Markets*

The financial data and stock returns data of listed firms are from the **China Stock Market and Accounting Research (CSMAR)** Database. We **exclude firms in Chinext board**.（ChiNext is an exchange established expressly for younger, riskier, start-up firms. CSRC regulations forbid firm listed in ChiNext from participating in RMs.）

**The initial RM sample is from Tong Hua Shun (THS)**, a major financial data service company in China. THS collects the RM sample generally by following the CSRC definition for reverse mergers.10 In particular, THS checks whether a proposed deal has the following two characteristics. First, the control right of the listed firm is changed. Second, the transaction value is larger than the book value of total assets of the listed firm prior to the announcement of the deal.

**We use several ways to cross-validate the THS sample**. First, we get a RM sample from WIND, another major financial data vendor in China. We find that the RM in THS is more comprehensive and accurate. We also check the data from CSMAR. We find the CSMAR data often misclassify or miss the shell transactions. Second, we collect the financial analyst reports on shell firms, and we also consult practitioners at investment banks. We find the THS sample is comprehensive and accurate.

In some special cases, **THS slightly modifies the CRSC criteria**. First, if both the listed firm and the unlisted firm are ultimately owned by the state, THS looks at the change of the controlling shareholders instead the change of ultimate control right. This ensures a change in control from one branch of government to another will be reflected in the RM sample. Second, THS will include some deals in which the transaction value is only slightly less than the value of listed firms’ total assets. This would be the case if the listed firm makes a clear statement that the deal is a RM and is subject to CSRC regulations.



We start with a sample of 260 RMs that are announced from **January 1st, 2007 to April 30th, 2016**.11 We manually collect their RM proposals from [巨潮资讯](http://www.cninfo.com.cn/), a CSRC authorized information disclosure website that collects documents and filings of listed firms. These proposals, which average about 700 to 1000 pages, describe the RM transaction in detail. We read each proposal and extract the information needed to calculate shell value.

**We start from 2007 for two reasons**. First, the split-share reform was completed at the end of 2006. In many cases, major corporate restructuring was a necessary part of the split-share reform (see, e.g., Liao et al., 2014). Although some restructuring cases meet the RM definition, the nature of the transaction is different from a regular RM. Second, CSRC set up the Mergers and Acquisition Committee in July 2007 as a formal legal entity to supervise the mergers and acquisitions of listed firms, and it represents a major regime change in the regulation.

需要排除的样本：

1. we **excluded 78 deals that are either still in process or have failed**.
2. We also drop 50 deals in which the unlisted firms had acquire shares of the listed firm over time before a RM announcement, because the shell value is difficult to estimate in such case.
3. We further exclude 5 deals in which no new shares are issued. These deals are among SOEs, and the listed firms issue debt to unlisted firms.
4. Finally, we exclude 3 deals in which there are transferred shares from listed firms to unlisted firms but the transferred price is not reported

In the end, we have 137 clean RMs, of which 134 had the information needed to calculate the shell value

![image-20211011174707621](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20211011174707621.png)

we first calculate an “expected shell value to market” (ESVM) variable for each firm at the
beginning of May in each year. ESVM is defined as ESP × Avg_SV2 / ME. Avg_SV2 is the
average SV2 value at the beginning of the current quarter. ME is the market value of equity
of the listed firm and is winsorized at 5% level for each tail every year in the ESVM
calculation. ESP is the expected shell probability, which is the predicted value from a rolling
logit regression using past 4 years of data with the specification in Column (1) of Table 4. In
each rolling regression

### IPO 还是借壳：什么影响了中国企业的上市选择？*

本文的样本由借壳上市企业和IPO企业两部分组成，样本区间为2007~2015 年。借壳上市样本来自于手工搜集。根据中国证监会的界定和监管标准，借壳上市需同时满足两个条件：

1. （1）控制权发生变更。
2. （2）交易标的总资产占上市公司控制权变更前一年度上市公司总资产的100%以上。

控制权发生变更一般是指实际控制人变更，但国资委控制下的企业很多，当涉及实际控制人是国资委的时候，本文以控股股东是否变更来判断控制权是否发生变更。另外，对于那些虽然注入资产比例不足100%，但在公告中明确说明其交易类型为借壳上市并接受证监会相关监管的交易，本文也认为其属于借壳上市。



为了研究中国企业的上市方式选择问题，本文手工搜集和整理了2007~2015年的借壳上市样本以及企业在上市前的财务数据，并与IPO 企业进行比较。

本文发现借壳上市数量与IPO上市数量的总体变化趋势相反，特别是IPO 暂停期间，借壳上市数量有明显上升，这说明在**中国企业更多地将借壳上市作为IPO 上市的一种替代手段**，而Brau 等（2003）和Gleason 等（2005）发现美国借壳上市和IPO 上市呈现同向变化趋势，在IPO 市场火热时借壳上市的数量也更多。

本文还发现**借壳企业与IPO企业的行业分布有显著差异**，借壳企业的行业分布比IPO 企业的行业分布更加分散，并且在证监会对IPO 限较多的行业（如房地产行业），借壳上市的企业较多。

**证监会的行业分类**：[上市公司行业分类指引 (csrc.gov.cn)](http://www.csrc.gov.cn/pub/newsite/scb/ssgshyfljg/201304/t20130402_223007.html)

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20211011174155854.png)

本文共识别了252例借壳交易作为初始的研究样本，并**进行如下筛选**：

1. 剔除交易尚未完成或在随后的公告中宣布失败的样本；
2. 剔除在资产注入前非上市公司就已经取得上市公司股权的样本；
3. 剔除交易报告中会计信息缺失的样本。

经过上述筛选后，本文共得到136个成功借壳上市的样本。





### 上市公司売价值与资源配置效

本文选取2006年到2015年的所有上市公司作为研究样本，并**剔除了金融企业**。另外，由于证监会规定创业板企业不能被借壳，因此我们在样本中剔除了创业板公司。

为了计算壳价值含量指标(ESV/MV),我们还搜集了样本区间内所有借壳上市样本及其相关交易信息。上市公司的财务数据和股票交易数据来自于 CSMAR数据库，借売交易相关信息来自于手工搜集的上市公司交易公告。



### 数据申请邮件



Dear Prof. Yuanyu Qu:

Thank you for reading!

I am Hao Wu, a Master of Finance student from School of Economics, Xiamen University in China.

I am very interested in your publication entitled "[Going public in China: Reverse mergers versus IPOs](https://www.sciencedirect.com/science/article/pii/S0929119918302487?via%3Dihub)", published in *Journal of Corporate Finance* on April 12th  2019. You and your team did a lot of excellent related work and gave me a lot of inspiration.

I want to do some further research based on your estimation methods of shell values. Since your RM samples covered from January 2007 to December 2015, to keep the model updated, I am going to add recent RM samples to the datasets. I have started collecting data following the procedures in your paper, but I am still afraid of making same mistakes during the whole complicated process. 

**So I am wondering if you could kindly send me the datasets including the RM samples and their shell value.** I promise to use it only for research and it is absolutely confidential. If it is not convenient, I hope that you will not be angry for my unreasonable request.

Thank you very much for your kind consideration and I am looking forward to your early reply.

All the best,

Hao Wu
