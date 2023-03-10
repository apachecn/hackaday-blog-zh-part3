# Arduino 的 ISM 通信

> 原文：<https://hackaday.com/2017/07/09/ism-communications-for-arduino/>

如果你想在设备之间进行无线通信，WiFi 和蓝牙是显而易见的选择。但是也有您使用的 ISM(工业、科学和医疗)波段。有像 SX1278 这样的廉价模块可以使用 LoRa 调制来处理这一问题，但它们不能方便地与 Arduino 一起使用。[简]注意到了同样的事情，并着手[建造一个防护罩，允许 Arduino 使用 LoRa](http://www.deviceplus.com/how-tos/arduino-guide/arduino-long-range-communication-tutorial-lorenz-shield/) 进行通信。你可以在 [GitHub](https://github.com/jgromes/LoRenz) 上找到设计数据。[简]称之为洛伦兹盾。

根据[Jan]的说法，每块电路板的制造成本约为 20-30 美元，其中大部分成本用于运输 PC 板。LoRa 允许你用数据速率换取带宽，但是典型的数据速率是相当适中的。至于范围，这也取决于很多因素，但我们已经看到了以英里数表示的[范围。](https://hackaday.com/2017/04/29/simple-range-testing-for-lora-modules/)

根据您的居住地，使用 SX1278 等收音机可能会受到法律限制。在购买 ISM 频段之前，您应该了解当地的法律。我们不确定这是否明智，但这块板可以和其他三块类似的护盾共存。因此，如果你有一个 Arduino，你就可以让 4 个无线电同时运行，并且可以管理电源、RF 和其他相关问题。模块使用的分线板有一个天线连接器，因此根据您当地的法律，您可以获得其中一个的良好范围。

[Jan]承诺在库上发布一个帖子，让它很快就能工作，但是你现在可以在 GitHub 上找到代码。如果您查看 examples 目录中的代码，这似乎非常简单。你不得不放弃一些软件，但 SX1278 可以支持除 LoRA 以外的其他模式，包括 FSK 和其他数据调制技术。

我们见过其他的[劳拉护盾](https://hackaday.com/2017/01/06/ces17-arduino-unveils-lora-modules-for-the-internet-of-things/)，但不多。如果你对[其他无线技术](https://hackaday.com/2016/05/05/which-wireless-tech-is-right-for-you/)感兴趣，我们已经谈了很多。如果你想对 LoRa 有一个基本的了解，下面的视频是一个很好的开始。

 [https://www.youtube.com/embed/hMOwbNUpDQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hMOwbNUpDQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

