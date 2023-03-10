# PID 控制的木炭烧烤炉——在上面放一个 Arduino！

> 原文：<https://hackaday.com/2017/09/27/pid-controlled-charcoal-bbq-put-an-arduino-on-it/>

在刚刚过去的这个周末密尔沃基的 Maker Faire 上，[地下室技术]展示了他的最新作品，[一个 PID 控制的木炭烤架](https://www.youtube.com/watch?v=zS59ZTs4JmM)。虽然它还没有在真正的食物中测试过，但理论上它确实有效。

PID(一种反馈回路，带有一些奇特的数学运算，用于调整输入，以获得一致的输出)控制烹饪通常用于真空烹饪，在真空烹饪中，人们将水浴加热到受控温度，以烹饪塑料袋中的食物。保持水温相当容易。控制木炭烧烤要困难得多。[地下室技术]通过控制通风和风扇来实现这一点。木炭烧热后盖上盖子，有两种方法可以控制温度；通风以排出热空气，并向煤吹气以使其更热。一个插在烤架上的热电偶传感器给出了内部空气的读数，附近的 Arduino 读取该读数并相应地调整通风口和风扇。

该视频详细介绍了该项目的细节，并描述了他在这个过程中遇到的一些挑战，例如防止电子设备和伺服系统熔化。

 [https://www.youtube.com/embed/zS59ZTs4JmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zS59ZTs4JmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



烧烤季节剩下的时间不多了，所以我们希望[地下室技术]有机会享受他的劳动成果。也许他可以和[杰森]以及他的[PID 控制的肉食熏制者](http://hackaday.com/2016/09/24/see-a-cheap-meat-smoker-get-an-automation-power-up/)交换食物。