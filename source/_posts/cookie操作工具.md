---
title: cookie操作工具
date: 2019-03-13 13:47:54
tags:
---


* 在写爬虫时不免需要分析请求cookie，需要排查必要鉴权键值。这里介绍个Chrome插件 -> [EditThisCookie](http://www.editthiscookie.com/)

  可以通过block每队键值，找到关键
  比如itunes connect的cookie，myacinfo即为鉴权键值

  <a href="https://i.imgur.com/hHSfETT.png)"><img src="https://i.imgur.com/hHSfETT.png)"/></a>

  p.s.通过插件新增myacinfo，已设双重验证itunes connect账号登陆仍然会遇到手机短信验证(待研究)，但是却可以直接访问app信息 [url](https://appstoreconnect.apple.com/WebObjects/iTunesConnect.woa/ra/ng/app) 。
  之前有做开发itunes connect账号通过requests协议方式登陆取值，某天某账号被设为two-factor-auth(hsa2)方式，https://idmsa.apple.com/appleauth/auth/signin 请求返回HTTP409，所获取的cookie键值相较普通用户，刚好缺失myacinfo。


* 有的网站会通过javascript动态修改cookie，可借助工具 [break-on-access](https://github.com/paulirish/break-on-access)，自动在js修改cookie时debugger暂停。