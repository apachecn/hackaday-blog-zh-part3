# 简化基本 LED 效果

> 原文：<https://hackaday.com/2018/06/13/simplifying-basic-led-effects/>

曾经有一段时间，在一个项目上有一个闪烁的蓝色 LED 是你成为一个酷孩子所需要的一切。但是现在你需要更复杂的东西。发光二极管不应该只是亮着，它们应该淡入淡出。还有眨眼？今天的热点是呼吸发光二极管。如果这是你想要的那种项目，你应该去看看[jandelgado 的] [jled 库](https://github.com/jandelgado/jled)。

乍一看，一个用于 LED 控制的 Arduino 库似乎是多余的，但是如果你对漂亮的效果感兴趣，为它们编码可能会有点麻烦。如果你不介意在让一个 LED 变亮(或变暗)时停止一切，那么当然，你只需要写一个循环，它只有几行代码。但是如果你想在其他事情继续执行的时候让它发生，那就有点不同了。这个库使它变得非常简单，而且文档也很好。

显然，要创建一个特效 LED，需要创建一个 JLed 对象。然后，您可以在该对象上使用修改器方法来获得某些效果。唯一的开销是您需要定期调用 LED 上的 update 方法。这是项目中的一个例子:

```
#include <jled.h>

// connect LED to pin 13 (PWM capable). LED will breathe with period of
// 2000ms and a delay of 1000ms after each period.
JLed led = JLed(13).Breathe(2000).DelayAfter(1000).Forever();

void setup() { }

void loop() {
   led.Update();
}
```

相当容易和可读。请记住，有些 Arduinos 不能在引脚 13 上进行 PWM，因此您可能需要进行调整。我们唯一的抱怨是你必须更新每个 LED。如果 JLed 构造函数保存一个所有 Led 对象的链表就好了，这样您就可以拥有一个类方法，通过一次调用就可以更新所有这些对象。在示例中，作者将所有 led[保持在一个阵列](https://github.com/jandelgado/jled/blob/master/examples/multiled/multiled.ino)中，并逐步通过该阵列。然而，这将很容易分叉和添加。哦，等等，[我们是为你做的](https://github.com/wd5gnr/jled)。该库确实做了很多工作，例如，利用 ESP8266 提供的更高 PWM 分辨率。

该库可以打开或关闭 LED(包括延迟)，使 LED 永久闪烁或呼吸一定次数，或者使 LED 渐亮或渐暗。除了预设，如果你想做一些自定义的模式，你可以提供自己的亮度功能。您可以通过指定之前或之后的延迟、重复计数(可以是永远)来修改大多数操作，您还可以告诉库您的 LED 是低电平有效的，因此您不必记住翻转代码中的所有内容。

火箭科学？不。但是我们喜欢。阻碍 LED 效果是不好的，这使得花哨的异步 LED 变得简单。为什么不用呢？最新的 ide 可以从管理库对话框安装它，所以只需要一秒钟。

实际上，库是构建简单系统的关键。为什么不站在别人的背上？我们最喜欢的一些处理 [SPI](https://hackaday.com/2014/08/01/arduino-spi-library-gains-transaction-support/) 和[比例积分微分(PID)控制](https://hackaday.com/2011/07/21/demystifying-pid-control-with-a-look-at-the-new-arduino-pid-library/)。