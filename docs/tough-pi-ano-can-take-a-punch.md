# 强悍的皮阿诺能承受一拳

> 原文：<https://hackaday.com/2017/09/04/tough-pi-ano-can-take-a-punch/>

对于[24 小时工程师]来说，不会有微妙的独奏。它是为了在音乐治疗中吸收来自攻击性青少年的惩罚，特别是那些自闭症和唐氏综合症患者。坚韧的皮亚诺将被用重型搁板托架栓在墙上，这样它就不会落在任何人身上。键盘被塑料覆盖，它没有任何暴露的金属，所以不会有碎片。

[24 小时工程师]做了一个简短的视频演示，如果你仔细听，他除了一句话外，其他都是双关语。我们喜欢 YouTube 视频中的那种复活节彩蛋。休息之后来看看。

48 键乐器内部有四个树莓 Pi 零点，每个 Pi 控制一个八度音程。冗余确保了硬件故障只丢失一个八度音阶，孩子们可以继续玩，直到替换部件到来。每个 Pi 都有相同的编程，一个指轮开关告诉它将模拟哪个八度音阶。

编程是用 Python 和 Pygame 完成的，所有的输入都运行到一个自制的“帽子”上，在那里焊接电线。Pygame 的唯一职责是监控 GPIO，然后在按钮被按下、拍打、击打或坐在上面时播放适当的音符。

名称相似的是，[触摸钢琴](http://hackaday.com/2015/12/18/touch-piano-hits-all-the-right-notes/)没有活动部件，或者也许你更愿意在[立式钢琴](http://hackaday.com/2015/09/06/its-an-upright-piano-its-a-looper-its-a-pi-project/)中使用树莓皮。

 [https://www.youtube.com/embed/osa0Yo6ODDY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/osa0Yo6ODDY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

