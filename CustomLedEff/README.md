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
## 自定义灯效配置
   * 自定义灯效允许用户对每一个按键的轴灯设定一个24位颜色深度的颜色
   * 可以导入一个对应显示矩阵大小的24位颜色深度的图片作为背光图片显示
   * 支持5种简单的灯效展示
   * 可单独为每个灯效设置运行速度
   * 最多可设定8组灯效
   * 最多可导入100幅图片
   * **请注意：默认所有的图片都是白色，也就是说，RGB颜色分量值是255,255,255**
   ![](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help/blob/master/CustomLedEff/CustomLedEffect.png)
   * 1-> 选择编辑第几个自定义灯效编组，从0-7，共计8个组
   * 2-> 这个组使用的图片编号（第几个图片），与(7)对应，从0-99
   * 3-> 灯效的运行速度
   * 4-> 5种简单的灯效，选择即会自动产生对应的效果
   * 5-> 设置完毕，点击“上传”即可保存到键盘内
   * 6-> 载入一个外部的24位BMP图片，分辨率最好与键盘的背光显示矩阵相同（PCB的说明内会有说明矩阵的大小），否则显示效果会很难看
   * 7-> 当前编辑第几个图片，从0-99，共计100张图片
   * 8-> 把所有的轴灯设置为随机的颜色
   * 9-> 从键盘内下载当前选择的图片编号的数据到驱动上，便于编辑和查看
   * 10-> 把当前编辑的图片上传到键盘内，请注意这个操作只会上传当前选择的编号的图片到键盘内
   * 11-> 把所有的轴灯设置相同的颜色
   * 12-> 1像素的轴灯显示矩阵参考
   * 13-> 16倍放大的轴灯显示矩阵参考，点击即可设置颜色，鼠标悬停时如果提示**“显示”**，则表示这个轴灯是会被展示的，如果显示**“隐藏”**，则表示这个轴灯虽然可设置，但由于实际键盘矩阵排列的关系，不会被展示
   * 14-> 实际按键配列排列的显示矩阵参考，点击即可设置颜色，鼠标悬停时，会显示按键的内部编号和RGB的颜色分量值
   * 15-> 鼠标悬停时显示的提示信息，内部编号和RGB分量值
   ****
   [返回主目录](https://github.com/lswhome/LDN_RGB_KeyBoard_FirmwareV0.2-help "点击返回")
   
  
   
   
