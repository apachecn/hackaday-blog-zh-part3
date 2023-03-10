# IPad 控制的相机滑块

> 原文：<https://hackaday.com/2015/09/08/the-ipad-controlled-camera-slider/>

[Daniel]和[Tobias]涉足视频摄影，虽然他们喜欢由他们最喜欢的设备控制的相机滑块，但商业电动相机滑块很贵，而且没有很好的开源替代产品。[他们决定为自己建造一个](https://github.com/dangrie158/cc-franz)可以通过 PS3 控制器或借助 ESP8266 WiFi 模块的 iPad 应用程序进行控制。

相机滑块是一个双轴的考验，一个轴沿着两个坚固的轨道滑动相机，另一个轴平移相机。电路板由这些家伙研磨而成，包括一个控制两个 Pololu 步进驱动器的 ATMega328。ESP8266 是一种混合技术，很容易在设备上实现；它只是一个 MAX232 芯片，侦听 WiFi 模块的 Tx 和 Rx 线路，并将其转换为 ATMega 可以理解的内容。

到目前为止，这个项目最令人印象深刻的部分是 iPad 应用程序。这款应用程序可以被“实时”控制，动作可以被记录下来供以后播放。或者，该应用程序有一个简单的脚本功能，可以随着时间的推移执行各种操作，如移动和旋转。第二种模式非常适合延时拍摄。因为这个摄像头滑块使用 websockets 进行连接，所以这些人也应该能够为滑块编写一个 web 客户端，以防万一他们想要最终的网络摄像头。

你可以看看[丹尼尔]和[托拜厄斯]的演示卷轴，他们的相机滑块如下。

 [https://www.youtube.com/embed/dEtsxm3rubo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dEtsxm3rubo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

