# 树莓派 3B+作为特别提款权-没有特别提款权！

> 原文：<https://hackaday.com/2018/04/14/the-raspberry-pi-3b-as-an-sdr-without-the-sdr/>

我们已经习惯于将软件定义无线电作为无线电实验的未来，我们中的许多人都将拥有某种形式的 SDR 硬件。从 10 美元的 RTLu 盘到价格令人垂涎的会唱歌会跳舞的模特，每个人都有一个特别提款权。

没有任何外部硬件的 SDR 的想法怎么样？与其往你的 Raspberry Pi 里塞东西，不如直接使用 Pi 本身，不加修改？[这正是 Nexmon SDR 项目所实现的目标](https://github.com/seemoo-lab/mobisys2018_nexmon_software_defined_radio)，这是通过巧妙使用板载 Broadcom 802.11ac WiFi 芯片实现的。结果是一个支持 TX 的 SDR，尽管它只能在 WiFi 使用的 2.4 GHz 和 5 GHz 频谱内工作。

该团队之前曾与 Nexus 5 手机中的芯片组广泛合作，SDR 扩展首先在该平台上可用。然后出现了 Raspberry Pi 3 B+,它具有足够相似的 WiFi 芯片组，相同的黑客可以移植到该平台，瞧:Pi 3 B+上的 WiFi SDR。

如果你还没有看过 Pi 3 B+，我们希望你能看到我们的评论。如果你没有 Nexus 5，并且你想做一些 WiFi 波段的 SDR 工作，这看起来是一笔惊人的交易。

途经[rtl-sdr.com](https://www.rtl-sdr.com/nexmon-sdr-using-the-wifi-chip-on-a-raspberry-pi-3b-as-a-tx-capable-sdr/)。