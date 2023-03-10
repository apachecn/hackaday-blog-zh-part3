# Pi 在 1.5 GHz 保持冷却

> 原文：<https://hackaday.com/2016/12/20/pi-zero-keeps-cool-at-1-5-ghz/>

从台式电脑到 Arduinos，黑客超频 CPU 的历史由来已久。[Jacken]想要为他的基于树莓 Pi 的媒体中心增加一点活力，所以他自然想提高时钟频率。和大多数超频一样，最大的限制是你能从芯片上释放多少热量。

[Jacken]移除了正常的散热器，并用廉价的铜垫片、导热化合物和强力胶为[建造了一个新的](http://www.jackenhack.com/raspberry-pi-3-overclocking-heatsink-cheap/)。结果不是很漂亮，但它确实让他在 1.5 GHz 可靠地运行~~零~~ Pi。散热器非常低调，不会妨碍将其他东西插入主板。当然，您的结果可能在时钟频率和稳定性上有所不同。

错开垫片以提供更多的暴露表面。虽然铜是良好的热导体，但使用多块铜可能会削弱这一优势。另一方面，在零件之间使用热化合物应该会减少垫片之间的微间隙，这样会有所帮助。

除了超频之外，[Jacken]在所有内核都处于活动状态的情况下进行了一些功耗测量，得出了一个令人惊讶的低功耗(远低于 1A)。不过，这只是一个例子，所以如果有关系的话，你应该自己测量一下

这不是我们看到的第一个[【Jacken】超频](http://hackaday.com/2016/03/03/overclocking-the-raspberry-pi-3-for-tasty-speed-increases/)，但新的方面是低姿态散热器。如果你只是为了运动，你甚至可以超频一台 [Arduino](http://hackaday.com/2015/08/04/clocking-or-overclocking-an-avr/) 。你可以运行在 65 兆赫，只要你不介意供应液氮。