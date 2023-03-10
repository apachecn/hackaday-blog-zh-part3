# EKG 名片温暖我们的心

> 原文：<https://hackaday.com/2016/03/13/ekg-business-card-warms-our-hearts/>

送出一张纸质名片太 60 年代了。分发一张 PCB 名片，会让你进入 21 世纪初。如今，如果你真的想脱颖而出，就给他们一张名片上写着功能齐全的 EKG。(注意:如果你领导一个开源[心电图](https://en.wikipedia.org/wiki/Electrocardiography)项目，效果最好。)

翻看[原理图(PDF)](http://mobilecg.img/cardsch.pdf) ，卡上没多少。一切的中心是一个 [ADuC7061](http://www.analog.com/en/products/processors-dsp/analog-microcontrollers/arm7-core-products/aduc7061.html#product-overview) ，这是一个配备了 *24 位*ADC 的 ARM 微处理器，它还有一个连接到用户一个拇指的内部 DAC 驱动电压基准。这一点，加上一点缓冲电路，似乎足以将你双手之间的微小电位差转化为内置有机发光二极管显示器上的美丽信号。非常好！

一切(包括他们的 EKG 的大版本)都是开源的，并且是在一个开放的工具链上制造的。如果你对健康和医疗传感感兴趣，你应该去该项目的 GitHub 看看。独立的开放式 EKG 是基于一个更加复杂的电路，并且更加精确。但是名片版实在是太可爱了！

感谢[Ag Primatic]的提示！