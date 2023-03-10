# LAMEBOY 是 ESP8266 上的手持游戏

> 原文：<https://hackaday.com/2017/09/30/lameboy-is-handheld-gaming-on-the-esp8266/>

我们关注[Dave Darko]的 LAMEBOY 项目已经有一段时间了，这是一款与经典任天堂 Game Boy 外形大致相同的手持设备。便携式电子设计变得如此平易近人，这一点非常引人注目，这也正是它的有趣之处。这个设计很漂亮，你看得越仔细，你就越尊重[戴夫]正在做的事情。

[![](img/3a3b93004a6182027036961d57c7f2e2.png)](https://hackaday.io/project/26823-lameboy-another-esp12-handheld/log/66990-a-slightly-redesigned-pcb) 现在他的概念证明有一个 3D 打印的外壳，它的表面是印刷电路板。我们喜欢 PCB 的左下角滑入外壳的口袋中，这样就可以只用一个螺钉将右上侧的两个部分固定在一起。

LAMEBOY 是围绕 ESP8266 模块构建的。任何使用过这款芯片的人都知道，它有相当大的马力，但很少 I/O。[戴夫]有一个 LCD 屏幕，六个用户按钮，一个 USB 转 I/O 芯片和一个 SD 卡插槽。他采取了两种方法来解决这个难题。首先，他获得了一个 PCF8574 端口扩展器，其次，他将屏幕背光的颜色控制卸载到 ATtiny85(运行 BlinkM 克隆)。

下面你可以在 perfboard 原型上看到一些早期游戏测试。我们还没有在最新的原型上看到游戏(在他的最新项目日志中有一个屏幕颜色测试视频),但是听起来似乎[戴夫]计划利用[Gamebuino](http://gamebuino.com/)框架。这应该意味着不会缺少很酷的 rom 来加载。

 [https://www.youtube.com/embed/zHU11TpP5T4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zHU11TpP5T4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

