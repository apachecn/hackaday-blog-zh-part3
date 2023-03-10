# FM 101 和发射机由阿曼制造

> 原文：<https://hackaday.com/2016/01/09/fm-101-and-transmitter-build-with-afroman/>

我们最喜欢的电子知识提供者之一又来了。这一次， [[Afroman]解释了调频是如何工作的，同时在他在奥什公园的一块板上组装了一个短程调频发射机](http://www.youtube.com/watch?v=ZUxDXXBO3eA)。

该设计基于 MAX2606 压控振荡器(VCO)芯片，工作频率为 70-150MHz。[Afroman]使用 390nH 电感将其设置为约 100MHz 的振荡频率。他还在 2606 的调谐针上放了一个电位计分压器。通过电位计发出的电压变化会以很小的增量改变发射频率，这样就可以很容易地调到适合你的广播频道。加上一个驻极体麦克风和大约一米长的实芯线，你就有了一个适用于大约 20 米范围的调频发射机。

有很多方法可以构建一个小型 FM 发射器，允许进行一些实验，并且不需要放置 SMD 元件。[去年夏天我们报道了一个构建](http://hackaday.com/2014/07/30/a-dead-simple-well-constructed-fm-transmitter/)，它使用了几个 3904，并搭载了一个从一个没电的电池中回收的 9V 连接器。缺点是晶体管发射机的频率稳定性不如 VCO 芯片。

 [https://www.youtube.com/embed/ZUxDXXBO3eA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZUxDXXBO3eA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

