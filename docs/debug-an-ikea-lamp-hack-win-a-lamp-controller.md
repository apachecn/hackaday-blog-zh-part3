# 调试宜家灯具，赢得灯具控制器

> 原文：<https://hackaday.com/2015/09/14/debug-an-ikea-lamp-hack-win-a-lamp-controller/>

[Limpkin]，又名 Hackaday alum [Mathieu Stephan]，又来了，[把一盏宜家灯变成一盏视觉唤醒灯](http://www.limpkin.fr/index.php?post/2015/08/30/A-Connected-Clock-to-Wake-Me-Up)。他希望建立一个可以远程触发的警报，他的这个项目基于一个处理通信和定时的 ESP8266 和一堆 10 瓦 RGB LEDs 的组合。然而，他遇到了一个问题:每次他初始化将控制 led 水平的 PWM(脉宽调制)信号时，[他的 ESP8266 开发板就会重启](http://www.esp8266.com/viewtopic.php?p=26692)。因此，他为发现问题的人提供了一份有趣的赏金:找出问题所在，他会把灯送给你。好吧，无论如何，PCB 和组件:你必须添加你自己的宜家灯。这是一种调试硬件问题的有趣方法，所以请随意看看。完整的硬件和软件细节都在他的 [GitHub 库](https://github.com/limpkin/espalarm)上。