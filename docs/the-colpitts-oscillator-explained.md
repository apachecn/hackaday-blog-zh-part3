# 科尔皮兹振荡器解释说

> 原文：<https://hackaday.com/2018/06/18/the-colpitts-oscillator-explained/>

Colpitts 振荡器是经过时间考验的设计，始于 1918 年。[The Offset Volt]有几个视频涵盖了这些电路的设计，包括一个运算放大器和一个晶体管版本。你可以找到下面的视频。

你可以通过反馈电路中的两个电容来辨别科尔皮兹振荡器。这些电容构成了电路的有效电容(假设你有 C1 和 C2)，它是 C1 和 C2 的乘积除以这两个电容之和。有效电容和电感构成一个带通滤波器，在目标频率下非常尖锐，允许放大器在该频率下建立振荡。

展示运算放大器振荡器并不常见，思考视频中讨论的设计变化和限制也很有趣。这个视频不仅仅是理论上的。他还建立了电路，并期待在现实世界的表现。

观察运算放大器和双极性电路之间的差异也很有趣。当然，您也可以使用 FET 等其他有源器件。当晶体代替电感作为反馈电路的一部分时，这也是一个重要的电路。

我们看到很多这样的低功率无线电发射机。如果你想看不同的振荡器设计，我们之前讨论过 [Pierce 振荡器](https://hackaday.com/2016/03/22/oscillator-design-by-simulation/)。

 [https://www.youtube.com/embed/3c5u_HRp8m8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3c5u_HRp8m8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/BXcJxeEQo-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BXcJxeEQo-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

