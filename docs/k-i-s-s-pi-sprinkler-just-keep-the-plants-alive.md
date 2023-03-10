# K.I.S.S. Pi 洒水器——保持植物存活

> 原文：<https://hackaday.com/2016/05/06/k-i-s-s-pi-sprinkler-just-keep-the-plants-alive/>

一个项目良好的第一步是知道你想做什么。[本·菲诺]明确表示，他为妻子花园设计的[树莓派喷水控制系统](http://www.instructables.com/id/Raspberry-Pi-Controlled-Irrigation-System)只有一个目标:让植物存活。由此产生的项目就是这样做的，仅此而已。

电路和管道很简单，在说明书中有很好的解释。所有的电子器件都由 Pi 和 MOSFET 组成，将 3.3v GPIO 转换为 5v 以控制继电器。控制水的阀门需要 28v 交流电，这需要继电器来控制。还有三个发光二极管:一个用于电源，一个用于指示阀门何时打开，还有一个是额外的用于将来的用途。

[![](img/eacc596ace28dbbc959ed8b3e0f9c505.png)](https://hackaday.com/2016/05/06/k-i-s-s-pi-sprinkler-just-keep-the-plants-alive/fc9rpdain4p8qu2-large/)[![](img/701e348256c0ec47d27f0bf55db16a7b.png)](https://hackaday.com/2016/05/06/k-i-s-s-pi-sprinkler-just-keep-the-plants-alive/fiawkviin4p8pzn-large/)

有趣的部分是使用来自网络的天气数据来确定最近是否下雨。由[Ben 的]朋友[Mark Veillette]提供的 Python 脚本使用气象站点 API 来获取降雨量数据。主脚本设置为每 24 小时运行一次。[Ben]将他的系统设置为水，除非前一天有足够的雨水。降雨量和回望天数是可编程的。

多么伟大的接吻原则的应用:保持简单，笨蛋——除了第三个没有目的的 LED。