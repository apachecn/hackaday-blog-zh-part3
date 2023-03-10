# 汽车的反向工程媒体控制器是安卓的好朋友

> 原文：<https://hackaday.com/2018/06/04/reverse-engineered-media-controller-from-car-is-best-friends-with-android/>

对于黑客来说，CAN 总线是一个可以挖掘的丰富矿脉:允许当前大多数车辆的电子元件被重新利用并轻松控制。[MikrocontrollerProjekte]对 CAN 总线媒体和导航控制器进行了逆向工程，并将其连接到 STM32F746G-Discovery 板。STM32 依次连接到 Android 手机，并允许媒体控制器触发手机上的大量功能，包括音乐播放、地图和一般的 Android 导航。

![](img/52482a07a0c57fdf28ded4ad745f016a.png)

在对控制器进行逆向工程时，[MikrocontrollerProjekte]采用了多种方法。在网上发现了少量信息，对随机 CAN 总线 id 和消息进行了一些模糊处理，并使用车内设备进行了一些数据记录，以识别总线上相关 id 的消息数据。

STM32F746G-Discovery 板充当人机接口设备(HID)，模拟通过 USB OTG 连接到 Android 手机的鼠标和键盘。LCD 屏幕显示击键和触摸板区域的输出。鉴于这款手机有触摸屏，我们不确定鼠标模拟会有多大用处，但媒体功能非常好，也将成为 PC 上非常时髦的音乐控制器。

我们已经报道了很多其他很酷的 CAN 总线黑客，比如[逆向工程这个标致 207](https://hackaday.com/2017/05/04/reverse-engineering-the-peugeot-207s-can-bus/) ，或者这个[通用 CAN 嗅探器](https://hackaday.com/2011/03/08/can-sniffing-for-steering-wheel-button-presses/)。

 [https://www.youtube.com/embed/jIJ5Ien4ODc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jIJ5Ien4ODc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

