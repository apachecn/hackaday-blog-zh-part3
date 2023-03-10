# 高度控制的 led 夹克会随着你的攀爬而改变颜色

> 原文：<https://hackaday.com/2016/09/03/altitude-controlled-led-jacket-changes-color-as-you-climb/>

当你的攀岩馆举办“黑暗中发光”派对时，你如何脱颖而出？对马丁来说，答案显而易见。他制作了一件夹克，上面装饰着 32 个 WS2812 可寻址发光二极管，其颜色可以根据他所攀登的高度进行寻址。

该构建以 Arduino Pro Mini 为中心，配有气压传感器和用于无线电通信的 NRF24L01。一对口袋里装着 AA 电池作为动力，他已经准备好攀爬了。具有相同设置的基站 Arduino 传输地面温度的最新读数，该读数与来自气压传感器的本地读数进行比较，并用于计算 led 的新颜色。卡尔曼滤波器处理压力读数上的噪声，以确保稳定的结果。该项目的 Hackaday.io 页面上提供了两端的 Arduino 草图。

发光二极管安装在夹克的弹力面料上，幕后有多余的电线来满足弹力。你可以在视频短片中看到这件衣服。

 [https://www.youtube.com/embed/QW9pVjYWHOw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QW9pVjYWHOw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们在英国的[电磁场](https://www.emfcamp.org/)节上看到了这件夹克(感谢[Jasmine]的提示！)、 [LED 夹克是节日最爱](http://hackaday.com/2014/09/26/a-very-bright-led-jacket/)。这些年来，我们有很多 LED 夹克，[这是我们在 2013 年](http://hackaday.com/2013/10/06/led-costumes-and-clothing/)做的总结。