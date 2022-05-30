---
title: "Stata笔记"
date: 2021-06-09T21:17:53+08:00
lastmod: 2021-06-10T21:17:53+08:00
draft: false

description: ""
upd: "Stata奇技淫巧"

tags: ['笔记', 'Stata']
categories: []

math: true
---

## 学习资源

[Stata Cheat Sheet 2021](https://www.stata.com/bookstore/statacheatsheets.pdf)

[UCLA 教程](https://stats.oarc.ucla.edu/)

[陈强教授的计量经济学及Stata主页 (econometrics-stata.com)](http://www.econometrics-stata.com/)

## 快捷操作

`Ctrl+L`：选中一行

**`Ctrl+D`:** D 就是 do的意思，do文件中在选中了目标命令之后 `Ctrl+D` 便可以执行；若不选中具体命令，则执行全部命令。

[【Stata写论文】Stata 17可以大幅提高效率的快捷键有哪些？ - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/377150995)

[Stata15快捷键：键盘就是你的武器 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/29728762)

[stata显示存储的变量 - 简书 (jianshu.com)](https://www.jianshu.com/p/ea9e11615f1f)

## 数据输入输出

[请问直接导出部分变量到excel的stata命令 - Stata专版 - 经管之家(原人大经济论坛) (pinggu.org)](https://bbs.pinggu.org/thread-7144789-1-1.html)

## 数据预处理

变量类型转换

[数值型字符型转换，destring tostring _stata-数据分析 (cdadata.com)](http://www.cdadata.com/16014)

[Stata入门——合并数据(merge)_哔哩哔哩_bilibili](https://www.bilibili.com/video/av90542118/)

[聊一聊Stata中时间变量的处理 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/103817704)

## 回归

### 聚类稳健标准误

vce(robust) 和 vce(cluster) 等价，均给出面板稳健标准误——同时考虑了残差的异方差 和序列相关性问题。

vce(cluster groupvar) 还可以指定按组类计算聚类标准误。

### 引入交乘项

两种方法完全等价

- 法一：虚拟变量前加i，连续变量前加c
- 法二：直接生成乘积变量

```
// 方法一
reg Q c.Pr_Shell##i.ST controls, robust

//方法二
gen cross1 = Pr_Shell*ST
reg Q Pr_Shell ST cross1 controls, robust
```

### 模型选择

[Stata: AIC / BIC / MSE / MAE 等信息准则的计算_arlionn的博客-CSDN博客_信息准则](https://blog.csdn.net/arlionn/article/details/95541749)

[关于root mse? - Stata专版 - 经管之家(原人大经济论坛) (pinggu.org)](https://bbs.pinggu.org/thread-378753-1-1.html)

### 结果导出

esttab回归结果输出

- [esttab功能挖掘：“Yes”or“No” (stata-club.github.io)](https://stata-club.github.io/stata_article/2016-09-14.html)
- [esttab输出结果，如何删除年份以及调整排列顺序 - 统计软件培训班VIP答疑区 - 经管之家(原人大经济论坛) (pinggu.org)](https://bbs.pinggu.org/thread-4198787-1-1.html)



更新第三方库

```stata
ssc install eventstudy2, replace
* 更新所有库
update all
```

