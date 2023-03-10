# 口袋猎犬的实时音频

> 原文：<https://hackaday.com/2018/02/25/real-time-audio-for-the-pocketbeagle/>

BeagleBone 长期以来一直是实时 I/O 的最爱，现在随着 pocket bone——钥匙链大小的小型 beagle bone——的发布，这种小型可编程实时 Linux 模块的用途越来越多。刚刚发布的 Bela Mini 是最新的附加斗篷，利用了微型口袋骨的处理能力。

Bela Mini 是 Bela T1 的缩小版，是 BeagleBone 的 cape 附件。原始信号分为 8 路模拟输入和 8 路模拟输出，均为 16 位深度。通过增加有源扬声器输出，Bela 将 BeagleBone 变成了完美的微型音频-Linux-东西，特别强调纯数据和其他音频魔法。

Bela Mini 取消了有源扬声器输出，代之以三针连接器上的立体声音频输入和立体声音频输出端口。与原来的 Bela 相比，Mini 失去了 8 个 16 位模拟输出，但仍保留模拟输入。

已经有很多尝试将实时音频添加到微控制器和 Linux 主板上，但是很少有例子像宣传的那样成功。大多数时候，这归结为微控制器或模块的选择；基于 ATmega 的 Arduino 没有真正的模拟输出，而是依赖于 PWMing 数字信号。基于 Raspberry Pi 的纯数据盒子没有实时 I/O。这就是 PocketBone 的选择显示其优势的地方。PocketBone 使用与 BeagleBone 相同的芯片，随之而来的是可编程实时单元(PRUs)。这使得 Bela 能够通过专用控制器实时处理信号。这正是您想要的音频应用。