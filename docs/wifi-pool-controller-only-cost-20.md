# WiFi 泳池控制器仅售 20 美元

> 原文：<https://hackaday.com/2018/06/07/wifi-pool-controller-only-cost-20/>

泳池已经走过了漫长的道路。过去你有一个泵，如果你幸运的话，上面有一个机械定时开关。就这样。现在你有了数字控制器、水疗喷头和加热器。你甚至可以让它们连接到你的家庭自动化系统。如果你的泳池还不够新，还不能这样做，你可以买一系列附加配件。是有代价的。[Rob]花了 500 美元买了一个泳池遥控器。它甚至不是无线网络，只是一个简单的射频遥控器。三年后，发射器烧坏了(更换一个需要 300 美元)，他觉得自己受够了。花费 20 美元，[Rob]使用 ESP8266 将 [MQTT 控制和监控](https://www.youtube.com/watch?v=QcaJlpVOJ8U)添加到他的池中。你可以在下面看到该项目的视频描述。

自然，这些说明是针对他的 Pentair 系统的。然而，它并不像你想象的那么专业。该项目依赖于大多数现代泳池系统支持的有线“温泉侧遥控器”的连接。这些的电气连接不是很标准，但它们都非常相似，所以假设你有这些有线遥控器的连接，你有一个很好的机会为你的设置重现这一点。

遥控器有几个按钮和状态指示灯。LED 根据池的当前模式有不同的反应，因此连接到那里不仅可以让您控制，还可以让您提供一些有限的状态。它不会让你监控泵电流或任何奇怪的东西，但它是一个简单的地方获得访问。使用 Arduino 脉冲输入功能可以轻松感知 LED 是亮着、熄灭还是闪烁。另一个传感器读取水温。控制器使它可用，但它不容易读取，所以该项目只是从现有的热敏电阻读取原始传感器电压，并计算温度。

[Ron]很好地解释了一些基本概念，比如使用光隔离器。然而，视频的真正价值在于它是连接现有控制器的简单方式。家庭自动化中的一点配置完善了这个项目。

如果您有一个较旧的系统，您可能希望看到更多的[池系统重建](https://hackaday.com/2016/09/05/enjoy-the-last-throes-of-summer-with-a-nice-pool-automation-project/)。如果你对[控制池化学](https://hackaday.com/2016/08/06/home-pool-added-to-home-automation/)感兴趣，我们以前也见过。

 [https://www.youtube.com/embed/QcaJlpVOJ8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QcaJlpVOJ8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

