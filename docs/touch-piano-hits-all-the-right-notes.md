# 触摸钢琴击中所有正确的音符

> 原文：<https://hackaday.com/2015/12/18/touch-piano-hits-all-the-right-notes/>

我们喜欢好的音乐建筑，这个也不例外。为了他们的 ECE4760 最终项目，【江文典】、【金】和【王麟】建造了[我们很久以来见过的最好看的触摸钢琴](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2015/wj225_hj424_lw569/wj225_hj424_lw569/wj225_hj424_lw569/index.html)。它有五个 4051 多路复用器，从 37 个由铝箔和铜带制成的电容式触摸键接收输入。由于良好的去抖代码，即使键盘支持四音符复调，声音也很干净。

PIC32 和[充电时间测量单元(CTMU)模块](http://people.ece.cornell.edu/land/courses/ece4760/PIC32/index_CTMU.html)产生小而稳定的电流，为按键充电。PIC 持续扫描引脚，等待触摸输入。当检测到人体电容时，使用 ADC 将该值与基本电容进行比较，并使用[卡普勒斯-斯特朗算法](https://ccrma.stanford.edu/~jos/pasp/Karplus_Strong_Algorithm.html)产生声音。

该小组最初的项目计划包括一个 TFT 屏幕来显示五线谱上演奏的音符。虽然那会很棒，但是已经发生了太多的事情，以至于无法准确地捕捉到音符以及它们的持续时间。休息之后来看看。

 [https://www.youtube.com/embed/DLuvaPAe0XE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DLuvaPAe0XE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

