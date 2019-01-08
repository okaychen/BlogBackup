---
title: Git分布式版本工具的部署与使用
date: 2019-01-07 20:48:24
tags:  
    - git
categories:
    - 版本控制
---

git目前是最快，最流行，也是最简单的分布式版本控制工具，相比svn这种的集中式管理，
分布式版本管理最大的`特点`就是“去中心化”，每个人的电脑上都相当于一个完整的版本库，我们不需要像集中式版本管理那样，每次都要从"中央处理器"下载全部文件后在进行更改，如果文件较大，在不同的局域网下，带宽小，时间会浪费在不断的下载更新文件之间。
git的`优势`是具有强大的分支管理，因为我们只需要master分支，就不在介绍了

<!--more-->

# 方案一：使用GUI clients(图形化客户端)
第一种方法是用老师说的图形化客户端，
- 优点是图形可视化操作简单，直观；
- 缺点是图形化客户端封装不完全，有些复杂的概念还是需要git命令；正常的软件开发流程下，相比图形化客户端，使用命令行至少可以提高15%的效率。

[点击打开git官网](https://git-scm.com/)

点download for windows

![download for](http://www.chenqaq.com/assets/photos/gitGUI01.png)

然后左侧｀GUI Clients｀,右侧可以根据系统版本选择不同的git图形化客户端，windows或者mac下建议用老师说的｀GitHub Desktop｀,

![GUI client](http://www.chenqaq.com/assets/photos/gitGUI02.png)

`GitHub Desktop`操作简单，一目了然，下载之后，关联好自己的账号，大概用10-30分钟就可以正常使用了。没有linux版本的`github Desktop`，我就不在试啦，有问题的话可以多问下百度，或者私聊我。

# 方案二：Git命令行
对于使用git命令行入手也非常容易，在官网，下载对应版本的git，一般是 `windows x64`

![windows x64](http://www.chenqaq.com/assets/photos/gitGUI03.png)

需要注意的是首次使用git需要命令行进行配置，在下面会演示一下
```sh
git config --global user.name "My Name"
git config --global user.email "myEmail@example.com"
```

情况一：初次无文件未初始化的，仅对于课程设计需要，最简单的办法建议先起一个文件名建一个空file，浅蓝色部分下面`creating a new file`
![无文件](http://www.chenqaq.com/assets/photos/gitGUI04.png)

情况二：已经根据情况一的情况创建过了（或者其他办法），仓库存在了文件

<video src="https://www.chenqaq.com/assets/videos/git.mp4" controls allowfullscreen="true" loop="true" autoplay="autoplay" muted width="100%" min-height="100%">embed: xss--chrome_test</video>

`git clone`:从远程仓库拉取一个项目，克隆到本地

克隆到本地之后一次正常的流程：

`git pull`: 拉取项目变化（注意每次要修改本地文件前先从远程仓库pull一下，更新本地文件之后修改）

`git add .`:将本地全部修改添加到暂存区（关于暂存区想要了解可以百度一下）

`git commit -m "something changes"`:将本地修改批量添加到分支，（-m "xxx"，给本次提交添加说明注释）

`git push`:将当前master分支全部推送到远程

push之后刷新客户端页面，就可以看到本次修改变化，github码云是一样的。
更多命令可以看新建的github的[studynotes](https://github.com/okaychen/studynotes/blob/master/git/git-command-lookup.md)仓库，或者可以通过网上学习git分布式版本控制更多更深入的内容。