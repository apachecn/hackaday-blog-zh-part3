# 在你的工具箱里放一个逆向工程功率计

> 原文：<https://hackaday.com/2016/07/11/put-a-reverse-engineered-power-meter-in-your-toolkit/>

似乎可以在网上买到便宜的电表，嗯，就是这样。它们工作得很好，但是要把它们用在其他任何事情上(比如数据记录或控制等等)，它们需要更多的工作。好消息是，[Thomas Scherrer]，别名[OZ2CPU]，刚刚为我们做了那个[逆向工程工作](http://webx.dk/oz2cpu/energy-meter/energy-meter.htm)。

在这些廉价的功率计中，你会发现一个 LCD 驱动器、一个电源监控芯片和一个 STM32F030，这是一个低成本的 ARM Cortex M0 芯片，单独使用很有趣。[Thomas]追踪到电源监控芯片用来与微控制器对话的 SPI 线路，并闯入窥探信号。一旦他理解了所有的数据，将 ATmega88 芯片扔在 SPI 线上，他就可以通过一个方便的异步串行接口将其解密。

[![](img/3979eef920991ed9145fd682156f2339.png)](https://hackaday.com/wp-content/uploads/2016/07/peacefair-pzem-021-pcb-ic.jpg)

如果你打算自己动手，你应该注意到功率表的内部是在线电压下运行的——给微控制器供电的 3.3 V 电压浮动在[Thomas]墙上插头输出的 230 V 电压之上。在测试设备时，他使用隔离变压器采取了[必要的预防措施，并且没有受到电击。这意味着要获得串行数据，需要使用光隔离(或无线电！)在串行线上。](http://hackaday.com/2016/05/11/looking-mains-voltage-in-the-eye-and-surviving-part-1/)

既然我们知道了这个东西在内部是如何工作的，现在是电源管理黑客的开放季节。把一个电源插座和一个 ESP8266 放在一个盒子里，你就有了一个可以在任何地方使用的 WiFi 日志功率表，所有这些都不到 20 美元。太好了。