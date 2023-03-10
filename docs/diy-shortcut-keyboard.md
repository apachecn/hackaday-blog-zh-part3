# DIY 快捷键盘

> 原文：<https://hackaday.com/2017/06/19/diy-shortcut-keyboard/>

使用 CAD 程序需要专注于手头的任务，键盘快捷键非常方便。大多数软件包允许用户自定义这些快捷键，但最终，某些复杂的组合键会分散用户的注意力。

Sparkfun 的[awende]创造了一个 [Cherry MX 键盘](https://github.com/awende/Cherry_MX_Keyboard)，它将 Autodesk Eagle 的所有快捷方式整合到一个 4×4 矩阵中。该项目利用 Arduino Pro Mini 通过 USB 模仿 HID 设备的能力，从而实现 DIY 键盘。Arduino 读取连接到 GPIOs 的按钮，并将相应的快捷键发送到主机。

使用两个旋转编码器和 Teensy 编码器库实现附加功能。第一个旋钮用作音量控制，按钮用作静音按钮。编码器用于控制网格间距，嵌入式按钮用于在英制和公制单位之间切换。整个代码和原理图都可以在 [GitHub](https://github.com/awende/Cherry_MX_Keyboard) 上找到，以满足你的黑客乐趣。这是一个完美的项目，只等你去适应。

该项目可以扩展到与 Gimp 等其他计算机软件一起使用，按键可能会被电容触摸传感器取代，使其更加坚固。[可以添加蓝牙](http://hackaday.com/2017/05/20/the-tiniest-mechanical-keyboard-ever/)来实现无线化，你还可以使用[双动键盘](http://hackaday.com/2017/04/28/hackaday-prize-entry-a-double-action-keyboard/)来进一步扩展功能。

 [https://www.youtube.com/embed/EzlC36aDjfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EzlC36aDjfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

