---
layout: post
title: usb sniffer
categories: usb sniffer  
description: 软件使用方法
keywords: 逻辑分析仪, usb sniffer, 
---

**目录**

* TOC
{:toc}
### 安装软件下载


软件使用版本1.2.40。下图就是WS2811驱动芯片和LED的PCB板，WS2811是单总线协议，用于控制LED灯的颜色。

两根是电源线，一根是WS2811数据线。

<img src="/images/posts/WS2811/LED_1.png" alt="WS2811LED图片"/>

### WS2811协议软件设置方法

+Analyzers分析里面选择，show more analyzers.选择Addressable LEDs(Async)

<img src="/images/posts/WS2811/LED_2.png" alt="增加分析协议"/>

LED Channel 里面选择当前接线的通道，

LED Controller 里面选择WS2811协议。完成设置开始分析。

<img src="/images/posts/WS2811/LED_3.png" alt="增加分析协议，选择通道"/>