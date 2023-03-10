# 数字钟随波逐流

> 原文：<https://hackaday.com/2017/05/29/digital-clock-goes-with-the-grain/>

这个[好看的时钟](http://www.instructables.com/id/Wooden-Digital-Clock/)看起来是由一块木头制成的，下面漂浮着 LED 数字。实际上，它是一块覆盖着木质单板的 PLA 塑料(嗯，[androkavo]称之为单板，但我们认为它可能只是一张接触纸或带有木质图案的乙烯基)。这产生了惊人的效果，我们可以想到其他可能利用该技术的项目，特别是因为木材表面看起来比通常的 3D 打印部件更加完美。

你可以在下面看到时钟运行的视频。时钟电路本身没有什么特别的。只有一个 MAX7218 LED 驱动器和一个显示器以及一个 STM32 ARM 处理器。该时钟具有 DHT22 温度和湿度传感器，以及用于报警的扬声器。

设置时钟是一件轻而易举的事情，因为它提供了一个 WiFi 接口，当然这要归功于 ESP8266。还有一个震动传感器来切断警报。如果你想以不同的方式处理事情，你可以改变软件来适应。例如，我们可以让振动传感器暂停工作，并要求用户访问网页来关闭闹铃，以确保我们真的醒了。

接触纸有多种表面处理，因此这项技术可以将 3D 打印的盒子变成纯色、大理石图案甚至模拟碳纤维的盒子。

我们不禁想到将一些我们见过的[不寻常的 LED 时钟](https://hackaday.com/2017/05/05/4-led-octal-clock-demands-colorful-math/)放在这种外壳中。说不定连[一个带字的](https://hackaday.com/2017/03/16/a-wordsearch-twist-on-the-word-clock/)。

 [https://www.youtube.com/embed/_LKyAY3VJ14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_LKyAY3VJ14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

