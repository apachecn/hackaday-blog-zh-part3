# 将任何 USB 键盘转换为蓝牙

> 原文：<https://hackaday.com/2016/09/04/convert-any-usb-keyboard-to-bluetooth/>

[DastardlyLabs]看到一个关于将 PS/2 键盘转换为蓝牙的视频，意识到他已经没有任何 PS/2 键盘了。所以他用 USB 键盘玩了同样的把戏[。在此过程中，他制作了三个视频来解释这一切是如何运作的。](https://www.youtube.com/playlist?list=PLVfmdw6Y3COp4Via7KergjVs8i194ffJS)

该项目使用一个普通的 DuinoFun USB 迷你主机保护罩，经过修改后可以在 5V 电压下工作。Arduino mini pro 提供了大脑。FT-232 USB 转串行板用于对 Arduino 进行编程。标准蓝牙模块必须安装 HID 固件。[卑鄙地]制造了一个自制的子板——呃，护盾——来连接 Arduino。

结果是一个漂亮的小三明治，有一个 USB 插头，一个蓝牙天线，以及一些必要时用于重新编程的引脚。抑制住焊接蓝牙板的冲动——因为它与 Arduino 用于编程的端口相同，你必须在上传新代码前移除它。

如果你需要帮助重新编程 HC-05 蓝牙模块，我们之前已经讨论过这个问题。这个项目从【埃文的】类似项目[的 PS/2 键盘](https://hackaday.com/2016/04/14/minions-turn-your-keyboard-into-a-bluetooth-keyboard/)中汲取灵感。

 [https://www.youtube.com/embed/5qXv7TJI324?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5qXv7TJI324?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/qyRJgtwX0cY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLVfmdw6Y3COp4Via7KergjVs8i194ffJS](https://www.youtube.com/embed/qyRJgtwX0cY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLVfmdw6Y3COp4Via7KergjVs8i194ffJS)

