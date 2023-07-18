---
layout: post
title: How to improve the speed of a logic analyzer
categories: 逻辑分析仪24M  
description: How to improve the speed of a logic analyzer
keywords: 逻辑分析仪, 24M, 
---

**目录**

* TOC
{:toc}
### 产品出货标准

| 测试项目                     | 测试标准                               | 判断标准                       |
| ---------------------------- | -------------------------------------- | ------------------------------ |
| 高速采样测试                 | 24M采样，连续采集60S,采集数据量为1.44G | 正常采样为合格                 |
| 信号有效测试                 | 上面采样完，看输入信号的频率。         | 每个通道输入<br />跟给定量一致 |
| 逻辑分析仪<br />抽样测试比例 | 100%全部测试                           | 高速采样+信号有效性            |
| USB线测试                    | 连接USB线和逻辑分析仪                  | 可以正常连接并采样24M          |
| USB线<br />抽样测试比例      | 100%全部测试                           | USB线连接测试                  |

### How to improve the speed of a logic analyzer

All of the factors in this table can affect the sampling speed of a logic analyzer.

| priority | cause of the problem                           | method of solution                                           |
| -------- | ---------------------------------------------- | ------------------------------------------------------------ |
| 1        | USB contact resistance is too high             | Replace the USB cable with a new one                         |
| 2        | Sampling rate issue with the computer USB port | Test on a different computer, we recommend<br /> the laptops ThinkPad, MacBook Air, MacBook Pro,<br /> and desktops from Lenovo. |
| 3        | This USB port's speed is not good enough       | Try using a different USB port on the current computer       |
| 4        | The adapter interference is too high           | Unplug the power adapter of the laptop computer and <br />use battery power instead |
| 5        | software version issue                         | Alternate testing of software versions 1.2.40 and 2.3.47     |

