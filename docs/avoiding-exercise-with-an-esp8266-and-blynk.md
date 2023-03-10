# 避免使用 ESP8266 和 Blynk 进行锻炼

> 原文：<https://hackaday.com/2016/07/11/avoiding-exercise-with-an-esp8266-and-blynk/>

[迈克·戴蒙德]厌倦了爬下(再爬上)40 层楼梯去查看他的邮箱。他决定使用 ESP8266 连接到他的 WiFi 来创建一个邮箱警报。想法很简单:让 ESP8266 使用磁铁和簧片开关监控邮箱盖何时打开。不过，一如既往，细节决定成败。[Mike]在一些帮助下让事情运转起来，不仅分享了[完成的设计，还分享了他是如何完成的](http://www.whatimade.today/esp-8266-mailbox-notifier-using-deepsleep-and-blynk/)。

为了处理电子邮件的发送，[迈克]使用了 [Blynk](http://www.blynk.cc/) 应用程序。你经常认为 Blynk 是一种在可以控制 Arduino 的 Android 或 iOS 设备上构建用户界面的方法。不过，在这种情况下，[Mike]使用 ESP8266 的库，并让它代表他发送电子邮件。

这个程序很简单，但有一个问题:让设备一直开机并连接到 WiFi 会持续消耗电池。这就是[迈克]如何发现深度睡眠功能的。使用这个有所帮助，但即使定期唤醒设备也太消耗电池了。对硬件做了一点改动，但最终[迈克]和他的朋友[阿米尔]设计出了一种只在必要时给设备通电的方法。另外，通知还会报告电池电压，这样你就知道什么时候给设备充电了。

我们以前报道过 Blynk(不是一次的[，而是两次](https://hackaday.com/2016/03/10/app-control-with-ease-using-blynk/)的[)。我们还看到了](https://hackaday.com/2016/03/10/app-control-with-ease-using-blynk/)[邮箱项目](https://hackaday.com/2016/04/05/make-your-mailman-nervous-with-a-wifi-enabled-mailbox/)。如果你不喜欢调整普通邮箱的内部结构，那就仔细阅读如何从头开始构建一个超级邮箱。