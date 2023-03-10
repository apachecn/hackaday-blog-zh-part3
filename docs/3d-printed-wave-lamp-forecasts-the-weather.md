# 3D 打印波浪灯预报天气

> 原文：<https://hackaday.com/2018/01/06/3d-printed-wave-lamp-forecasts-the-weather/>

在浏览 Thingiverse 时，[Dushyant Ahuja]发现了一个相当令人愉快的波浪灯，由于仅仅一个灯本身是不够的，他增加了一种方法，通过改变它的颜色来提供天气警报。

公平地说，浪灯不是为胆小的人印制的，他花了 30 个小时才完成。然而，它有一个有趣的特点，即不需要支撑或木筏。该灯还有一个底座，设计用于容纳一条可寻址的 led，他修改了它的设计，以安装一个包含 ESP8266 模块和电平转换器芯片的小 PCB。ESP 的代码依赖于 OpenWeatherMap API，并根据降雨预报改变 LED 的颜色。

回想十年前，这款灯让人想起了很久以前的 Nabaztag 产品，最好的描述是一只联网的塑料拟人化兔子，它可以通过点亮和耳朵的运动让你随时了解天气或股市趋势等信息。这是一个定价过高的想法，捆绑在 2004 年的专有在线后端上。或许是为 2017 年重新包装的商用微控制器板 Nabaztag 终于找到了它的应用。

有一个简短的视频显示了颜色的变化和 LED 动画，我们把它放在了休息。

 [https://www.youtube.com/embed/38-309qH0DA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/38-309qH0DA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

