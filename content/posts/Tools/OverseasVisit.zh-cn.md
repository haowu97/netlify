---
title: "科学上网"
date: 2021-02-25T17:17:08+08:00
draft: false

description: ""
upd: ""

tags: ['科学上网']
categories: []
---

以下是目前流行的科学上网软件：

- SSR: SSR简单来说是一个客户端代理，软件，支持SSR开头节点，出身较早，匹配成熟
- Clash: Clash支持Ss,SSR,V2ray以及 . Trojan节点，既是平台，也是工具，更强调策路分流规则，复杂但是强大！
- V2ray更像一个平台，可以作为开发工具 使用，支持Vmes开头的节点，同时支持 Trojan节点的导入，更加全面，正流行
- Trojan模仿互联网常见的Https协议进行科学上网，常用网站伪装，匹配不完善，末来可期

Sock5代理方式(Shadowsocks, ShadowsocksR)优于VPN。

## PC端 SSR

SSR Windows下载地址: https://github.com/shadowsocksrr/shadowsocksr-csharp/releases

设置要点：

- 日常中取消负载均衡

- 服务器更新时，不通过代理

Bug处理：

- [经常开机显示SSR的1080端口被占用解决办法](https://diary.dorcandy.cn/posts/dabba837/)
- [故障解决：端口已被占用 1080](https://blog.csdn.net/longintchar/article/details/79680589)


## 安卓端 ShadowsocksR

配置步骤

1. SSR 安卓下载地址: https://github.com/shadowsocksrr/shadowsocksr-android/releases，直接手机下载或者电脑下载后用QQ传给手机后安装。
2. 打开 ShadowsocksR，点击左上角的「ShadowsocksR」进入配置文件管理页面。
3. 复制好SSR节点，然后点击右下角的加号按钮，在弹出的选项中选择「从剪贴板导入」即可导入节点。

![](https://i.loli.net/2019/01/13/5c3a7bac1fee1.jpeg)

## IOS端 - `Shadowrocket`

使用步骤：

1. 因为国内App Store已经无法下载`Shadowrocket`，需要用一个美区账号登陆App Store下载。其中，Ipad更换app store账号：点击头像，直接滑到底然后退出登录。
2. 下载好之后，直接复制SSR节点，然后打开`Shadowrocket`软件即可添加节点。
3. 点击“延迟测试”，可以查看服务器的延迟，理论上延迟越低上外网越快；
4. 点“未连接”那一栏右边的开关，开启vpn。首次使用会弹出添加vpn确认框；
5. 点击“允许”，弹出密码界面，输入iphone/ipad的解锁密码，软件界面的按钮变蓝表示成功开启，同时状态栏出现vpn图标.

如果配置没有问题且到服务端的网络正常的话，应该就可以用浏览器打开youtube，同时twitter、youtube等app也可以正常联网使用了。

配置参考：

- [小火箭/Shadowrocket介绍](https://ssrvps.org/archives/10495)
- [iOS小火箭(Shadowrocket)怎么用教程/配置/节点](https://garygeng.net/others/shadowrocket/)

免费境外ID: 

- [境外apple id信息汇总](https://v2xtls.org/%e5%a2%83%e5%a4%96apple-id%e4%bf%a1%e6%81%af%e6%b1%87%e6%80%bb/)
- [境外apple id信息汇总](https://ssrvps.org/archives/1455)

注意: **免费账号，使用时不要登录icloud，使用完后请自觉退出**。

其他IOS端口参考：

- [获取ios科学上网客户端](https://tlanyan.me/get-proxy-clients/)

## 节点

### 免费

使用中：

- 电脑端V2Ray：[教学以及免费节点分享](https://www.youtube.com/channel/UCs9DTlP6bRIuLkAZ8egC12g)
- IOS(Shadowrocket)/安卓端(V2RayNG/Clash)：[教学](https://www.youtube.com/channel/UC277PQOP9AnRF83500JLfww)；[免费节点](https://share.weiyun.com/JEpTcCH0)

### 付费

[高速机场导航](https://docs.google.com/document/d/1yZ8Q36z7oFFTYvwQjexDpuE-OFbhZTCOVDXgK83o3uA/edit)

http://vmessnode.xyz/doc/#/Windows/ShadowsocksR

http://skssrsk.ys168.com/

附教程，password:8888

https://tianhang.pro/auth/register

https://sspool.herokuapp.com/