---
layout: post
title: "使用七牛云存储来托管静态博客"
description: "使用七牛云存储来托管静态博客"
category: Essays
tags: [Cloud Storage, 七牛云存储]
---
{% include JB/setup %}

你喜欢使用 [Markdown](#http://daringfireball.net/projects/markdown/) 文档来记录，喜欢使用 [Jekyll](#http://jekyllrb.com/) 这样小巧的工具来生成静态博客，并且喜欢将静态网站部署到 [Github](#http://www.github.com/) 上去。我也喜欢。

现在，你也可以将生成的静态博客部署到 [七牛云存储平台](#http://www.qiniutek.com/) 了。如果你文章的大多数目标读者在国内，七牛云存储平台是你目前最好的选择。

### Jekyll

首先，你需要[安装 Jekyll](#https://github.com/mojombo/jekyll/wiki/Install)，它是一个 Ruby Gem，在类 Unix 系统上非常容易安装，中文介绍请看 [这里](#http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)。

安装好之后，需手动创建设置文件和模版，我推荐使用 [Jekyll Bootstrap](#http://jekyllbootstrap.com/)，它让你能够快速的搭建好一个博客，并且有许多博客 [Theme](#http://themes.jekyllbootstrap.com/) 可选择。如果你想省去以上麻烦，可以直接使用 [我用 Jekyll Bootstrap 创建的库](#https://github.com/ikbear/ikbear.github.com)，里面内置了 [Twitter](http://themes.jekyllbootstrap.com/preview/twitter/) 主题（你现在所看到的这个静态博客就是用这个库创建的）。

### 七牛云存储

[七牛](#http://www.qiniutek.com) 是一个提供企业云存储服务的公司，七牛云存储主要存储以文件形式存在的非结构化数据，如视频和音频文件、图片、PDF和Word文档等。你可以 [注册](#https://dev.qiniutek.com/signup) 试用一下。

由于你的静态博客不涉及数据库，只涉及一些不常改动的静态文件，因此也可以存储在七牛的云端。同时，你在七牛创建的每个存储空间都可以绑定无数个域名（七牛提供免费的三级域名，无需备案。如果你要绑定自己的域名，就需要备案）。因此，你可以像使用 [Github Pages](#http://pages.github.com/) 一样使用七牛云存储服务来发布静态网站。

与 Github Pages 使用 Git 来发布网站不同的是，七牛为你了一个方便的命令行辅助同步工具 [qrsync](#http://docs.qiniutek.com/v3/tools/qrsync/)，让你方便的将本地上某个目录同步到云端。对于使用 Jekyll 生成的静态网站而言，你只需将 Jekyll 生成的 `_site` 目录同步到云端即可。

如果你的博客用的是 Wordpress 等使用了数据库的 CMS 系统呢？可以先 [迁移](#https://github.com/mojombo/jekyll/wiki/Blog-Migrations) 到 Jekyll。当然，这里所说的是托管静态博客，实际上任何形式的静态网站都可以用它来托管。

演示： [http://ikbear.dn.qbox.me/](#http://ikbear.dn.qbox.me/)