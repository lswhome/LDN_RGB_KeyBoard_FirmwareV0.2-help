李大拿的键盘固件V0.2说明
=====================
LDN_RGB_KeyBoard_FirmwareV0.2-help
=====================
李大拿的键盘固件V0.2的帮助文件，各种设置功能的说明和例子等等，我不懂英文，所以英文的是使用谷歌翻译的，国际友人凑合看吧。<br>
LDN keyboard firmware V0.2 help files, descriptions and examples of various settings functions, etc., I don't know English, so English is to use Google Translate, international friends can make it look.
****
Editor:LDN

[返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")

****
## 功能层
   * [概述](#概述)
   * [配置界面](#功能层的配置界面)
   * [扫描规则](#扫描规则)
   * [配置例子](#配置例子)
****
   #### 概述
   * 功能层类似多个不同按键功能的键盘的集合，使用**功能层**管理器来管理这个集合
   * 每个功能层就相当于一个不同功能的键盘，其上每个按键的功能，都可以被重新配置
   * 每个层都有自己的开关，默认是打开的，当一个层被关闭，扫描器就会跳过那个层，跳过的层上所配置的所有功能都会被忽略
   * 当一个关闭的层被设置为最高优先级的时候，这个层的开关会自动被打开
   * 当层的状态被改变（切换了层、层被打开关闭），会同步显示在驱动软件上（如果同时你打开了驱动软件的话）
   * 功能层一共有8个层，编号从0-7
   * 0层的优先级最高，7层的优先级最低
   * 扫描顺序从**0->7，默认0层的优先级最高**
   * 通过设置某层为最高优先级，扫描顺序可以被改变
   * 每个层的每个按键都具备2个触发事件：**按下事件** 和 **释放事件**
     * **按下事件：** 当你按下一个按键的时候，触发 **按下事件**
     * **释放事件：** 当你释放一个被按下的按键时，触发 **释放事件**
     * *按下事件* 和 *释放事件*总是成对触发，先触发 **按下事件**，再触发 **释放事件**
   * 按键**默认没有被配置**，没有被配置的按键为**透明模式**
   * 按键可以被配置为**禁用模式**，这样可以禁止扫描器扫描比这个层优先级更低的层上对应的按键
   * 设置都会保存在键盘内部，掉电不会丢失，工作的时候，无需驱动软件的参与
****
   #### 功能层的配置界面
   ![PNG File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayerAll.png "")
   
   * 1  功能层标签页
   * 2  KeyBoard Connected表示已连接键盘固件，BootLoader Connected表示键盘进入了BootLoader模式，并且已连接
   * 3  HwVer:0.1 硬件的版本号
   * 4  FwVer:0.1 固件的版本号
   * 5  BootLoaderVer:0.1 表示BootLoader的版本号
   * 6  当前编辑的功能层，通过这里选择编辑哪个层
     ![PNG File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayerEditLayers.png)
        * 1-> **橘黄色**表示当前正在编辑的层
        * 2-> **蓝色**表示其他未编辑的层
        * 3-> Layer0 - Layer7表示8个层的编号
        * 4-> **鼠标左键**单击，会**切换**到这个层
        ****
   * 7  当前功能层的优先级以及开关状态，通过这里改变层的优先级以及开关状态
     ![PNG File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayerLayerSwitch.png)
        * 1-> **浅绿色** 表示层的状态为**打开状态**
        * 2-> **橘黄色** 表示这个层当前为**优先级最高**
        * 3-> **灰色** 表示这个层是**关闭状态**
        * 4-> **鼠标左键** 单击，切换层的**打开关闭状态**
        * 5-> **鼠标右键** 单击，把某层设置为**最高优先级**，注意：当右键单击一个被关闭的层的时候，这个层会自动被打开
        ****
   * 8  功能层的管理功能，上传或者下载配置到键盘内，也可以把配置保存为文件，方便保存和共享给好友
     ![PNG File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayerManager.png)
        * 1-> 下载配置，把配置从键盘内下载到驱动上，**注意：这个操作仅仅下载当前选择的层的数据**
        * 2-> 上传配置，把配置上传到键盘内，**注意：这个操作仅仅上传当前选择的层的数据**
        * 3-> 加载配置，载入之前保存为文件的层配置到当前选择的层
        * 4-> 清空本层数据，会删除当前选择的层的所有配置，恢复到空白的状态
        * 5-> 保存配置，把当前选择的层的配置信息保存为文件，便于保存和共享给好友
        * 6-> 应用配置，**如果改变了层的开关状态和优先级，点击“应用配置”之后才会生效**
        * 7-> **注意：由于是通用固件，因此不同的键盘的配置会有所不同，错误的导入别的键盘的配置，可能会导致不可预知的问题 ，甚至完全无法工作。**
        
        ****   
   * 9  当前键盘的配列图示以及编辑区，同时会显示每个按键配置的功能
     ![PNG File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayerEditer.png)
        * 1-> 编辑器的布局，不同的键盘由于配列不同，这里的显示也会不同(如图显示的是一个60%的键盘配列)
        * 2-> 在方框(**按键**)的**上半部分**，表示 **释放事件** 所配置的功能，**鼠标左键单击上半部分会弹出功能选择窗口**
        * 3-> 在方框(**按键**)的**下半部分**，表示 **按下事件** 所配置的功能，**鼠标左键单击下半部分会弹出功能选择窗口**
        * 4-> 方框(**按键**)的右边的数字编号，表示 **这个按键在键盘内部的编号，很重要，很多功能都需要使用这个编号**
        * 5-> **鼠标右键单击**某个按键的上半部分或者下半部分，则**清除那个事件的配置**
        * **注意：** 对于 **常规按键** 和 **多媒体按键**，操作系统要求成对的接收到键码数据，也就是说，如果你只设置 **按下事件** 而不设置 **释放事件**，这会导致操作系统认为你的**按键一直处在按下状态**，这将导致问题；对于这两种的按键的编程，只需要点击**下半部分**进入**功能能选择窗口**，功能选择完成后会自动设置**释放事件**的设置，如果您点击**上半部分**进入**功能选择窗口**，则不会自动设置**按下事件**，请注意！！！
        ****
   * 10 在方框(**按键**)的**上半部分**，表示 **释放事件** 所配置的功能，**鼠标左键单击上半部分会弹出功能选择窗口**
   * 11 在方框(**按键**)的**下半部分**，表示 **按下事件** 所配置的功能，**鼠标左键单击下半部分会弹出功能选择窗口**
   * 12 方框(**按键**)的右边的数字编号，表示 **这个按键在键盘内部的编号，很重要，很多功能都需要使用这个编号**
   * 13 当鼠标悬停在某个方框(**按键**)上的时候，会弹出提示框，显示这个按键所配置的功能详解
     ![PNG File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayerTip.png)
        * 1-> 当前配置的功能，不同的功能有不同的提示
        * 2-> 当前配置的功能具体的功能
        * 3-> 如果配置的是键码，则显示键码的USB编码     
****
   #### 扫描规则<br>
   ![Png File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayerScan.png)
      * 当前图示的前提是，层0,1,2,3,5,6,7开启，层4关闭，层2优先级最高
      * 1-> 层2优先级最高，所以层2最先被扫描，如果层2上对应的按键有配置功能，则输出那个配置的功能，同时停止扫描；如果没有配置功能(默认为透明模式)，则继续从层0开始扫描，直到碰到有配置的按键或者扫描到最后一个层为止；如果**按键被禁用**，则停止扫描
      * 2-> 层4被关闭，扫描的时候会跳过层4的扫描，层4上**所有被配置的功能都会被忽略**
****
   #### 配置例子<br>
   * 更改按键功能
      * 将层0的**A**键更改为**B**：
      ![Png File](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayer_example_1.png)
           * 1-> 点击 **功能层配置**
           * 2-> 点击默认层 **Layer0**
           * 3-> 点击 **下载配置**
           * 4-> 点击**A的下半部分**，会弹出如下的窗口
           ![](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayer_example_2.png)
           * 1-> 点击 **常规按键** (默认)
           * 2-> 点击 "B"，窗口会自动关闭
           ![](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/FunctionLayer/FuncLayer_example_3.png)
           * 1-> "A"按键已经变成了"B"
           * 2-> 鼠标悬停在刚才更改的"B"上，会提示具体的功能
           * 3-> 点击 **上传配置**，完成改键，此时再次按下键盘的"A"，输出的就是"B"
      
   
****

[返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")

