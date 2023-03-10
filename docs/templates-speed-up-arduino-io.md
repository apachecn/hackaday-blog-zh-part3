# 模板加速 Arduino I/O

> 原文：<https://hackaday.com/2017/05/11/templates-speed-up-arduino-io/>

这很容易忘记，但是 Arduino 确实使用 C++。通常，C++部分在库和框架中，大多数人倾向于用 C 风格编写他们的主程序，只使用库对象，如 C 语言扩展。[Fredllll]最近创建了[一个模板库](https://github.com/fredlllll/FredUtil-Arduino/blob/master/fredOptimization.h)来加速 Arduino I/O，他在 GitHub 上分享了它。

如果你曾经使用 Arduino 做过任何严肃的事情，你可能知道虽然 digitalWrite 很方便，但它在后台做了很多工作来确保 pin 被设置，这增加了每个调用的开销。[Fredllll 的]模板版本可以在两个周期内切换引脚的状态。如果您不介意干扰同一端口上其他引脚的状态，您可以将其减半。

你可以用一个常量来打开一个管脚，就像这样:

```
switchOn<1>();
```

如果你不喜欢使用幻数(这很聪明)，你可以定义一个常数:

```
const uint8_t ledPin=1;
switchOn<ledPin>();
```

因为你可能想做一些花哨的计时，也有一个 nop 模板，让你延迟一定数量的周期。这里有一些来自 Reddit 的测试代码，可以产生 1.3 MHz 的方波，例如:

```
const uint8_t myPin = 5;
void loop(){
 cli(); //disable interrupts as they would screw up the timing
 do {
    switchOnExclusive<myPin>(); // 1 cycle
    nop<5>(); // 5 cycles
    switchOffPortOfPin<myPin>(); // 1 cycle
    nop<3>(); // 3 cycles
 } while(1) //jump back to do is 2 cycles
}
```

显然，这也不是最大值，因为环路中有八个延迟周期。

使用这个库你不需要知道太多关于模板的知识，但是如果你想知道更多，我们已经在过去的中讨论过了。我们之前已经注意到 [digitalWrite 比直接端口访问大约慢 50 倍](https://hackaday.com/2010/01/06/arduino-io-speed-breakdown/)，其他 I/O 操作也好不到哪里去。探索模板是否能使其他操作更有效将是很有趣的。