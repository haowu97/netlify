---
title: "Typora配置Picgo+Github图床"
date: 2021-03-04T18:58:21+08:00
lastmod: 2021-03-04T18:57:57+08:00
draft: false

description: ""
upd: ""

tags: ['Typora', '图床']
categories: []
---

因为七牛云需要自己的域名，所以放弃使用，转而使用Github作为图床。

## 1. Picgo+Github图床

[Picgo下载地址](https://github.com/Molunerfinn/PicGo/releases)，下载exe文件然后安装即可

[Github+Picgo图床配置方法](https://picgo.github.io/PicGo-Doc/zh/guide/config.html#github图床)(官方文档)

### 1.1 补充说明

自定义域名设定：jsDelivr     默认要直接在仓库名后面 @ ，所以真正其是 https://cdn.jsdelivr.net/gh/username/repo@branch/file 的形式。当然，如果你放在仓库的默认分支，还可以直接将 branch 这个关键字直接删了，变成 https://cdn.jsdelivr.net/gh/username/repo/file 一样能获取到！所以 GitHub 图床设置中将链接设置为 https://cdn.jsdelivr.net/gh/username/repo 

### 1.2 Bug

**图床指定的存储路径必须提前创建好**

错误：{"success",false}：原因是文件名冲突了，如果你上传过一张image1.jpg的图片，再上传名称一样的图片就会失败；**打开picgo设置，将【时间戳重命名】打开，如果该错误仍然出现，尝试勾选【上传前重命名】**

报错：failed to launch Picgo App，可能是因为App路径中存在空格等不被识别的路径字符，**建议安装在没有空格的路径下**

**Failed to fetch**，解决方法：打开picgo设置，点击设置Server选项，将端口改为36677端口，这是picgo推荐的默认端口号。

 图片不显示 Package size exceeded the configured limit of 50 MB问题解决方案：

https://blog.csdn.net/weixin_43571641/article/details/109817266

## 2.Typora配置修改

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210303191458.png)

**配置信息示例**

```
Henrry-Wu/FigBed
master
Figs/
https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed
```

