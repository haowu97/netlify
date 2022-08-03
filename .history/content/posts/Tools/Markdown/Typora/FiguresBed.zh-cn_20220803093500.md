---
title: "Typora配置Picgo图床"
date: 2021-03-04T18:58:21+08:00
draft: false

description: "Github、Gitee图床。"
upd: "Github、Gitee图床。"

tags: ['Typora', 'Markdown']
categories: []
---

<!--more-->

因为七牛云需要自己的域名，所以放弃使用，转而使用Github作为图床。

最近Github的图床需要科学上网才能显示，但好过Gitee图床时不时抽风不能显示。

尝试了[Markdown Nice](https://editor.mdnice.com/)平台的Github图床成功了(**需要科学上网**)。

# Picgo+Github图床

[Picgo下载地址](https://github.com/Molunerfinn/PicGo/releases)，下载exe文件然后安装即可

[Github+Picgo图床配置方法](https://picgo.github.io/PicGo-Doc/zh/guide/config.html#github图床)(官方文档)


## 补充说明

自定义域名设定：jsDelivr  默认要直接在仓库名后面 @ ，所以真正其是 https://cdn.jsdelivr.net/gh/username/repo@branch/file 的形式。当然，如果你放在仓库的默认分支，还可以直接将 branch 这个关键字直接删了，变成 https://cdn.jsdelivr.net/gh/username/repo/file 一样能获取到！所以 GitHub 图床设置中将链接设置为 https://cdn.jsdelivr.net/gh/username/repo 


**Picgo配置信息示例**

```
henrywu97/FigBed
master
Figs/
https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master
```

## Bug

**图床指定的存储路径必须提前创建好**

错误：{"success",false}：原因是文件名冲突了，如果你上传过一张image1.jpg的图片，再上传名称一样的图片就会失败；**打开picgo设置，将【时间戳重命名】打开，如果该错误仍然出现，尝试勾选【上传前重命名】**

报错：failed to launch Picgo App，可能是因为App路径中存在空格等不被识别的路径字符，**建议安装在没有空格的路径下**

**Failed to fetch**，解决方法：打开picgo设置，点击设置Server选项，将端口改为36677端口，这是picgo推荐的默认端口号。

 图片不显示 Package size exceeded the configured limit of 50 MB问题解决方案：

https://blog.csdn.net/weixin_43571641/article/details/109817266



图片无法访问，打开网页后提示：

```
Failed to fetch version info for xxx/xxx.
```

解决方法：可能是因为太久没有使用GitHub，登陆并访问GitHub图床仓库后，即可解决。

# Picgo+Gitee图床

GitHub图床有时会上传不上去，因此采用Gitee作为替代方案，两者同时使用。相对于GitHub，Gitee的仓库有容量大小限制，但是胜在速度快。

- Gitee 单仓库容量上限为 500M，用户总仓库容量为 5G
- GitHub单个仓库建议在1G以内，总仓库容量应该不设限，具体参考[官方说明](https://docs.github.com/en/github/managing-large-files/working-with-large-files/what-is-my-disk-quota)

个人对图床的使用强度较大，根据过去一年的经验，按照200M/年的速度计算，500M可以使用2.5年，5G可以用25年，问题不大。

配置的详细教程参考[PicGo + Gitee(码云)实现markdown图床 - 简书 (jianshu.com)](https://www.jianshu.com/p/b69950a49ae2)，使用的插件为`gitee 2.0.3`，个人的配置信息如下：

```json
"owner": "henrywu97",
"path": "Figs",
"repo": "figbed"
```

注意，**owner中原来的大写字母也必须改写为小写**，否则上传的路径不正确。

其他参考：

1. [PicGo + Gitee 搭建免费的个人图床 - Skykguj 's Blog (sky390.cn)](https://blog.sky390.cn/archives/96/)
2. [Typora+PicGo+Gitee实现图片上传_萌太浪-CSDN博客](https://blog.csdn.net/u013206259/article/details/105911868)

# Typora配置修改

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210303191458.png)




