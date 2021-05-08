---
title: "Advanced Derivatives Analysis"
date: 2021-03-04T10:30:57+08:00
lastmod: 2021-03-05T10:30:57+08:00
draft: true

description: ""
upd: ""

tags: []
categories: 
---

4月15日，CTP交易系统讲座

## 真格量化

外推收益：样本外区间的收益率

### 模拟交易账号

18702711703

13860133805

- 个股期权初始资金： 200 万。
- 证券初始资金： 200 万。

### 家庭作业5

请以小组为单位，构建一个到期期限约为三周的股票对冲组合（可以借助于一些免费的模拟平台和数据库）。该组合以股票现货为多头（具体选择哪些股票可以自己决定），以股指期货为空头（哪种合约也由自己决定），具体对冲比例需要手动计算。组合建好后，请记录三周左右的组合表现，并形成一份策略报告。报告内容包括**构建过程、成本分析、盈利分析**。

该作业请于5 月 27 日前交给助教。

[股指期货对冲比例](https://zhuanlan.zhihu.com/p/142808944)

### 家庭作业 4：

请使用此前作业2中期货、期权的合约数据（价格、成交量、持仓量等），计算每个品种合约的收益率和波动率。列出并观察各合约每个交易日的前 20 名大户持仓成交排名情况（交易所官方网站有公布，比如：http://www.shfe.com.cn/statements/dataview.html?paramid=kx）。综合以上内容和前期家庭作业，并做跨产品比较分析，撰写一份所在组分配的期货、期权品种的产品研究报告（包括但不限于此前家庭作业中的合约条款、保证金、手续费等要素）。最终结果以PDF形式呈现。

此作业于课程结束时（4 月 15 日晚 12 点前）提交。

### Homework 3

[50ETF期权的隐含波动率 交易分析](http://finance.eastmoney.com/a/201912131322421451.html)

构建交易策略，跟踪交易策略，汇报交易情况，对应的措施，风险管理方法

[真格量化](https://quant.pobo.net.cn/login)：期货期权模拟实盘

上周及今天我们介绍了备兑开仓, 这周四还将介绍牛市价差、熊市价差、蝶式、（宽）跨式、鹰式、转换和反向转换以及盒式套利等期权交易策略。

这次作业要求每组同学运用所学知识，结合实际市场数据，构建两个期权组合策略并作有关分析。注意：

（1）可以任选以上两种策略组合；

（2）必须采用真实期权市场上的交易数据，可以是 ETF期权或股指期权，也可以是商品期权；

（3）要详细说明构建所选策略组合的理由和逻辑；

（4）要观察、分析和记录所选策略组合在这段时期内的收益表现，并根据情况决定是否要进行调整以及如何调整；

（5）要适当考虑真实的市场交易成本，比如买卖价差，手续费，保证金等；

（6）要结合组合表现结果，形成一份具体的投资分析报告，如果仅提交类似 Excel 的表格将视为不合格；

（7）可以使用期权模拟交易平台进行模拟测试，比如东财的 http://qqmoni.eastmoney.com。是否采用可自行决定。

 （8）课程结束时提交本次作业。

一周后的

### Homework 1

[上期所](http://www.shfe.com.cn/) 能源化工7种

请各组就自己分配的期货（期权）品种收集和整理各品种的**合约条款和交易规则**。通过此练习尽快熟悉各大交易所的期货和期权品种。

下周二上课前提交电子版给：hanqian@xmu.edu.cn, 邮件标题请注明组别和负责的品种。

### Homework 2

请每组根据本组被分配的期货和期权品种，下载并统计各个品种及其合约的以下交易信息：

\1. 历史价格走势（日度）；

\2. 历史成交量（日度）；

\3. 历史持仓量（日度）.

注意：（1）数据应包括各品种的连续/连一、连二、连三、连四合约（不同合约的数据请用 excel 的不同 worksheets 储存）。

​          关于何为连续、连二、连三、连四合约，请参见：

​           https://zhidao.baidu.com/question/2207738006065246628.html

​          注意：这里的“连续合约”不一定跟“主力连续合约”相同。主力连续合约是由每天挑选成交量最大的合约拼接而成，但是成交量最大的合约不一定是最近到期的合约。这要视具体品种而定。作业中大家不用管主力连续合约，只需要构建或者下载连续、连二、连三、连四合约即可。

​      （2）样本期长度：选择过去五年的日度数据即可，如果品种交易时间短于五年，则下载和统计所有数据。

​      （3）作业中应包括：原始下载数据、相应描述性统计量、图表。

​      （4）可通过校图书馆万得、CSMAR（国泰安）或其他数据库（如米筐）下载有关数据。

请于下周二上课前提交至助教的电子邮箱：wrkworld@163.com。



Lectures recorded and posted online @ 9am every Monday and Wednesday

Q&As

- hanqian@xmu.edu.cn
- QQ group chat: 834774719


课程简介

Lecture 1: Introduction

- Intro. of global derivatives markets
- “327” Bond futures trading scandal

Lecture 2-6:  Derivatives Theory

- Binomial option pricing models
- Hedging issues associated with options
- Current situation of the Chinese derivatives markets
- Debates about the derivatives’ role and function

Lecture 7-9：How do the options markets perform?

Lecture 10-15: Product design

Lecture 16-20: Commodity futures settlement, Several cases

Lecture 23-26: Leverage of financial institutions

Lecture 27-28: Derivatives use by real economy 

业界讲课

- 期货套期保值案例分析-农产品产业链分析与产业应用
- 期货品种产业链与企业需求分析、套期保值策略案例分析等（大商所农产品品种） 天津三嘉国际贸易有限公司副总经理 王耀
- 商品交割流程及实务经验 商品期货品种交割流程及案例介绍（大商所品种为主）
- 中建材供应链管理有限公司新业务发展部负责人 李秀丽 
    评分标准

Groups: At most 3 persons per group,Each group is responsible for a product design

Grading Policy：一周内提供分组，所有作业都以分组形式完成

- Attendance and participation (30%)
- Homework projects (30%)
- Final project (40%)

期货市场历史相关书籍：

- 姜洋，《发现价格:期货和金融衍生品》，中信出版集团，2019
- 《当代中国期货市场口述史》，大连商品交易所，2019

参考资料

- John Hull, Futures, Options and Other Derivatives, 10 ed.
- 韩乾、薛晓明译，《金融衍生品：资本、货币与竞争》，北京大学出版社，2020 年：从人文科学角度来理解衍生品
     https://weidian.com/item.html?itemID=3346629674&spider_token=88ca