# 黑掉触摸屏来计数脉冲

> 原文：<https://hackaday.com/2017/07/09/hacking-touch-screens-to-count-pulses/>

可 DIY 使用的心率传感器采用光体积描记法，该方法照亮皮肤并测量光吸收的变化。这些传感器很便宜，但是将它们连接到其他设备所需的电路却不便宜。[pet Teri hyv rinen]正在成功研究将电容式触摸屏用于心率感应以及其他应用。

现代设备上的电容传感器层具有检测触摸的元件网格。典型地，有一个接口 IC 将检测到的触摸转换成可以被更高级应用使用的过滤数字。【optisimon】首先想出了[从触摸屏](http://optisimon.com/raspberrypi/touch/ft5406/2016/07/13/raspberry-pi-7-inch-touchscreen-hacking/)获取原始数据的方法。[pet Teri hyv rinen]采取下一步措施，使用 Python 脚本检测所获得数据的时间变化。FT5x06 接口的刷新率足够高，数据通过 Arduino 在 35 秒内通过 UART 发送到 PC。信号中的变化非常小，然而，通过平均然后使用自相关函数，信号被肯定地识别为脉冲。

如果结果可以在其他设备上复制，许多应用程序都可以从这项技术中受益。旧设备有可能被回收，成为低成本的医疗设备，其成本只是旧设备的一小部分。在物联网方面，对新闻、社交媒体和视频等媒体的心率反应可以用来对内容进行分类。

查看我们对电容触摸成像的原始[黑客](http://hackaday.com/2016/08/18/capacitive-imaging-with-a-raspberry-pi-touch-screen/)以及使用压电传感器的[的相同应用。](http://hackaday.com/2015/03/19/measuring-heart-rate-with-a-piezo/)