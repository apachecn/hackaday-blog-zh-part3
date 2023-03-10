# 电子墨水显示驱动的 DIY

> 原文：<https://hackaday.com/2017/04/20/e-ink-display-driven-diy/>

电子墨水显示器棒极了。人类花了几个世纪阅读非背光设备，坦率地说，这对眼睛更容易。但是你有没有考虑过自己驾驶这种动物呢？简直是噩梦。所以*起首部分！*感谢【Julien】他基于 [FPGA 的实现](https://hackaday.io/project/21168-fpga-eink-controller)，它不仅使用了[我们最喜欢的开源 FPGA 工具链](http://hackaday.com/2015/12/29/32c3-a-free-and-open-source-verilog-to-bitstream-flow-for-ice40-fpgas/)，还为其他感兴趣的人提供了一个开放的参考实现。

在电子墨水显示器上只显示黑白相对容易——只需用相同的信号反复击打墨水像素，直到它们放弃。灰度是通过施加更细微的电压来实现的，因为像素在某种程度上取决于状态。例如，如果想要的终点是 50%的灰色，如果像素现在是白色，而现在是黑色，你会用不同的脉冲序列来击中它。(有没有注意到你的电子书屏幕会周期性地黑白闪烁？它会将所有像素重置为已知状态。)而且这还没有考虑到电子墨水显示器所需的各种疯狂的电压，这些电压[Julien]明智地交给了专用芯片。

最后，该设备必须在屏幕上运行 20-50 次才能刷新一次用户可见的屏幕。[Julien]发现普通的微控制器无法达到他想要的速度，于是有了 FPGA 和定制波形表。我们以前见过电子墨水黑客，朱利安站在巨人的肩膀上，最著名的是彼得里·艾莫宁和 T2·斯皮雷特。[朱利安]的黑客有我们见过的最快的更新。

我们仍然不能等待廉价的通用电子墨水驱动芯片问世的那一天，因为使用电子墨水，我们用背光显示器制作的几乎每个项目都会看起来更好，并且更慢地消耗电池。同时，[Julien]的 FPGA 实现非常接近，而且是完全开放的。

 [https://www.youtube.com/embed/PNuZ6NTleZI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PNuZ6NTleZI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

