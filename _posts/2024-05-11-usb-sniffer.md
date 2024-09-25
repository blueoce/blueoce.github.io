---
layout: post
title: usb_sniffer
categories: usb_sniffer  
description: 软件使用方法
keywords: 逻辑分析仪,usb_sniffer, 
---

**目录**

* TOC
{:toc}
# 0常见问题解答---非常重要---真的非常重要---真的真的非常重要

## 问题1：usb插件在哪里下载？

参考《1安装软件下载》 右边的USB插件驱动包里面。在插件驱动包里面。找到【usb_sniffer_win.exe】+操作说明v1]，下载。

## 问题2：Wireshark没有 USB Sniffer的选项？

参考《3插件安装》必须找到 【C:\Program Files\Wireshark\extcap】这个文件夹，并拷贝usb_sniffer_win.exe到其目录下。才会有USB Sniffer选项.

## 问题3：找不到usb_sniffer_win.exe文件？！！！多次询问！！！

参考《1安装软件下载》 右边的USB插件驱动包里面。在插件驱动包里面。找到【usb_sniffer_win.exe】+操作说明v1]，下载。

## 问题4：解析的数据感觉不对，没有USB数据包？

参考《4软件使用---USB抓包方法》里面《2 正确的选择捕捉速度》，尝试用三种不同的速度（低速，全速，高速）去捕捉，能看到USB数据包就是正确的速度。

## 问题5：如何设置USB捕捉速度？

参考《4软件使用---USB抓包方法》里面《双击打开Wireshark软件》，看左边圆形的图标，点击进入。设置捕捉速度。

## 问题6：为啥我的捕捉不到数据？

对于初始使用USB snifer,建议先测USB鼠标设备，鼠标一直会发数据包，比较容易看。捕捉速度：低速。

## 问题7：捕捉不到数据？

建议，先开启软件捕捉功能，在去插如USB设备，这样才是正确的顺序，先插设备，再开捕捉会丢失很多数据。

## 问题8：文档的图片我看不到怎么办？

参考《1安装软件下载》里面《由于服务器在国外，未翻墙国内用户请直接下载网页的PDF版本》右边最新pdf的提交版本。

## 问题9：一直采集不到数据？

host端必须也接线到电脑。

参考《6 常见问题详解---HOST没有接线》有图文说明。

## 问题10：怎么判断设备是 低速 全速 高速？

没有特别好的方法，先假设是一种，然后看数据包是否正确。正确则说明是猜中的速度。
比如，猜测，鼠标是低速设备，在测试的过程中，只有选择低速设备才可以解除正确的数据包，
选择其他速度，都无法解除正确的包，则说明是低速设备。
参考《7 常见问题详解---怎么判断设备的连接速度》有图文说明。

## 问题11：device设备无法识别到，HOST线已经插了？

请重新插拔一次PC-M，USB线就可以了，device设备就可以正确识别到了。  待测设备device口usb无法识别，重新插拔PC-M线。

## 问题12：USB转串口设备，全速USB，捕捉数据卡顿。

在设备速度选择的选择框下面有一个，折叠空白包的功能，Fold empty frames,当捕捉卡顿的时候，建议勾选节省CPU和RAM的资料，让捕捉响应更及时。
参考《8 常见问题详解---空包过滤》有图文说明。

## 问题13：USB3.0设备有限支持，测U盘等大容量存储时，建议使用USB2.0U盘

在测试U盘这种大容量存储时，建议使用USB2.0设备，USB3.0数据量太大容易发生错误，USB2.0U盘可以很好的解决这个问题。

## 问题14：如何用命令行工具捕捉数据

详细参考《10 命令行工具》。


[HS]  .\usb_sniffer_win.exe -s hs -c -f hs_capture.pcapng    
[HS_fold]  .\usb_sniffer_win.exe -s hs -l -c -f hs_capture.pcapng

[FS] .\usb_sniffer_win.exe -s fs -c -f fs_capture.pcapng
[FS_fold] .\usb_sniffer_win.exe -s fs -l -c -f fs_capture.pcapng

[LS] .\usb_sniffer_win.exe -s ls -c -f ls_capture.pcapng 
[LS_fold] .\usb_sniffer_win.exe -s ls -l -c -f ls_capture.pcapng 

## 提问注意：首先感谢大家的提问！！！提问时请注意：请先拍照，或截图，最好拍视频，反应问题，再发文字描述，这个可以提高提问的效率，避免我司技术人员猜测老板们的实际情况，浪费宝贵的时间。

各位各样的问题我们都遇到过，相信专业的力量！！！



# 1安装软件下载

| 版本描述                                                     | Wireshark                                                    | USB插件驱动包↓↓↓                                             |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 2024年9月最新版本【Version 4.4.4】                           | [Version 4.4.4](https://bluepi.lanzouo.com/i5Uql2av05aj)     | [【usb_sniffer_win.exe】+操作说明v1](https://bluepi.lanzouo.com/i3DZI1yjm7ti) |
|                                                              | [Version 4.2.7](https://bluepi.lanzouo.com/iu59S2av00ze)     |                                                              |
|                                                              | [Version 4.2.5](https://bluepi.lanzouo.com/iyOtA2av0dda)     |                                                              |
|                                                              | [Version 4.2.4](https://bluepi.lanzouo.com/iLg1L1yj7fjg)     |                                                              |
| 由于服务器在国外，未翻墙国内用户可能无法打开图片，请直接下载网页打印PDF版本，最新版本——》 | [[提交版本[792217b4]_网页](https://bluepi.lanzouo.com/iX9zd226im8j) | updata 2024/6/19                                             |
|                                                              | [[提交版本[0e1bf1b5]_网页](https://bluepi.lanzouo.com/iIZoB213nafa) | updata 2024/6/7                                              |
|                                                              | [提交版本[e35b59a1]_网页](https://bluepi.lanzouo.com/ij3Cx20v426b) | updata 2024/6/5                                              |
|                                                              | [提交版本[ae3e5fce]_网页](https://bluepi.lanzouo.com/iVhoS20s22wh) | updata 2024/6/4                                              |
|                                                              | [提交版本[78bf8a6]_网页](https://bluepi.lanzouo.com/iGRMs1zeoocb) | updata 2024/5/21                                             |
|                                                              | [提交版本[c25a352]_网页](https://bluepi.lanzouo.com/iCwyi1z2mxaj) | updata 2024/5/18                                             |
| 最新软件获取网址                                             | [官网下载](https://www.wireshark.org/download.html)          |                                                              |

# 2软件安装

   安装 Wireshark的软件，安装路径最好在C盘，用默认路径就是在C盘。所以安装好以后软件的路径就是 【C:\Program Files\Wireshark】

   软件安装默认下一步安装就行，直到软件安装完成。软件无需破解，安装完成就可以使用。

step1 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S1.png" alt="2软件安装_S1.png"/>

step2 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S2.png" alt="2软件安装_S2.png"/>

step3 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S3.png" alt="2软件安装_S3.png"/>

step4 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S4.png" alt="2软件安装_S4.png"/>

step5 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S5.png" alt="2软件安装_S5.png"/>

step6 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S6.png" alt="2软件安装_S6.png"/>

step7 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S7.png" alt="2软件安装_S7.png"/>

step8 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S8.png" alt="2软件安装_S8.png"/>

step9 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S9.png" alt="2软件安装_S9.png"/>

step10 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S10.png" alt="2软件安装_S10.png"/>

step11 如下图所示：

<img src="/images\posts\sniffer/2软件安装_S11.png" alt="2软件安装_S11.png"/>

# 3插件安装

配置驱动接口，wireshark支持软件USB抓包和硬件USB抓包的两种方式。软件抓包叫USBPcap ,在安装软件的时候可以勾选，由于我们有USB  sniffer 这个硬件抓包接口，所以并不会调用软件抓包这个接口。

调用硬件抓包接口需要添加驱动文件，如果我们的安装目录在【C:\Program Files\Wireshark】下，就找到 【C:\Program Files\Wireshark\extcap】这个文件夹，如果没有可以创建一个文件夹，加入 硬件调用接口【usb_sniffer_win.exe】。复制粘贴 【usb_sniffer_win.exe】到 【C:\Program Files\Wireshark\extcap】目录下。

如下图所示：

<img src="/images\posts\sniffer/3软件安装_插件目录.png" alt="拷贝调用接口到指定文件夹"/>

# 4软件使用---USB抓包方法

1 双击打开Wireshark软件。

<img src="/images\posts\sniffer/3软件使用_捕捉方法.png" alt="3软件使用_捕捉方法"/>

2 正确的选择捕捉速度

<img src="/images\posts\sniffer/3软件使用_捕捉速度.png" alt="3软件使用_捕捉速度.png"/>

3 双击开始捕捉，如图4.1里面所示的方法。

# 5 软件使用---数据过滤方法

在过滤框里面输入过滤关键字，如下图所示。

<img src="/images\posts\sniffer/5软件使用_过滤关键字.png" alt="5软件使用_过滤关键字.png"/>



| 过滤关键字                  | 功能                                      | 类型分类     |
| --------------------------- | ----------------------------------------- | ------------ |
| usb                         | 过滤usb协议内容                           | 协议分类     |
| usbll                       | 过滤usbll协议内容                         | 协议分类     |
| syslog                      | 过滤syslog协议内容                        | 协议分类     |
| usb.src =="host"            | 过滤源地址是“host”内容                    | 地址分类     |
| usb.dst =="0.25.0"          | 过滤目标地址是“0.25.0”内容                | 地址分类     |
| usbll.pid == 0xc3           | 过滤usbll.pid(usb通讯层，节点地址) 是0xc3 | 地址分类     |
| frame.len == 7              | 过滤帧的数据长度是7的包                   | 数长度分类   |
| usb.bInterfaceClass ==“hid” | 过滤接口类型是hid的包                     | 接口类型分类 |
| syslog.msg == "VBUS ON"     | 过滤syslog.msg 是 "VBUS ON"的 包          | 数据内容分类 |
| usb.idVendor                | 过滤包含usb.idVendor的包                  | 数据内容分类 |
| usb.idProduct               | 过滤包含usb.idVendor厂商信息的包          | 数据内容分类 |



运算符号

| 运算符     | 举例             |      |
| ---------- | ---------------- | ---- |
| 比较运算符 | ">"   "<"   "==" |      |
| 关系运算符 | “&&”   “\|\|”    |      |
| 括号运算符 | （）             |      |
| 取反运算符 | ！               |      |

```
例子1：usb.src=="0.10.1"&& (usb.dst=="host")&&(usb.bInterfaceClass=="hid")&&(frame.len != 100)
例子2：!(syslog.msg == "USB PHY error") &&!(usbll.invalid_pid) && !(usbll.pid == 0x5a) && !(usbll.pid == 0xa5) && !(usbll.pid == 0x69)
例子3：syslog && frame.len ==38
例子4：syslog && frame.len ==38 && syslog.msg =="Hardware buffer overflow"
例子5：(syslog && frame.len ==38 && syslog.msg =="Hardware buffer overflow") || (usb.idProduct && usb.dst =="host")
例子6：subll.data contains 80:06:00:01:00:00:12:00 
例子7：过滤空包的第二种方法 (frame.len != 24) && (frame.len > 3)
例子8：过滤空包的第三种方法 (syslog.msg != Keep-alive) || (usb)
```

# 6 常见问题详解---HOST没有接线

<img src="/images\posts\sniffer/客户问题—接线图.png" alt="客户问题—接线图"/>
下图是正确的示例：
host线必须接，host线必须接，host线必须接！！！
<img src="/images\posts\sniffer/客户问题_接线图_正确1.png" alt="客户问题_接线图_正确1.png"/>

# 7 常见问题详解---怎么判断设备的连接速度
下图是判断设备是否连接正确的方法：
<img src="/images\posts\sniffer/客户问题_选择速度是否正确.png" alt="客户问题_选择速度是否正确.png"/>

# 8 常见问题详解---空包过滤

下图是空包折叠功能的使用方法，当捕捉数据卡顿时候建议勾选。以节省电脑资源。让反应更及时。

<img src="/images\posts\sniffer/软件_折叠空帧.png" alt="软件_折叠空帧.png"/>

# 9 常见问题详解---常见设备数据包示例

下图1 ，USB低速设备USB鼠标的数据示例：

<img src="/images\posts\sniffer/软件_低速鼠标.png" alt="软件_低速鼠标.png"/>

下图2 ，USB全速设备USB转串口的数据示例：

<img src="/images\posts\sniffer/软件_全速设备.png" alt="软件_全速设备.png"/>

下图3 ，USB高速设备U盘的数据示例：

<img src="/images\posts\sniffer/软件_高速U盘.png" alt="软件_高速U盘.png"/>

# 10 命令行工具



```c
Usage: .\usb_sniffer_win.exe [options]

General:
  -h, --help                     print this help message and exit

Capture:
  -s, --speed <speed>            select USB speed: 'ls', 'fs' (default) or 'hs'
  -l, --fold                     fold empty frames
  -n, --limit <number>           limit the number of captured packets
  -t, --trigger <type>           capture trigger: 'disabled' (default), 'low', 'high', 'falling' or 'rising'
  --test                         perform a transfer rate test

Wireshark extcap:
  --extcap-version <version>     show the version of this utility
  --extcap-dlts                  provide a list of dlts for the given interface
  --extcap-interfaces            provide a list of interfaces to capture from
  --extcap-interface <name>      provide the interface to capture from
  --extcap-config                provide a list of configurations for the given interface
  -c, --capture                  start capture
  -f, --fifo <name>              output fifo or file name

Firmware update:
  --mcu-sram <name>              upload FX2LP firmware into the SRAM and run it
  --mcu-eeprom <name>            program FX2LP firmware into the EEPROM
  --fpga-sram <name>             upload BIT file into the FPGA SRAM
  --fpga-flash <name>            program JED file into the FPGA flash
  --fpga-erase                   erase FPGA flash
```

