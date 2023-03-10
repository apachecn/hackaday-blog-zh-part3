# 升压转换器背后的科学

> 原文：<https://hackaday.com/2017/05/05/the-science-behind-boost-converters/>

【Ludic Science】向我们展示了隐藏在[不起眼的升压转换器](https://www.youtube.com/watch?v=FRG01YOEQGY)背后的基本原理。我们都认为它们是理所当然的，尤其是当你可以[自己制作升压转换器](http://hackaday.com/2016/11/22/a-buck-boost-converter-from-the-ground-up/)或者只花几美元买一个的时候，但是有时候回归基础并准确理解事情是如何工作的也是很好的。

对于升压转换器来说，这个问题中的电路可能非常简单，并不是一个真正实用的设计。然而，它有助于直观地了解正在发生的事情，以及升压转换器是如何工作的，只需要几个零件，一个螺钉，漆包线，二极管，电容器和一个安装在电路板上的按钮。

视频继续向我们展示升压转换器背后的科学，从添加电池开始，电感器以电磁场的形式存储电荷。当释放按钮时，磁场消失，这在电路中产生电压，然后通过二极管馈入，给电容器充电一点点。如果你足够快地拨动开关，电容器将继续充电，其电压将开始上升。这将在输出端产生比输入电压更大的电压，具体取决于电感值。如果你要在现实生活中使用这种设计，你当然会使用晶体管而不是按钮来进行切换，这样更快，而且你不会感到手指疼痛。

这是非常基本的东西，但视频为我们提供了电路中发生的事情及其原因的精彩解释。如果你喜欢这篇文章，我们相信你会喜欢 Hackaday 自己的[Jenny List]解释你需要知道的关于电感的一切。

(感谢[Unferium]的更新——我犯了一个错误，当按钮被按下时磁场会崩溃，而实际上这是在按钮被释放时发生的。抱歉造成混乱。)

 [https://www.youtube.com/embed/FRG01YOEQGY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FRG01YOEQGY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

