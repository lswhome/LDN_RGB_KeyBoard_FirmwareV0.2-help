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
## 系统功能
   * 更新固件
   * 恢复默认值
   * 选择新的皮肤
   * 选择不同的语言
   * 设定关机后背光的状态
#### 配置界面
![](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/SystemCfg/SysCfg.png)
* 1-> 点击立即切换到BootLoader模式，只有在这个模式，才可以更新固件以及恢复默认值
* 2-> 在正常模式，刷入硬件配置文件用，由于是通用固件，不同的键盘通过硬件配置文件来区分，注意：如果错误的刷入了不匹配的硬件配置文件，有可能导致完全无法工作甚至损坏主控，请注意！！！
* 3-> 在BootLoader模式，点击可恢复默认值，**恢复后所有信息清空，请重新刷入硬件配置文件和默认的功能层0配置，否则键盘无法使用**
* 4-> 在BootLoader模式，点击可启动键盘固件，从而进入正常工作模式
* 5-> 在BootLoader模式，点击选择一个新的固件文件，如果固件文件不匹配，则会提醒错误，无法刷入
* 6-> 在BootLoader模式，如果刚才选择的固件文件检查正常，则本按钮可用，点击即可刷入新的固件，完成后会自动启动新的固件
* 7-> 刷新固件的时候，会显示一个进度条
* 8-> 提示信息在这里显示，如果刷写过程中产生任何信息，会在这里显示
* 9-> 选择UI界面的皮肤，选择后必须重新打开驱动软件，才会生效
* 10-> 多语言支持，从列表内选择一个支持的语言，选择后部分界面会立即改变，但一些动态生成的控件，无法改变，必须要在重新打开驱动软件，才会生效
* 11-> 关机后背光的工作状态，启用了这个功能后，才可以设定具体的关闭哪些灯光
* 12-> 可选择是否关闭4个WS2812灯效和背光灯效，相应的项目打勾表示启用，则当USB断开连接（数据断开连接，并非电源断开连接）的时候，相应的灯光会被关闭，如果是首次通电，则仍然会展示背光，直到10s后，如果仍然没有连接USB，则相应的灯光会被关闭，设置完毕后，点击**关闭**即可立即生效
****
[返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")
