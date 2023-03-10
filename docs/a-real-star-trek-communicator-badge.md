# 一个真正的星际旅行通信徽章

> 原文：<https://hackaday.com/2017/02/21/a-real-star-trek-communicator-badge/>

《星际迷航》从未让科技妨碍一个好故事。吉恩·罗登伯里和该剧的编剧们想出了一些惊人的小玩意，从传送器到复制器再到曲速核心本身。星际迷航:下一代给我们带来了标志性的通信员徽章。在 1987 年，一个可以装进大头针的远程无线电设备还是科幻小说。随着 [2017 年黑客日科幻竞赛](https://hackaday.io/contest/19541-hackadays-2017-sci-fi-contest)的参赛，[让这些徽章更接近真实世界](https://hackaday.io/project/19700-star-trek-communicator-badge)。

![trek-thumb](img/f82a930e4e76958d93421b3459b6bf77.png)乔处理的第一个问题是找到一种可以用手表电池供电的无线电，并提供相当大的远程操作。他选择了 HopeRF RFM69HCW。让虚构更接近现实，这个模块已经被用于与低成本卫星的[轨道通信。](http://www.50dollarsat.info/)

徽章的处理器是一个小小的 LC。[Joe]正在开发他自己的 Teensy，这意味着使用 PJRC 的 bootloader 芯片以及主微控制器。将主微处理器投入运行是[乔]目前陷入困境的地方。在试验板和表面贴装 PCB 的第一次旋转之间的某个地方，事情有点偏离了方向。振荡器正在运行，但没有 USB 通信。[乔]正在尝试另一个旋转板。他做了一些改进，并且已经有了新的电路板。改用烤面包机烤箱或煎锅锡膏和焊料装置肯定会帮助他获得新的徽章。