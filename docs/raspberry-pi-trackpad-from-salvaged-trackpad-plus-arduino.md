# Raspberry Pi 触控板，来自回收的触控板加 Arduino

> 原文：<https://hackaday.com/2017/07/19/raspberry-pi-trackpad-from-salvaged-trackpad-plus-arduino/>

旧的笔记本电脑很容易找到，许多笔记本电脑都有一个带有 PS/2 接口的触控板。[Build It]想要一个这样的触控板，用于他正在制作的 DIY Raspberry Pi 笔记本电脑。但是 Raspberry Pi 没有 PS/2 输入，他读到 PS/2 转 USB 适配器不够可靠。他的解决方案？将触控板连接到 Arduino，然后[让 Arduino 将触控板的 PS/2 转换为 USB](https://www.youtube.com/watch?v=ssTFgNUH_qk) 。

卸下几个螺丝后，他就把触控板从笔记本电脑上拆下来了。在网上查找触控板的零件号时，他找到了用于数据、时钟和五伏电压的焊盘。他把自己的电线焊接到它们上，也焊接到触控板的接地层上，然后从那里连接到他的 Arduino Pro Micro 上。在安装了 Arduino [PS/2 鼠标](https://playground.arduino.cc/ComponentLib/Ps2mouse)和[鼠标和键盘](https://www.arduino.cc/en/Reference/MouseKeyboard)库之后，他写了一些代码(见他的[可引导页](http://www.instructables.com/id/Arduino-Controlled-USB-Trackpad/))。点睛之笔是使用大量的热熔胶将所有的电线和 Arduino 固定在触控板的背面。通过将 USB 电缆插入 Arduino，他现在拥有了一个可以作为 USB 触控板插入任何地方的触控板。观看[构建]在下面的视频中一步一步地将它们组装起来。

 [https://www.youtube.com/embed/ssTFgNUH_qk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ssTFgNUH_qk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



想用触控板做点别的事情。像斯科特那样把 16 个组合成一个很棒的 MIDI 控制器怎么样？