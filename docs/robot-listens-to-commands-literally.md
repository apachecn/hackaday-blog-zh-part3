# 机器人听命令——真的

> 原文：<https://hackaday.com/2015/12/10/robot-listens-to-commands-literally/>

你可能会看到一个罐子，[亚当·库姆普夫]看到一个机器人。[亚当的]机器人(名为[Canny])不会四处走动，但它确实有富有表情的眉毛、五彩缤纷的眼睛和一张说话的嘴。然而，[有趣的是，它通过佩戴的耳机](http://research.kumpf.cc/2015-ProgrammingWithHeadphones/)接收音频命令。你可以在下面的视频中看到[Canny]的行动。

耳机使用 AFSK(音频频移键控)将音频音调耦合到[Canny's]麦克风。[Canny]使用运算放大器提高麦克风电平，然后使用 567 PLL IC 解码音频音调。[Adam]为标记和间隔选择了两个巧妙的频率(12345 Hz 和 9876 Hz)。除了在数字上具有娱乐性之外，这些频率相距很远，很容易被检测到，通过耳机没有问题，并且没有谐波相关。

567 IC 只能检测其中一种音调。忽略一个音调并不总是很好地抑制噪声，但对于这种用途来说应该绰绰有余，并减少了器件数量。为了避免错误的命令，数据包含标记、长度和校验和。567 为 Arduino 供电，Arduino 处理所有的机器人控制。

你如何创造声音传到耳机里？你用一个[网页](http://research.kumpf.cc/2015-ProgrammingWithHeadphones/audioserial/)。当然，您也可以用其他方式生成低波特率音调。AFSK 调制解调器在业余无线电圈很常见，当然也有[大量的调制解调器设计](http://hackaday.com/2014/05/15/micromodem-for-data-transmission-explorations/)。此外，这种电路的简单性也有令人满意的地方。[Canny]的吸引力也不会伤害任何人。

 [https://www.youtube.com/embed/780A0cv1qgA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/780A0cv1qgA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

