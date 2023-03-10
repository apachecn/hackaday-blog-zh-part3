# ESP8266 作为磁带机

> 原文：<https://hackaday.com/2017/11/03/esp8622-as-a-tape-drive/>

1976 年发布了 Apple I，这是基于 MOS 6502 芯片的几款电脑之一。MOS 自己发布 KIM-1(键盘输入显示器)最初是为了展示芯片的威力。单板计算机上有两个连接器，其中一个可用于磁带录音机的长期存储。当[Willem Aandewiel]2016 年去荷兰苹果博物馆时，他看到了一个，并对自己的青春感到怀旧。他能够得到一个复制品，microKIM，并建造它，但他想使用新技术与旧技术相结合，所以他决定使用 ESP8266 作为固态磁带录音机。

KIM-1 发布时如此受欢迎的原因之一是有大量可用的文档。[Willem]利用这份文件找出 KIM-1 如何将数据保存到记录设备中。ATTiny85 用于解码 KIM-1 在保存时发送的脉冲流，因为时间太紧，无法“监听”和解码这些位，也无法转换和存储它们。为了加载程序，数据可以以 1 和 0 的数字形式发送到 KIM-1。这意味着 ATTiny 仅用于解码，而不必重新编码数据。正因为如此，保存很慢，但加载非常快。

为了完成这个项目，[Willem]添加了四个按钮，分别用于倒带、录制、播放和快进，以及一个屏幕，这样您就可以看到当前选择了哪个节目，并可以从一个节目切换到另一个节目。作为一个很好的回溯触摸，保存时必须同时按下录音和播放。对于更多的 6502 项目，检查这个基于 [6502 的 DIY 计算机](https://hackaday.com/2017/08/21/this-6502-computer-project-is-a-work-of-art/)，或者这个由分立部件组成的 [6502。](https://hackaday.com/2016/05/16/a-dis-integrated-6502/)

 [https://www.youtube.com/embed/R_zD5T_khKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R_zD5T_khKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

