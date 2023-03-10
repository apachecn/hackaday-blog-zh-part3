# 反向散射你自己的调频盗版电台

> 原文：<https://hackaday.com/2017/03/09/backscatter-your-own-fm-pirate-radio-station/>

如果你住在城市里，你会不断地在无线电频率能量的浓汤中游泳。调频广播电台向空中发射数百千瓦的能量。华盛顿大学的学生[安冉·王]和[维克拉姆·伊耶]自问是否能利用这种背景辐射来发射他们自己的调频广播电台，哪怕只是在当地。[的回答是惊人的肯定](http://smartcities.cs.washington.edu/)。

下面嵌入的预告片视频展示了几个潜在的应用，但是[论文](http://smartcities.cs.washington.edu/fmbackscatter.pdf) (PDF)为感兴趣的人提供了更多细节。基本上，他们在选定的频率上打开和关闭吸收天线，以便将强调频信号调制到另一个相邻频道。对这种反向散射载波频率进行频率调制会将音频(或数据)添加到产品站。

他们用这个系统实现的一个更酷的技巧是将第二个(立体声)通道注入单声道调频电台。由于调频广播是作为单声道信号广播的，左减右信号在旁边发送，他们可以通过重新创建立体声导频载波，然后添加自己的差频通道来制作双通道立体声电台。相当狡猾。当然，他们也可以使用这种技术发送数据。

为什么要这么做？使用反向散射的小型无线电台不必将其功率预算花费在载波上。取而代之的是，这种设备可以在微瓦下工作。当然，它在任何给定的方向上只有几英尺，但该电台向现有的调频收音机广播，而不需要购买 RFID 阅读器或类似的设备。这是一个伟大的黑客技术，它以两种方式利用现有的基础设施。如果这看起来有点熟悉，这里有一个来自同一个实验室的类似想法，它正在实现[本质上与室内 WiFi 信号](http://hackaday.com/2016/02/26/passive-wifi-on-microwatts/)相同的技巧。

那么谁想要本地的反射式盗版电台呢？

 [https://www.youtube.com/embed/Aj056yXtq7g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Aj056yXtq7g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



由于