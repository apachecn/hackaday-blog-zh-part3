# 这台自动售货机里没有微控制器。

> 原文：<https://hackaday.com/2018/06/09/no-microcontroller-in-this-vending-machine-doh/>

你可能认为需要一个微控制器来处理自动售货机的逻辑。首先，只有正确的变更应该激活它们，错误的变更应该被返回。如果检测到正确的变化，那么按下按钮应该将正确的食物输送到分配器。但是如果你喜欢拼图，你可以试着想一个不用微控制器的方法。毕竟，整个电路可以被认为是几个马达、一个电源和一组开关，包括大小合适的硬币。

这就是[小海雀]接近甜甜圈自动售货机的方式。真正有趣的是观看下面的视频，并想知道当你看到每个部分被放置到位时，逻辑将如何组合在一起。例如，直到快结束时，你才看到作为电路一部分的硬币是如何从电路中取出来用于下一次购买的(我们不会破坏它)。太小的硬币会被迅速退还给顾客。为了处理尺寸合适但太重的硬币，一种改进方法是让它们通过弹簧调节的活板门落下，然后被退回。我们不确定如何处理大小合适但太轻的硬币。

我们真的很喜欢这些低技术含量的黑客，他们做着看似高科技的事情。看看这个型号为的机电喷气发动机，它有一个聪明的开关机制，会让你挠头。或者，如果你渴望更多的自动售货机食品，请尽情享受 [Venduino，这是](https://hackaday.com/2016/07/02/venduino-serves-snacks-shows-vending-is-tricky-business/)的下一步，它配备了一个 Arduino，一个 LCD 屏幕，内部被点亮，并配备了一个激光切割的桦木胶合板外壳。

 [https://www.youtube.com/embed/q55TLdKc68w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q55TLdKc68w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

