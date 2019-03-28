---
title: MemoryError问题
date: 2019-03-06 09:24:10
tags:
---

### 问题

由于跑脚本的GCE VM instance低配的g1-small，内存只有1.7GB，定时任务总是由于MemoryError被Kill掉

<a href="https://i.imgur.com/35MbUxg.png)"><img src="https://i.imgur.com/35MbUxg.png)"/></a>

<a href="https://i.imgur.com/eltws9c.png)"><img src="https://i.imgur.com/eltws9c.png)"/></a>

Error:

<a href="https://i.imgur.com/RWAtZmc.png)"><img src="https://i.imgur.com/RWAtZmc.png)"/></a>

<a href="https://i.imgur.com/HU6PjI9.png)"><img src="https://i.imgur.com/HU6PjI9.png)"/></a>


### 方案
* 添加虚拟内存

  参考 [Linux下如何添加虚拟内存](http://www.lining0806.com/linux%E4%B8%8B%E5%A6%82%E4%BD%95%E6%B7%BB%E5%8A%A0%E8%99%9A%E6%8B%9F%E5%86%85%E5%AD%98/)

  * fdisk -l和df -Th命令来查看硬盘信息和挂载信息，来确定分区的大小

    <a href="https://i.imgur.com/hG8HMVp.png)"><img src="https://i.imgur.com/hG8HMVp.png)"/></a>

    <a href="https://i.imgur.com/iQq9qbO.png)"><img src="https://i.imgur.com/iQq9qbO.png)"/></a>

  * 使用dd命令，来创建大小为2G的文件swapfile

        dd if=/dev/zero of=/mnt/swapfile bs=1M count=2048
  * 格式化交换文件

        mkswap /mnt/swapfile
  * 挂载交换文件

        swapon /mnt/swapfile

  * <a href="https://i.imgur.com/BsbeB9R.png)"><img src="https://i.imgur.com/BsbeB9R.png)"/></a>


* 命令行释放内存

      echo 1 > /proc/sys/vm/drop_caches


* 使用hcache

  [https://mp.weixin.qq.com/s/EkoqlElIp-CWVqabB13z_g](https://mp.weixin.qq.com/s/EkoqlElIp-CWVqabB13z_g)