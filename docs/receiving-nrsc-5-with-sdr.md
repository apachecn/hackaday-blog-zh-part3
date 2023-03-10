# 用 SDR 解码 NRSC-5 进入你的汽车

> 原文：<https://hackaday.com/2017/06/21/receiving-nrsc-5-with-sdr/>

NRSC-5 是一种高清无线电标准，主要在美国使用。它允许数字和模拟传输共享原始的 FM 带宽分配。Theori 是美国的一家网络安全研究初创公司，已经着手建造一种可以捕捉和解码这些信号的接收器，用于研究目的，并在网上记录了这一过程。

他们的研究始于 NRSC 网站，那里记录了 NRSC-5 标准，然而该团队注意到音频压缩细节明显缺失。然后，他们一步一步地通过物理层、复用层，最后是应用层，一点一点地拆开标准。这一切最终导致该集团为 NRSC-5 号开发了一个[开源接收器，可与 RTL-SDR—](https://github.com/theori-io/nrsc5)[一起使用，这可能是世界上最普遍的 SDR 平台。](https://hackaday.com/2012/06/27/getting-started-with-software-defined-radio/)

集团对 NRSC-5 的主要兴趣在于它作为车载娱乐系统的一部分出现在汽车上。由于 NRSC-5 允许以各种格式传输数据，该组织怀疑没有安全处理这些数据的车辆可能存在安全隐患——例如，通过发送[坏的 ID3 标签](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=id3)通过娱乐系统进入你的汽车。我们期待看到这项正在进行的研究的结果。

【感谢 Gary McMaster 的提示！]