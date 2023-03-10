# 劳拉是网络

> 原文：<https://hackaday.com/2017/10/24/lora-is-the-network/>

我们已经习惯于看到 LoRa 出现在这些页面上的项目中，作为一个低带宽的无线数据链路，它的工作范围很大。通常，这些 LoRa 项目采用与中央互联网连接节点对话的客户端形式，允许远程无线连接设备通过该节点连接到互联网。

有趣的是，我们看到了一个来自[Mark C]，[的普通应用程序，它是一个聊天应用程序，旨在使用一组 LoRa 节点作为对等网络](https://hackaday.io/project/27817-lora-chat)。实际上，LoRa 变成了网络，而不仅仅是一个访问它的工具。他在给我们的电子邮件中乐观地将 LoRa networks 描述为新的 FidoNet，这可能是一个大胆的声明，但我们肯定可以看到一些相似之处。值得注意的是，该应用程序仅仅是一个可演示的概念证明，但是我们同意它有一些潜力。

该项目使用的硬件是基于 Heltec ESP32 的 LoRa 板，它带有一个方便的有机发光二极管屏幕，信息显示在屏幕上。就其现状而言，需要一个 PC 连接来通过串行接口提供文本输入，但是也可以想象其他更独立的接口。如果你感兴趣，代码可以从 GitHub 库下载[，所以这可能成为更广泛的点对点 LoRa 网络的种子。](https://github.com/unprovable/LoRaChat)

这些年来，这里并不缺少 LoRa 项目。最近的新闻包括[一个便捷的本地 LoRa 数据包嗅探器](https://hackaday.com/2017/08/22/sniff-your-local-lora-packets/)，以及[一个气球上 LoRa 节点](https://hackaday.com/2017/09/11/the-things-network-sets-702-km-distance-record-for-lorawan/)的极限距离记录。