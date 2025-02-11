---
categories: 
- develop
date: "2017-10-15T16:44:11Z"
title: 浮点误差
---

浮点运算不同于整数运算，是存在大量误差的。这是因为在计算浮点时，为了处理下溢问题，引入了“舍入”和“截断”

# 截断

这是最简单的处理方式，直接截断特定位数后的所有数据。这样会产生诱导误差。而且这个误差是偏置的，所有截断后的数一定小于原数据。

# 舍入

这个是相对减少数的位数的技术。如果丢弃的位的值大于剩余数最低位的一半，则将剩余数的最低位加1。这样统计总体上而言是相对精确的。

# 使用

在一般使用中，是可以无视浮点误差。现代计算中，这类误差已经小到几乎可以忽略了。但是在一些科学计算领域或者高精度要求的方面，需要注意这个问题。有必要时可以考虑使用整数（放大）代替浮点。或者自行封闭浮点操作。

