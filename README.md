===============================================================================
# asrock-Z490M-itx/ac-hackintosh  opencore0.6.6
===============================================================================



更新部分

☆ 升级kext驱动到最新正式版本

☆ 音频输出 增加了核显（DP或者HDMI）显示器音频输出

☆ 精简ACPI ，添加系统判断，避大部分免OC引导windows蓝屏

☆ device properties 内包含RX55000xt\5600&5700优化信息，需要手工启用（去掉前置#就行）

☆ 更换OC主题包（支持OC UI 随意切换有三个背景选择，改名为Background.icns即可）

☆ 正常直升11.2 （支持11.3 beta x）

![](https://github.com/Xmingbai/hackintosh-opencore--UI-theme/blob/main/TipsBackground.png)


===============================================================================
# asrock-Z490M-itx/ac-hackintosh  opencore0.6.4
===============================================================================

更新部分

☆ 升级kext驱动到最新正式版本

☆ 新增一组配置文件 AMD RX5XX& IGPU.plist

☆ 更换OC主题包

☆ 正常直升11.1 20C69

![](https://github.com/Xmingbai/asrock-Z490M-itx-ac-hackintosh-Opencore/blob/main/11.1%2020C69.png)

![](https://github.com/Xmingbai/asrock-Z490M-itx-ac-hackintosh-Opencore/blob/main/%E6%96%B0OC%E4%B8%BB%E9%A2%98.png)






================================================================================

# asrock-Z490M-itx/ac-hackintosh  opencore0.6.3
================================================================================

asrock Z490M itx hackintosh Catalina 10.15.x &   big sur 11.0.1


# 1.基本硬件配置清单 及截图

CPU：i7-10700（可以支持所有十代）

主板：Asrock Z490M itx/ac

SSD：SN750 500G

Wi-Fi：intel wifi 更换为 BCM94352Z

内存；十铨火神DDR4 3000  16gx2

# 若有其他问题请加Q群：1125705781，备注小明或者B站，也欢迎关注B站：小明和他的女朋友

此份操作指南 同步 发布于B站专栏，方便国内访问  

https://www.bilibili.com/read/cv8721205 

# 2.macOS 状况

OC0.6.3 支持Catalina 10.15.x 和Big Sur 11.0.1 支持OTA升级，支持直装

## PC截图

![](https://github.com/Xmingbai/asrock-Z490M-itx-hackintosh/blob/main/%E5%85%B3%E4%BA%8E%E6%9C%AC%E6%9C%BA.png)

![](https://github.com/Xmingbai/asrock-Z490M-itx-hackintosh/blob/main/CPU%20geekbench.png)

![](https://github.com/Xmingbai/asrock-Z490M-itx-hackintosh/blob/main/IGPU%20DP%25HDMI.png)

## 基本功能

CPU正常睿频

核显双硬解正常

核显支持双4K显示器，DP支持4K60HZ，HDMI支持4K30HZ

若使用独显5500、5600、5700 配置文件自带显卡性能优化

音频输出正常（alcid=50）

支持有线双网卡（1000M+2.5G）

蓝牙、WiFi正常  支持隔空、接力、随航

睡眠及唤醒正常，支持USB唤醒

支持开机启动音，支持双系统启动界面选择

未修正的地方 ：暂未发现

# 3.bios 设置参考指南   

https://www.bilibili.com/read/cv7393476


另 四大主板厂商华擎、华硕、微星、技嘉 针对性 详细截图 黑苹果bios设置 参考B站专栏


https://space.bilibili.com/591453294/article


# 4.OC0.6.3 引导使用指南 

## 4.1 基本驱动及对应版本

Lilu.kext----------------------------1.4.9

VirtualSMC.kext--------------------1.1.8 

WhateverGreen.kex----------------1.4.4

AppleALC.kext---------------------1.5.4

IntelMausi.kext---------------------1.0.4

LucyRTL8125Ethernet.kext---------1.0.0

NVMeFix.kext----------------------1.0.4


## 4.2 OC配置文件config.plist如何使用

### 情景NO.1  无独显默认config.plist      

支持核显双4K输出，DP支持4K60HZ，HDMI支持4K30HZ

### 情景NO.2  AMD RX5500t& IGPU.plist     

支持AMD RX5500XT 仿冒成Radeon Pro W5500X  ，IGPU核显作为加速 ，id为0300C89B

### 情景NO.3  AMD RX5600/5700& IGPU.plist 

支持AMD RX5600XT、5700、5700XT 仿冒成Radeon Pro W5700X  ，IGPU核显作为加速，id为0300C89B

### 情景NO.4  AMD RX5XX& IGPU.plist  

支持独显AMD RX560、570、580、590等  ，IGPU核显作为加速，id为0300C89B

### 根据自己实际情况，选择对应配置文件改名为config.plist，最好自己重新生成三码。


## 4.3 USB端口定制了15个端口，见USBports截图

![](https://github.com/Xmingbai/asrock-Z490M-itx-hackintosh/blob/main/USBports.png)

双网口附近的4个USB支持10G速率


### USB具体分布如下图

![](https://github.com/Xmingbai/asrock-Z490M-itx-hackintosh/blob/main/%E4%B8%BB%E6%9D%BFUSB%20%26%E6%9C%BA%E7%AE%B1%E5%89%8D%E7%BD%AEUSB.png)


![](https://github.com/Xmingbai/asrock-Z490M-itx-hackintosh/blob/main/%E5%90%8E%E7%BD%AEUSB.png)



## 4.4 如何使用2.5G有线网卡
 
 联网设置：系统偏好设置—-网络—以太网—高级——硬件—配置有自动改为手动，速率手工设置为1000 全双工（或100，取决于网线链接路由器的端口速率），见图


![](https://github.com/Xmingbai/asrock-Z490M-itx-hackintosh/blob/main/2.5G%E7%BD%91%E5%8D%A1%E8%AE%BE%E7%BD%AE.png)

# 若有其他问题请加Q群：1125705781，备注小明或者B站

# 也欢迎关注B站：小明和他的女朋友

https://space.bilibili.com/591453294?spm_id_from=333.788.b_765f7570696e666f.2

