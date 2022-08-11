---
title: "GitHub使用经验汇总"
date: 2021-02-17T18:07:31+08:00
draft: False

description: ""
upd: "git是一个非常好用的分布式版本管理工具，功能比svn强大，与SVN不同点是Git去中心化，每一个分支都是一个中心，并且支持本地仓库存储，像如今很多大公司都用git做版本控制。"

tags: []
categories: []
---

git是一个非常好用的分布式版本管理工具，功能比svn强大，与SVN不同点是Git去中心化，每一个分支都是一个中心，并且支持本地仓库存储，像如今很多大公司都用git做版本控制。

<!--more-->


git拉取远程代码

```java
git clone  https://xxx.git
```

git拉取远程指定分支下代码（-b 分支名称）

```java
git clone -b v2.8.1 https://xxx.git
```

初始化一个本地仓库，在同级目录下会出现一个隐藏的.git文件

```csharp
git init
```

## `.gitignore`

忽略指定文件/目录

```
# 忽略指定文件
filename.md

# 忽略指定文件夹
public/
```

[Git 修改.gitignore如何生效？](https://blog.csdn.net/weixin_41287260/article/details/89787203)


[GitHub上如何创建文件夹](https://blog.csdn.net/y_bccl27/article/details/87980986)

## 权限管理

[Github上怎么修改别人的项目并且提交给原作者！图文并茂！](https://blog.csdn.net/qq_26787115/article/details/52133008)

[GitHub给队友开放仓库权限](https://blog.csdn.net/qq_40306266/article/details/107906817)

[Organization权限管理](https://blog.csdn.net/Q85038427/article/details/115748308)

## 关于仓库容量

建议仓库保持较小，理想情况下小于 1 GB，强烈建议小于 5 GB。

查看仓库大小，点`settings-->repositories`进入[链接](https://github.com/settings/repositories)。参考：[查看GitHub仓库大小的几种方法](https://blog.csdn.net/weixin_41287260/article/details/101224658)

官方文档[GitHub仓库大小限制](https://docs.github.com/cn/repositories/working-with-files/managing-large-files/about-large-files-on-github)