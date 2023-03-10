# 巨大的互动填字游戏

> 原文：<https://hackaday.com/2017/02/10/huge-interactive-crossword/>

给孩子一些有责任和挑战性的任务，你会对结果感到惊讶。在华沙国家博物馆举办的“一切皆有可能”展览旨在进行博物馆学和教育实验。69 名 6-14 岁的儿童被分成小组，负责准备博物馆的主要临时展览。六个多月来，他们在每周四小时的会议中筹备展览。他们准备脚本，为多媒体演示提供想法，并策划了近 300 件作品进行展示。其中之一是【罗伯特·莫德松】的[巨型互动纵横字谜](http://www.mordzon.net/blog/uncategorized/huge-interactive-crossword/)。

该建筑分为两部分。嵌入了 RFID 标签的字母瓷砖看起来显然是建造中最容易的部分。桌子，看视频(休息后)，可能需要更多的努力和劳动。它分为两半，以使施工更容易。有 130 个盒子需要填入正确的字母来完成填字游戏。每个盒子都包含一组电子设备，包括一个 Arduino Nano、一个 RFID 阅读器和一组 16 个 WS2812B LEDs，所有这些都组装在一个定制的 PCB 上。算一算，你会发现有 2080 个 led，每个都能够在全亮度下消耗 60 毫安。在 5 V 电压下，总电流要求接近 125 安培。加上所有的 Arduino，并且[Robert]需要强大的 750 W 功率，通过四个开关模式电源供应。

每个 Arduino Nano 都是 I2C 总线上的从机。I C master 是 Arduino Mega 2560，它通过串行与计算机通信。当盒子是空的时，发光二极管是暗的，当一个错误的字母被放置时，它们变成红色，当正确的字母被放置时，它们变成绿色。如果一个单词完成了，就会播放一个特殊的单词动画。这些信息也被传送到计算机，然后计算机在一个巨大的墙壁屏幕上放映一个与这个单词相关的动画。填字游戏完成后，桌子爆发出声音(通过电脑)和灯光“迪斯科”表演，并揭示了展览这一部分的主要格言——“扮演英雄”。

 [https://www.youtube.com/embed/5py432CC4L0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5py432CC4L0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

