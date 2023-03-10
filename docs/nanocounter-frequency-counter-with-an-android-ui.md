# Nanocounter:带有 Android 用户界面的频率计数器

> 原文：<https://hackaday.com/2016/03/29/nanocounter-frequency-counter-with-an-android-ui/>

你有没有开始一个项目，遇到一个问题，开始一个新的项目来解决问题，而完全忘记了原来的项目？[Andy]陷入了一个兔子洞，需要一个工具来校准 MCU 振荡器，但没有精确的方法来测量频率。大多数人会买一个频率计数器就完事了，但是[安迪]决定自己做一个。

纳米计数器是一款精确的开源频率计数器，使用安卓手机作为显示屏。它基于高精度温度补偿晶体振荡器(TCXO ),馈入锁相环(PLL)以产生高频、精确的参考时钟。

该参考时钟与待测信号一起被发送到 Xilinx FPGA，该 FPGA 使用一种称为等精度测量的方法来确定频率。STM32F072 微控制器使用 SPI 接口从 FPGA 获取数据，并控制整个系统。最后，廉价的 HC-06 蓝牙模块有助于与 Android 设备通信。

该项目实现了频率计数的目标，尽管[Andy]不记得是什么项目激发了建造它的想法。([经典牦牛剃毛](https://en.wiktionary.org/wiki/yak_shaving)！)但结果是一篇详细的文章，你可以在休息后观看纳米计数器的视频。在我们看来这是一个胜利。

 [https://www.youtube.com/embed/c8_JnJcHIVg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/c8_JnJcHIVg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

