# 控制你的 Furby

> 原文：<https://hackaday.com/2017/01/21/taking-control-of-your-furby/>

Furbys 已经存在了一段时间，它们是一种有趣的(如果令人讨厌的话)玩具，可以教会孩子们与他们最终的机器人统治者相处融洽。与此同时，机器人伴侣/玩具/烦恼的最新版本使用蓝牙 LE 与主人通信，而[Jeija]一直在监听蓝牙通信，试图对协议进行[逆向工程，以便在 Furby 上运行代码](https://github.com/Jeija/bluefluff)。

【Jeija】进步很多，已经可以控制 Furby 的动作，天线，背光颜色，通过改变 Furby 的饥饿，疲倦等数值来改变 Furby 的情绪状态。[Jeija]创建了一个运行在 Node.js 之上的程序，它可以与 Furby 通信并更改其属性。[Jeija]还发现了一个秘密的调试菜单，可以显示在 Furby 的眼睛里。还有待发现的是如何在 Furby 上运行自己的代码，然而，[Jeija]能够将自定义音频添加到官方 DLC 文件中，并将它们上传到 Furby 中。

[Jeija]指出，所有这些都是在没有拆开 Furby 的情况下完成的，只是通过嗅探机器人和控制应用程序(Android/iOS 设备)之间的蓝牙通信。)看看上一代 Furbys 上的一个[类似的黑客](https://hackaday.com/2013/01/28/reverse-engineering-the-furby/)，以及为它们准备的一个[替代大脑](https://hackaday.com/2016/01/29/open-furby-opens-the-furby/)。我们只是希望设计者包括一个红/绿 LED，这样我们就能知道 Furbys 什么时候从好变坏。

 [https://www.youtube.com/embed/FkblA_CxHgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FkblA_CxHgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

