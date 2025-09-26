+++
date = '2025-09-24T11:03:16+08:00'
draft = false
title = 'Claude-Relay-Service部署过程'
description = 'Claude-Relay-Service部署'
tags = ['docker']
categories = ['AI']
author = 'Ushaio'
showToc = true
TocOpen = false
hidemeta = false
comments = false
disableHLJS = false
disableShare = false
searchHidden = false
+++

## 前提

今天刚在Zouter买了一个1h1g的小鸡，想着部署一下csr，这样就可以直接可以讲所有claude中中转平台集中管理了，免去切换环境变量的操作了。

但是

也不知道这些写文档的可能都是感觉大家都不是小白或者很明白某个部署方式吧，给我弄得晕头转向了反正=_=。。。

![image.png](https://img.yunbiu.top/file/20250926/1758850932211_image.png)

## 解决方案
最后问了佬友，问题在于其默认环境变量没有指定`redis_host`
最后在环境变量添加了

````
REDIS_HOST=redis
````
