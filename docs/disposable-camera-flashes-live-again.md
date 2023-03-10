# 一次性相机再次闪光直播

> 原文：<https://hackaday.com/2016/04/06/disposable-camera-flashes-live-again/>

为了提高他网站上照片的图像质量，[Jean]需要一个外部闪光灯。

无论你怎么说一次性相机，但它们是大规模生产的，现在几乎已经过时，这意味着它们绝对是电子元件的宝库，只要你能以极低的价格买到它们。所以[Jean]决定把他的几个[一次性相机变成他的 DSLR](https://tibounise.com/articles/diy-flash.html) ( [翻译为](https://translate.google.ca/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https%3A%2F%2Ftibounise.com%2Farticles%2Fdiy-flash.html&edit-text=&act=url))的外接闪光灯系统。

他首先拆开一台柯达数码相机，检查电路板。按键 1 使电容器(相机打开开关)充电，SW1 位于快门下。

现在他所要做的就是用他的 DSLR 上的电子触发器代替 SW1。

为此，他构建了一个基于三端双向可控硅开关和光隔离器的定制电路，如下所示:

[![ssd-relay-schematic-960](img/9cbe785202847265d6312984448f6ddd.png)](https://hackaday.com/wp-content/uploads/2016/04/ssd-relay-schematic-960.png)

这种隔离确保电路在触发时不会被电容损坏。最后，他制作了一个印刷电路板，可以安装在他的 DSLR 的 hotshoe 适配器上，接受 5V 的触发——就是这样！

说到相机闪光灯，既然你已经在用了——为什么不造一个 2 美元的高速激光相机闪光灯传感器来进行高速摄影呢？