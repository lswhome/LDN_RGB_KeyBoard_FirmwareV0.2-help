李大拿的键盘固件V0.2说明
=====================
LDN_RGB_KeyBoard_FirmwareV0.2-help
=====================
李大拿的键盘固件V0.2的帮助文件，各种设置功能的说明和例子等等，我不懂英文，所以英文的是使用谷歌翻译的，国际友人凑合看吧。<br>
LDN keyboard firmware V0.2 help files, descriptions and examples of various settings functions, etc., I don't know English, so English is to use Google Translate, international friends can make it look.
****
Editor:LDN<br>
[返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")
****
## 扩展灯效和指示灯动作配置
   * 最多可控制32颗使用WS2812/SK6812协议的RGB灯珠
   * 这些灯珠可被分为1-4组独立控制
   * 根据不同的设计，部分PCB型号会板载一部分灯珠作为氛围灯，32颗的限制也包含了这些灯珠
   * 三颗指示灯(CAPS SCROLL NUM)具备动作触发功能，在点亮或者熄灭的时候，都可以配置一个触发事件
#### 配置界面
![](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/ExLedEff_LedActionCfg/ExEffect.png)
   * 1-> 选择WS2812的灯效编组，从0-3，共计4组
   * 2-> 启用：打勾表示启用这个组，否则禁用这个组
   * 3-> 选择使用灯珠的编号，从第几个编号的灯珠开始控制
   * 4-> 选择使用灯珠的百年好，到第几个编号的灯珠结束，例如从6到10，则表示从第7个灯珠开始（编号为0的灯珠为第一个）到编号为10的灯珠结束，**共计5颗灯珠，不是4颗哦，请注意**
   * 5-> 当前组使用的5种灯效，选择即可
   * 6-> 当前灯效的运行速度，滑动即可调节
   * 7-> 如果选择了设定的颜色（呼吸或者渐变），则通过0-3的颜色选择，固件可通过这4个设定的颜色，产生一些灯效
   * 8-> 全部设置完毕后，点击“上传”即可立即生效
   * 9-> CAPS指示灯的动作触发配置，打勾表示启用，否则禁用
   * 10-> 如果设置完毕，点击上传立即生效
   * 11-> 点击即可弹出功能选择窗口，可选择一个功能用于当CAPS指示灯点亮的时候，所做的事
   * 12-> 点击即可弹出功能选择窗口，可选择一个功能用于当CAPS指示灯熄灭的时候，所做的事
   * **SCROLL NUM的配置方法相同**
   ****
   [返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")

