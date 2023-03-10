# PostMarketOS 拯救旧智能手机

> 原文：<https://hackaday.com/2018/01/09/postmarketos-saves-old-smartphones/>

现代智能手机，甚至是经济型手机，都是令人印象深刻的科技产品。强大的 ARM 处理器，大量的 RAM，以及数量惊人的传感器和无线电被打包到一个设备中，在某些情况下，当你注册一个服务计划时，它实际上是免费赠送的。不幸的是，制造商没有义务跟上软件更新，虽然硬件可能愿意继续战斗，但用户经常由于长期过时的软件而被迫升级。即使你不是那种会因为使用没有最新最好的操作系统的手机而却步的人，在移动设备越来越成为攻击者目标的世界里，缺乏软件安全更新也构成了明显的威胁。

但是如果你手机上的操作系统更像你电脑上的操作系统会怎么样呢？这是 postmarketOS 的梦想，post marketos 是由[Oliver Smith]创建的 Linux 发行版，旨在安装在过时的(主要是 Android)智能手机和平板电脑上。[他最近发表了一篇全面的博文，介绍了项目开始 6 个多月以来的状况，我们不得不说，到目前为止，事情看起来非常令人印象深刻](https://postmarketos.org/blog/2017/12/31/219-days-of-postmarketOS/)。

[![](img/dd607cbd036e707aa0b37f392bd06540.png)](https://hackaday.com/wp-content/uploads/2018/01/postmarket_detail.png)post marketos 的主要目标之一是避免以前试图用社区开发的操作系统取代 Android 的分散性。通过避免二进制 blobs 并专注于让主线 Linux 内核在尽可能多的硬件上运行，没有必要为每个支持的设备制作不同的分支和版本。通过尽可能统一操作系统，可以将上游更新推送到所有运行 postmarketOS 的设备，而不管它们的品牌和型号，就像传统的 Linux 发行版一样。

这篇博客文章非常清楚地表明了两件事:社区非常兴奋并致力于在旧的智能手机和平板电脑上运行本质上是桌面 Linux 的前景，以及 postmarketOS 仍然有很长的路要走。在早期，按照大多数标准，许多设备都不能被视为“日常驱动程序”。事实上，这篇博文提到，他们已经决定在谈论设备时放弃“受支持”这个词，并且除了将会启动之外，不做任何声明。

尽管如此，从主线内核开发到运行 Gnome、MATE 和 XFCE4 等标准 Linux 桌面，一切都在取得令人难以置信的进展。编译和打包操作系统本身组件的后端过程也已经完成，有望加快开发时间，即使对于那些没有强大机器进行编译的人来说也是如此。这篇博客文章的结尾列出了读者可以做的有助于支持 postmarketOS 的事情，从制作自己的 t 恤到移植到新硬件。

在 Hackaday 上，我们看到相当一部分黑客和制造商[重新利用旧的智能手机和平板电脑](https://hackaday.com/2016/05/17/smartphone-based-robotic-rover-project-goes-open-source/)，让它们[远离垃圾填埋场，否则它们几乎肯定会被扔进垃圾填埋场](https://hackaday.com/2016/11/17/instrument-apps-on-your-phone-the-christmas-cracker-novelties-of-the-test-bench/)。一个旨在让[破解这些廉价且极其有用的设备变得更加容易的项目，对我们来说简直是天籁之音](https://hackaday.com/2015/09/10/want-a-low-cost-arm-platform-grab-a-prepaid-android-phone/)。