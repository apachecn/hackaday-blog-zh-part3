# 用 Go 解锁无人机

> 原文：<https://hackaday.com/2018/04/27/unlocking-drones-with-go/>

正在寻找一门相对较新的语言的第一个项目来拓展你的能力吗？[罗恩]是，所以他[黑了一架商用无人机，并开放了它的许多功能](https://gobot.io/blog/2018/04/20/hello-tello-hacking-drones-with-go/)，同时用 Go 编写客户端软件。

这架无人机是 DJI 泰洛，它有一些令人印象深刻的硬件，如 14 核英特尔处理器和出色的视频处理能力。还有一个充满活力的社区和大量的支持，使它成为这样一个项目的理想平台。它通过 WiFi 与基站通信，使用 Wireshark [Rob]等工具能够破译大量通信，并为无人机创建一个全新的驱动程序。虽然无人机可以用传统方式控制，但用户也可以编写程序来控制无人机。

该项目既是对廉价无人机进行逆向工程的一个令人印象深刻的壮举，也是用 Go 语言编程的一个有趣例子。由于无人机的乐趣和兴奋，它们已经成为一个受欢迎的黑客平台，从[增加它们的范围](https://hackaday.com/2012/08/23/extending-the-range-of-the-ar-drone-2-ways/)到[成为开发 AI 的平台](https://hackaday.com/2017/11/29/high-speed-drones-use-ai-to-spoil-the-fun/)。