# Hackaday 奖品入口:袖珍串行终端

> 原文：<https://hackaday.com/2017/04/06/hackaday-prize-entry-pocket-serial-terminal/>

当你面前的工作台上有一个微控制器或其他微型计算机，并且它缺少现代台式计算机熟悉的键盘和显示器时，当你希望对它进行编程或发出命令时，你该怎么办？除非你是一个渴望一套 Altair 风格的拨动开关的复古电脑爱好者，否则你很可能会找到它的串行端口并连接一个终端。

串行终端是一种包含屏幕和键盘的设备，连接起来可以从串行端口发送和显示文本，曾经是计算的主要部分，但作为独立设备，它们现在相当罕见。如今，在大多数情况下，使用串行终端意味着在你的现代操作系统、Linux、Windows 或 MacOS 中打开一个终端模拟器，但是仍然有对独立硬件的使用。[Kuldeep Singh Dhaka]肯定是这样认为的，因为他正在制造一款带有 LCD 屏幕的非常好的便携式终端。

该终端模拟了一个古老的 DEC VT-100 终端，但由于它是围绕 STM32F105 ARM 微控制器构建的，我们确信它可以通过适当的软件模拟其他模型。它要么使用 USB 键盘，要么使用 PS/2 键盘，所以我们希望在使用时看到它配有一个合适的小型便携式键盘。目前还没有可用的源代码，因为这在很大程度上仍然是一个正在开发的项目，我们现在正在展示它，因为它是 2017 年 Hackaday 奖的参赛作品，但他向我们保证代码将会在路上，并将获得 GPL 许可。

他甚至发布了一个视频，我们把它放在了运行中的设备的中断处，连接到运行 MicroPython 的机器上。不过，我们可能会关掉哔哔声。

 [https://www.youtube.com/embed/UHGNkTDYr1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UHGNkTDYr1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想看真正的 VT100，[这里有一个我们展示给你的小猎犬骨](http://hackaday.com/2013/10/16/vt100-gets-beagleboned/)。但是，如果国产终端是你的东西，那么[一个 LED 屏幕是它真正在](http://hackaday.com/2016/11/08/when-a-crt-isnt-retro-enough-leds/)的地方。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)