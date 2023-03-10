# 安静空间的互动植物灯

> 原文：<https://hackaday.com/2018/03/14/interactive-plant-lamps-for-quiet-spaces/>

如果你在图书馆呆过很长时间，你可能会注意到它们吸引了那些想要或需要独处而不被孤立的人。在这个空间里，形成了一种无声的共同体。这一现象是建立一个相互连接的室内植物网络的灵感[MoonAnchor23],这是一门关于物理互动和实现的课程所需要的。但是你不会发现这些植物在推特上释放他们的干巴巴的智慧。他们只和彼此以及附近的人说话。

在这个项目中，没有活的植物受到伤害——无论如何，树叶可能不会让太多的光通过。这些植物都配备了一条可寻址的 RGB LEDs 和一个由 Arduino Uno 控制的柔性传感器。两者都被热粘在叶子的下面，并用绿色胶带隐藏起来。默认情况下，植物被设置为提供环境光。但是，如果有人用弯曲传感器抚摸叶子，它会向另一株植物发送秘密信息，诱导光模式。

现在，这些植物在本地电脑上使用 OpenFrameworks 服务器通过蓝牙进行通信。最终，该计划是使用主从配置，这样工厂可以相距更远。点击鼠标按钮，休息后观看简短演示视频。[MoonAnchor23]还使用[DIY Perks]的结构焊接方法，用硅胶和保鲜膜制作了 LED 蘑菇簇，这也是在休息之后。它们的工作原理类似，但使用力感测电阻，而不是弯曲感测电阻。

将几家工厂联网可能会很快变得昂贵，但 DIY 柔性传感器将有助于降低 BOM 成本。

 [https://www.youtube.com/embed/LcF-5bZ3rXw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LcF-5bZ3rXw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/D5LjGFkpApw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/D5LjGFkpApw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

