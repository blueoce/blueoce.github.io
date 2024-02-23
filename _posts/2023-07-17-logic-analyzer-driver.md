---
layout: post
title: 24M逻辑分析仪驱动安装方法
categories: 逻辑分析仪24M
description: 24M逻辑分析仪驱动安装方法图解
keywords: 逻辑分析仪, 24M
---

**目录**

* TOC
{:toc}
### 首先要保证短路帽要连接正常

如下图所示：

<img src="/images/posts/driver/driver_install_plus.png" alt="短路帽的连接方法" />

### 插上USB设备，软件显示未连接

1.2.40 或者其他1代的软件版本，插上USB后未连接如下图所示。

<img src="/images/posts/driver/unlink_a.png" alt="1代软件连接失败" />

2.3.47 或者其他二代的软件版本，插上USB后未连接如下图所示。

<img src="/images/posts/driver/unlink_b.png" alt="2代软件连接失败" />

### 查看设备管理器，显示未知设备

<img src="/images/posts/driver/driver_1.png" alt="显示未知设备" />

### 反复插拔USB，直到出现问号的设备

<img src="/images/posts/driver/driver_2.png" alt="显示未知设备有叹号" />

### 给未知设备更新驱动程序

驱动程序就在软件的安装目录下，软件安装目录，如下所示：

C:\Program Files\Logic\Drivers                               二代软件

Logic-1.2.40-Windows (1)\Logic-1.2.40\Drivers    一代软件

<img src="/images/posts/driver/driver_3.png" alt="更新驱动程序" />

### 安装完驱动，设备管理器就可以正常识别到设备了

<img src="/images/posts/driver/driver_4.png" alt="正确识别到设备" />

### 再返回软件就可以看到已经连接的状态

1.2.40 或者其他1代的软件版本，插上USB后已经连接如下图所示。

<img src="/images/posts/driver/link_a.png" alt="一代软件已经连接" />

2.3.47 或者其他二代的软件版本，插上USB后已经连接如下图所示。

<img src="/images/posts/driver/link_b.png" alt="二代软件已经连接" />

### 如果尝试了以上的方法还不行 请查看VID码

在设备管理器中，查看VID码可以判断设备连接的状态。如下图：

<img src="/images/posts/driver/driver_VID.png" alt="二代软件已经连接" />

### 手动指定类型安装的方法

如下图所示，按照图示一步一步操作，直到第七步安装成功，第四步如果没有找到saleae LLC的厂商，就选择标准USB控制器。

<img src="/images/posts/driver/driver_force.png" alt="二代软件已经连接" />

### 如果按照上述方法还不能正常按照驱动（建议先换自己私人的电脑先测试一下）

是公司加密系统的问题，请看下面的聊天记录。换个电脑试试是最省时间的方法。

<img src="/images/posts/driver/driver_custom_1.png" alt="客户聊天记录1" />

<img src="/images/posts/driver/driver_custom_2.png" alt="客户聊天记录2" />

<img src="/images/posts/driver/driver_custom_3.png" alt="客户聊天记录3" />

