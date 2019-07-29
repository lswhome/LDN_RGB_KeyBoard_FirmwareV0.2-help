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
## 宏
   * 宏可以把各种序列化的重复的工作，制作成一个顺序执行的“脚本”，比如输出一个字符串，或者控制键盘的一些功能，比如开关层，切换层，管理背光等；宏具备跳转功能，因此可以制作带有循环功能的“脚本”，也支持把多个宏连接起来，变成一个超长的宏
   * 最多可编辑100组宏，从0-99
   * 每一组宏最多可编辑512步，从0-511
   * 宏执行器每隔1毫秒(0.001s)执行一条指令
   #### 配置界面
   ![png File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/Macro/Macro_Manager.png)
   * 1-> 当前要编辑的组的编号，从0-99
   * 2-> 把宏数据从键盘下载到驱动上，以便观察和修改
   * 3-> 把当前编辑的宏上传到键盘内
   * 4-> 把当前组的宏数据保存为一个文件，以便保存和共享给好友
   * 5-> 把之前保存的宏重新读入，便于修改和上传到键盘内
   * 6-> Step ID，表示当前宏的第几步，宏是按照一步一条指令执行的
   * 7-> FuncTions，当前这步宏的命令，双击即可重新选择指令，双击空白处即可增加新的指令
   * 8-> **右键菜单->清除当前步数据**，点击会清除当前选择的步的数据
   * 9-> **右键菜单->清除所选步数据**，点击会清除当前选择的所有步的数据
   ****
   [返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")
