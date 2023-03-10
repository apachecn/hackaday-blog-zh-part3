# 采用 TO-220 封装的 DIY 5V-3V 开关转换器

> 原文：<https://hackaday.com/2018/03/13/a-diy-5v-3v-switching-converter-in-the-space-of-a-to-220-package/>

我们喜欢小型化项目。把任何东西塞进一个足够小的包装里，你可能会引起我们的注意。让它变得既小又有用，比如[这款采用 TO-220 尺寸封装的 5 伏至 3.3 伏转换器](https://blackmesalabs.wordpress.com/2018/03/03/bml-dc-dc-switcher-for-5v-to-3v-at-750ma-in-a-to-220-7805-footprint/)，这是一件令人兴奋的事情。它是一种开关模式电源，与传统的线性稳压器占用相同的空间。

诚然，[凯文·哈伯德]的小型降压转换器的重任是由 PAM2305 DC-DC 降压转换器芯片完成的，它只需要几个支持元件。但是[Kevin]将所有东西都挤在一块 9 毫米长的 PCB 上的工程设计令人印象深刻。板上最大的无源器件是 0805 中的电感。其他的都在 0603，所以如果你决定做这个，你将会考验你的 SMD 焊接技能。休息后查看视频，快速浏览手工焊接过程。

包括[开源 PCB](https://oshpark.com/shared_projects/NTidU0d2) 在内的总 BOM 仅运行一两个降压器，最终结果是电源具有稳定的 750mA 输出，可以处理 5 秒钟的 1a 浪涌。我们想知道一个小散热片是否对此没有帮助；随着一些黑色环氧树脂灌封，它至少会完成 TO-220 的外观。

[凯文]的布莱克梅萨实验室有生产有趣项目的历史，从 Arduino 的合法视频卡到银元大小的 100 瓦回流焊接电炉[。不管接下来会发生什么，我们都很期待——如果我们能看到的话。](https://hackaday.com/2016/04/01/tiny-hotplate-isnt-overkill/)

> 需要一个小型 DC/DC 3W 开关来将 7805 至-220 引脚排列中的 5V 降至 3V？或者可能只是想学习表面贴装焊料 0603 元件。看看这个来自布莱克梅萨实验室的价值 3 美元的 OSH 项目。来自 [@oshpark](https://twitter.com/oshpark?ref_src=twsrc%5Etfw) 的 0.60 美元 PCB，来自 [@digikey](https://twitter.com/digikey?ref_src=twsrc%5Etfw) 的 2 美元 BOM。https://t.co/YmB9mbYFbW[pic.twitter.com/HaTes33O9f](https://t.co/YmB9mbYFbW)
> 
> —凯文·哈伯德(@ bml _ khubbard)[2018 年 3 月 4 日](https://twitter.com/bml_khubbard/status/970093461067083776?ref_src=twsrc%5Etfw)