---
layout: post
title: My first blog
date: 2021-02-03  18:31:43  +0800
categories: CS
tags: CS
author: Peng Huiyang
description: 既然搭了那就讲讲咋搭的吧
---
第一步 在GitHub上创建一个仓库
===========================
New repository–>输入仓库名称格式为：用户名.github.io(如：stardustblog.github.io)->Create repository
嗯，如此这般那般之后，我们就得到了一个仓库，这个仓库可以通过用户名.github.io访问。

但是呢，这个时候，我们的仓库里面什么都没有。所以输入用户名.github.io会直接404，为了验证我们确实得到了这样一个
GitHub托管仓库，我们随便往里面塞一点什么HTML文档之类的，嗯，然后我们就会发现我们确实能访问他了。

第二步 安装Jekyll（一整套）
========================
以Windows系统为例：

先安装[Roby installer](https://rubyinstaller.org/)
(PS:建议装推荐的2.7版)

然后装[RubyGems](https://rubygems.org/pages/download)
直接装zip格式的就好了，下载下来解压，把解压的位置记住。

接着我们打开Windows的命令行，进入前面那个解压完成的目录，然后在命令行键入：

    ruby setup.rb

等一会儿，他自己就安装好啦

然后呢，继续在命令行输入:

    gem install jekyll

这个时候，Jekyll就安装好啦

第三步 找Jekyll模板
==================
这里是Jekyll的[主题官网](http://jekyllthemes.org/)

点进去之后，我们会找到很多主题，点进任何一个主题之后，点击Homepage可以跳转到GitHub界面，点击Download可以下载该
主题的压缩包，点击demo可以预览该模板的效果。

好，我们找到一个我们喜欢的主题，然后把他download下来，解压缩到一个合适的位置。

这个时候，理论上来说，只要我们把这个文件夹里面的东西全部上传到我们在第一步里面创建的GitHub库就好了，对不对？

但是，凡事都有但是，经过这样尝试之后，我发现这个网页没有我想要的样式。

怎么办呢，我们在命令行中进入到这个文件夹的目录，然后运行：

    jekyll server

然后下面会出现一大坨奇怪的东西，不要管他，如果生成链接失败，他让你装什么就装什么，我们只看最后生成的那个链接，
把那个复制到浏览器里面，按下回车——神奇的是，没有问题！

那么问题来了，问题在哪儿？

答案是url和baseurl，我们打开_config.yml这个配置文件，把里面的url改为：

url: https://github.com/stardustblog/stardustblog.github.io

baseurl改为：

baseurl: '/stardustblog.github.io'

好啦，问题解决啦！

然后我们就可以根据自己的需要去对里面的细节进行更改，并用markdown在上面发布文章了！