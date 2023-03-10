# 用 FPGA 进行相位调制

> 原文：<https://hackaday.com/2017/05/06/phase-modulation-with-an-fpga/>

每个人都应该知道两种无线电调制方案。调幅改变了载波频率的振幅——或者你可以称之为“音量”——并将所有的广播变成由教堂拥有和运营的频道。频率调制改变载波频率的音调，并且完全由纯信道运行。业余无线电操作员熟悉几十种其他调制方案，但有一种几乎无人问津。相位调制很奇怪，几乎闻所未闻，但这并不意味着您不能在 FPGA 上实现它。[ nckm]在 FPGA 上使用[相位调制传输音频(俄语，这里是](https://marsohod.org/projects/proekty-dlya-platy-marsokhod3/349-pm-radio-transmitter) [Google Translatrix](https://translate.google.com/translate?sl=ru&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https%3A%2F%2Fmarsohod.org%2Fprojects%2Fproekty-dlya-platy-marsokhod3%2F349-pm-radio-transmitter&edit-text=) )。

这个硬件只是一个 Altera MAX10 板，具有一个用于要传输的音频串行数据的输入，以及两个输出，每个输出连接到四分之一波长天线的几个比特的导线。不，除了几根电线之外，没有输出滤波器或其他任何东西。这是个实验，冷静点。

该项目的 Verilog 接收单声道、22050 BPS、8 位无符号样本的串行数据形式的音频信号。这些样本馈入 FPGA 中具有相移的动态 PLL。移动相位也会改变频率，所以[nckm]可以用他手机上的调频发射机接收这个音频信号。

如果是调频收音机接收，这真的是相位调制吗？呃，也许吧。PM 和 FM 是密切相关的，但是作为调制方案，它们本身是有区别的。你可以在 gits 上获取[nckm]的代码[，或者查看下面的视频演示。](https://github.com/marsohod4you/Fpga-PM-Radio)

 [https://www.youtube.com/embed/2iFfx41gSww?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2iFfx41gSww?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

