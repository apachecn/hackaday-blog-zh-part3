# Leap Motion 通过 Arduino 无线控制假手

> 原文：<https://hackaday.com/2015/10/22/leap-motion-wirelessly-controlling-a-prosthetic-hand-with-an-arduino/>

Leap Motion 控制器是一个相当令人印象深刻的小传感器条，能够生成大量的 3D 点云，并识别手和手指，以允许基于手势控制的计算。它已经问世几年了，但是我们还没有看到多少黑客在玩它。[anwarullah]以前也曾摆弄过它，但当要向印度首届创客节提交东西时，他决定试着用它做一个实际的项目。

检查了最新的 Leap Motion SDK 后，[anwarullah]意识到已经做了许多改进，他不得不重写一些原始代码来反映这些变化。这一次，他选择使用 ESP8266 WiFi 模块，而不是蓝牙模块。他打印了一只[猛禽手](http://enablingthefuture.org/upper-limb-prosthetics/the-raptor-hand/)(来自 e-NABLE 的优秀员工)，并将其与一些遥控伺服系统连接起来，让他可以控制一只漂亮的机器人手。

发送到 Arduino 的实际代码非常简单。Leap Motion SDK 完成了所有复杂的工作，最后，它只是向 Arduino 发送一系列命令，告诉它看到了多少个手指，以便控制手。

[https://player.vimeo.com/video/142728193](https://player.vimeo.com/video/142728193)

关于这个项目的更多信息，你可以在这里查看他最初对 Leap Motion Arduino 控制的尝试。关于更多使用 Arduinos 的 Leap Motion 控制事物的例子，[为什么不控制一个可爱的电子台灯呢？](http://hackaday.com/2013/07/11/animating-a-lamp-with-the-leap-motion/)