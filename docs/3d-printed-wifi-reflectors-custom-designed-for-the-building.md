# 专为建筑定制的 3D 打印 WiFi 反射镜

> 原文：<https://hackaday.com/2017/11/18/3d-printed-wifi-reflectors-custom-designed-for-the-building/>

你是天线设计方面的专家吗？你可能从来没有尝试过，但是这个工具可以改变这种情况。互联网上大多数自制的 WiFi 信号增强天线计划都有一个共同的特点:它们是定向天线或反射器。但是 [WiPrint 是一个设计定制 WiFi 反射器](http://dartnets.cs.dartmouth.edu/wiprint)的工具，可以映射到特定的应用。

如果我们想在两个或三个不同的位置增加信号强度，传统的解决方案是全向天线。问题是，虽然一个好的全向天线会在我们想要的那些位置增加信号功率，但也会在我们不想要的地方增加信号功率。

由达特茅斯学院(Dartmouth College)领导的一组研究人员创建了 WiPrint，允许用户将平面图、WiFi 接入点的位置和所需的信号地图输入系统。该软件使用优化算法为该平面图生成定制的反射器形状。然后，可以制造反射器并将其放置在接入点天线旁边，以将信号反射并集中在指定区域，同时降低其外部的信号强度。最棒的是:你实际上可以 3D 打印反射器，只需在上面粘上锡纸！

结果显示，优化的反射器可以分别减弱或增强目标区域中的信号达 10 或 6 dB，并导致吞吐量变化达-63.3%或 55.1%。正如研究人员指出的那样，这不是唯一的优势:

> 我们的方法提供了四个好处。首先，它通过限制无线信号的物理范围来提供强大的物理安全性，因此为无线信号创建了一堵虚拟墙。第二，它依赖于低成本(35 美元)、可再生的 3D 反射器，在环境或覆盖要求发生重大变化时，可以很容易地更换该反射器。第三，它为非专业用户提供了一个易于访问和配置的解决方案。用户只需要指定覆盖要求和一个粗略的环境模型，我们的系统就可以计算出适合建筑环境的反射器形状。最后，适用于没有定向或多天线的商品低端 Wi-Fi AP。

令人难过的是，目前还没有可用的软件。这项研究和结果刚刚在 ACM 的 BuildSys 2017 上发表。如果能看到这样的开源软件就太好了。同时，这进一步证明了当[他告诉你使用管道胶带](https://hackaday.com/2017/01/30/increase-the-range-of-an-esp8266-with-duct-tape/)来获得更好的无线覆盖范围时【Brian Benchoff】知道他在做什么。