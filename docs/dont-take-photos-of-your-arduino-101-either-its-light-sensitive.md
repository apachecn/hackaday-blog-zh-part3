# 也不要给你的 Arduino 101 拍照，它是感光的

> 原文：<https://hackaday.com/2016/05/05/dont-take-photos-of-your-arduino-101-either-its-light-sensitive/>

晶圆级芯片便宜且非常小，但正如[Kevin Darrah]所展示的，没有其他芯片封装标准的保护性塑料外壳，[容易受到强光照射](https://www.youtube.com/watch?v=_o-s2XkfL6c)。

当[树莓 Pi 2](http://hackaday.com/2015/02/08/photonic-reset-of-the-raspberry-pi-2/) 问世时，我们报道过类似的现象。一个用户正在为他的 Pi 拍照以记录一个项目。每当他的相机闪光灯熄灭，它会重置董事会。

[Kevin]把一块新的 Arduino 101 板搬进了他的实验室。该主板拥有一个英特尔处理器、一个加速度计和蓝牙低能耗开箱即用，同时保持与 Atmel 版本相同的相对价格。他正在欣赏这块板，这时他注意到其中一个部件在灯光下闪闪发光。出于好奇，他打开了电路板的原理图，发现是芯片在桶形插孔和 USB 之间切换电源。不仅如此，它还是一个晶圆级封装。

所以，他拿出了他的相机和激光。果然，只要包装暴露在强光下，两者都会导致电力下降。Raspberry Pi 基金会后来写了关于这种现象的更详细的报道。他们说这不会影响正常使用，但如果你打算将你的设备暴露在高能光线下，只需将它放在一个盒子里，或者用胶带、Sugru 或不导电的油漆覆盖芯片来屏蔽它。

编辑:[Kevin]还在阳光下测试了它，并找到了它可以重置的条件。休息后的视频。

 [https://www.youtube.com/embed/_o-s2XkfL6c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_o-s2XkfL6c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/bqeAKE1-X3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bqeAKE1-X3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

