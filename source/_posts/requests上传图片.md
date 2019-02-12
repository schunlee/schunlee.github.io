---
title: requests上传图片
date: 2019-02-11 11:53:38
tags:
---

### 前言
   最近遇到一需求，需要程序上传图片，以前没接触过，故记之。

### 代码
   通过浏览器开发者工具查看对应请求，如下图:

   <a href="https://i.imgur.com/aGbxO2w.png)"><img src="https://i.imgur.com/aGbxO2w.png)"/></a>

   需要使用第三方库 => requests_toolbelt

   <script src="https://gist.github.com/schunlee/2e45379de176240d2f450c568e3d5421.js"></script>

### 附言
   之前尝试使用requests, files参数，但总是报<b>422 ('{"errors": "Must upload a file"}')</b>，还需空了研究.

