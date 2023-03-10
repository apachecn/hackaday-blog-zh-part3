# 黑客入侵物联网:解码 LoRa

> 原文：<https://hackaday.com/2016/01/31/hacking-the-internet-of-things-decoding-lora/>

将软件定义无线电(SDR)工具交到社区手中对于开发和解码世界各地以前加密的无线电信号非常重要。只要有新的协议或调制方法，它就会出现在每个人的视线中。很多人都在研究 LoRa，海牙 RevSpace 的[bertrik]也做了一些自己的工作，并整理了一份令人惊叹的艺术状态摘要。

LoRa 是一种新的(ish)低功率无线电调制方案。[它的专利是](https://www.google.com/patents/US7791415)，所以有一些关于它的信息。但它也是专有的，这意味着你需要一个许可证来生产使用这种编码的收音机。为了与今天的流行词保持一致，LoRa 被作为物联网的广域网进行营销。HopeRF 制造了一个相当便宜的 LoRa 模块，自然[bertrik]已经[为使用它编写了一个 Arduino 库](https://github.com/bertrik/loratest)。

所以手里拿着一个 LoRa 收音机，和一个连接到笔记本电脑的 15 美元 RTL-SDR 加密狗，[bertrik]获得了一些捕捉，将 FM 调制的啁啾声转换成音频，并进行了大量的手部分析。他确认现有的 sdrangelove 插件已经(大部分)完成了它们应该做的，他把它们都写了出来，包括一组奇妙的链接。

还有更多的工作要做，所以如果你对 LoRa 感兴趣，或者只是想看看这个新的调制方案，你现在已经有了一个很好的起点。