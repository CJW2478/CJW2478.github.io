---
layout:     post
title:      dns欺骗
subtitle:   对win7进行dns欺骗
date:       2019-3-23
author:     陈建武
header-img: img/post-bg-re-vs-ng2.jpg
catalog: true
tags:
    - Blog
---

>开始操作

# 前言
# Ettercap运行在linux中，其功能有嗅探、ARP欺骗、DSN劫持、中间人攻击等等，是一款强大的安全测试工具
## 先在我们的主机上开始web服务,并浏览器测试能否访问到页面.

# 命令:/etc/init.d/apache2 start

![](https://s2.ax1x.com/2019/03/23/AG2g8f.md.png)

![](https://s2.ax1x.com/2019/03/23/AG2228.md.png)

## 接着修改ettercap的dns文件.

# 命令:vim /etc/ettercap/etter.dns

![](https://s2.ax1x.com/2019/03/23/AGfU2V.md.png)

## 运行ettercap的图形界面.

#命令:ettercap -G

![](https://s2.ax1x.com/2019/03/23/AGfN80.png)

![](https://s2.ax1x.com/2019/03/23/AGfQKS.png)

![](https://s2.ax1x.com/2019/03/23/AGfavT.png)

![](https://s2.ax1x.com/2019/03/23/AGf8Ej.md.png)

![](https://s2.ax1x.com/2019/03/23/AGftCq.png)

![](https://s2.ax1x.com/2019/03/23/AGfJ5n.md.png)

![](https://s2.ax1x.com/2019/03/23/AGfKv8.md.png)

![](https://s2.ax1x.com/2019/03/23/AGfGUs.md.png)

![](https://s2.ax1x.com/2019/03/23/AGfugf.md.png)

## 最后去win7打开浏览器查看效果.

![](https://s2.ax1x.com/2019/03/23/AGflDg.md.png)
