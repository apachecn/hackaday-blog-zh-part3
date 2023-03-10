# 精密基准电压源

> 原文：<https://hackaday.com/2017/11/23/precision-voltage-reference-source/>

[barbouri]发现一些旧的(葡萄酒？)在他的零件箱里翻找时发现了 80 年代早期的零件，并很快旋转出一个小 PCB 来使用这些旧 IC 构建[10.000V 基准电压源。他将少量器件组装在一起，构建了一个足够好的源，可以用作另一个电路的基准电压源，或者为他的一些分辨率为 1 mV 甚至 100 μV 的台式仪器提供快速校准检查。](https://www.barbouri.com/2017/08/14/10-volt-reference-using-vintage-ics/)

![](img/efd61e20b6151fa6922b473f8203d681.png)[ad 584 *引脚可编程精密基准电压源](http://www.analog.com/en/products/linear-products/voltage-references/ad584.html#product-overview)自 20 世纪 80 年代问世，提供 10.000 V、7.500 V、5.000 V 和 2.500 V 四种可编程输出电压。该芯片经过激光调整，可确保高精度和低温度系数，只需少量外部元件即可工作。它提供 TO-99 密封金属罐和 8 引脚 DIP 两种封装。[barbouri]使用的器件的“S”版本在-55°C 至+125°C 的温度范围内提供最大 30 ppm/°C 的温度系数，但其他版本的芯片提供更好的稳定性。ADI 公司似乎已经停产了[“L”版本](http://pdf.datasheetcatalog.com/datasheet/analogdevices/AD584L.pdf) (pdf)，因为它不再列在当前的数据手册中，但您仍然可以从[几个来源](http://www.findchips.com/search/AD584LH)获得它们。“L”型的温度系数仅为 5 ppm/℃

通过使用高稳定性电阻器和带有镀金触点的 TO-99 PTFE 插座等优质部件，他的观察证实了该装置在 30 μV 内是稳定的，电压每 6 小时缓慢增加几微伏。一个 15 V 线性稳压器利用来自外部壁式电源适配器的输入功率为该器件供电。一个小的铝制外壳容纳了该设备，带有两个镀金的 4 毫米输出插座。如果你想建立自己的，他的板设计是托管在奥什公园，或者你可以下载鹰 CAD 设计文件。他在博客上发布了所有链接，并提供了所用零件的零件号。[barbouri]一直在为他的工作台构建方便的设备方面做得很好——看看我们之前介绍过的他精心制作的[毫欧计](https://hackaday.com/2017/01/24/milliohm-meter-version-1-5/)。