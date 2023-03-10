# 树莓派零驱动微型遥控卡车

> 原文：<https://hackaday.com/2018/01/24/raspberry-pi-zero-drives-tiny-rc-truck/>

我们不知道哪个更有趣——在你的工作台上组装一辆带有零件的小型遥控卡车，或者在 Linux 终端上驾驶它。我们将采取简单的方法，说它们都同样有趣。[technodict]有了一些空闲时间，决定[造一辆这样的卡车](https://omkarjr.in/posts/projects/Rpi0-WiFi/)。

他从一个很棒的小底盘开始，这个底盘可以作为许多项目的基础。驱动四个马达的是一个便宜的小型双 H 桥[马达驱动器](https://www.aliexpress.com/item/15931-Free-Shipping-New-Dual-H-Bridge-DC-Stepper-Motor-Drive-Controller-Board-Module-L298N-MOTOR/32355666632.html?ws_ab_test=searchweb0_0,searchweb201602_5_5130011_10152_10065_10151_10344_10068_10345_10342_10343_51102_10340_10341_10609_5000011_10541_10084_10083_10307_10539_5080015_10312_10059_10313_10314_10534_100031_10604_10603_10103_10605_10594_10596_5060011_10142_10107,searchweb201603_2,ppcSwitch_5&algo_expid=80ee8326-0672-417c-b538-71aeb23ce967-0&algo_pvid=80ee8326-0672-417c-b538-71aeb23ce967&rmStoreLevelAB=0)和几个充电电池。但是这个构建中最巧妙的部分是它使用了一点 python 来控制，并且直接从终端驱动，当然这是由 Raspberry Pi Zero 实现的。

随着 Raspberry Pi Zero 现在内置了 WiFi 和蓝牙功能，我们应该会看到更多的项目涌现出来。请务必访问[technodict 的]博客，了解完整的源代码和详细信息。请告诉我们您将如何在您的下一个移动项目中使用这个小机箱！