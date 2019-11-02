李大拿的键盘固件V0.2说明
=====================
LDN_RGB_KeyBoard_FirmwareV0.2-help
=====================
李大拿的键盘固件V0.2的帮助文件，各种设置功能的说明和例子等等，我不懂英文，所以英文的是使用谷歌翻译的，国际友人凑合看吧。<br>
LDN keyboard firmware V0.2 help files, descriptions and examples of various settings functions, etc., I don't know English, so English is to use Google Translate, international friends can make it look.
****
Editor:LDN
****
## 驱动下载
**注意：低版本的固件，连接高版本的驱动，驱动软件会主动提示需要更新固件，并且在点击了提示的确定按钮后，会自动切换到BootLoader模式，此时直接选择固件文件并点击更新即可！不要再问切换到BootLoader的按钮为何点不了，因为已经是BootdLoader模式了。**<br><br>
最新版本的驱动下载，已支持音乐律动（默认中文）：[下载](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Drivers/(19-11-02)C3_LDN_RGB_KeyBoard_Drivers_v1.0_Chinese.rar?raw=true)<br>
The latest version of the driver download, has supported the music rhythm（Default Language English）：[DownLoad](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Drivers/(19-11-02)C3_LDN_RGB_KeyBoard_Drivers_v1.0_English.rar?raw=true)<br>
最新版本的硬件配置工具下载（只有中文，无教程，配置键盘硬件的工具，错误的配置可能导致主控损坏，请三思）:[下载](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Drivers/LDN_FW_Config_Tools.rar?raw=true)
****
## 更新日志
12:40 2019/11/2
**本次更新固件之后，之前的灯效配置会丢失，需要重新选择灯效。**<br>
增加了WS2812的音乐电平显示功能，底灯或者四灯也支持音乐电平显示了（会根据音乐跳动）<br>
支持修改不同版本的WS2812的颜色数据格式，默认是GRB格式<br>
支持调整WS2812的亮度，每一组都是独立可调的亮度（通过损失颜色位数从而降低亮度），降低亮度从而降低了耗电，避免USB口供电不足<br>
增加了新的背光驱动方案，同时兼容老的方案，消隐效果更好，驱动能力也更好（颜色更明亮鲜艳）<br>


14:44 2019/10/12
修复了M4处理器的BIOS识别BUG

15:50 2019/8/20
修复了休眠模式无法唤醒的BUG

15:21 2019/8/14
增加了音乐律动支持，目前有2个律动灯效

16:15 2019/7/14
支持STM32F405/F407主控

17:19 2019/6/26
修复了驱动上的触发层编辑器中，【清空本层数据】功能，实际上是清空了，但是界面没有刷新的BUG。

12:08 2019/6/5
更新了英文语言包


10:53 2019/6/4
更新了3个灯效，固定灯效从0-14
更新了版本匹配逻辑，驱动与固件不匹配，无法使用


## 驱动文件说明：<br>
Readme.txt           ->自述文件<br>
xxxx.ldn             ->最新版本的固件<br>
KeyBoardCode.ini     ->USB键码配置文件<br>
MediaKeyCode.ini     ->多媒体键码配置文件<br>
Skin.ini             ->皮肤和语言配置文件<br>
xxxx.bmp             ->测试用的24位色BMP图片<br>
LDNKBConfigTools.exe ->驱动主程序<br>
**C3_LDN_LedEffectTools.exe ->律动的支持程序，要使用律动功能，必须打开这个程序，要使用律动，必须打开这个工具**<br>
Update log.txt       ->更新日志<br>
ConfigFiles          ->文件夹，保存不同的键盘的硬件配置文件和默认功能层0的键位<br>
ConfigFiles\\[KeyBoard Name]\HWConfig.PhyCfg ->对应键盘的硬件配置文件<br>
ConfigFiles\\[KeyBoard Name]\FunctionLayer_0_Config.FLCfg ->对应键盘的功能层0的配置文件<br>
Language\xxx.ini ->对应语言的语言包，可自行翻译，按照格式即可<br>
****
# 软硬件特性
#### 硬件特性
   * 使用STM32F103(72Mhz) or STM32F405/407(168Mhz) ARM核心的处理器
   * 独立的SPI FLASH芯片储存配置信息
   * 独立的LED驱动芯片(MBI5042GP)具备16位PWM精度(RGB颜色：256x256x256=1677万色)，36/33.6Mhz PWM灰度时钟频率，最多可驱动128颗RGB全彩灯珠
   * 行扫描频率从800~3000HZ连续可变
   * 行扫描数量从1~8连续可变
   * 按键矩阵从1x1到22x8可配置
   * 硬件支持全健无冲
   * 使用USB 1.1 HID协议
   * 支持WS2812/SK6812 RGB灯珠通信协议
   
   ----
   
#### 软件特性
   * 使用LDN自己研发的实时调度核心，提供极速的实时响应
   * 矩阵键盘支持1~176个按键，连续可配置
   * 软件支持全键无冲（NKRO）和6键无冲（6KRO）
   * 1000Hz的USB回报率
   * 1677万色的RGB背光灯
   * 最多支持32颗 WS2812/SK6812 协议的RGB全彩氛围灯，可分4组配置灯效
   * 支持四灯小板
   * 可以自定义背光灯效
   * 内置一些固定的全彩灯效，可随意切换展示
   * **支持全局音乐律动，任何播放器都可以律动了**
   * CAPS SCROLL NUM三个指示灯可以使用任意LED来指示（轴灯或者氛围灯）
   * 当点亮或者熄灭三个指示灯的时候，可以编程为任意功能
   * 具备配置功能工具(目前只有WINDOWS版本)，提供大量的实时可编程功能
   * 几乎支持所有的USB键码和多媒体键码(有的键码需要操作系统支持)
   * 强大的宏功能，可以模拟键盘的绝大多数操作，可控制键盘的几乎所有功能
   * __所有的设置都是保存在键盘的SPI FLASH内，掉电不会丢失__
   * __所有的重要设置，都可以保存为文件，便于保存和恢复以及共享给好友__
   * __可以通过驱动软件恢复默认值，更新固件，就算故意中断固件的更新也不会损坏键盘__
   
   ----
    
#### 具备8个功能层，每个层独立又有关联，编程方式灵活易用
   * 每一个功能层就相当于一个键盘
   * 具备优先级规则，**优先级最高的最先扫描**，其后的按照0~7的顺序扫描
   * 每个层的每个按键都可以独立配置 **[按键按下]** 事件和 **[按键释放]** 事件
   * 每个层的每个按键都可以配置为具备的任何功能
   * 每个层都有独立的开关
   * 同时只能把一个层设置为最高优先级
   * 当开关状态或者优先级改变的时候，驱动软件会同步显示
   * 可以通过编程的方式，打开/关闭/设置某层为最高优先级
   
   ----
   
#### 具备8个触发层，每个层独立工作，可与8 个功能层的任意层搭配实现复杂的功能 
   * 每一个触发层可以配置8个FN键，任意键都可以是FN键，同时FN键还**支持条件触发功能**
   * 每一个触发层可以配置48组组合键，配合FN键，可实现多种触发功能
   * 每一个触发层可以配置64组连击键，一个按键变成N个按键的功能
   * 每一个触发层可以配置64组二合一键
   * 每一个触发层可以配置64组按下保持键，触发方式更灵活
   * 同时只能激活一个触发层
   * __触发层的优先级高于功能层__
   * 可以通过编程的方式，自动激活某个触发层
   
   ----

# 说明文档的索引

## [基本知识点](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Basic/README.md "点击跳转")
   * [操作系统如何识别按键被按下和释放](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Basic/README.md#操作系统如何识别按键被按下和释放 "点击跳转")
   * [USB报告率](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Basic/README.md#USB报告率 "点击跳转")
   * [全键无冲/6键无冲](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Basic/README.md#全键无冲6键无冲 "点击跳转")
   * [1677万色](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Basic/README.md#1677万色 "点击跳转")
   ----
## [功能层](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/README.md "点击跳转")
   * [概述](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/README.md#概述 "点击跳转")
   * [配置界面](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/README.md#功能层的配置界面 "点击跳转")
   * [扫描规则](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/README.md#扫描规则 "点击跳转")
   * [配置例子](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/README.md#配置例子 "点击跳转")
----

## [触发层](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md "点击跳转")
   * [概述](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#概述)
   * [主界面](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#主界面)
   * [管理功能](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#管理功能)
   * [FN键配置](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#FN键配置)
   * [组合键配置](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#组合键配置)
   * [连击键配置](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#连击键配置)
   * [二合一键配置](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#二合一键配置)
   * [按下保持键配置](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#按下保持键配置)
   * [配置示例](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/TriggerLayer/README.md#配置示例)
----
## [宏](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Macro/README.md "点击跳转")
----
## [锁定键](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/KeyLock/README.md "点击跳转")
----
## [按键灯（轴灯）配置](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/KeyLedCfg/README.md "点击跳转")
----
## [扩展灯效和指示灯动作配置](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/ExLedEff_LedActionCfg/README.md "点击跳转")
----
## [自定义背光灯效](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/tree/master/CustomLedEff/README.md "点击跳转")
----
## [系统功能](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/tree/master/SystemCfg/README.md "点击跳转")
----
## [功能选择](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionSelect/README.md "点击跳转")
   * [概述](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionSelect/README.md#概述)
   * [常规按键](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionSelect/README.md#常规按键页面)
   * [多媒体按键](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionSelect/README.md#多媒体按键页面)
   * [开关控制](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionSelect/README.md#开关控制页面)
   * [宏功能](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionSelect/README.md#宏功能页面)
   * [灯光控制](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionSelect/README.md#灯光控制页面)
----
## [配置示例](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Example/README.md)
   * [通过FN键和层来实现更多功能](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Example/README.md#通过FN键和层来实现更多功能)
   * 更多的待更新...
----











