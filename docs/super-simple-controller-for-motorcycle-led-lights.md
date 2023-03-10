# 摩托车 LED 灯超级简易控制器

> 原文：<https://hackaday.com/2017/09/09/super-simple-controller-for-motorcycle-led-lights/>

对于汽车，尤其是摩托车，增强前灯的辅助照明可能非常有用，尤其是当你需要驾驶/骑行通过雾天、光线差或无光的道路和泥路时。大多数车辆上的初级照明仍然依赖效率非常低的钨丝灯。廉价、高效的 LED 模块有助于为车辆增加额外的照明，而不会增加电力供应的负担。如果你想增加亮度控制，你需要购买一个调光模块，或者自己动手。[路径]从 WhiskeyTangoHotel 选择后一条路线，并为他的 KLR650 自行车建造了一个超级简单的 LED 控制器。

[![](img/8e7edd6193a56b74c5a3cb2487b271a5.png)](http://hackaday.com/?attachment_id=272194) 他选择了一个常见的 18 W 灯条模块，内含 6 个 3 W 的发光二极管。然后，他决定制造一种基于微控制器的调光器，提供 33%、50%和 100%的亮度。由于更多的代码不会给他带来任何额外的成本，他增加了呼吸和闪光模式。硬件尽可能精简，包括 Arduino Nano、线性稳压器、功率 MOSFET 和控制开关，以及一些分立元件。安装在车把上的控制开关是一个普通的摩托车附件，它有两个按钮(喇叭、前灯)和一个滑动开关(转向指示灯)。一个在按钮上的各种亮度模式中循环，而滑动开关激活频闪功能。状态指示灯 LED 与 Nano 相连，安装在车把控制开关上。它提供编码闪烁来指示选择的模式。

遗憾的是，“呼吸”效果受到专利保护，至少在未来几年内是如此，所以如果你打算在路上使用这种模式，请小心。还有闪光灯模式——请不要用它——永远不要用。有可能引发癫痫发作，这对所有相关人员都不好。除非你遇到了可怕的紧急情况，需要引起别人的注意来寻求帮助。

 [https://www.youtube.com/embed/TcvZu41Uejo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TcvZu41Uejo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

