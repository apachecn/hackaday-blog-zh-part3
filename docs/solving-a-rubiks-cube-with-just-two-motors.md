# 只用两个马达解魔方

> 原文：<https://hackaday.com/2017/12/02/solving-a-rubiks-cube-with-just-two-motors/>

我们都看过魔方冠军能在 5 秒内解出谜题的视频。还有扭曲魔方的机器人可以更快地解开魔方，通常不到一秒钟。这个魔方解算器不是那些机器人中的一个，但它仍然很酷。

我们喜欢德克斯特工业公司的“BricKuber”的原因不是因为它的闪电般的速度——它需要一两分钟来解决这个难题。我们喜欢的是操作立方体方法的简单性。BricKuber 由乐高零件制成，包括 Mindstorms 马达和 BrickPi 控制器，仅使用两个马达来工作立方体。一个电机为立方体所在的方形转盘提供动力，而另一个电机为具有双重功能的手臂提供动力——它要么夹紧立方体，使转盘可以旋转一层，要么倾斜立方体，使其在转盘上翻转 90 度。使用 Pi Cam 开销，装备对所有六个面进行成像，计算立方体的解，然后翻转和扭曲立方体来求解。观看起来既令人难以置信，又令人异常放松。

所有代码都是开源的，我们强烈怀疑没有乐高零件也能造出类似的可能更快的机器人。你甚至可以用冰棒棍和 Arduino 做一个。

 [https://www.youtube.com/embed/7QUF8TZSGrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7QUF8TZSGrA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5YNxKrUrdDo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5YNxKrUrdDo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

