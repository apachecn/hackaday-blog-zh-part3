# 将 NES 移植到 ESP32

> 原文：<https://hackaday.com/2016/10/10/porting-nes-to-the-esp32/>

当谈到树莓派零度时，房间里有一头大象。Pi Zero 是一款非常受欢迎的单板电脑，但第一年的缺货问题可能是由于一个简单的事实:你可以在上面运行任天堂模拟器。没有像集群、CNC 控制器和基于 Linux 的 throwies 这样酷的项目，Pi Zero 的所有潜力最初都浪费在拯救公主上了。

Espressif 推出了一款新芯片 ESP32，这是一款神奇的物联网产品。它很便宜，功能异常强大，尽管我们预计股票问题的解决速度会比 Pi Zero 更快，但仍然存在一个危险:如果 ESP32 可以模仿 NES，它可能会太受欢迎。就在 24 小时前，我在本周的 Hackaday Links 帖子中提出了假设的供应问题。

Hackaday fellow，Hackaday Supercon speaker，Espressif 员工，以及一个非常棒的家伙[Sprite_tm] [刚刚将一个 NES 仿真器移植到了 ESP32](https://www.youtube.com/watch?v=ympmRydFMmE) 。看起来 Espressif *真的*知道如何销售芯片:只要给你的一个工程师一个 YouTube 频道。

昨天当[Sprite]走进他的办公室*时，他发现一个新的电路板正等着他去测试。该板具有 [ESP-WROOM-32](https://espressif.com/en/content/esp-wroom-32-datasheet) 模块，并在背面分出一些引脚到 microSD 卡、FT2232 USB/UART 模块、JTAG 支持、一组 GPIOs 和 320×240 LCD。[Sprite]当天的工作是测试这个板，但他每天早上都喝一杯咖啡阅读 Hackaday(像任何文明的黑客一样),并把 links 帖子视为挑战。结果是将 NES 仿真器移植到 ESP32。*

ESP-32-NESEMU 基于 Nofrendo 仿真器构建，在仿真方面，ESP32 能够保持更高的帧速率。按照[Sprite]的说法，显示器是瓶颈；SPI 供电的显示器更新不够快。[Sprite]也没有足够的时间来处理声音，但是项目的源代码是可用的，即使这个开发板没有。

现在，你可以*订购一台 ESP32 我的卡在离长滩港几英里的一艘集装箱船上。供应仍然是一个问题，现在[Sprite]已经确保 ESP32 将成为近年来最受欢迎的嵌入式开发平台。所有这一切都发生在 24 小时内。这太棒了。*

 [https://www.youtube.com/embed/ympmRydFMmE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ympmRydFMmE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在你等待一个开发板上岸的时候，让你自己加快速度。[埃利奥特·威廉姆斯]已经发布了第一个系列教程。