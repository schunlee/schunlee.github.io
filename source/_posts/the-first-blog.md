---
title: the_first_blog
date: 2018-09-22 07:07:59
tags:
---
### 前言
* 第一次搭建Hexo+NexT博客，以此来整理并分享技术点滴。虽然网上已有了不少教程，但亲自动手还是遇到不少问题。

### 注意事项
* themes目录下git clone NexT主题，不注意会多生成一个themes文件夹导致报错。next文件夹应该与hexo默认生成的landscape同级。
  ![](https://i.imgur.com/0m202K4.png)
* 在部署站点时，_config.yml，各配置项冒号后需保留一个空格，否则不能成功部署(不会有报错信息)。
* 
	    deploy:
		   type: git
		   repo: git@github.com:schunlee/schunlee.github.io.git
		   branch: master
