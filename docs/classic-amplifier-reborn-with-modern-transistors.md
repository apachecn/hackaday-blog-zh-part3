# 用现代晶体管重生的经典放大器

> 原文：<https://hackaday.com/2016/05/15/classic-amplifier-reborn-with-modern-transistors/>

有人让[兰辛]注意到一个报废的马兰兹放大器，这是一个上世纪 80 年代的相当不错的型号，一个声道完全报废，另一个非常安静。他对修理的描述很简单，但是如果你发现自己的工作台上也有类似的东西，他会给你一些启发。

打开盒子，他看到了 35 年来积累的灰尘。这是打开经典套件令人烦恼的一面，我们都有自己的[尘封的恐怖故事](http://www.theregister.co.uk/2009/11/13/ventblockers/)。他的第一项任务是例行公事:更换所有单元的电容器。自 amp 问世以来，作为欧盟协调的一部分，法国的电源电压已经从 220 伏提高了 10 伏，达到 230 伏，因此他使用了具有适当更高额定值的电容器进行补偿。我们可能会等到其余的放大器被证明是固定的，然后再花钱买帽子，但也许我们更节俭。

静音通道修复原来是来自静音电路，旨在保持放大器在打开阶段安静，并抑制恼人的“砰砰声”。一个坏了的晶体管被替换了，一切正常。不过，死通道中有一大堆死晶体管，这就把问题从修复问题变成了晶体管等效问题。相当一部分 20 世纪 80 年代的零件已经不再可用，所以必须找到现代的替代品。

人们很容易认为所有的小信号晶体管在功能上都是等效的。在逻辑和开关电路中，器件不是开着就是关着，永远不会介于两者之间，但在像 Marantz 这样的音频放大器中，事情就不那么简单了。设计者已经做了大量的工作来计算流经它们的电流的电阻，以提供正确的 DC 偏置点，而不会使电路进入剧烈振荡。该计算的一个重要部分来自相关晶体管的电流增益。[Lansing]必须仔细选择等效晶体管，尽管在某些情况下，他必须做一些创造性的引线弯曲，以适应不同的引脚排列。

因此，所有的死晶体管被替换为适当的等价物，放大器获得了新生。成功，非常值得努力！

我们过去已经讨论过很多放大器。有些已经死了，像这个小放大器和吹电容器，或者这个 T2 冒烟的低音炮。其他的就比较深奥了，像这个[离子风 1KV 电子管创作](http://hackaday.com/2015/11/21/hacklet-85-alternative-audio-amplifiers/)。