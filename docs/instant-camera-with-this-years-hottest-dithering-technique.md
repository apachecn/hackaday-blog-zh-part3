# 采用今年最热门抖动技术的即时相机

> 原文：<https://hackaday.com/2016/12/24/instant-camera-with-this-years-hottest-dithering-technique/>

数码相机很棒，因为你可以拍成千上万张照片而不会用光胶卷。但是，有一个可以拿在手中的有形图像还是有道理的。过去的宝丽来相机在这方面很棒，但现在很难找到，每张照片的价格也贵得离谱。

![dither](img/6a26ac82b639d2fa294d3eb06a738d7c.png)

Dithering allows the camera to print a much better image.

在过去的几年里，一些人一直在寻找一种以较低成本制作印刷照片的方法。最好的方法之一是找到比宝丽来胶片便宜得多的东西——比如热敏纸。

[【杨奇煜-乔托】的热敏打印相机](https://hackaday.io/project/18913-diy-instant-camera)并不是第一台——你已经有了 Gameboy 相机/打印机和其他一些东西来感谢它。但这是一个很好的例子。该相机结合了 Adafruit 热敏收据打印机和 OpenMV 相机，这两者都很容易获得，如果不是很便宜的话。它甚至增加了一个 ST7735 LCD，用于实时显示相机的图像，就像消费级相机一样！

然而，这不仅仅是一个拼凑起来的零件箱组件。虽然热敏打印机只能打印黑色或白色像素，但它的分辨率远远高于相机的图像。这使得相机可以使用一个 3×3 的打印像素块来表示相机的单个像素，并且通过一些奇特的抖动技术，可以非常有效地模拟灰度。正是像这样的技巧真正为项目增添了光彩，并在一天结束时对图片质量产生了很大的影响。

这并不是我们看到的第一台热敏打印机相机——[ Ch00f]的[木纹即时相机](https://hackaday.com/2014/12/18/towards-more-interesting-instant-cameras/)强调了在追求这种类型的构建时谨慎选择相机的问题。

休息后的视频。

 [https://www.youtube.com/embed/5dyqzRtlMxI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5dyqzRtlMxI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

