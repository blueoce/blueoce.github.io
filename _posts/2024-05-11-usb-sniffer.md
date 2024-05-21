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

参考《1安装软件下载》 右边的USB插件驱动包里面。在插件驱动包里面。

## 问题2：Wireshark没有 USB Sniffer的选项？

参考《3插件安装》必须找到 【C:\Program Files\Wireshark\extcap】这个文件夹，并拷贝usb_sniffer_win.exe到其目录下。才会有USB Sniffer选项.

## 问题3：找不到usb_sniffer_win.exe文件？

参考《1安装软件下载》 右边的USB插件驱动包里面。在插件驱动包里面。

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

## 感谢大家的提问！！！



# 1安装软件下载

| 版本描述                                                    | Wireshark                                                    | USB插件驱动包                                                |
| ----------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 2024年5月最新版本【Version 4.2.5】                          | [Version 4.2.5](https://bluepi.lanzouo.com/iLg1L1yj7fjg)     | [win+linux+操作说明v1](https://bluepi.lanzouo.com/i3DZI1yjm7ti) |
|                                                             | [Version 4.2.4](https://bluepi.lanzouo.com/iLg1L1yj7fjg)     |                                                              |
| 由于服务器在国外，未翻墙国内用户请直接下载网页的PDF版本——》 | [提交版本[78bf8a6]_网页](https://bluepi.lanzouo.com/iGRMs1zeoocb) | updata 2024/5/21                                             |
|                                                             | [提交版本[c25a352]_网页](https://bluepi.lanzouo.com/iCwyi1z2mxaj) | updata 2024/5/18                                             |
| 最新软件获取网址                                            | [官网下载](https://www.wireshark.org/download.html)          |                                                              |

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

```

