---
layout: post
title: 400M逻辑分析仪 开箱使用说明  
categories: 逻辑分析仪400M  
description: 400M逻辑分析仪软件下载 支持协议 触发阈值 
keywords: 逻辑分析仪, 400M, 
---

**目录**

* TOC
{:toc}
### 400M逻辑分析仪安装软件下载地址

| 支持协议    \    支持软件                | DSView 下载地址                                              | PulseView 下载地址                                           |
| ---------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| windows 64位(包含 win7 win8 win10 win11) | [window_64位_1.3.0](https://bluepi.lanzouo.com/iTw8H1ttrpna) | [window_64位_0.4.2](https://bluepi.lanzouo.com/ivhzN13bm3sj) |
|                                          | [window_64位_1.3.1](https://bluepi.lanzouo.com/iYe6s1ttqgkh) |                                                              |
| windows 32位(包含 win7 win8 )            | [window_32位_1.3.1](https://bluepi.lanzouo.com/iAkhX1ttqiod) | [window_32位_0.4.2](https://bluepi.lanzouo.com/ipqyo13bunmb) |
| Ubuntu 等 Linux版本64位                  | [linux_1.3.1](https://bluepi.lanzouo.com/ifI1I1ttrcze) 密码:19so | [linux_64位_0.4.2](https://bluepi.lanzouo.com/i9Go313blp4b)  |
| Ubuntu 等 Linux版本32位                  |                                                              | [linux_32位_0.4.2](https://bluepi.lanzouy.com/iMP1k13a2afc)  |
| Mac_OS X10.13 及以上版本64位             | [Mac_OS_1.3.0](https://bluepi.lanzouy.com/iMP1k13a2afc)      | [Mac_OS_64位_0.4.2](https://bluepi.lanzouy.com/iMP1k13a2afc) |
|                                          | [Mac_OS_1.3.1](https://bluepi.lanzouo.com/iV3001ttrbpi)      |                                                              |
| 区别                                     | 有触发阈值调节                                               | 无触发阈值调节                                               |

### PulseView安装驱动文件的方法

C:\Program Files (x86)\sigrok\PulseView\share\sigrok-firmware 软件PluseView安装目录下，加入两个驱动文件。[点击下载驱动](https://bluepi.lanzouy.com/it6WD13a7lve)

如下图所示在安装目录里面加入驱动文件：

<img src="/images/posts/dslogic/dslogic_fw.png" alt="400M分析仪固件"/>





### 400M逻辑分析仪支持软件和协议



### 触发电压选择

| 支持协议    \    支持软件 | DSView              | PulseView |
| ------------------------- | ------------------- | --------- |
| 触发阈值调节              | 0.1V-5.0V(0.1V步进) | 不支持    |

触发电压方法如下图所示。

<img src="/images/posts/dslogic/trig_voltage.png" alt="触发电压设置方法"/>



