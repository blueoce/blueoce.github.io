---
layout: post
title: 高频问题汇总
categories: 逻辑分析仪24M  逻辑分析仪400M
description: 总结之前客户常见的售前咨询问题
keywords: 逻辑分析仪, 24M, 400M, 
---

**目录**

* TOC
{:toc}

### 发货时间，发货地点，发货方式

| 快递方式，客户可选择           | 顺丰快递到付                                                 | 默认普通快递        |
| ------------------------------ | ------------------------------------------------------------ | ------------------- |
| 发货时间                       | 1个小时内顺丰把货取走。                                      | 每天晚上9点前发货。 |
| 发货地点                       | 深圳龙华                                                     | 深圳龙华            |
| 发货时效---顺丰跑腿---美团跑腿 | 对于在深圳市清湖地铁周边的客户。配送价格按照距离收费。       | 不支持              |
| 发货时效---顺丰同城件          | 对于在深圳市内的客户，上午下单，下午可以到，就是同城当天件。 | 不支持              |
| 发货时效---空运                | 对于距离远的客户，北京，四川，重庆，空运是很好的选择。       | 不支持              |
| 发货时效---陆运                | 顺丰陆运配送由专人负责，不会出现货在菜鸟驿站不好找的情况。到货时间可控。 | 支持                |
| 详细地址和真实号码             | 选择发顺丰快递，请留---详细的地址----真实的手机号码---给客服，才能在顺丰平台下单。<br />虚拟号码，模糊的地址，顺丰下单平台无法下单，也影响收货时效。非常感谢您的支持。 | 普通快递不要求      |

### 常见通信接口

| 接口类型         | 24M逻辑分析仪       | 400M逻辑分析仪 | 测试方法                     |
| ---------------- | ------------------- | -------------- | ---------------------------- |
| 232接口          | 可以分析            | 可以分析       | 最稳定的方法，加232转TTL模块 |
| 485接口          | 可以分析            | 可以分析       | 最稳定的方法，加485转TTL模块 |
| Modbus接口       | 可以分析            | 可以分析       | 最稳定的方法，加485转TTL模块 |
| LIN接口          | 可以分析            | 可以分析       | 最稳定的方法，加LIN转TTL模块 |
| CAN接口          | 可以分析            | 可以分析       | 最稳定的方法，加CAN转TTL模块 |
| CANOPEN接口      | 可以分析            | 可以分析       | 最稳定的方法，加CAN转TTL模块 |
| 低速USB(12M)     | 可以分析            | 可以分析       | 直接可测。                   |
| 高速USB(大于12M) | 不可分析            | 可以分析       | 直接可测。                   |
| PWM_3.3V-5V      | 可以分析            | 可以分析       | 直接可测。                   |
| IIC接口          | 可以分析            | 可以分析       | 直接可测。                   |
| SPI接口          | 可以分析,最快测到6M | 可以分析       | 直接可测。                   |

### 采样速度，分析信号速度

**注：**经验证此方法也适用于 Win10，但是完成后需要**重启**。

因为个人习惯输入大写字母时使用「Shift + 字母」的方式，所以 Caps Lock 键并没有什么用，而且经常使用 Vim，偶尔使用 Emacs，都需要频繁地按 Ctrl 键，在 Mac OS X 下已经将 Caps Lock 键映射为 Ctrl，为了统一体验和按键方便，也需要在 Windows 下做一个映射。

先说方法：

将如下代码保存为 .reg 文件然后执行即可。

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout]
"Scancode Map"=hex:00,00,00,00,00,00,00,00,02,00,00,00,1d,00,3a,00,00,00,00,00
```

再说原理：

Scancode Map 这个键值的讲解实例参见 [Keyboard and mouse class drivers (Windows Drivers)](https://msdn.microsoft.com/en-us/library/windows/hardware/jj128267(v=vs.85).aspx#code-snippet-1)，我们这里填写的值

```
00000000 00000000 02000000 1d003a00 00000000
```

可以对应理解如下：

| 值         | 说明                                     |
|------------|------------------------------------------|
| 0x00000000 | Header: 版本。全部设置为 0。             |
| 0x00000000 | Header: 标志。全部设置为 0。             |
| 0x00000002 | 2 条映射条目（包括结尾的 null 条目）。   |
| 0x003a001d | Caps Lock --> Left Ctrl (0x3a --> 0x1d). |
| 0x00000000 | 终止符，即 null 条目。                   |

### 标题4

1. 右键任务栏库图标，右键弹出菜单里的“Windows 资源管理器”，单击“属性”。

   ![](/images/posts/windows/library-to-computer-step-1.jpg)

2. 在弹出对话框里将“目标”一栏的 `%windir%\explorer.exe` 改为 `%windir%\explorer.exe ,`，即加上一个空格一个逗号。

   ![](/images/posts/windows/library-to-computer-step-2.png)

参考：[如何将Win7/Win8任务栏库图标变为打开计算机](http://jingyan.baidu.com/article/046a7b3ee71d61f9c27fa91a.html)

### Win10 x64 下使用 ComMonitor

ComMonitor 算是比较好用的串口调试工具了，但是已经很久没有更新，在 Win10 下无法直接使用，打开会弹出错误提示：

```
没有找到 C:\Windows\system32\msrd3x43.dll
```

要在 Win10 64 位操作系统下正常使用 ComMonitor 的步骤是：

1. 下载 msrd3x43.dll，放到 C:\Windows\SysWOW64 下；

2. 右键 ComMonitor.exe -- 属性 -- 兼容性 -- 以兼容模式运行这个程序，选择 “Windows XP (Service Pack 2)”，应用。

我使用的 ComMinotor v4.5 版本及 msrd3x43.dll 文件可以到百度网盘下载：

<https://pan.baidu.com/s/1nuDa0JJ>

### Win10 下 Chrome 最新版崩溃

突然有一天就什么也打不开了，不断的报 XX 插件崩溃，反正是所有插件都崩溃，设置页面都进不去。

解决方法：

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Chrome]
"RendererCodeIntegrityEnabled"=dword:00000000
```

将以上内容保存为 chrome.reg 文件然后运行。
