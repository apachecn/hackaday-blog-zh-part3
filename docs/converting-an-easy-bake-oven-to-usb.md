# 将简易烤箱转换成 USB

> 原文：<https://hackaday.com/2017/03/19/converting-an-easy-bake-oven-to-usb/>

[【杰森】将简易烤箱改装成 USB](https://www.reclaimerlabs.com/blog/2017/3/14/usb-c-easy-bake-oven) 。如果你一定要问为什么你永远不会知道。

自从你在简易烤炉里安装了一个 100 瓦的灯泡，烧毁了你的房子之后，简易烤炉已经发生了很大的变化。现在，简易烤炉是很好的材料。这是一根镍铬合金线，通过一个开关连接在主电源上。镍铬合金线的一部分是用来给灯供电的电阻分压器。这个灯组件只是一个 LED、一些电阻器和一个反向并联到 LED 的二极管。

这是一个为 120 V 设计的设备，但[Jason]希望它在 USB-C 上运行。虽然有 USB-C 充电器可以为一个简单的烤箱提供足够的电力，但电压被限制在 20 V。Jason 没有提高 USB-C 的电压，而是添加了一些镍铬合金线，将其分成六个相等的部分，然后将所有部分并联起来。这使电压降低了六分之一，电流增加了六倍。够好了。

这次黑客使用的电源是[苹果官方 87W 交易](http://www.apple.com/shop/product/MNF82LL/A/87w-usb-c-power-adapter)，带一个 USB-C 分线板([在 Tindie 上有](https://www.tindie.com/products/ReclaimerLabs/usb-type-c-power-delivery-phy-breakout-board/)，在 Tindie 上买点东西。超级即时广告)连接到 I2C 引脚的 Arduino Uno。几个[位的代码](https://github.com/ReclaimerLabs/USB_PD)之后，【杰森】通过 USB 电缆获得了大量的能量。

随着简易烤箱的完全改造，[杰森]搅打了一批饼干混合物。大约 15 分钟后，饼干变脆了，看起来几乎让人胃口大开。

虽然结果很奇怪——到底谁会想要一个 USB 供电的简易烤箱——但老实说，这是对[Jason]的 USB-C PHY 分线板的一次奇妙的测试。有什么比大电阻负载更好的测试 USB-C 的方法，有什么比简易烤箱更好的电阻负载？既精彩又搞笑。