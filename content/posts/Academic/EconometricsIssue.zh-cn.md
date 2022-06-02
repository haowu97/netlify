---
title: "计量经济学问题汇总"
date: 2021-05-31T14:14:45+08:00
draft: true

description: ""
upd: "计量好难啊！"

tags: ["学术"]
categories: []
---



[混合截面数据和面板数据有什么区别？ - 知乎 (zhihu.com)](https://www.zhihu.com/question/302837292)

[DID大法续论 | 听说混合截面数据也能做DID - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/343081715)

[非平衡面板数据与混合横截面数据(pool data)有什么区别? - 第2页 - 爱问频道 - 经管之家(原人大经济论坛) (pinggu.org)](https://bbs.pinggu.org/thread-1344786-2-1.html)

[笔记 | 杂谈控制固定效应这件事，控制固定效应什么意思](https://blog.csdn.net/Claire_chen_jia/article/details/116244528)

[行业固定还是公司固定效应？ - 知乎 (zhihu.com)](https://www.zhihu.com/question/324046090)

## 稳健标准误

异方差稳健标准误robust

- 可以修正异方差
- 适用于截面数据
- 别名White(1980)标准误

聚类稳健标准误cluster

- 可以修正异方差与组内自相关
- 适用于面板数据

稳健标准误在回归结果表格中说明

```
注：括号内为聚类至公司层面的稳健标准误，*、**、***分别表示在10%、5%和1%水平上显著。
```



