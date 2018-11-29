---
title: Pycharm使用
date: 2018-10-31 11:31:27
tags:
---

### 注意事项
* 今天通过Pycharm git pull代码时，突然遇到以下错误提示：

  <a href="https://i.imgur.com/IuujM4E.png"><img src="https://i.imgur.com/IuujM4E.png"/></a>

  刚开始以为是网络问题，但重新克隆的项目同样无法远程仓库拉代码，于是怀疑可能是IDE配置问题，果不其然，查询 [stackoverflow](https://stackoverflow.com/questions/27566999/git-with-intellij-idea-could-not-read-from-remote-repository)，原来是自己不小心将项目版本控制SSH设置为内建Built-in的了(正确需要设置为<span color=red>Native</span>)，自然因为权限问题无法访问Github仓库。

  <a href="https://i.imgur.com/VBCuVbW.png"><img src="https://i.imgur.com/VBCuVbW.png"/></a>