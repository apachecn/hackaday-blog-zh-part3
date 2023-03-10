# 疯狂的 WiFi 之眼

> 原文：<https://hackaday.com/2017/11/21/mad-eye-for-the-wifi/>

在《哈利·波特》的世界里，穆迪教授戴着一只假眼，因此被赋予了“疯眼”的绰号，这或许有些不公平。他的眼睛仍然是技术头脑的 cosplayers 的挑战，旨在重现这种独特的头饰的外观和感觉。[【cyborg workshop】已经掌握了基础眼，但是想更进一步。](https://cyborgworkshop.org/2017/11/19/mad-eye-moody-v2-with-wifi/)

最初的构建依靠一个亚微型伺服系统来移动眼球。这是随机进行的，试图模拟书籍和电影中眼睛的行为。然而，想要更多，[cyborgworkshop]决定让眼睛对周围的环境更加敏感。使用用于 ESP8266 的分线板 [Adafruit Huzzah](https://www.adafruit.com/product/2471) ，快速生成代码来检测该区域的 WiFi 接入点数量。接触点越多，眼睛的运动就越频繁和不稳定。根据当地 WiFi 环境的饱和程度，在眼睛再次恢复疯狂扫射之前，偶尔较慢的运动周期会被编码。

这是这个项目的一个重大转折，而且[cyborgworkshop]也提供了初始构建的更多细节。如果你认为你有似曾相识的感觉，[看看这个用回收部件建造的建筑](https://hackaday.com/2017/11/16/servo-controlled-eyeball-makes-a-muggle-moody/)。