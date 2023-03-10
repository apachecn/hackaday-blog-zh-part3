# 编程数千个 AVR

> 原文：<https://hackaday.com/2017/01/18/programming-thousands-of-avrs/>

有趣的是，几乎所有事物都有自己的一系列问题。富人抱怨税收。名人抱怨他们缺乏隐私。这可能不会发生在我们身上，但一些 Kickstarter 活动家发现他们太成功了，必须尽快扩大生产规模。我们很乐意解决这些问题。

[林普金]发现自己就在那种情况下。他必须为数千个 Atmel 芯片编程。的确，你可以让主要经销商对它们进行编程，但在这种情况下，他想要唯一的序列号、加密密钥和其他编程的每芯片数据。所以他决定建立自己的[大众编程工作台](http://www.limpkin.fr/index.php?post/2017/01/13/A-Mass-Programming-Bench-for-ATMega32u4-MCUs)。

工作台一次编程九个器件(由于可用 I/O 的数量)，并使用 Raspberry Pi 来协调操作。微控制器监控编程请求，并使用 led 显示每个插座的状态。它还驱动一个状态 LCD。总费用约为 1500 美元。不便宜，但比其他选择便宜，如果您需要这种能力，这确实很划算。

该设备的布局可同时容纳三名操作员，以最大限度地提高产量。这是你在扩展时必须考虑的事情。如果你有幸遇到这个问题，我们之前已经讨论过[生产](https://hackaday.com/2016/11/25/a-tale-of-electronic-manufacturing/)的规模，你可以从经历过这个问题的[人那里学到一些经验](https://hackaday.com/2016/05/06/how-to-design-manufacture-and-document-a-hardware-product/)。