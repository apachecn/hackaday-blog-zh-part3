# 使用 100 瓦 LED 进行冻结时间摄影

> 原文：<https://hackaday.com/2015/10/05/frozen-time-photography-with-a-100w-led/>

高速摄影很有趣。超高帧率视频，更是如此。但是由于我们中没有多少人能使用价值 10，000 美元的 HFR 相机……我们不得不凑合着用长曝光拍摄一个**完美定时的相机闪光灯。你可以设计一个系统在正确的毫秒触发闪光——但是它们通常还是很贵的。**

 **[Electronupdate]有一个 100 瓦的 LED 模块和对 Arduino Nanos 的偏好——所以他想知道他是否能制造一个负担得起的高速相机装备——[他做到了。](http://electronupdate.blogspot.ca/2015/10/frozen-time-photography-and-super.html)

这是一个非常巧妙的小装置。他在一块木头的钉子上安装了一个限位开关——当水球落在上面时，就会触发机械开关。Arduino 然后触发 LED 闪烁，这是一个相当大的负载，需要[一个高端开关](http://hackaday.com/2015/09/16/learn-and-build-a-high-side-switch/)来操作。一个小的液晶显示器和一系列的按钮让他能够拨准时间偏差，以便拍下一些水球爆炸的精彩照片。

 [https://www.youtube.com/embed/znsD5XVkcTs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/znsD5XVkcTs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



或者，你可以用该死的激光达到同样的效果。**