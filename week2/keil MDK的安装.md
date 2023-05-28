# keil MDK的安装

## 一、获取文件夹

解压文件，文件夹下有四个文件夹，分别为`keil MDK及注册机`、`pack`、`固件库`和`驱动`，其中`keil MDK及注册机`用来下载软件并破解，`pack`里存放着F1的pack包，`固件库`里存放着F1的标准库，`驱动`存放着计算机驱动。

## 二、安装keil MDK

打开`keil MDK及注册机`文件夹里的`MDK524a.EXE`,开始安装。

点击Next。勾选I agree，然后Next。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/1.png)

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/2.png)

更改安装路径，安装路径可以自行选择，注意路径中不要带有特殊字符和**中文**。然后Next。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/3.png)

填写个人信息，随便填即可，然后Next。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/4.png)

等待软件的安装。期间可能会弹出是否安装ULink驱动，安装即可。

取消掉这个勾，要不会弹出发布文档，然后Finish。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/5.png)

## 三、安装器件支持包

### 1.离线安装

打开`pack`文件夹里的`Keil.STM32F1xx_DFP.2.2.0.pack`。

直接点击Next。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/6.png)

等待安装，然后Finish。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/7.png)

### 2.在线安装

打开keil，点击pack installer，如图：

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/8.png)

点击OK，等待列表的更新(需要联网，并且速度极慢)。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/9.png)

在STMicroelectronics下找到STM32F1 Series，在右边找到Keil::STM32F1xx_DFP，点击右侧的install下载。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/10.png)

等待安装。

对于其他芯片也可以使用此方法获取器件安装包

## 四、软件注册（破解）

以管理员身份运行Keil MDK，在菜单栏中，找到File，点击License Management，复制CID。（界面先不要关闭）

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/11.png)

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/12.png)

打开`keil MDK及注册机`文件夹里的`keygen_new2032.exe`。将CID粘贴进去，Target选择ARM，点击Generate，复制生成的序列码。（温馨提示：不要打开声音）

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/13.png)

回到Keil MDK的License Management界面，将序列码粘贴到New License ID Code的位置，点击Add LIC。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/14.png)

破解完成。

## 五、安装驱动

### 1.ST-Link驱动

打开`驱动`文件夹，`dpinst_amd64.exe`是64位计算机的驱动，`dpinst_x86.exe`是32位计算机的驱动，根据自己的情况进行选择。

点下一步，点完成。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/15.png)

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/16.png)

驱动安装完成。

### 2.USB转串口驱动

打开`驱动`文件夹里的`CH341SER.EXE`。

点击安装，等待安装完成。

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/Keil%20MDK/17.png)

驱动安装完成。

## 六、结束

相信，经过此文档，你已经完成了对STM32F1系列芯片开发环境的搭建。如果仍不清楚，请观看视频[P3 2-1](https://www.bilibili.com/video/BV1th411z7sn?p=3&vd_source=d2cca62dad1d803aec61ecad5974de67)