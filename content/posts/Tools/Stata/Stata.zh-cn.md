---
title: "Stata笔记"
date: 2021-06-09T21:17:53+08:00
draft: false

description: "Stata奇技淫巧。"
upd: "Stata奇技淫巧。"

tags: ['笔记', 'Stata']
categories: []
---

<!--more-->


[Stata 矩阵操作](https://www.cnblogs.com/IAMSTARBOY/p/12608994.html)


## Basic

### 外部库

安装/ 更新第三方库

```stata
ssc install eventstudy2, replace
* 更新所有库
update all
```

### 开机设定

```
*-PLUS 和 PERSONAL 文件夹  
*-有关这一部分的完整设定命令，请输入 help set 命令进行查看
  sysdir set PLUS "`c(sysdir_stata)'ado\plus"    // 外部命令的存放位置
  sysdir set PERSONAL "`c(sysdir_stata)'ado\personal"  // 个人文件夹位置

*-采用相似的方式，可添加其它允许stata搜索的目录
  adopath + "`c(sysdir_stata)'\ado\personal\_myado"
 *adopath + "路径2"

*-结果显示格式
set cformat  %4.3f  //回归结果中系数的显示格式
set pformat  %4.3f  //回归结果中 p 值的显示格式      
set sformat  %4.2f  //回归结果中 se值的显示格式     
```

[Stata 开机设定 - profile.do 文档](https://zhuanlan.zhihu.com/p/50554434)

### 注释

Stata 注释，可以通过 `help comments` 查看帮助文档

```
o begin the line with *;
o begin the comment with //; or
o place the comment between /* and */ delimiters.
```
参考：

- [Stata基础：do文档中代码注释的三种姿势](https://www.bilibili.com/video/BV1Qk4y1m7wM/?spm_id_from=333.788&vd_source=72bc6e91029460a37b604a94e554618d)

### 工作目录

```
cd D:\Workfiles
```

### 变量名

```
*变量名stat重命名为status
rename stat status

*将变量名stat和inc重命名为status和income
rename (stat inc) (status income)

*例如，janstat重命名为stat1，janinc重命名为inc1
rename jan* *1
```

[stata命令详解-rename group](https://www.jianshu.com/p/37eaf291eb26)

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

**读取 csv 文件**：直接窗口操作，然后复制并保留代码。

[请问直接导出部分变量到excel的stata命令 - Stata专版 - 经管之家(原人大经济论坛) (pinggu.org)](https://bbs.pinggu.org/thread-7144789-1-1.html)

## 数据预处理

变量类型转换

[数值型字符型转换，destring tostring _stata-数据分析 (cdadata.com)](http://www.cdadata.com/16014)

[Stata入门——合并数据(merge)_哔哩哔哩_bilibili](https://www.bilibili.com/video/av90542118/)

[聊一聊Stata中时间变量的处理 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/103817704)

## 描述统计

[STATA 学习笔记 ：相关系数](https://blog.csdn.net/mpeipeisu/article/details/114668963)


## 时间序列

Hourly

```
tsset time, clocktime delta(1 hour)
```

[【Stata小诀窍】烦人的日期型数据的如何处理？](https://zhuanlan.zhihu.com/p/338320151)

[聊一聊Stata中时间变量的处理](https://zhuanlan.zhihu.com/p/103817704)

[Converting a string date into a tsset format](https://www.statalist.org/forums/forum/general-stata-discussion/general/1342501-converting-a-string-date-into-a-tsset-format)

[如何在stata中生成滞后项、前推项、增长率？](https://jingyan.baidu.com/article/77b8dc7f564ed26174eab618.html)

[stata时间序列操作命令大全——基本命令](https://zhuanlan.zhihu.com/p/41005312)

[stata如何筛选日期？](https://bbs.pinggu.org/thread-4811609-1-1.html)

### VAR

[VAR模型stata建模详细步骤](https://zhuanlan.zhihu.com/p/366069360)

[VAR模型研究USDCNY汇率影响因素（Python）](https://www.jianshu.com/p/e7eee3312aaf)

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

实际上esttab是estout程序的一个命令，你需要安装estout

```
ssc install estout, replace
```

esttab回归结果输出

- [用好 esttab，导遍表格都不怕[中文 rtf 无乱码]](https://www.bilibili.com/read/cv15830360)
- [stata输出命令estout](https://zhuanlan.zhihu.com/p/430119565)
- [esttab功能挖掘：“Yes”or“No” (stata-club.github.io)](https://stata-club.github.io/stata_article/2016-09-14.html)
- [esttab输出结果，如何删除年份以及调整排列顺序 - 统计软件培训班VIP答疑区 - 经管之家(原人大经济论坛) (pinggu.org)](https://bbs.pinggu.org/thread-4198787-1-1.html)
- [合并输出回归结果和其他检验结果——esttab和estadd](https://stata-club.github.io/stata_article/2017-01-19.html)


## 编程

[Doing things quietly in Stata](https://www.techtips.surveydesign.com.au/post/doing-things-quietly-in-stata)


### 循环

`var'多数时候可以直接替代原变量。

```
local sentname CCew CCfw CCqw CCrw VADERew VADERfw VADERqw VADERrw
foreach sent of local sentname {
	quietly{
		var Return `sent' if tin(17aug2017 04:00:00, 01jan2018 00:00:00), lags(1/24)
		vargranger
		estadd scalar sent2return r(gstats)[1,1]
		estadd scalar p1 r(gstats)[1,3]
		estadd scalar return2sent r(gstats)[3,1]
		estadd scalar p2 r(gstats)[3,3]
		est store `sent'_sub1

		var Return `sent' if tin(01jan2018 00:00:00, 01jan2019 00:00:00), lags(1/24)
		vargranger
		estadd scalar sent2return r(gstats)[1,1]
		estadd scalar p1 r(gstats)[1,3]
		estadd scalar return2sent r(gstats)[3,1]
		estadd scalar p2 r(gstats)[3,3]
		est store `sent'_sub2
	}
	
	* Show the results
	esttab `sent'_sub*, replace star(* 0.1 ** 0.05 *** 0.01) ///
	b(%12.3f) se(%12.3f) compress nogap ///
	stats(sent2return p1 return2sent p2 N r2_1, ///
		fmt(%12.3f %12.3f %12.3f %12.3f %12.0f %12.3f) ///
		label("Granger: S → R" "{\i p}-value" "Granger: R → S" "{\i p}-value" ///
			"N" "Adj. {\i R}-squared"))

	* Export the results
	esttab `sent'_sub* using Granger\\`sent'_subperiod.rtf, replace star(* 0.1 ** 0.05 *** 0.01) ///
	b(%12.3f) se(%12.3f) compress nogap ///
	stats(sent2return p1 return2sent p2 N r2_1, ///
		fmt(%12.3f %12.3f %12.3f %12.3f %12.0f %12.3f) ///
		label("Granger: S → R" "{\i p}-value" "Granger: R → S" "{\i p}-value" ///
			"N" "Adj. {\i R}-squared")) ///
		title("Subperiods Granger causality test for `sent'") ///
		mtitles("2017" "2018" "2019" "2020" "2021" "2022") ///
		keep(L*.`sent') 
}
```

### Bug

[factor variables and time-series operators not allowed](https://bbs.pinggu.org/thread-1214045-1-1.html)