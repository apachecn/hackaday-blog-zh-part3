# Pi 时间–一个织物 RGB Arduino 时钟

> 原文：<https://hackaday.com/2017/04/16/pi-time-a-fabric-rgb-arduino-clock/>

Pi Time 是一个由布料和新像素制成的迷幻时钟，由 Arduino UNO 控制。时钟开始是一个绗缝的圆周率符号。[Chris 和 Jessica]想在圆周率周围做一些东西，并添加了一些 RGB 灯。同时，他们想做一些有用的东西，于是他们决定用 Neopixels 制作一个时钟。

Neopixels 或 WS2812Bs 是可寻址的 RGB LEDs，可以由微控制器单独控制，在本例中是 Arduino。布料上绣有螺旋数字(3.1415926535……)，实际的时间读数与你所习惯的不同。要解读时钟，你必须回忆可见的色谱或彩虹色，从红色到紫色。彩虹从中间的圆周率开始，所以小时会是红色、黄色或橙色，这取决于需要多少位数字来显示时间。例如，当它是 5:09 时，5 是红色的，9 是黄色的。当 5:10 时，5 是橙色，第一分钟(1)是蓝绿色，第二分钟(0)是紫色。圆周率符号每秒闪烁一次。

有更简单的和更复杂的[方法来完成计算时间的简单任务…](http://hackaday.com/2016/10/03/who-could-resist-a-color-coded-clock/)

我们不确定这些数字是根据它们在圆周率序列中的第一次出现而点亮的，还是只是随机的，因为视频只显示了恍惚的 led，但效果非常好:

 [https://www.youtube.com/embed/FJk4iCJ5_tE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FJk4iCJ5_tE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

