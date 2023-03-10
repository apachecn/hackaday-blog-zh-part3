# 廉价 WiFi 设备是硬件黑客黄金

> 原文：<https://hackaday.com/2016/01/27/cheap-wifi-devices-are-hardware-hacker-gold/>

廉价的消费 WiFi 设备非常棒，至少有三个原因。首先，它们几乎都运行嵌入式 Linux 发行版。其次，它们很便宜。如果你打算在打开东西的过程中弄坏几个设备，没有经济上的担忧是很好的。第三，它们的生产利润非常低，安全费用是制造商无法承受的——这意味着它们通常非常容易进入。

一个很好的例子:[q3k]提交了一个小小的支持 WiFi 的 SD 读卡器设备，这是他和他的同胞[emeryth]和[informatic]在[的帮助下完成的[Benjamin Henrion]](http://www.zoobab.com/zsun-sd11x-wifi-card-reader)的一些早期工作。有问题的设备是 USB 总线供电的，内置一个 SD 读卡器和一个 AR9331 WiFi SOC。它旨在为没有足够板载存储空间的手机提供无线 SD 卡支持。

黑客从[Benajmin]在端口 11880 上找到一个 telnet 提示符开始，然后以 root 用户身份登录，使用所有 Zsun 设备都使用的相同密码:`zsun1188`。好像他们想让你进去。(如果你会说中文，你会认出这些数字是“想发财”的发音。所以我们有了公司名称和一个老生常谈的双关语。这基本上相当于中文的“密码 1234”。)在此过程中，[Benjamin]还指出，该设备会执行输入其网络界面的任意代码。例如，将其配置为使用 ESSID“reboot ”,设备将重新启动。我的天啊。

[![zsun_gpio_bootstrap_annot](img/7e8a6f5d01f782f71b358a9d4293e854.png)](https://hackaday.com/wp-content/uploads/2016/01/zsun_gpio_bootstrap_annot.jpg) 从这里,【q3k】和公司接手并将 OpenWRT 移植到设备上，并记录其串行端口和 GPIOs 在物理板上的位置。但这还不是全部。他们还记录了如何以及在哪里连接有线以太网适配器，如果你想把这个东西放在一个非无线网络上，或把它作为一个桥梁，或任何东西。简而言之，它是一个包装中的微型 WiFi 路由器和 Linux 盒子，大小约为一枚(欧元硬币|美国硬币)大小，成本低于一顿好的晚餐。只需添加 USB 电源，您就可以开始工作了。

干得好！