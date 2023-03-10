# Pi 气象灯让熔岩灯相形见绌

> 原文：<https://hackaday.com/2018/01/14/pi-weather-lamp-puts-lava-lamps-to-shame/>

以一种易于理解的方式在 LED 灯上呈现天气可能很困难，但[Gosse Adema]的[天气/矩阵灯](http://www.instructables.com/id/WeatherMatrix-Lamp/)不仅让天气一目了然，还提供了一个非常有吸引力的显示。下雨时，光线向下移动，刮风时，光线向侧面移动。温度用从红色到蓝色的一系列颜色显示，因为他位于荷兰，所以他需要雪，他显示为白色。在多雨、多风的日子，灯光会向下和向侧面移动，以温度信息作为背景。

![Weather matrix lamp](img/03c4f7e0782ec7437446e3626591fe78.png)

为了实现这一点，他将 LED 灯条安装在一个 3D 打印的圆柱体内，每个 LED 都有反射器，所有这些反射器都安装在一个从网上购买的另一盏灯上取下的玻璃圆柱体内。它的大脑是一个树莓 Pi Zero W，和一个风扇一起放在底部。led 和风扇都由 Pi 控制。他非常关注电源管理，首先计算 led 消耗的电流，然后编写 Python 代码来限制这种消耗。然而，经过测量，电流消耗比预期低得多，因此他适当地调整了电源的大小。他还注意正确确定电线的尺寸，并用特制的配电板正确分配电力。总的来说，我们真的很喜欢他所做的彻底的工作。

但是话说回来，有什么不喜欢[戈斯]的项目。在照明领域，他用 [WiFi 控制的圣诞树装饰品](https://hackaday.com/2017/01/01/wifi-controlled-christmas-ornaments/)让我们眼花缭乱，但他也用基于[Prusa i3 的乐高 3D 打印机](https://hackaday.com/2015/06/08/lego-printer-prints-lego/)让我们高兴，他在打印机上打印了乐高零件，然后[制造了一个特殊的挤压机来打印巧克力](https://hackaday.com/2015/09/26/printing-chocolate-with-a-lego-3d-printer/)。