# 教一个 85 岁的男孩说脏话

> 原文：<https://hackaday.com/2015/10/21/teach-an-attiny-85-to-swear/>

老实说，当我们遇到像 Speak-n-spell 这样的语音合成器时，我们首先做的事情之一就是尝试说脏话。【亚历克·斯梅彻 】将这一点铭记在心，构建了一个由 ATTiny 85 驱动的简单蜂鸣器机制，当你连接它时[会重复发誓](http://cassettepunk.com/blog/2015/07/06/2-7-5-5vdc-fuck/)。这是一个相当简单的项目(或者，正如[Alec]自己所说，这是一个“令人满意的极简构建”)，但它做得相当好。

8 khz 语音样本(取自 Google Translate)存储在代码中，并从一个定时环路写入 ATTiny85 的 PWM 输出之一，直接驱动小扬声器。因此，所有需要的是蜂鸣器的情况下，一个小扬声器，ATTiny85，一个电源和一些电线。这是极简设计的一个很好的例子:ATTiny85 几乎可以直接驱动扬声器，并且可以直接用电池运行，不需要电源控制器。有时候保持事情简单是值得的，尤其是在说脏话的时候。

感谢[ 皮乌金斯 阿森尼斯】的提示！更新:帖子于 10 月 21 日更改，以澄清提交者和作者。

 [https://www.youtube.com/embed/a97pWOZQKTs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a97pWOZQKTs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

