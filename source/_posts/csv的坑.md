---
title: csv的坑
date: 2018-11-29 11:17:01
tags:
---

### 问题
  之前写过一个获取公司github上各项目仓库使用外链情况的脚本，每条信息以append方式写入csv文件，再上传BigQuery。脚本是在Mac上开发的，一切正常，后来迁移至Windows PC发现表格中多了很多的空行。

### 代码
<script src="https://gist.github.com/schunlee/562425c307c6e977d5391e59ee084343.js"></script>

### 解决方案
  通过参考 [https://www.crifan.com/python_csv_writer_writerow_redundant_new_line/](https://www.crifan.com/python_csv_writer_writerow_redundant_new_line/)，csv的writer，打开文件时需要小心，要通过binary模式打开，而不能通过文本模式，否则使用writerows写内容到csv时，会产生多余的CR，导致多余的空行。
  <script src="https://gist.github.com/schunlee/818486f0e26deb06a654842e33eae271.js"></script>
