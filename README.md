李大拿的键盘固件V0.2说明
=====================
LDN_RGB_KeyBoard_FirmwareV0.2-help
=====================
李大拿的键盘固件V0.2的帮助文件，各种设置功能的说明和例子等等，我不懂英文，所以英文的是使用谷歌翻译的，国际友人凑合看吧。<br>
LDN keyboard firmware V0.2 help files, descriptions and examples of various settings functions, etc., I don't know English, so English is to use Google Translate, international friends can make it look.
****
Editor:LDN
****
## 软硬件特性
#### 硬件特性
   * 使用STM32F103(72Mhz) or STM32F405/407(168Mhz) ARM核心的处理器
   * 独立的SPI FLASH芯片储存配置信息
   * 独立的LED驱动芯片(MBI5042GP)具备16位PWM精度(RGB颜色：256x256x256=1677万色)，36/33.6Mhz PWM灰度时钟频率
   * 行扫描频率从800~3000HZ连续可变
   * 行扫描数量从1~8连续可变
   * 按键矩阵从1x1到22x8可配置
   * 硬件支持全健无冲
   * 使用USB 1.1 HID协议
   * 支持WS2812/SK6812 RGB灯珠通信协议
#### 软件特性
   * 矩阵键盘支持1~176个按键，连续可配置
   * 软件支持全键无冲（NKRO）和6键无冲（6KRO）
   * 1000Hz的USB回报率
   * 1677万色的RGB背光灯
   * 最多支持32颗 WS2812/SK2812 协议的RGB全彩氛围灯，可分4组配置灯效
   * 支持四灯小板
   * 可以自定义背光灯效
   * 内置一些固定的全彩灯效，可随意切换展示
   * CAPS SCROLL NUM三个指示灯可以使用任意LED来指示（轴灯或者氛围灯）
   * 当点亮或者熄灭三个指示灯的时候，可以编程为任意功能
   * 具备配置功能工具(目前只有WINDOWS版本)，提供大量的实时可编程功能
   * 具备8个功能层，每个层独立又有关联，编程方式灵活易用
   * 具备8个触发层，每个层独立工作，可与8 个功能层的任意层搭配实现复杂的功能 
   
   
