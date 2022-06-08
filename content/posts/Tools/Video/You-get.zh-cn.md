---
title: "you-get：一行代码下载Bi站视频源文件"
date: 2021-08-28T12:11:59+08:00
draft: false

description: "you-get：一行代码下载Bi站视频源文件。"
upd: "you-get：一行代码下载Bi站视频源文件。"

tags: ["软件", "视频"]
categories: []
---

<!--more-->

>`you-get`是开源的Python第三方库，通过它我们仅用一行代码就可以下载Bi站等视频网站的视频源文件，是获取素材的非常方便的途径。

## 法一

首先介绍一种比较简单的下载Bi站源文件的方式：在视频链接中的`bilibili`后添加`jj`。例如将`https://www.bilibili.com/video/av87176938`，改为`https://www.bilibilijj.com/video/av87176938`即可进入视频下载界面，点击右侧`MP4`即可下载。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20220608172744.png)

然而，可以看到该视频没有达到缓存要求，点击后显示“目前缓存最低要求为视频发布7天内播放量超过1万”，并且该方法也无法下载番剧，适用范围比较窄。

## 单个视频下载

[vtool解析网-哔哩哔哩,B站,bilibili在线解析,小红书,抖音,快手去水印](https://vtool.pro/bilibili.html)



## you-get: 批量下载

`you-get`是GitHub上Python的一个开源库，非常好上手，**下面简单介绍一下安装与使用方法**，具体可参考[GitHub地址](https://github.com/soimort/you-get)，[You-Get官网](https://you-get.org/).

**安装**：与其他Python第三方库相同，在`cmd`输入`pip3 install you-get`即可完成安装。

**下面演示如何下载鬼灭之刃第一集MP4文件**：



首先获取其网页链接`https://www.bilibili.com/bangumi/play/ep267851`，然后在`cmd`输入这行命令即可完成下载：

```python
you-get https://www.bilibili.com/bangumi/play/ep267851
```

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20220608172852.png)

### 选择下载版本

我们还可以通过以下命令**查看视频的相关信息**：

```python
you-get -i https://www.bilibili.com/bangumi/play/ep267851
```

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20220608172839.png)

可以看到有上面4种不同清晰度的文件可供下载，**默认下载第一个版本(一般是最清晰的版本)**，根据上面查询到的`format`信息，可以**指定下载清晰度最高的版本**：

```python
you-get --format=dash-flv https://www.bilibili.com/bangumi/play/ep267851
```

进一步，可以通过以下命令**指定文件输出的地址**：

```python
you-get --format=dash-flv -o D:/Download https://www.bilibili.com/bangumi/play/ep267851 
```

使用`--playlist`选项可以下载有多个Page的视频：

```powershell
you-get -i https://www.bilibili.com/video/BV1GE411h7LB
you-get --playlist -o D:/Download/BiliBili https://www.bilibili.com/video/BV1GE411h7LB
```



`you-get`在官方文档中给出的适用范围包括了几国内外的几乎所有主流视频网站（YouTube、优酷、爱奇艺等），然而在我的使用过程中效果并不理想，爱奇艺视频文件无法下载，优酷视频文件下载到一半程序中止。但仍然不可否认的是，这是一个非常好用的获取视频源文件的API。

以上是本篇的全部内容，欢迎关注我的[知乎](https://www.zhihu.com/people/wu-hao-69-57/activities)|[简书](https://www.jianshu.com/u/eec9c995a8dc)|[CSDN](https://me.csdn.net/weixin_44533530)|[微信公众号](https://mp.weixin.qq.com/mp/profile_ext?action=home&__biz=Mzg5NjIyMTQyMw==&scene=124#wechat_redirect)`PurePlay` , 会不定期分享研究与学习干货。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20220608172823.png)









