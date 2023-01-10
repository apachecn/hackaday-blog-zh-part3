# OpenPLC 准备黑客攻击

> 原文：<https://hackaday.com/2016/06/07/openplc-is-ready-for-hacking/>

距离我们报道[Thiago]的 OpenPLC 项目已经过去将近四年了。他从未停止过对它的研究，现在它处于一种高度抛光的状态。

如果你读了我们对这个项目的最初报道，很容易认为他只是想控制一些万圣节装饰品。他实际上是位于亨茨维尔的阿拉巴马大学的博士生。他的研究课题是 SCADA(又名工业控制系统)网络安全。他的目标是找到 PLC 的漏洞，并有希望修复它们。然而，没有 PLC 制造商发布他们的源代码，他很难深入理解如此封闭的东西。

所以，既然没人会为他开放他们的代码和硬件，他就自己做了。OpenPLC 可以用所有 5 种 IEC 61131-3 语言编程:ST、IL、LADDER、FBD 和 SFC。最重要的是，它通过兼容所有最受欢迎的 Arduino、Raspberry Pi、Windows、Linux 等，降低了开发这种工业硬件的门槛。

> “OpenPLC 是第一款全功能标准化开源 PLC。我们相信，打开 PLC 的黑匣子将为人们研究其概念、创造新技术和共享资源创造机会。”