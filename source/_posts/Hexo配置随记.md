---
title: Hexo配置随记
date: 2018-04-01 11:40:05
tags:
    - 随记
    - Hexo
---
![](/images/hexo-banner.jpg)

> 你看起来不错，来做我的菜吧 ~

<!-- more -->

## 前置

一键搭建？不存在的!

在安装 `Hexo` 之前，需要已经安装好 `Node.js`, `Git` 环境，没有的话，下面链接，了解一下？

- [Node.js](https://nodejs.org/en/)
- [Git](https://git-scm.com/)

如果安装好了，接下来就是 `Hexo` 的安装

```bash
npm install -g hexo-cli
```

## 开始建站

安装完之后，接下来就是建站了

```bash
hexo init <hexo_name>

cd <hexo_name>

npm install

```

建站之后，就请去 官网了解一下 [建站文档](https://hexo.io/zh-cn/docs/setup.html)， 这里说的比已经很全面了

## 开始配置

配置文件 `_config.yml` 可以到官方的 [配置文档](https://hexo.io/zh-cn/docs/configuration.html) 了解一下？这边只聊一些，必须知道的几个配置项

### 基本配置

参数 | 描述 | 备注
-- | -- | --
title | 网站标题 |
subtitle | 网站副标题 |
description | 网站描述 | 简单加点描述 有利于SEO
author | 您的名字 |
language | 网站使用的语言 | zh-Hans（中文） 建议最好
timezone | 网站时区 |

#### 部署配置 `deploy`

一键建站是不太可能的，配置好之后一键部署上线还是可以的，这里我们关注的是 `Git` 上面的部署，其余部署配置，[部署文档](https://hexo.io/zh-cn/docs/deployment.html) 了解一下？ 顺便 `Github` 官方配置 [GitPage](https://pages.github.com/) 了解一下？图文教学了，简直不要太友好。

首先先安装

```bash
npm install hexo-deployer-git --save
```

```json
deploy:
  type: git
  repo: <repository url> //库（Repository）地址
  branch: [branch] //分支名称
  message: [message] //自定义提交信息，默认是更新日期
```

## 指令

部署完成之后，大概就差不多了，我们首先看几个指令

新建文章指令，`layout` 指的是文章格式，详情了解一下[基本操作-写作](https://hexo.io/zh-cn/docs/writing.html)，`title` 为文章标题

```bash
hexo new [layout] <title>
//example
hexo new post Hexo配置
```

文章写完之后，需要生成为静态文件，再部署上传，即可看到自己的文章了。

```bash
//生成静态文件，快捷指令：hexo g
hexo generate

//部署上传文件，快捷指令：hexo d
hexo deploy
```

若是对自己的文字或者配置不太自信的，可以使用本地测试指令，启动服务器，默认情况下，访问网址为： `http://localhost:4000/`

```bash
hexo server
```

## 总结

其实大部分的而配置指令，都是可以在官方的[文档](https://hexo.io/zh-cn)这边大概是一丢丢配置，以及常用指令的总结，后续看反馈，可以继续写一篇 [NexT](http://theme-next.iissnan.com/) 主题上面的配置，如果写不下，`本酱` 就直接在这里更吧~

好了，今年的 4月到了，1号完美的没有人跟`本酱`表白~

感谢阅读~

感谢[学姐大人](https://yufan.me/)很久以前（大概3年前）的推荐；

感谢[小心校长大人](http://www.liaoyunduo.com/)的配置指导文章(http://www.liaoyunduo.com/2017/10/01/1/)；

感谢两位同学的催更，[天亮](#)，[凯荣](#)；
