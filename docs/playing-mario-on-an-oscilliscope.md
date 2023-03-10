# 在示波器上播放马里奥

> 原文：<https://hackaday.com/2017/09/23/playing-mario-on-an-oscilliscope/>

任何显示器都可以连接到微控制器，并作为显示器使用，如果你知道要使用的协议，并有足够的电力在你的微控制器。有时，使用一个奇怪的显示器只是“因为它在那里”Reddit 用户[phckopper]似乎就是这种情况，他使用 STM32 和 PS2 操纵杆在示波器上玩了一个版本的马里奥游戏。

没有太多的技术细节，但[PHC copper]让我们知道渲染是使用 STM 上的 SPI 完成的，通过 DMA 传输，与馈入示波器 X 轴和 Y 轴的两个锯齿波同步。控制点亮度的 Z 轴由 MOSI 提供。通过使示波器的范围遍及整个屏幕，类似于 CRT 的电子枪所做的那样，[]能够绘制精灵，而不是矢量图形。显示器的分辨率为 400×400，每个子画面为 16×16。输入来自连接到[PHC copper]电脑的 PS2 操纵杆，信息通过 UART 使用简单协议进行通信。

休息之后，我们在视频中看不到太多的比赛，但这仍然是一项令人印象深刻的工作，尤其是当你意识到[phckopper]在他 16 岁时就做了这个项目！在 Hackaday 还有几个其他的示波器项目，像[这个](https://hackaday.com/2017/03/31/jaw-dropping-ic-free-pong-on-an-oscilloscope/)，一个在示波器上播放的 pong 的伟大版本，或者[这个](https://hackaday.com/2016/05/02/amazing-oscilloscope-graphics/)，展示了一些伟大的图形。

 [https://www.youtube.com/embed/n0j8Q-DUvt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n0j8Q-DUvt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [Reddit](https://www.reddit.com/r/electronics/comments/706dew/i_made_a_mario_clone_run_in_an_oscilloscope_using/?st=j7mg19aq&sh=18712b3b)