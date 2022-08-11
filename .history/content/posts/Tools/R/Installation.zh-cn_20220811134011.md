---
title: "R、Rsudio以及相关包的安装"
date: 2021-05-23T11:07:06+08:00
draft: false

description: "工欲善其事，必先利其器。"
upd: "工欲善其事，必先利其器。"

tags: ['笔记', 'R']
categories: ['R语言使用经验']
---

<!--more-->

[安装R与Rstudio](https://zhuanlan.zhihu.com/p/109468400)；[安装R语言（Rstudio、R、RTools）](https://zhuanlan.zhihu.com/p/146289185)

R语言更新，运行以下代码即可：

```R
install.packages("installr")
require(installr)
updateR()
```

在更新时会提示你**是否需要把旧版本里安装过的 R 包复制到新版本里**，可以根据需求选择。

更新R包

```R
update.packages()
```

删除已经安装的包


```R
 remove.packages("name")
```

参考：

- [R语言版本和Rstudio的更新](https://www.jianshu.com/p/5989f295b9e9)；
- [R | 如何更新R版本及Rstudio r更新](https://blog.csdn.net/weixin_41859179/article/details/97570369)


The downloaded source packages are in

‘C:\Users\Wuhao\AppData\Local\Temp\RtmpSWPDov\downloaded_packages’

 

The downloaded binary packages are in

C:\Users\Wuhao\AppData\Local\Temp\RtmpkbO0yi\downloaded_packages


Bug
 

##  各种包

万能的[R包本地安装](https://blog.csdn.net/zdx1996/article/details/86629965)，很多命令不能安装的包都可以通过该方法解决。



[Rtools安装-cnds](https://blog.csdn.net/weixin_42098685/article/details/105864543);[官网](https://cran.rstudio.com/bin/windows/Rtools/)；[官网镜像](https://mirrors.tuna.tsinghua.edu.cn/CRAN/)

 

[TSA安装解决办法](https://blog.csdn.net/chen_dal/article/details/106193038)；[TSA包官网地址](https://cran.r-project.org/src/contrib/Archive/TSA/)；

 

Xlconnect:[Java环境安装](https://www.jianshu.com/p/169bc950316b)；[rjava安装](https://www.cnblogs.com/ohshit/p/6159644.html)；然后直接安装和使用Xlconnect即可

 

[quantstrat安装](https://stackoverflow.com/questions/44891437/install-quantstrat-for-r-latest-r-version)



## Bug

[R语言non-zero exit status处理：非零状态_dltan-CSDN博客](https://blog.csdn.net/tandelin/article/details/87719623)

[compilation failed for package 'X'](https://www.jianshu.com/p/e52a091902d3)