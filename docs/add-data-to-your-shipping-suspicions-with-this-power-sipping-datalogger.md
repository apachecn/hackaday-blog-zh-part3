# 使用这款省电的数据记录器，为您的运输疑虑添加数据

> 原文：<https://hackaday.com/2016/11/04/add-data-to-your-shipping-suspicions-with-this-power-sipping-datalogger/>

一个人只需要通过一个集装箱运送一两件东西，在你开始怀疑你的发货人之前，你会在另一端收到奇怪的损坏。他们是不是打开了这个盒子，然后跺了一下脚？我是不是不小心承包了一艘潜艇而不是一艘船？他们绕过太阳了吗？这怎么可能融化呢？

[【Jesus Echavarria】](http://hackaday.com/2015/05/24/absolute-overkill-ikea-lampan-lamp-hack/)他的朋友对他将要从西班牙运往中国的一个箱子也有类似的担心和怀疑。所以[耶稣]开始工作，并建立了这个漂亮的数据记录器，以发现真相。由于记录器可能要运行几个月，所以这是一个低功耗设计的练习。

建筑的核心是一张不起眼的照片。它的工作是从环境光、温度和湿度传感器套件中获取信息，并将其全部转储到 SD 卡中。除了 RTC，这都是由一个普通的脂肪电池供电。第一次迭代一次充电可以运行 10 天，而且没有启用微控制器的任何低功耗特性。一旦它能让自己休眠一段时间，它应该能坚持更长时间。

它被装在一个 3D 打印的盒子里，用一些磁铁把它粘在集装箱的外壳上。考虑到商业数据记录器惊人的天文价格，这是一个很好的建设！