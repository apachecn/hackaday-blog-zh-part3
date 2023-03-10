# 低功耗和引脚受限

> 原文：<https://hackaday.com/2015/11/07/low-power-and-pin-constrained/>

我们都经历过。你正在建立一个微控制器项目，你希望你可以只添加“一个更多的功能”，但你受到硬件的限制。是时候开始思考了。(或者，可以说，买下一个型号。)

[Sam Feller]发现自己处于这种境地，他添加了一个旋钮来设置时间，并添加了一个按钮来启动他的模拟电压表时钟的闹钟，他想出了一种方法来[实现通断开关，并只用微控制器的两个引脚](http://blog.awkwardengineer.com/post/132375886222/extremely-low-power-input-sensing)轮询一个按钮和一个电位计。

低功耗设计中电位计的问题在于，它们总是会泄漏功率。也就是说，除非你不用的时候把它们关掉。因此，理想的解决方案是从微控制器上的一个 GPIO 引脚给电位计供电，并用另一个引脚读取其值。这是电位计的两个 GPIO 引脚。但是[Sam]也需要从按钮上读取输入，他没有别针。

 [![Not pressed: pot sees VCC and VCC/2](img/b537e2871c1b8aa82a1deaeb90ac3530.png "tumblr_inline_nx60jsY1zd1qk6hal_500")](https://hackaday.com/2015/11/07/low-power-and-pin-constrained/tumblr_inline_nx60jsy1zd1qk6hal_500/) Not pressed: pot sees VCC and VCC/2 [![Pressed: pot sees VCC/2 and GND](img/1eb6cb86757cb1fcc222db3bbed1e46b.png "tumblr_inline_nx60jtoSIL1qk6hal_500")](https://hackaday.com/2015/11/07/low-power-and-pin-constrained/tumblr_inline_nx60jtosil1qk6hal_500/) Pressed: pot sees VCC/2 and GND

他聪明的解决方案是根据按钮的状态将两个电阻接入或断开电路，这样当开关被按下时，电位计的电压范围在 VCC 和 VCC/2 之间，或者当开关未被按下时，在 VCC/2 和 GND 之间。

如果 ADC 读数高于 VCC/2，则微控制器知道按钮被按下，反之亦然。电位计的设置决定了电压在任一范围内的确切位置。

完了，完了。如果您发现自己处于类似的情况，需要从一整串按钮而不是电位计中读取值，那么您可以尝试使用连接到按钮的 R-2R DAC 来读取(模拟)值，以确定按下了哪些按钮。(如果你眯着眼睛看，这种解决方案与 R-2R DAC 1 相同，只是 R-2R DAC 的最高有效位被电位计取代。)

工具箱的另一个工具。谢谢[山姆]。