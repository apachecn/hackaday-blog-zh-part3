# 在爱普生 PX-8 笔记本电脑上浏览现代论坛

> 原文：<https://hackaday.com/2018/04/18/browsing-modern-day-bbs-on-the-epson-px-8-laptop/>

当你读到这里的时候，世界各地仍有人在电子公告板上聊天。运行在新编写的软件上，不需要实际使用拨号调制解调器，这些(稍微)更现代的昔日 BBS 对于那些可能想从当代社交网络中减压的人来说，可能是令人信服的转移。

[Blake Patterson]就是这些人中的一员，他写信告诉我们他最近在现代化的 BBSs 上使用一个特别华丽的例子 Epson PX-8“Geneva”笔记本电脑进行的实验。该设备的外形使其成为一个相当方便的聊天客户端，尽管屏幕有些不寻常。幸运的是，现代 BBS 软件能够处理 PX-8 的 80 字符×8 行液晶显示器，这只是一个上网的问题。

诀窍是将 PX-8 作为串行终端连接到 Linux 机器上。[Blake]必须为笔记本电脑构建串行电缆，然后使用基本的 USB 转串行转换器将其连接到 Raspberry Pi。一旦你通过串口登录，你可以简单地发出一个 telnet 命令来连接到你选择的 BBS。在休息后的视频中，他演示了使用 PX-8 在 BBS 上浏览和聊天的感觉。这个屏幕当然需要一点时间来适应，但是考虑到 BBS 界面的性质，它实际上工作得相当好。

[Blake]最近向我们展示了基于 ESP8266 的复古电脑的 Wi-Fi“调制解调器”,如果你想在没有 Pi 的情况下浏览你最喜欢的 BBS。

 [https://www.youtube.com/embed/I92UP5-F3Gw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I92UP5-F3Gw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

