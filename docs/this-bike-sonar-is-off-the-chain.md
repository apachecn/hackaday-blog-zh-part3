# 这个自行车声纳坏了

> 原文：<https://hackaday.com/2017/01/11/this-bike-sonar-is-off-the-chain/>

理论上，骑自行车是一种很好的交通方式。不仅有一些明显的健康益处，对环境的影响也比任何不是由人类直接驱动的东西要小得多。但让我们面对现实:骑自行车在实践中可能会相当可怕，尤其是在与汽车和卡车相同的道路上。如果后脑勺没有一双眼睛，就很难分析出背后可能隐现的威胁。

![radar-sweep-display](img/7237f38817e963169cdf0305e1d14627.png)【Claire Chen】和【赵又廷】提出了下一个最好的东西——[自行车声纳](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/clc288_yz424/clc288_yz424/clc288_yz424/index.html)。这是一个由两部分组成的系统，它从超声波测距仪获取信息，并使用它在骑手的耳朵中创建声音定位脉冲。测距仪附在安装在座位杆上的伺服系统上。它来回扫描以探测 4 米内的物体，这些信息通过 PIC32 在 TFT 屏幕上显示为雷达扫描式的图形。

虽然图形显示看起来很棒，但它的反馈很慢，而且一直往下看有点危险——音频反馈是迄今为止最有用的。自行车侧电路以 2.4GHz 的频率向安装在头盔上的另一个 PIC 发送角度和距离数据。这张图片使用声音定位来创建一个与你尾巴上的任何东西的距离和位置相匹配的 ping 噪音。ping 音量是相对于物体的距离而言的，你只要把耳机插到音频插孔就能听到。兔子跳过休息时间去看看。

 [https://www.youtube.com/embed/lE78EBFh9pA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lE78EBFh9pA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示，[布鲁斯土地]！