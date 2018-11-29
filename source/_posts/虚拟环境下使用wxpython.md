---
title: Mac虚拟环境下使用wxpython
date: 2018-11-07 16:10:43
tags:
---

#### 问题
* Mac下Python虚拟环境运行wxpython脚本，会报以下错误，无法运行脚本

    ![](https://i.imgur.com/ZOu0UqQ.png)

#### 解决方案
* virtualenv/bin文件夹下创建sh文件(pythonw.sh)，内容为

  <script src="https://gist.github.com/schunlee/909168d2526e62b32017967d056ee94b.js"></script>

* sh脚本中，`PYTHON`为本机python位置

* Pycharm中配置如下

  ![](https://i.imgur.com/NTbny5q.png)

#### Pip
* wxPython-Phoenix==3.0.3.dev2902+a79cd32

#### 参考
* [https://wiki.wxpython.org/wxPythonVirtualenvOnMac](https://wiki.wxpython.org/wxPythonVirtualenvOnMac)