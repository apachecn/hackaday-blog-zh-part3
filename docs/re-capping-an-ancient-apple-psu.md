# 给一个古老的苹果 PSU 加盖

> 原文：<https://hackaday.com/2016/04/30/re-capping-an-ancient-apple-psu/>

当你看着一件你可能新买的、仍然认为是相当高科技的硬件时，有时会感到震惊，并意识到它是在 25 岁左右的人出生之前制造的。这是维隆·杰宁斯歌词中的一个瞬间，关于惊奇地看着镜子，头发披在肩上，眼睛里有年龄。是的，那些二十多岁的人甚至从未听说过维隆·杰宁斯。

[史蒂夫]在大混乱 o'Wires 有一个 Mac IIsi 从 20 世纪 90 年代初，不会启动。[他已经在主板上更换了过期的电解电容，所以主要怀疑是电源](http://www.bigmessowires.com/2016/04/21/capacitor-replacement-in-a-vintage-power-supply/)。这个技术奇迹现在已经过去了四分之一世纪，并显示出它的年龄。如果有人想说他们不像以前那样做了，史蒂夫的 PSU 应该会打破这个神话。

写这篇文章的电子工程师很容易想到:那又怎样？只要打开盖子，取出旧的，放入新的，工作就完成了！但也很容易忘记，不是每个人都有相同的经历，如果你不习惯使用线路电源，打开电源 PSU 会有些战战兢兢。[Steve]不熟悉 mains PSUs，曾考虑过将其发送给其他人，但决定他应该能够这样做。

苹果 PSU 是一种开关模式设计。今天无处不在，但在那个年代仍然是一个价格较高的项目，因为你会知道，如果你有一个早期的准将阿米加，其巨大的大 PSU 盒子看起来一样，但重量是后来的兄弟姐妹的十倍。简而言之，电源电压被整流为高压 DC，以高频斩波，然后通过一个小巧轻便的铁氧体磁芯变压器产生较低的电压。这意味着它有相当多的电解电容器，其中一些明显受到热和电压的压力。

同一台 PSU 上的论坛帖子确定了三个替换的候选对象——高压平滑电容器和 PWM 控制板上的几个 SMD 电容器。我们很想说，当你打开它的时候，把它换掉，但是[史蒂夫]已经着手做这三件事了。平滑帽用真空脱焊枪取出，但他对 SMD 帽有一些问题。使用热风枪移除它们，他设法去除了一些其他 SMD 组件，导致需要大量的清理和返工。我们建议下一次放弃气枪，使用一个精细的烙铁依次熔化每个端子，盖子只有两个，应该能够用一对钳子将每个端子分开。

所以到最后，他有了一台可以正常工作的 Mac 电脑和一台 PSU，应该还能再用 20 年。他获得了信心来更新主电源。

如果你想看看主电源的内部，只要你尊重它，你不一定会被它处理电源电压的事实所吓倒。除非是通过隔离变压器，否则不要在打开的情况下给它上电，并且要始终记住，它会产生致命的电压，因此要非常小心，不要在它上电时以任何方式触摸它。如果有疑问，就不要在打开时启动它。如果您担心电容器在关断时仍有高电压，只需用万用表测量这些电压即可。如果有剩余，通过合适的电阻放电，直到无法再测量为止。对于好奇的黑客来说，在开关模式下有很多东西要学。PSU，为什么电子工程师要享受所有的乐趣呢？

这不是我们报道的第一个故事，毫无疑问也不会是最后一个。[浏览我们的概述标签](http://hackaday.com/tag/recapping/)了解更多信息。