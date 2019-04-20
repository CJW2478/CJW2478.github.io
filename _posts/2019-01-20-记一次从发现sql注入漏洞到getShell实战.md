---
layout:     post
title:      sql注入实战getshell
subtitle:   详细记录从发现sql注入漏洞,到getShell;
date:       2019-4-20
author:     陈建武
header-img: img/post-bg-re-vs-ng2.jpg
catalog: true
tags:
    - Blog
---

> 一次比较顺利的getshell;

# 前言

# (1)发现漏洞

### 最近一直想着找个站实战练习下学到的技能,于是在某漏洞平台翻了下,找了个站,百度后发现还是个上市公司,而且离我家不远处还有个分公司,
然后先抱着试试看的心态丢到某漏扫工具跑了下,结果跨站脚本漏洞N个,post请求sql盲注点一个.

### bp抓包复制到一个文件,

![](https://s2.ax1x.com/2019/04/20/ECRo6K.md.png)

### 丢到神器sqlmap跑起来;

![](https://s2.ax1x.com/2019/04/20/ECfAbD.md.png)

### 常规流程管理员信息一步步信息曝出来20个,个个都是弱口令,然而这不是getshell的重点,
因为我御剑扫了下并没有找到后台;场面一度很尴尬;

### 于是先看下数据库的用户信息;

![](https://s2.ax1x.com/2019/04/20/ECf7IH.png)

![](https://s2.ax1x.com/2019/04/20/EChpdg.png)

### 接下来就是获取交互式shell,找到网站根目录写入木马文件了.然而...................

### dir后显示有4786行数据,每秒一个字符,这得等到什么时候;

### 然而,灵光一闪,去网站url里找个文件搜索行不行?

### 于是随便找了个文件shared.css,交互式shell,搜索之---得到以下数据;

d:\website\css\shared.css
d:\website\EN\css\shared.css
d:\website_bak\css\shared.css
d:\website_bak\EN\css\shared.css
d:\website_old_upload_error\css\shared.css
d:\website_old_upload_error\EN\css\shared.css

### 根据信息判断,最像的那个路径,丢一句话进去,然后去访问,出现404,说明不对,继续试直到可以访问到;

### 最后!!

![](https://s2.ax1x.com/2019/04/20/ECISeK.png)

### 接下来无非就是,找后台,破解管理员密码,登录一下试试;







