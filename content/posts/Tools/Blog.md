---
title: "Hugo博客搭建"
date: 2021-02-01T20:56:47+08:00
draft: false
tags: [LaTeX, Hugo, font]
categories: [Mac, Linux]
---

## Hugo

### 安装

Hugo官方下载地址: https://github.com/gohugoio/hugo/releases

选择对应的最新版本hugo0.80._windows-64bit.zip

压缩包解压后含有一个 exe 文件，把它加入到环境变量即可。

命令行(cmd)窗口输入`hugo version`，输出对应版本，例如`Hugo Static Site Generator v0.80.0-792EF0F4 windows/amd64 BuildDate: 2020-12-31T13:37:57Z`即为安装成功。

### 建立博客站点

创建新的博客项目，cmd进入任意目录运行以下命令即可在该目录生成对应的myBlog博客文件夹

```
hugo new site myBlog
```

*注：后续命令未经说明，均在cmd中的myBlog根目录下运行*

创建完成后，根目录myBlog包含以下文件

```
.
├── archetypes: default.md是生成博文的模版
├── assets # 存放被 Hugo Pipes 处理的文件
├── content # 存放markdown文件作为博文内容
├── data # 存放 Hugo 处理的数据
├── layouts # 存放布局文件
├── static # 存放静态文件 图片 CSS JS文件
├── themes: 存放不同的主题
└── config.toml: 博客配置文件支持 JSON YAML TOML 三种格式配置文件
```

### 主题下载

官方主题网站: https://themes.gohugo.io/

主题推荐: 

- Pure: https://themes.gohugo.io/hugo-theme-pure/
- Loveit: https://themes.gohugo.io/theme/LoveIt/
- uBlogger: https://themes.gohugo.io/ublogger/
- m10c: https://themes.gohugo.io/hugo-theme-m10c/
- hello-frien-ng: https://themes.gohugo.io/hugo-theme-hello-friend-ng/
- Eureka: https://themes.gohugo.io/hugo-eureka/

将主题下载至博客文件夹中的themes文件夹下即可。例如在根目录myBlog下运行以下代码，即可下载pure主题

```
git clone https://github.com/xiaoheiAh/hugo-theme-pure themes/pure
```



```
git submodule add https://github.com/rhazdon/hugo-theme-hello-friend-ng.git themes/hello-friend-ng
```

然后在根目录下的 `config.toml`文件中添加新的一行:

```toml
theme = "pure"
```

### 新建博文

要建立新的博文 `test.md`，使用下面的命令：

```bash
hugo new post/test.md
```

此时 `content` 文件夹下就多了一个 `test.md` 文件，打开文件就可以看到时间、文件名等信息已经自动生成了

```markdown
---
title: "Test"
date: 2018-08-05T20:56:47+08:00
draft: true
---
```

两条 `---` 间的信息是文章的配置信息，有的信息是自动生成的 (如：`title`、`date` 等)，简单介绍以下各项配置

**以下项目是自动生成的:**

- `title:` # 文章标题
- `date:` # 写作时间
- `draft:` # 是否为草稿，如果为 `true` 需要在命令中加入 `--buildDrafts` 参数才会生成这个文档

**以下项目需要自行添加:**

- `description:` # 描述
- `tags:` # 标签，用于文章分类
- `categories` # 指定文章的类别

`自动生成` 和 `执行添加` 的内容并不是绝对的，你可以根据自己的喜好配置模板文件 `archetypes/default.md`

这个命令会在 `content` 目录下建立 `post` 目录，并在 `post` 下生成 `test.md` 文件，博文书写就在这个文件里使用 Markdown 语法完成。博文的 front matter 里`draft` 选项默认为 `true`，需要改为 `false` 才能发表博文，建议直接更改上面说的`archetypes` 目录下的 `default` 文件，把 `draft: true` 改为 `draft: false`，这样生成的博文就是默认可以发表的。

在博文的 front matter 里面，使用 `tags` 指定文章的 tag，使用`categories` 指定文章的类别，示例如下：

```
tags: [LaTeX, Hexo, font]
categories: [Mac, Linux]
```

### 生成网页

为了查看生成的博客的效果，在cmd中运行以下命令，即可在http://localhost:1313/中查看博客的网页效果。

```
hugo server
hugo server -t m10c --buildDrafts
hugo server --buildDrafts -w
```

简单介绍一下参数：

- `-t m10c`：使用m10c主题
- `--buildDrafts`: 生成被标记为 「草稿」 的文档
- `-w`: 监控更改，如果发生更改直接显示到博客上 (非常有用，这也是我最喜欢的一点特性了)

但此时只能在本地访问 (相当于预览博客，如果与期望值不符，可以随时更改)，如果想发布到 `Github Pages` 上需要先将文章配置信息中的 `draft:` 改为 `false` 然后执行命令

```plaintext
hugo
```

此时你的博客目录下会多出一个 `public` 文件夹来。这便是 Hugo 生成的网站

### 参考

- Hugo安装: https://blog.csdn.net/qq_40992152/article/details/105370757
- 把博客从 Hexo 迁移到 Hugo: https://jdhao.github.io/2018/10/10/hexo_to_hugo/

## 部署github pages上

前提：已注册GitHub账号，登录

1、登录后，点击右上角，出现下拉菜单，点击 Your repositories 进入页面
![img](https://img2018.cnblogs.com/blog/488437/201908/488437-20190829162641399-1240861082.png)

2、点击 New

![img](https://img2018.cnblogs.com/blog/488437/201908/488437-20190829162830662-722937324.png)

3、进入 Creat a new repository 页面
![image-20210121195836444](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210121195836444.png)

4、图中的 yourname 要换成自己的github的用户名，即上图中Owner显示的用户名。最后点击Creat repository即完成

站点目录**`config.toml`**中**`baseURL`**要换成自己建立的仓库，如baseURL = "https://yourname.github.io/"

进入**站点根目录**下，执行：

> $ **`hugo`**

执行后，站点根目录下会生成一个 `public` 文件夹，该文件下的内容即Hugo生成的整个静态网站。每次更新内容后，将 pubilc 目录里所有文件 push到GitHub即可。

首次使用的时候要执行以下命令：

```
cd public
git init
git remote add origin https://github.com/[Github 用户名]/[Github 用户名].github.io.git # 将本地目录链接到远程服务器的代码仓库
git add -A
git commit -m "[介绍，随便写点什么，比如日期]"
git push -u origin master
```

以后每次**站点目录**下执行 `hugo` 命令后，再到`public`下执行推送命令：

```
git add -A
git commit -m "[介绍，随便写点什么，比如日期]"
git push -u origin master
```

之后就可以到GitHub上看提交到分支的内容，也可访问 YOURNAME.github.io看页面了。

### 总结

以上整个环境部署好之后，接下来的常用命令就是以下几个：

**站点目录**下，新建文章，执行：

> $ **`hugo new post/文章名.md`**

添加文章内容或修修改改，包括修改主题之类的，在本地都可以实时看到

修改完成，确定要上传到GitHub上后，**站点目录**`myBlog`下执行：

> $ **`hugo`**

进行编译，没错误的话修改的内容就顺利同步到`public`下了，然后**`cd public`**下，执行提交命令：

> $ **`git add -A`**
>
> $ **`git commit -m "20200204-1"`**
>
> $ **`git push -u origin master`**

至此OK，顺利的话应该是一步到位的。若是遇到问题的话再百度咯

### bug解决

解决 fatal: Not a git repository (or any of the parent directories): .git 问题: https://blog.csdn.net/wenb1bai/article/details/89363588

解决Git fatal: unable to auto-detect email address问题: https://blog.csdn.net/u013914471/article/details/88394310

解决hint: Updates were rejected because the remote contains work that you do: https://www.cnblogs.com/czwangzheng/p/5086903.html

[hexo + github pages搭建博客样式加载不出来_banjw的博客-CSDN博客_hexo样式加载不了](https://blog.csdn.net/banjw_129/article/details/82261165?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.control)

### 域名绑定

Github Pages可以绑定自己的域名，例如在阿里云/腾讯云购买好域名之后，首先进行**实名认证**(根据工信部2017年全面域名实名认证的要求，所有存量域名以及新注册域名均需完成域名实名认证)。然后添加相应的解析：

![image-20210121215641671](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210121215641671.png)

其中`185.199.109.153`是用`ping`命令找到的存放github pages的主机的IP地址，在cmd命令行中输入`ping xxx.github.io`便可获取：

![image-20210121221541289](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210121221541289.png)

最进入到Github pages仓库Setting页面，并滑动到Github Pages这一栏，在Custom Domain填上刚刚添加解析的域名并保存：

![image-20210121222010131](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210121222010131.png)

### 参考

- 使用 Hugo + GitHub Pages 搭建个人博客（包含部署脚本）: https://mogeko.me/2018/018/
- Hugo + Github Pages 搭建个人博客: https://www.cnblogs.com/stevexu/p/10779375.html
- Windows+Hugo+GitHub制作静态个人博客: https://blog.csdn.net/weixin_43386341/article/details/103586415
- 三步搞定Github Pages自定义域名: [https://www.jianshu.com/p/2647e079741f](https://www.jianshu.com/p/2647e079741f)
- 托管到Netlify: https://kuleyu.github.io/hexolog/post/31808.html

## Netlify

对于想要使用Jekyll、[Hexo](https://hexo.io/)、Hugo等静态搭建网站，又害怕复杂的本地环境配置的朋友，Netlify支持自动编译Jekyll、[Hexo](https://hexo.io/)、Hugo等常见的静态博客程序。另外，Netlify也是一个非常好的静态空间，如果你有用[纸小墨 inkPaper](http://www.chole.io/)或者Html网页，可以直接上传发布到空间上。

### Github仓库生成

首先须要建立一个新的Github仓库(*这里与直接利用Github Pages搭建博客用到的仓库不一样*)，然后在博客目录文件加下生成`.gitignore`文件，内容为`public/`从而不上传该文件夹。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204205844.png)

然后上传至仓库: 

```
git init
git remote add origin https://仓库地址 # 将本地目录链接到远程服务器的代码仓库
git add -A
git commit -m "[介绍，随便写点什么，比如日期]"
git push -u origin master
```

### Netlify连接至Github仓库

进入Netlify官网: https://www.netlify.com/，申请注册一个账号，可以使用Github、Gitlab以及Bitbucket直接授权登陆。然后登录到空间管理中心，点击的`New site from Git`添加网站。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204204601.png)

然后根据自己的托管平台，这里使用GitHub作为托管平台。

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204204720.png)

验证登陆后选择此前生成的仓库。

![image-20210204204825869](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204204828.png)

站点基本设置如下：

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204211915.png)

点击`Deploy site`即可生成网站，此时网站可能构建失败：虽然 Netlify 可以自动检测网站程序，但是最好能够匹配电脑上装的那个静态网页生成器的版本。所以，建议在`Site settings`中修改 Netlify 构建网站的静态网页生成器版本号：`Build & deploy` --> `Enviroment` --> `Environment variables`，填入 `HUGO_VERSION` `0.80.0` （具体版本号以使用的为准），其中可以在命令行输入`hugo version`查询hugo版本。

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210204215828746.png)

`Site settings`中`Change site name`可以改变站点的链接为自己想要的链接(格式为`site name.netlify.app`)。

![image-20210204222258469](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20210204222258469.png)

### 域名绑定

域名绑定需要在`Domain management`中点击`Add custom domain`，添加自己的域名

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204222619.png)

例如：

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204222819.png)

点击确定后还需要验证DNS:

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204230546.png)

这里使用Netlify提供的DNS服务

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204230530.png)

一直点击确认后，来到最后一步

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204230523.png)

拿到这个DNS服务器地址之后，进入阿里云控制台，域名管理：

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed/Figs/20210204230520.png)

然后，修改DNS为Netlify提供的DNS服务器。回到设置界面后，绑定的域名后有绿色的`Netlify DNS`标志即表示域名绑定成功。

### Bug解决

Hugo中绑定域名后，同时需要改变网站根目录中`config`文件的域名参数，例如`baseURL = "https://www.wuhao.ink/"`，否则展示的网页可能有问题。

### 参考

按重要性排序

1. 英文视频讲解: https://www.youtube.com/watch?v=gSiAcyTWU3c
2. Github Pages访问太慢？通过Netlify免费加速: https://www.cnblogs.com/37Y37/p/12551839.html
3. 域名绑定参考: https://hero.github.io/categories/Hexo/netlify/
4. 同时部署 Hugo 静态博客到 Netlify 和 Github Pages: https://www.nashome.cn/posts/hugo-netlify/

