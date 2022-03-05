估算壳价值所需要的上市公司数据

2011至今

| MV      | 市值                                                         |      |
| ------- | ------------------------------------------------------------ | ---- |
| SOE     | 是否为国企， 是取1， 否则取0                                 | √    |
| Rsize   | log( 上市公司市值/沪深300 公司的总市值) the logarithm ratio of the firm’s market value to the median market equity of the market | √    |
| ROA     | 经营利润率 operating profit to assets ( 营业收入－ 营业成本－ 销售费用－ 管理费用－ 营业税金及附加) /总资产 | √    |
| sales_g | 主营业务收入增长率                                           | √    |
| ST      | 如果企业被ST 处理则取1，否则取0                              | √    |
| IPO_rej | IPO 拒绝率，等于1 － ( 通过IPO 审核的企业数量/上会的总企业数量) |      |
| insider | 内部人持股比例，等于董事会、监事会和高管持有的股份比例之和（csmar[公司研究系列 ](http://cndata1.csmar.com/csmar.html?v=1645616383749#/datacenter/singletable?serId=3)**/**[治理结构](http://cndata1.csmar.com/csmar.html?v=1645616383749#/datacenter/singletable/search?databaseId=14)） | √    |
| ret     | 前12 个月股票相对于市场的超额收益率                          | √    |



借壳上市成功案例

|      | 借壳上市公告 | 借壳上市成功 |
| ---- | ------------ | ------------ |
| 2007 | 8            | 7            |
| 2008 | 16           | 8            |
| 2009 | 19           | 14           |
| 2010 | 22           | 16           |
| 2011 | 32           | 26           |
| 2012 | 29           | 21           |
| 2013 | 24           | 18           |
| 2014 | 30           | 24           |
| 2015 | 48           | 34           |
| 2016 | 35           | 29           |
| 2017 | 16           | 8            |
| 2018 | 7            | 5            |
| 2019 | 17           | 9            |
| 2020 | 14           | 6            |

以最新公告日期为准

## 样本数据

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

## 2012版证监会行业分类

[证监会发布上市公司行业分类指引 _ 东方财富网 (eastmoney.com)](https://finance.eastmoney.com/news/1345,20121116259599843.html)

| 代码 | 类别名称 | 说明                                                 |                                                              |
| ---- | -------- | ---------------------------------------------------- | ------------------------------------------------------------ |
| 门类 | 大类     |                                                      |                                                              |
| A    |          | 农、林、牧、渔业                                     | 本门类包括01~05大类                                          |
|      | 01       | 农业                                                 | 指对各种农作物的种植                                         |
|      | 02       | 林业                                                 |                                                              |
|      |          |                                                      |                                                              |
|      | 030405   | 畜牧业渔业农、林、牧、渔服务业                       | 指为了获得各种畜禽产品而从事的动物饲养、捕捉活动             |
| B    |          | 采矿业                                               | 本门类包括06~12大类，采矿业指对固体(如煤和矿物)、液体(如原油)或气体(如天然气)等自然产生的矿物的采掘；包括地下或地上采掘、矿井的运行，以及一般在矿址或矿址附近从事的旨在加工原材料的所有辅助性工作，例如碾磨、选矿和处理，均属本类活动；还包括使原料得以销售所需的准备工作；不包括水的蓄集、净化和分配，以及地质勘查、建筑工程活动 |
|      | 06       | 煤炭开采和洗选业                                     | 指对各种煤炭的开采、洗选、分级等生产活动；不包括煤制品的生产和煤炭勘探活动 |
|      | 07       | 石油和天然气开采业                                   | 指在陆地或海洋，对天然原油、液态或气态天然气的开采，对煤矿瓦斯气(煤层气)的开采；为运输目的所进行的天然气液化和从天然气田气体中生产液化烃的活动，还包括对含沥青的页岩或油母页岩矿的开采，以及对焦油沙矿进行的同类作业 |
|      | 08       | 黑色金属矿采选业                                     |                                                              |
|      | 09       | [有色金属](http://topic.eastmoney.com/ysjr/)矿采选业 | 指对常用有色金属矿、贵金属矿，以及稀有稀土金属矿的开采、选矿活动 |
|      | 10       | 非金属矿采选业                                       |                                                              |
|      | 11       | 开采辅助活动                                         | 指为煤炭、石油和天然气等矿物开采提供的服务                   |
|      | 12       | 其他采矿业                                           |                                                              |
| C    |          | 制造业                                               | 本门类包括13~43大类，指经物理变化或化学变化后成为新的产品，不论是动力机械制造，还是手工制作；也不论产品是批发销售，还是零售，均视为制造建筑物中的各种制成品、零部件的生产应视为制造，但在建筑预制品工地，把主要部件组装成桥梁、仓库设备、铁路与高架公路、升降机与电梯、管道设备、喷水设备、暖气设备、通风设备与空调设备，照明与安装电线等组装活动，以及建筑物的装置，均列为建筑活动本门类包括机电产品的再制造，指将废旧汽车零部件、工程机械、机床等进行专业化修复的批量化生产过程，再制造的产品达到与原有新产品相同的质量和性能 |
|      | 13       | 农副食品加工业                                       | 指直接以农、林、牧、渔业产品为原料进行的谷物磨制、饲料加工、植物油和制糖加工、屠宰及肉类加工、水产品加工，以及蔬菜、水果和坚果等食品的加工 |
|      | 14       | 食品制造业                                           |                                                              |
|      | 15       | 酒、饮料和精制茶制造业                               |                                                              |
|      | 16       | 烟草制品业                                           |                                                              |
|      | 17       | 纺织业                                               |                                                              |
|      | 18       | 纺织服装、服饰业                                     |                                                              |
|      | 19       | 皮革、毛皮、羽毛及其制品和制鞋业                     |                                                              |
|      | 20       | 木材加工和木、竹、藤、棕、草制品业                   |                                                              |
|      | 21       | 家具制造业                                           | 指用木材、金属、塑料、竹、藤等材料制作的，具有坐卧、凭倚、储藏、间隔等功能，可用于住宅、旅馆、办公室、学校、餐馆、医院、剧场、公园、船舰、飞机、机动车等任何场所的各种家具的制造 |
|      | 22       | 造纸和纸制品业                                       |                                                              |
|      | 23       | 印刷和记录媒介复制业                                 |                                                              |
|      | 24       | 文教、工美、体育和娱乐用品制造业                     |                                                              |
|      | 25       | 石油加工、炼焦和核燃料加工业                         |                                                              |
|      | 26       | 化学原料和化学制品制造业                             |                                                              |
|      | 27       | 医药制造业                                           |                                                              |
|      | 28       | 化学纤维制造业                                       |                                                              |
|      | 29       | 橡胶和塑料制品业                                     |                                                              |
|      | 30       | 非金属矿物制品业                                     |                                                              |
|      | 31       | 黑色金属冶炼和压延加工业                             |                                                              |
|      | 32       | 有色金属冶炼和压延加工业                             |                                                              |
|      | 33       | 金属制品业                                           |                                                              |
|      | 34       | 通用设备制造业                                       |                                                              |
|      | 35       | 专用设备制造业                                       |                                                              |
|      | 36       | 汽车制造业                                           |                                                              |
|      | 37       | 铁路、船舶、航空航天和其他运输设备制造业             |                                                              |
|      | 38       | 电气机械和器材制造业                                 |                                                              |
|      | 39       | 计算机、通信和其他电子设备制造业                     |                                                              |
|      | 40       | 仪器仪表制造业                                       |                                                              |
|      | 41       | 其他制造业                                           |                                                              |
|      | 42       | 废弃资源综合利用业                                   | 指废弃资源和废旧材料回收加工                                 |
|      | 43       | 金属制品、机械和设备修理业                           |                                                              |
| D    |          | 电力、热力、燃气及水生产和供应业                     | 本门类包括44~46大类                                          |
|      | 44       | 电力、热力生产和供应业                               |                                                              |
|      | 45       | 燃气生产和供应业                                     |                                                              |
|      | 46       | 水的生产和供应业                                     |                                                              |
| E    |          | 建筑业                                               | 本门类包括47~50大类                                          |
|      | 47       | 房屋建筑业                                           |                                                              |
|      | 48       | 土木工程建筑业                                       | 指土木工程主体的施工活动；不包括施工前的工程准备活动         |
|      | 49       | 建筑安装业                                           | 指建筑物主体工程竣工后，建筑物内各种设备的安装活动，以及施工中的线路敷设和管道安装活动；不包括工程收尾的装饰，如对墙面、地板、天花板、门窗等处理活动 |
|      | 50       | 建筑装饰和其他建筑业                                 |                                                              |
| F    |          | 批发和零售业                                         | 本门类包括51和52大类，指商品在流通环节中的批发活动和零售活动 |
|      |          |                                                      |                                                              |
|      | 51       | 批发业                                               | 指向其他批发或零售单位(含个体经营者)及其他企事业单位、机关团体等批量销售生活用品、生产资料的活动，以及从事[进出口](http://data.eastmoney.com/cjsj/hgjck.html)贸易和贸易经纪与代理的活动，包括拥有货物所有权，并以本单位(公司)的名义进行交易活动，也包括不拥有货物的所有权，收取佣金的商品代理、商品代售活动；本类还包括各类商品批发市场中固定摊位的批发活动，以及以销售为目的的收购活动 |
|      | 52       | 零售业                                               | 指百货商店、超级市场、专门零售商店、品牌专卖店、售货摊等主要面向最终消费者(如居民等)的销售活动，以互联网、邮政、电话、售货机等方式的销售活动，还包括在同一地点，后面加工生产，前面销售的店铺(如面包房)；谷物、种子、饲料、牲畜、矿产品、生产用原料、化工原料、农用化工产品、机械设备(乘用车、计算机及通信设备除外)等生产资料的销售不作为零售活动；多数零售商对其销售的货物拥有所有权，但有些则是充当委托人的代理人，进行委托销售或以收取佣金的方式进行销售 |
| G    |          | 交通运输、仓储和邮政业                               | 本门类包括53~60大类                                          |
|      | 53       | 铁路运输业                                           | 指铁路客运、货运及相关的调度、信号、机车、车辆、检修、工务等活动；不包括铁路系统所属的机车、车辆及信号通信设备的制造厂(公司)、建筑工程公司、商店、学校、科研所、医院等活动 |
|      | 54       | 道路运输业                                           |                                                              |
|      | 55       | 水上运输业                                           |                                                              |
|      | 56       | 航空运输业                                           |                                                              |
|      | 57       | 管道运输业                                           |                                                              |
|      | 58       | 装卸搬运和运输代理业                                 |                                                              |
|      | 59       | 仓储业                                               | 指专门从事货物仓储、货物运输中转仓储，以及以仓储为主的货物送配活动，还包括以仓储为目的的收购活动 |
|      | 60       | 邮政业                                               |                                                              |
| H    |          | 住宿和餐饮业                                         | 本门类包括61和62大类                                         |
|      | 61       | 住宿业                                               | 指为旅行者提供短期留宿场所的活动，有些单位只提供住宿，也有些单位提供住宿、饮食、商务、娱乐一体的服务，本类不包括主要按月或按年长期出租房屋住所的活动 |
|      | 62       | 餐饮业                                               | 指通过即时制作加工、商业销售和服务性劳动等，向消费者提供食品和消费场所及设施的服务 |
| I    |          | 信息传输、软件和信息技术服务业                       | 本门类包括63~65大类                                          |
|      | 63       | 电信、广播电视和卫星传输服务                         |                                                              |
|      | 64       | 互联网和相关服务                                     |                                                              |
|      | 65       | 软件和信息技术服务业                                 | 指对信息传输、信息制作、信息提供和信息接收过程中产生的技术问题或技术需求所提供的服务 |
| J    |          | 金融业                                               | 本门类包括66~69大类                                          |
|      | 66       | 货币金融服务                                         |                                                              |
|      | 67       | 资本市场服务                                         |                                                              |
|      | 68       | 保险业                                               |                                                              |
|      | 69       | 其他金融业                                           |                                                              |
| K    |          | 房地产业                                             | 本门类包括70大类                                             |
|      | 70       | 房地产业                                             |                                                              |
| L    |          | 租赁和商务服务业                                     | 本门类包括71和72大类                                         |
|      | 71       | 租赁业                                               |                                                              |
|      | 72       | 商务服务业                                           |                                                              |
| M    |          | 科学研究和技术服务业                                 | 本门类包括73~75大类                                          |
|      |          |                                                      |                                                              |
|      | 73       | 研究和试验发展                                       | 指为了增加知识(包括有关自然、工程、人类、文化和社会的知识)，以及运用这些知识创造新的应用，所进行的系统的、创造性的活动；该活动仅限于对新发现、新理论的研究，新技术、新产品、新工艺的研制研究与试验发展，包括基础研究、应用研究和试验发展 |
|      | 74       | 专业技术服务业                                       |                                                              |
|      | 75       | 科技推广和应用服务业                                 |                                                              |
| N    |          | 水利、环境和公共设施管理业                           | 本门类包括76~78大类                                          |
|      | 76       | 水利管理业                                           |                                                              |
|      | 77       | 生态保护和环境治理业                                 |                                                              |
|      | 78       | 公共设施管理业                                       |                                                              |
| O    |          | 居民服务、修理和其他服务业                           | 本门类包括79~81大类                                          |
|      | 79       | 居民服务业                                           |                                                              |
|      | 80       | 机动车、电子产品和日用产品修理业                     |                                                              |
|      | 81       | 其他服务业                                           |                                                              |
| P    |          | 教育                                                 | 本门类包括82大类                                             |
|      | 82       | 教育                                                 |                                                              |
| Q    |          | 卫生和社会工作                                       | 本门类包括83和84大类                                         |
|      | 83       | 卫生                                                 |                                                              |
|      | 84       | 社会工作                                             | 指提供慈善、救助、福利、护理、帮助等社会工作的活动           |
| R    |          | 文化、体育和娱乐业                                   | 本门类包括85~89大类                                          |
|      | 85       | 新闻和出版业                                         |                                                              |
|      | 86       | 广播、电视、电影和影视录音制作业                     | 指对广播、电视、电影、影视录音内容的制作、编导、主持、播出、放映等活动；不包括广播电视信号的传输和接收活动 |
|      | 87       | 文化艺术业                                           |                                                              |
|      | 88       | 体育                                                 |                                                              |
|      | 89       | 娱乐业                                               |                                                              |
| S    |          | 综合                                                 | 本门类包括90大类                                             |
|      | 90       | 综合                                                 |                                                              |



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
