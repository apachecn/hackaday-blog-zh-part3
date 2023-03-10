# [CNLohr]，ESP8266，USB…

> 原文：<https://hackaday.com/2016/08/09/cnlohr-esp8266-usb/>

“围捕通常的嫌疑犯…”

[CNLohr]这些天来，人们对 ESP8266 总是爱不释手，现在他正在开发一个版本的 V-USB 软件低速 USB 设备仿真。( [GitHub 链接此处](https://github.com/cnlohr/espusb)，[视频](https://www.youtube.com/watch?v=-NxoNdTj_7U)也嵌在下面。)这不太可能是一个下午的项目，我们应该提醒你，这仍然是一个正在进行的项目，但他提供了一些正在进行的材料，如果你对 USB 或[CNLohr]的思维方式感兴趣，这值得一看。

在这个视频中，他非常依赖逻辑分析仪。他不是 USB 专家，也无法在网上找到合适的资源来实现 USB 驱动程序，所以他通过观察在桌子上晃动鼠标时传来的信号来自学。使用曾经流行的 Wireshark 也帮了他很多。然后是深入研究 Xtensa 汇编语言的时候了，因为时机非常关键。

说到计时，他做的第一件事就是编写一些分析程序，这样他就可以计算出每件事情需要多长时间。还有我们有没有提到[CNLohr]不知道 Xtensa assembly？所以他用 C 写例程，用 Xtensa GCC 编译器编译，退出汇编。最终的结果是两者的混合:当速度很重要时是组装，当更舒适时是 C。

总而言之，这是一种非常迭代的、实验性的编码、学习和黑客方法。视频有点长，有点曲折，但它让你很好地窥视了[CNLohr]的头骨。你也不能反驳他的结果。毕竟，这就是那个在 ESP8266 中对以太网进行比特攻击的家伙。

感谢[卢卡斯]和[乌列尔]几乎同时给出的提示！

 [https://www.youtube.com/embed/-NxoNdTj_7U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-NxoNdTj_7U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

