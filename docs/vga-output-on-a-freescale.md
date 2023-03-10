# 飞思卡尔上的 VGA 输出

> 原文：<https://hackaday.com/2016/02/26/vga-output-on-a-freescale/>

尽管 VGA 已经过时，并开始被弃用，但让这种视频输出在非标准硬件上运行是一些黑客的必经之路。[Andrew]是最近接受挑战的人。他在 Freescale i.MX233 上获得了 VGA 输出，同时也获得了一些深入研究 Linux 内核的经验。

Freescale i.MX233 是一台单板计算机，它有很好的文档记录，易于连接到其他设备，无需专门的硬件。它有 PAL/NTSC 格式的视频输出，但这对安德鲁来说还不够。获得内核源代码后，所有需要做的就是修补内核，构建内核，并构建一个自定义 DAC 来将 GPIO 引脚连接到 VGA 连接器。

(Andrew)做的第一件事是加载 Hackaday 主页，他注意到这要花很长时间，因为 i.MX233 的运行频率只有 454 MHz，内存只有 64 MB。虽然[我们的复古页面](http://retro.hackaday.com/)加载速度可能会快一点，但这仍然是一个令人印象深刻的版本，也是探索更多 Linux 内核的伟大的第一步。飞思卡尔 i.MX233 是一款流行的芯片，可以在单板计算机上运行 Linux，而且在这个社区中有很多。如果这更符合你的风格，也有一些[极端 VGA 黑客](http://hackaday.com/2015/12/17/attiny-does-170x240-vga-with-8-colors/)。