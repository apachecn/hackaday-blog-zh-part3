# 对焊接站的温度控制进行改进

> 原文：<https://hackaday.com/2018/04/07/retrofit-temperature-control-to-a-soldering-station/>

我们可能都见过广告上宣传的廉价 USB 烙铁，并认为它们不一定是最有用的工具。其中最便宜的没有任何真正的温度调节。[Paulo Bruckmann]进来了，他用 Kapton 胶带将一个热敏电阻连接到他的熨斗上，添加了一个带有旋转编码器和诺基亚 LCD 的 Arduino Uno 克隆，并将结果放入一个 3D 打印的盒子中，用于一个小型低功率温控焊接站。声称的成本只有 10 美元，鉴于 Arduino 克隆的低价，这似乎是可信的。

[软件](https://github.com/peekpt/MicroSolderingStation)提供了预期的 PID 控制，由于吸头的尺寸很小，具有非常快速预热的优点。电源是 9 V 而不是 USB 5 V，因此这种组合使熨斗能够在比未经修改时大得多的关节上工作。因此，他似乎已经从这个毫无希望的开始创造了一个似乎更有能力的铁，这让我们印象深刻。看看他在休息时间下面的视频。

我们去年回顾了其中一个小熨斗，[发现它是一个玩具，而不是一个笑话](https://hackaday.com/2017/08/31/review-aneng-lt-001-usb-soldering-iron/)。与此同时，我们也看到了一些[为他们设计的其他模型](https://hackaday.com/2017/12/04/upgrading-a-usb-soldering-iron/)，包括[一把脱焊镊子](https://hackaday.com/2016/12/07/turn-cheap-usb-soldering-irons-in-to-tweezers/)。

 [https://www.youtube.com/embed/iJwf-qWp4lI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iJwf-qWp4lI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

