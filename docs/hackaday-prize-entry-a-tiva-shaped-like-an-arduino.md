# Hackaday 奖参赛作品:一个形似 Arduino 的 Tiva

> 原文：<https://hackaday.com/2017/06/27/hackaday-prize-entry-a-tiva-shaped-like-an-arduino/>

德州仪器的 Tiva C LaunchPad 展示了 TI 的 ARM Cortex-M4F，这是一款基于 TM4C123GH6PM 的 32 位 80Mhz 微控制器。Tiva 系列 LaunchPads 相当于 TI 的 Arduino Uno，价格大致相同，只是处理能力更强，GPIO 引脚的几何形状也更合理。

Tiva 的处理器运行速度比标准的 ATMega328P 快 5 倍，它拥有 40 个多用途 GPIO 引脚和多个串行端口。就像 Arduino 有护盾一样，Tiva 有升压包，TI 提供了相当多的选择——但没有一样像 Arduino 的生态系统。

[Jacob]的 Arduino-Tiva 项目是 Hackaday Prize 的一个参赛项目，旨在通过构建一个基于 TM4C123GH6PM 的电路板来重新格式化 Tiva，该电路板使用与 Arduino 相同的 form 2 " x 3 "因素，允许使用所有这些屏蔽。当然，Arduino 屏蔽只使用两排引脚，所以[Jacob]的电路板会将备用引脚放在电路板的末端，屏蔽会放在预期的引脚上。

完成的项目可以通过 Arduino IDE 或 TI 的 Energia 平台进行刷新，对于那些已经掌握 Arduino 但正在寻求更多功能的人来说，这是一个简单的下一步。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)