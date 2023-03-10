# Hackaday 奖参赛作品:开源回流炉控制器 Reflowduino

> 原文：<https://hackaday.com/2017/11/07/hackaday-prize-entry-reflowduino-the-open-source-reflow-oven-controller/>

面对现实吧——你需要一个回流焊炉。即使最稳定的手和最好的眼睛也只能在 SMD 板上用手动熨斗产生“meh”结果，而忘记了能够放大生产。但是当你建造你的烤箱时，你应该使用什么控制器，它应该支持什么特性？不要担心——你可以拥有[这款开源回流焊炉控制器](https://hackaday.io/project/27900-reflowduino-bluetooth-reflow-oven-controller)的所有功能。

由于显而易见的原因，被称为回流炉的[Timothy Woo]的 Hackaday 奖参赛作品拥有回流炉控制器所需的一切，以及一些你从来不知道自己需要的东西。基于 ATMega32，Reflowduino 负责回流控制器的常规任务，即运行精确控制烘箱温度和控制加热曲线所需的 PID 回路。我们起初认为包含蓝牙模块有点奇怪，但[Timothy]解释说，在软件中实现控制器的 UI 比在硬件中容易得多，并且它节省了微控制器上的大量 IO。对 LiPo 电池的支持有些令人困惑，因为这种电池有用的情况似乎有限，因为烤面包机烤箱或热板仍然需要电源。但是当一个循环结束时播放星球大战曲调的音响呢？那只是为了好玩。

向[Timothy]致敬，他的构建一流，文档优秀，深入研究了 PID 理论，并给出了构建的每一步的详细说明。想试试低端回流？拔出[一盏卤素工作灯](https://hackaday.com/2017/07/13/a-bright-idea-for-reflow-soldering/)，或者也许[点燃丙烷火炬](https://hackaday.com/2016/09/01/blowtorch-smd-reflow/)。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)