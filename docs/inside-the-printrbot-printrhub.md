# Printrbot Printrhub 内部

> 原文：<https://hackaday.com/2016/12/16/inside-the-printrbot-printrhub/>

今年夏天发布了 Printrbot Simple 的新版本，这款时尚的新型号包含了一些非常令人向往的功能。金属外壳得到了改进，增加了线性导轨，增加了电源开关，最大的特点——触摸屏——使无头打印变得容易。

添加可用的显示器和实现可靠的 WiFi 是巨大的工程挑战，由于物联网，期待这些功能只会变得更加普遍。Printrbot 团队是如何实现的？[Philip Shuster]最近发布了一篇关于[Printrbot Printrhub 如何走到一起的文章](https://github.com/Printrbot/Printrhub)。

最新的 Printrbot 中的显示器和 WiFi 模块的故事始于大约一年前 Hackaday 上的一篇帖子。[【Philip】制造了小助手](http://hackaday.com/2015/12/25/little-helper-open-source-hardware-hacker-multitool/)，一个小小的电子瑞士军刀，能够进行基本的 IO，发送 PWM 脉冲，嗅探 I2C，以及其他一些方便的功能。Printrbot 团队找到了[Philip]，经过几次交谈后，他被拉入了 Printrhub 的开发团队。

与小助手略有不同的是，Printrhub 采用了与 Teensy 3 相同的微控制器、2.8 英寸 TFT 显示屏、电容式触摸传感器、microSD 卡插槽和用于处理 WiFi 连接的 ESP-12 模块。显示系统很棘手，但团队最终让它工作了。使用 ESP8266 作为打印机的 WiFi 模块[比你想象的](http://www.appfruits.com/2016/11/printrbot-simple-2016-commstack-explained/)更困难，但这也行得通。

在过去几年中，3D 打印机面临的一个更有趣的挑战是开发一种具有无线连接功能的良好打印机显示器。是的，那些连接到 Arduino 的图形液晶显示器仍然可以工作，但是 1980 年的显示器不卖打印机。仅仅几个月，Printrbot 团队就想出了一个相对简单、非常优雅的显示器，可以做任何事情，并且他们将所有硬件[作为开源](https://github.com/Printrbot/Printrhub)发布。这是一个好消息，我们迫不及待地想在其他品牌的 3D 打印机中看到类似的设置。