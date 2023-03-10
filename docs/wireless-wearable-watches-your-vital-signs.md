# 无线可穿戴手表您的生命体征

> 原文：<https://hackaday.com/2017/03/13/wireless-wearable-watches-your-vital-signs/>

这是[麦考伊博士]期待已久的医务室生物床，带有无线传感和生命体征显示吗？不完全是，但是这个可穿戴的病人监视器已经非常接近了。从它的外观来看，[亚瑟]的系统甚至可能比[骨头]监测更多的参数从原来的系列。

从[Arthur]之前对进行逆向工程的自动血压袖带开始，他开始添加传感器。脉搏、心电图、呼吸率、皮肤电反应和体温都可以通过一个小巧的可佩戴式手腕设备进行测量。它并不完全是无线的——指尖脉搏血氧仪电子狗和胸部电极仍然需要有线连接到中央单元——但传感器都与 Teensy 3.2 通信，然后通过蓝牙与 Android 应用程序通信，所以没有必要与显示器相连。说到电极，我们对[Arthur]使用的 ADS1292 芯片很感兴趣，它不仅可以检测心脏的电信号，还可以通过胸壁扩张和收缩时阻抗的变化来检测呼吸。当然，还有通过雷达进行的[呼吸描记术，也可以集成到这个传感器套件中。](https://hackaday.com/2015/08/15/arduino-radar-watches-you-breath/)

这一切都很酷，我们可以很容易地看到这个应用程序的修改版本显示在一个大平板电脑或显示器上，既是一个准确的道具重建，也是一个有用的医疗设备。

 [https://www.youtube.com/embed/U5jK3dh345U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U5jK3dh345U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

