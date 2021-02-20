---
title: "GitHub使用方法汇总"
date: 2021-02-17T18:07:31+08:00
draft: False

description: ""
upd: ""
---

git是一个非常好用的分布式版本管理工具，功能比svn强大，与SVN不同点是Git去中心化，每一个分支都是一个中心，并且支持本地仓库存储，像如今很多大公司都用git做版本控制。：


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