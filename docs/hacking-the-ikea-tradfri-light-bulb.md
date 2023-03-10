# 黑掉宜家 Trå dfri 灯泡

> 原文：<https://hackaday.com/2017/11/17/hacking-the-ikea-tradfri-light-bulb/>

[BasilFX]想要[将定制固件安装到他的 IKEA Trå dfri 灯泡](https://www.youtube.com/watch?v=yi_Z2WtmdDU)上。该产品包括一个 GU10 大小的灯泡和一个 LED 驱动器，以及控制这一切的宜家定制 ZigBee 模块。扩散器、外壳和爱迪生螺口灯头使整个装置具有与标准 A 系列灯泡相同的外形。Trå dfri 模块将宜家的家庭自动化产品结合在一起，由集成 2.4Ghz 无线电和 256 Kb 闪存的 ARM Cortex M4 MCU 组成，价格仅为 7 欧元！

巧合的是，[BasilFX]刚刚为 RIOT-OS(物联网的友好操作系统)贡献了 EFM32 支持，所以他已经成功了一半。他使用 JTAG/SWD 兼容调试器，在芯片仍然连接的情况下，在灯泡上闪烁芯片。

[BasilFX]承认，整个项目只是一个概念验证，还没有真正的用途，尽管他已经将目光转向让无线电工作，目标是创造一个灯泡网络。你可以在他的[代码库](https://github.com/basilfx/TRADFRI-Hacking)上找到更多信息。

今年早些时候，我们发表了一篇关于 Trå dfri 黑客攻击的文章，以及一篇关于用于发现灯泡秘密的[逆向工程过程](https://hackaday.com/2017/02/06/reverse-engineering-ikeas-new-smart-bulbs/)的文章。

 [https://www.youtube.com/embed/yi_Z2WtmdDU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yi_Z2WtmdDU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

