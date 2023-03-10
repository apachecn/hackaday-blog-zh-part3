# 弹簧针让物联网开关轻松工作

> 原文：<https://hackaday.com/2017/12/09/pogo-pins-make-light-work-of-iot-switches/>

住在公寓里，新鲜光线布线的机会不足给[Raphael Luckom]带来了一个问题，他通过使用一些现成的基于 ESP8266 的物联网电源开关解决了这个问题。如今，这本身并不是什么特别新的东西，但让他的开关特别的是，当面临复杂的焊接来重新编程时，他[制造了一个弹簧针夹具来制作所需的触点](https://rluckom.github.io/esp-programmer/posts/reprogramming-wifi-switch/)。

他的工作灵感来自于一个黑客日 io 项目，这个项目攻击了一些中国的交换式插座。它们包含一个标准的 ESP-12 模块，因此识别正确的引脚对其进行编程非常容易。他只需要用他的 3D 打印机为他的弹簧针制作一个夹具。当然，“简单地”不是一个合适的词，因为一路上他不得不通过多次重复印刷，但最终他用夹子将夹具固定在板上。

结果是:一个成功的继电器，没有棘手的焊接。我们知道，我们的许多读者对一点焊料没有问题，但对于那些没有问题的人来说，这里可能会有一点兴趣。

多年来，我们已经向您展示了许多 ESP8266 开关。这个[多合一插座系统](https://hackaday.com/2016/09/20/an-esp8266-in-every-light-switch-and-outlet/)相当聪明，但是我们也有[一些简单的开关](https://hackaday.com/2015/04/19/switch-mains-power-with-an-esp8266/)。