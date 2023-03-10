# Hackaday 奖参赛作品:低成本 KVM

> 原文：<https://hackaday.com/2017/08/05/hackaday-prize-entry-low-cost-kvm/>

在过去，当别人向你要串行电缆时，给他们一根 DB 串行电缆会让你送命，KVM 切换器是一个*东西*。这些设备是简单的盒子，带有几个 VGA 端口、几个 PS/2 端口和一个按钮或转盘，允许您的输入(键盘和鼠标)和输出(视频)用于多台计算机。早期的 KVM 实际上只是一个很大的旋转开关，有太多太多的电极。你还记得 PS/2 不能热插拔吗？这些 KVM 的设计者从来不知道这一点。

今天，KVM 切换器比简单的旋转开关要复杂一些。我们不再处理 VGA，我们有 HDMI 多路复用器。我们也不再处理 PS/2 了，USB 需要一点微电子来从一台计算机切换到另一台计算机。作为他众多 Hackaday 获奖作品中的一个，[KC Lee] [正在设计一款低成本的 HDMI 开关和 USB mux](https://hackaday.io/project/20326-low-cost-kvm-switch) 。它很有效，很便宜，如果你需要在盒子之间切换键盘、鼠标和显示器，这正是你需要的。

首先，HDMI 切换。为 HDMI 设计一个开关通常需要一些不起眼的部件、复杂的布线和大量的原型制作时间。[KC]找到了一个解决办法:[只需改装一个 5 美元的 HDMI 开关](https://hackaday.io/project/7700-collection-of-misc-small-project/log/51056-modding-hdmi-switch)。这款廉价的 HDMI 开关非常简单，一个 HDMI mux 完成繁重的工作，一个 8 引脚微控制器处理按钮和一个选择器 LED。

对于 USB，有更多的设计选择。对于 USB 1.x 切换，[KC]认为他可以使用 74HC4052 双 4:1 模拟多路复用器。是的，他在用模拟芯片做数字，异教徒。这也有缺点:所有东西都可能坏掉，而且它只是 USB 1.x。对于 USB 2.0 KVM，有几个更专业的选项。 [OnSemi NCN9252](http://www.onsemi.com/PowerSolutions/product.do?id=NCN9252) 是一个合适的 USB 2.0 多路复用器，在当前设计中。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)