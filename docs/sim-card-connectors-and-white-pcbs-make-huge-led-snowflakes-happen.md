# SIM 卡连接器和白色印刷电路板使巨大的 LED 雪花发生

> 原文：<https://hackaday.com/2016/09/28/sim-card-connectors-and-white-pcbs-make-huge-led-snowflakes-happen/>

【Mike Harrison】讲述了[设计和建造一个巨大规模的 LED 照明装置](https://www.youtube.com/watch?v=ojfXOPazrKA)，其中 PCB 被用作电气和机械元件，并在[电磁场 2016](https://www.emfcamp.org/line-up/2016/306-using-printed-circuit-boards-to-make-snowflakes) 上展示。该项目涉及 84，000 个 RGBW LEDs、14，000 个微控制器和 25，000 个 PCB。与小型工作相比，它需要解决一些不同的问题，但是[Mike]分享的技术同样适用于较小规模的项目或应用。他详细介绍了制造和装配设计、零件采购和现场组装。

[![](img/ea7516675deebef0f3e8b44418ae9ff8.png)](https://hackaday.com/wp-content/uploads/2016/09/snowflake-tree-pattern-square_thumbnail.png) 这个装置本身是 2015 年圣诞季香港一家高端商场的雪花展示。[Mike]想要少量的模块板，可以在现场连接在一起，组成正确的形状。为了尽量减少制造和所需零件的种类，他最终使用模块化白色印刷电路板作为结构元件和电气元件。除了一些像钢丝支架这样的小硬件之外，巨大雪花的任何部分都不需要通常 PCB 制造工艺之外的任何东西来制造。供应商越少，潜在的问题就越少。[迈克]在视频中的 [6:28](https://youtu.be/ojfXOPazrKA?t=385) 进入设计细节。

对于电路板之间的连接，他最终使用了手机专用的 SIM 卡连接器。一些测试选择了与用作垫片的 1.6 毫米 PCB 厚度匹配良好的连接器。其中大约有 28，000 个被使用，在 2015 年的一段时间里，很难找到那个特定的部分，因为他们已经把所有人都清空了！

[![](img/ec438fa06d9ee3e0d70102d5d8c7078e.png)](https://hackaday.com/wp-content/uploads/2016/09/snowflake-pattern.png)

Basic Snowflake Pattern

[![](img/d9d8a009aa5d8a35ee6c3c7d786bbc1b.png)](https://hackaday.com/wp-content/uploads/2016/09/snowflake-pcbs.png)

A small number of different modular PCBs made up the bulk of the installation. With the exception of some formed steel wire for support, all parts were made using normal PCB manufacturing methods.

[![](img/21fac007b52bc8ac21c1181d4192ee8b.png)](https://hackaday.com/wp-content/uploads/2016/09/snowflake-connections.png)

In between each of the visible rivets is a SIM card connector taking care of the contacts between boards.

视频进行到一半时([10:55](https://youtu.be/ojfXOPazrKA?t=657))【Mike】开始讲述微控制器和固件的细节。事实证明，PIC12F1501 非常适合，原因包括成本、宽工作电压范围、红、绿、蓝和白各 10 位 PWM，以及在工厂让微芯片编程固件的低成本。选择 RGBW LEDs 有许多原因，但主要是因为产生的白光在大型显示器上更具视觉一致性(与点亮每个 RGB 元素以产生白光相比)。)他确保如果需要的话，很容易对所有单元的固件进行重新编程，因为一次更新数千个微控制器是不可行的。

演示的视频嵌入在下面，但是如果您想直接观看完成安装的一些视频，它从 [21:38](https://youtu.be/ojfXOPazrKA?t=1298) 开始。

 [https://www.youtube.com/embed/ojfXOPazrKA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ojfXOPazrKA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



使用 PCB 材料作为结构元件有很大的潜力。我们已经在这个[聪明的微型 7 段显示器](http://hackaday.com/2016/08/23/charliplexed-7-segment-display-takes-advantage-of-pcb-manufacturers/)中看到了它，最近在 [PocketNC 的 FR4 机器盾](http://hackaday.com/2016/06/04/fr4-machine-shield-is-a-cnc-milling-machine-from-fr4-pcb/)中也看到了它。如果你有兴趣亲自尝试，你可以了解到[如何将 FR4 用于外壳](http://hackaday.com/2015/06/03/how-to-build-beautiful-enclosures-from-fr4-aka-pcbs/)的所有细节。