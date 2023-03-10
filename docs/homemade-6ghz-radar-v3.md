# 自制 6 GHz 雷达，V3

> 原文：<https://hackaday.com/2017/10/11/homemade-6ghz-radar-v3/>

第三版[Henrik Forstén] 6 GHz 调频连续波(FMCW)雷达[上线，看起来相当牛逼](http://hforsten.com/third-version-of-homemade-6-ghz-fmcw-radar.html)。FMCW 雷达是一种通过发射频率随时间线性变化的线性调频脉冲来工作的雷达。没有频率调制的简单连续波(CW)雷达设备不能确定目标距离，因为它们缺少精确定时发射和接收周期所需的定时标记，以便将该信息转换成距离。具有频率调制的发射信号允许雷达具有非常高的距离精度，并且还同时测量目标距离及其相对速度。

像以前的版本一样，[Henrik]设计了一个四层 pcb 板，并使用他自己的回流炉焊接所有的~350 元件。这个过程本身就是一个巨大的成就。该板比以前的版本大得多，现在包括通过 FPGA 进行数字信号处理。

[Henrik]的雷达之旅实际上[始于 2014 年](https://hackaday.com/2014/12/03/extremely-detailed-fmcw-radar-build/)，当时他的第一个版本的雷达在他的博客中有详细介绍和分享。一年后，他设法解决了一些问题，[设计了一个有重大改进的新电路板](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/)，并再次发布。令人印象深刻的第三版出来了，我们想知道第四版会是什么样子。

在[Henrik]骑着自行车在雷达前转圈的视频中，我们可以看到静态的灯柱和树木，而他看起来像一个小斑点，四处游荡:

[https://videopress.com/embed/teKfN2cO?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/teKfN2cO?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)