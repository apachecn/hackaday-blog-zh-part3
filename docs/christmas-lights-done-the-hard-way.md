# 艰难制作的圣诞灯

> 原文：<https://hackaday.com/2016/12/09/christmas-lights-done-the-hard-way/>

又到了一年中的这个时候，你不得不开始担心自己是否淘气到不接受任何礼物。希望闪烁的灯光能安抚圣尼克。抓住一条 RGB LEDs，把它们连接到 Arduino 和电源上，加上一些代码，这就是你的叔叔了。但是如果你想保持你的黑客信誉，你最好来硬的。这就是[roddersblog]今年在建造他的[圣诞星爆 LED Stars](https://roddersblog.wordpress.com/2016/10/29/a-star-is-born/) 时所做的——以及提前参加派对的奖励积分。

首先，他从易贝获得了 WS2812 电路板的面板(如 PCB 面板)。好处是它可以让你选择自己的音高和长度。另一方面，你需要拆除每块电路板，将其安装在夹具上，然后将三段连接线焊接到每个 LED 上。他设计了一个八面星形，每个星形有十个 LED。他造了三个。因此，至少可以说，线路是充实的。他不得不处理拒绝固化和硬化的硅酮密封剂。但是没有什么是勇气和决心解决不了的。

对于控制，他选择了 PIC16F1509 微控制器。该系列有一个被 PIC 称为“可配置逻辑单元”的特性，这篇[应用笔记](http://ww1.microchip.com/downloads/en/AppNotes/00001606A.pdf)描述了如何使用 CLC 将 PIC 与 WS2811 接口。他注意到由于 C 代码开销导致的处理延迟，这让他有些难过。经过一些试验后，他用汇编重新编写了整个程序，产生了令人满意的结果。你可以在 [GitHub 库](https://github.com/Rod63/StarBurst)上查看他的代码。

同样值得一看的是，他有一些锦囊妙计来提高自制 PCB 的质量。他建造了自己的带计时器的紫外线曝光装置，这本身就是一个有趣的项目。该布局采用 Eagle 设计，采用洪水填充，以最大限度地减少需要蚀刻掉的铜。他用激光打印出版面，在纸上涂上植物油，使其对紫外线更加透明，然后将照片对折，以获得良好的对比度。

一旦感光板在 UV 单元中曝光，他就使用弱但新鲜且温暖的氢氧化钠溶液作为显影剂来去除未曝光的 UV 光致抗蚀剂。为了蚀刻电路板，他使用标准的氯化亚铁溶液，用水族箱加热器保温，同时用水族箱气泵搅动溶液。他还描述了如何用同样的技术制作双面板。最终结果相当令人满意——休息后看看视频。

 [https://www.youtube.com/embed/QVpx1xNJkl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QVpx1xNJkl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

