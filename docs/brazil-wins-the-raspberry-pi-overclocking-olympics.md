# 巴西赢得树莓 Pi 超频奥运会

> 原文：<https://hackaday.com/2017/04/18/brazil-wins-the-raspberry-pi-overclocking-olympics/>

[Alex Rissato] [自豪地报告，他现在保持着 HWBOT](http://blog.everpi.net/2017/04/raspberry-pi-zero-overlock-extremo-1600mhz.html) ( [机器翻译](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=http%3A%2F%2Fblog.everpi.net%2F2017%2F04%2Fraspberry-pi-zero-overlock-extremo-1600mhz.html&edit-text=))的最高基准分数记录；他认为这不仅是个人的成就，更是令人钦佩的民族自豪感。超频一个 Raspberry Pi 并不像实现最高运行时钟速率那么简单。一条记录由 CPU 时钟、内存时钟、GPU 时钟和 CPU 内核电压的正确组合构成。如果你能做出这种特殊的酱料，这种混合物必须得到令人满意的冷却，最重要的是足够稳定，能够通过实际的性能基准测试。

![](img/518f14e73431518b944e64623800e2a2.png)

More POWAAA to the CPU!

[Alex]意识到实现所需 CPU 时钟的主要障碍是内部产生的 CPU 内核电压，因此受到限制；这是外部 LC 过滤，并路由回中央处理器的股票 Pi。[Alex]拆除 PCB 上的滤波器，为 CPU 提供外部产生的核心电压。

下一步，冷却必须被注意。空气冷却根本不能解决这个问题，所以必须设计一个基于 Peltier 的散热器接口，将热端浸入一桶盐水中。所有这些都转化为时钟速度为 1600 MHz 的 comfy 16C。

所有的努力都是合理的吗？我们当然认为是！尽管没有达到 Pi 零 CPU 时钟频率的记录，目前设定为 1620MHz，但[Alex]在[HW bot Prime 超频基准测试](http://hwbot.org/benchmark/hwbot_prime/rankings?hardwareTypeId=processor_2823&cores=1#start=0#interval=20)中赢得了第一名。巴西现在当然可以把这个加入它的奖杯陈列柜，可以说超过了 129 枚奥运奖牌。