# RPiTX 将 Rasberry Pi 变成多功能无线电发射机

> 原文：<https://hackaday.com/2015/11/04/rpitx-turns-rasberry-pi-into-versatile-radio-transmitter/>

自从发现一些 USB 电视调谐器加密狗可以用来监控大量频谱的无线电波以来，软件定义的无线电世界已经引起了人们的兴趣。然而，一个限制因素是软件狗只能接收信号；他们不能传送它们。【Evariste Okcestbon，F5OEO】(如果那是他的真名！Ok c ' est bon = Ok this good)编写了一些软件，可以让你[只用一个树莓 Pi 和一根线](http://www.rtl-sdr.com/transmitting-fm-am-ssb-sstv-and-fsq-with-just-a-raspberry-pi/)就能使用 SDR 进行传输。

过去有一些项目[使用 Pi 来广播电台(PiFM)](http://hackaday.com/2012/12/10/transmit-fm-using-raspberry-pi-and-no-additional-hardware/) ，但是这个新软件(RPiTX)将它向前推进了几步。只需使用一根大小合适的电线连接到一个 GPIO 引脚，Raspberry Pi 就能够使用 FM、AM、SSB、SSTV 或 FSQ 信号进行广播。这大大增加了这种简单的电脑发射机的潜力，任何人都应该能够得到它的大量使用。在休息时间下面的视频演示中，[Evariste]记录了一个无线门铃信号，然后仅使用 Rasbperry Pi 重新传输它。

如果你想尝试一下，RPiTX 代码可以在 GitHub 上找到。不言而喻，根据您所在的地区，您很可能需要某种业余无线电执照才能使用这些功能。如果你还没有业余无线电执照，[如果你想进入 SDR 的世界，你不需要收听](http://hackaday.com/2012/03/30/working-software-defined-radio-with-a-tv-tuner-card/)。但是业余爱好者执照并不难获得，而且在这一点上[不需要太多的说服](http://hackaday.com/2015/10/23/why-should-you-get-a-ham-radio-license/)你就能得到传输。

 [https://www.youtube.com/embed/UwgJiUhloho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UwgJiUhloho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

