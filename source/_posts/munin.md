---
title: munin
date: 2019-03-20 13:39:31
tags:
---

## munin + nginx搭建服务器性能检测工具
* 参考：
 * [https://github.com/jnstq/munin-nginx-ubuntu](https://github.com/jnstq/munin-nginx-ubuntu)
 * [https://www.cnblogs.com/rond/p/3777248.html](https://www.cnblogs.com/rond/p/3777248.html)
 * [https://serverfault.com/questions/615048/munin-dynamic-graph-zoom-dynazoom-not-working-nginx-php-fpm](https://serverfault.com/questions/615048/munin-dynamic-graph-zoom-dynazoom-not-working-nginx-php-fpm)
* nginx配置

 <a href="https://i.imgur.com/6OJ12FP.png"><img src="https://i.imgur.com/6OJ12FP.png"/></a>

* web截图

 <a href="https://i.imgur.com/WgxBkmJ.png"><img src="https://i.imgur.com/WgxBkmJ.png"/></a>

* 问题
 * dynazoom如果没有出现具体监控数据图，需要安装并运行cgi

    <a href="https://i.imgur.com/NdSxGv6.png"><img src="https://i.imgur.com/NdSxGv6.png"/></a>
