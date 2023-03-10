# 逆向工程开放三星 Gear VR 控制器

> 原文：<https://hackaday.com/2018/02/27/reverse-engineering-opens-up-the-samsung-gear-vr-controller/>

在 Hackaday，我们喜欢一点逆向工程，从一个设备与世界通信的方式中弄清楚它是如何工作的。来自[Jim Yang]的这个项目就是一个很好的例子:他[对三星 Gear VR 控制器](http://jsyang.ca/hacks/gear-vr-rev-eng/)进行了逆向工程，该控制器伴随着用于他们手机的[Gear VR 附件。通过深入研究连接设备和手机的 APK，他能够找出应用程序用来连接设备的蓝牙连接的细节。具体来说，他能够找到用于让设备发送数据的命令，并能够读取这些数据来确定设备的状态。然后，他可以用它来创建自己的 web 应用程序，以使用这些数据。](http://www.samsung.com/global/galaxy/gear-vr/)

这符合他的意图:能够在没有三星应用程序的情况下使用 Gear VR 控制器。他使用 [Web Bluetooth](https://webbluetoothcg.github.io/web-bluetooth/) 实现了这一点，它允许 Web 应用程序发现并连接到蓝牙设备，而不需要本地应用程序。这是一个相当新的标准，所以谷歌 Chrome 是目前唯一支持它的浏览器。[他的例子](https://webbluetoothcg.github.io/web-bluetooth/)使用这个标准在网页上读取和显示 Gear VR 控制器的方向，他已经[发布了使这成为可能的代码](https://github.com/jsyang/gearvr-controller-webbluetooth)。

如果你正在寻找一种廉价的方式来为一个项目添加运动控制器，这将是一个很好的开始:你可以在亚马逊上以不到 17 美元的价格买到一个 [Gear VR 控制器，代码允许你读取按钮按压、触摸板上的触摸以及控制器本身的方向。这比构建自己的控制器要容易得多。](https://www.amazon.com/gp/product/B06XHXRXP1)

 [https://www.youtube.com/embed/QGb5cKL8kZ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QGb5cKL8kZ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

