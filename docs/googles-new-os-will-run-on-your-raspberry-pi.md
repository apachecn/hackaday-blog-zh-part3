# 谷歌的新操作系统将在你的树莓派上运行

> 原文：<https://hackaday.com/2016/08/17/googles-new-os-will-run-on-your-raspberry-pi/>

根据来自 [Android Police](http://www.androidpolice.com/2016/08/12/google-developing-new-fuchsia-os-also-likes-making-new-words/) 和 [ZDNet](http://www.zdnet.com/article/google-waves-goodbye-to-linux-for-new-iot-os-fuchsia-coming-soon-to-raspberry-pi/) 的报道，你可能很快就会有一个来自谷歌的新操作系统在你的树莓 Pi 上运行。细节仍然极其稀少，[GitHub 页面上唯一的描述是](https://github.com/fuchsia-mirror)“粉色+紫色== Fuchsia(一个新的操作系统)”。但是，我们知道的是:

新的操作系统名为 Fuchsia，将基于 Magenta，而 Magenta 又建立在 LittleKernel 上。这意味着，令人惊讶的是，谷歌将不会为新操作系统使用 Linux 内核，而是更像嵌入式 RTOS。虽然 Google 针对的是嵌入式系统，但是能够在桌面上运行的可能性已经提到了，所以可能不会太简约。

谷歌的 Travis Geiselbrecht 已经明确地将 Raspberry Pi 3 命名为它将运行的一个系统，并表示它将很快上市。但是，似乎谷歌的目标是让它在各种 ARM 设备(32 位和 64 位)以及 64 位 PC 上运行。这是与目前可用的其他商业嵌入式操作系统竞争的直接努力，尤其是在物联网设备上。

如果你渴望了解这一切，你可以跟随[谷歌的快速启动食谱](https://fuchsia.googlesource.com/magenta/+/master/docs/getting_started.md)看看你能想出什么，尽管细节仍然不够粗略，我们只是要等一会儿。