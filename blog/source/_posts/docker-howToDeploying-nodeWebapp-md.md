---
title: Docker实践-Node应用部署
date: 2018-12-19 19:47:46
tags: 
    - Docker
categories: 
    - Docker
---
下面是一个简单的例子，用来实现如何在docker容器内运行node程序。

<!--more-->

<video src="https://www.chenqaq.com/assets/videos/test-2018-12-19_17.23.50.mp4" controls allowfullscreen="true" loop="true" autoplay="autoplay" muted width="100%" min-height="100%">embed: xss--chrome_test</video>

可以通过`sudo docker run -it mynodeapp /bin/bash`在新容器内开启一个终端并允许进行交互
![在新容器内开启一个终端并可以进行交互](https://www.chenqaq.com/assets/images/docker-bash01.png)

关于Dockerfile的简单说明，更新在我的[github的studynotes中](https://github.com/okaychen/studynotes/blob/master/docker/docker-deploying-node.md)