# JPEG 解码，Arduino 风格

> 原文：<https://hackaday.com/2017/07/12/jpeg-decoding-arduino-style/>

当您想到图像处理时，您可能不会想到 Arduino。[简·格罗姆斯]做了，虽然。使用相机和 Arduino Mega，[Jan]能够将来自 Arduino 连接相机的输入解码成[原始图像数据](http://www.deviceplus.com/how-tos/arduino-guide/jpeg-decoding-on-arduino-tutorial/)。我们不确定[Jan 的]用例，但我们可以想到很多原因，你可能想知道在相机的压缩 JPEG 中隐藏了什么。

超大内存是关键，因为正如你所料，你需要足够的内存来处理照片。还有一个 SD 卡辅助存储。相机代码很简单，将图像保存到 SD 卡中。有趣的部分是解码。

帖子中提到的用例是通过可能有损耗的通信信道发送图像数据。因为 JPEG 是以有损的方式压缩的，丢失 JPEG 的某些部分可能会使它变得无用。但是发送原始图像数据意味着丢失或错误的数据只会导致视觉假象(想想旧电视屏幕上的雪)，而你的大脑非常擅长解释这种有损图像。

为了测试这个理论，我们拿了一张(乔·金的)插图，保存为 JPEG 格式，只在其中的一个点上损坏了几个字节。下面可以看到之前(左)和之后(右)的图片。您可以理解，但是正如您所看到的，一个点中的几个字节的影响是深远的。

[![](img/34b3f78885dab043b0dc1ce45382f5ca.png)](https://hackaday.com/wp-content/uploads/2017/07/kim.png)

该代码使用一个返回 16 位 RGB 图像的库。这个库本来是用来在屏幕上显示图像的，但是它并不真正知道你在对结果做什么。不难想象使用这些数据来检测特定的颜色、在图像中寻找边缘、检测运动和其他简单的任务。

发送未压缩的图像数据可能对错误恢复有好处，但对没有耐心的人来说就不好了。在 115，200 波特的速度下，[Jan]说将一张 raw 图片从 Arduino 传输到 PC 大约需要一分钟。

我们已经看到 Arduino 一次处理一个像素。连[都换了颜色](https://hackaday.com/2014/10/20/a-single-pixel-color-digital-camera/)。Arduino 可能不是您图像处理平台的首选，但显然，您可以用它做一些事情。