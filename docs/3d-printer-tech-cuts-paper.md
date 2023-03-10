# 3D 打印机技术切割纸张

> 原文：<https://hackaday.com/2018/06/16/3d-printer-tech-cuts-paper/>

虽然 3D 打印本身是一件伟大的事情，但它也使机电硬件成为一种商品。由于规模经济和离岸制造，你现在可以非常便宜地买到所有东西，而不是从旧打印机中寻找来历不明的马达和杆。

[创新先生]用他最近的[切纸机](https://youtu.be/M6Vu3OT-UKg?t=5m42s)证明了这一点，它可以按照用户选择的宽度和数量输送和切割纸条。他的确从一台旧打印机上偷了一个滚筒组件，但大部分都是直接从 3D 打印机上拆下来的。有 NEMA 步进电机，模块化电机驱动板，光棒，皮带和滑轮。

刀具的刀片只是一个标准的折断盒刀具刀片。它是有角度的，所以当电机在切割后将它拉回到原位时，它不会拖动。老实说，我们可能会让纸张机制在那一点上收回纸张，但这很容易添加到设备的固件中。

你可能会认为自动切纸机有点懒惰，但我们可以看到你是否在为黑客空间活动切割传单，或者切割纸绝缘体以适合你少量销售的套件的外壳。

我们看到的最大问题是机器是开环的。将光学传感器放在辊和刀片之间会很有趣。当纸张覆盖传感器时，你就知道边缘的位置，然后可以精确地移动纸张，假设它不会滑动。另一个想法是将传感器放在刀片后面，这样它可以移动，这样一旦纸覆盖了传感器，切割就会发生。你也可以用微动开关或其他传感器做同样的事情。

尽管如此，对于一些剩余的 3D 打印机部件来说，这看起来是一个简单但有用的项目。小心打开的刀片。

我们不禁想到用[一个切割塑料的软盘刀片](https://hackaday.com/2016/06/11/plastic-cutter-made-of-3-5-floppy-disk/)来建造这个。或者你可以[安装一个激光器](https://hackaday.com/2015/01/31/paper-cutter-becomes-a-laser-engraver/)(但是请使用不同的电源)。

 [https://www.youtube.com/embed/M6Vu3OT-UKg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=191&wmode=transparent](https://www.youtube.com/embed/M6Vu3OT-UKg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=191&wmode=transparent)

