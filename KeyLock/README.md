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
## 锁定键配置
   * 锁定键类似操作系统的“粘带键”，允许触发之后，设定的按键一直保持在按下状态，直到再次被触发，则释放对应的按键；
   * 最多可配置64组锁定键
   * 每组最多可配置8个按键被锁定，编号从1-8
   * 所有的按键都可以用来锁定
   * 编号1的最先被锁定，编号为8的最后被锁定（因为无法同时锁定，因此有锁定顺序）
   * 锁定键编组作为一个被动触发的功能，他只能被某个事件触发而执行，不能主动执行
   * 第一次被执行的时候，锁定组内的所有按键，第二次执行则自动解锁
   * **注意：**如果交叉锁定，则交叉的按键会被解除锁定，例：在0组锁定了A,B这两个按键,在1组锁定了B,C这两个按键，则B则为交叉锁定的按键，当锁定0组的时候，AB被锁定，此时锁定1组，则ABC被锁定，如果此时解除0组的锁定，则AB被解除锁定，因为B被包含在0组，解锁的时候会被解除锁定
   #### 配置界面
   ![](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/KeyLock/LockKey_Manager.png)
   * 1-> 从键盘内下载所有组的数据到驱动上
   * 2-> 上传所有组的数据到键盘内
   * 3-> 保存所有组的数据为文件，便于保存和共享
   * 4-> 读取之前保存的数据文件，便于再次修改和上传到键盘内
   * 5-> Group ID，组的编号，从0-63，一共64组
   * 6-> Key1，每个组内的按键编号，从Key1 - Key8，编辑时不可跳过，从Key1,Key2...的顺序编辑，中间不可有空缺，否则会导致空缺后的不会被锁定
   * 7-> **右键菜单->清除整组数据**，当前选择的组，整组数据会被清空
   * 8-> **右键菜单->清除当前单元格**，把当前选择的组的当前单元格的数据清空
   * 9-> **右键菜单->清空所选组的数据**，如果选择了多个组，则可以使用这个功能把所选的所有组数据清空
   ****
   [返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")
   
