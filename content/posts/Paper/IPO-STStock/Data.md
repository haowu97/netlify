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

## 逆向回购数据

同花顺IFind：一般采用IFind

瑞思数据库：有

Wind：有



CSMAR：难以识别





We start with a sample of 260 RMs that are announced from January 1st, 2007 to April 30th, 2016.11 We manually collect their RM proposals from [巨潮资讯](http://www.cninfo.com.cn/), a CSRC authorized information disclosure website that collects documents and filings of listed firms.



**We start from 2007 for two reasons**. First, the split-share reform was completed at the end of 2006. In many cases, major corporate restructuring was a necessary part of the split-share reform (see, e.g., Liao et al., 2014). Although some restructuring cases meet the RM definition, the nature of the transaction is different from a regular RM. Second, CSRC set up the Mergers and Acquisition Committee in July 2007 as a formal legal entity to supervise the mergers and acquisitions of listed firms, and it represents a major regime change in the regulation.

需要排除的样本：

1. we **excluded 78 deals that are either still in process or have failed**.
2. We also drop 50 deals in which the unlisted firms had acquire shares of the listed firm over time before a RM announcement, because the shell value is difficult to estimate in such case.
3. We further exclude 5 deals in which no new shares are issued. These deals are among SOEs, and the listed firms issue debt to unlisted firms.
4. Finally, we exclude 3 deals in which there are transferred shares from listed firms to unlisted firms but the transferred price is not reported

In the end, we have 137 clean RMs, of which 134 had the information needed to calculate the shell value