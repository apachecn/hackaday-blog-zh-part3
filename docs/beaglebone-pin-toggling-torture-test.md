# 猎兔犬骨钉栓拷问试验

> 原文：<https://hackaday.com/2016/04/21/beaglebone-pin-toggling-torture-test/>

基准测试经常受到批评，因为它们不能像我们希望的那样完美地模拟真实世界的情况。因此，在有限的范围内理解接下来的内容，不要过度解读。[Joonas Pihlajamaa]在不同的单板计算机上尽可能快地切换硬件引脚的实验仍然可以向我们展示一些东西。

这个带回家的结果不会让任何使用过单板计算机的人感到惊讶:与直接的内存映射 GPIO 访问相比，更高级别的接口简直太慢了。但是*真的*慢。我们说的是从 Python 或任何基于文件的接口到引脚的频率约为 5 kHz，而直接访问的频率为 3 MHz。更糟糕的是，正如您所料，当非实时操作系统处于中间时，所有基于文件的方法都会出现大约 10 毫秒的故障。

[![](img/f6e273101dcf214bec7b230876e613ff.png)](https://hackaday.com/2016/04/21/beaglebone-pin-toggling-torture-test/cpp/)

File-mapped

[![](img/8d7aaa5b86c193e454e26387742b0b41.png)](https://hackaday.com/2016/04/21/beaglebone-pin-toggling-torture-test/cmmap/)

Memory-mapped

不过，这项测试只能告诉我们这么多，它并没有真正利用 BeagleBone Black 的王牌 PRUs——为系统带来实时 IO 功能的板载硬件处理器。例如，我们希望看到重写代码来利用 [libpruio](http://hackaday.com/2015/02/16/library-upgrade-to-pru-gives-fast-io-on-beaglebone/) 。对于 PRUs 来说，20 MHz 方波是小菜一碟。

当然不是交互，这大概是按照所写的标杆精神。但是如果 BeagleBone 上的原始硬件速度是目标，那么 pru 很可能会在解决方案中占据显著位置。