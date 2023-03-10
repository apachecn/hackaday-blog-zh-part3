# Discovery MIDI 示例播放器

> 原文：<https://hackaday.com/2015/09/13/discovery-midi-sample-player/>

[Igor b]在一个乐队中演奏，想要一种使用脚踏板来触发样本的方法。因为他手边有一个 STM32F429 评估板，所以他决定使用评估板、一个触摸屏、一个 SD 卡来构建 Stmpler，除此之外别无他物。

为了节省 pin 码，[Igor]使用 SPI 模式(而不是 SDIO)来访问 SD 卡。他使用滤波 PWM 产生音频输出，以保持设计简单。由于 PWM 的原因，位深度和采样速率之间存在折衷，因此[Igor]选择 20.5 kHz 的 12 位样本。

该软件使用 [Chibios/RT](http://www.chibios.org/dokuwiki/doku.php?id=chibios:product:rt:start) 作为 RTOS，使用 [GUI 库](http://ugfx.org/)来管理触摸屏。[Igor]说他还需要增加一些功能，但是他已经在他的表演中使用了。过滤后的 PWM 可能不完全高保真，但它可能比 3D 打印机听起来更好[。或者也许他会从我们这里得到一个提示，然后](http://hackaday.com/2015/03/09/3d-printer-plays-classic-midis/)[去无线](http://hackaday.com/2015/07/17/transmitting-midi-signals-with-xbee/)。

 [https://www.youtube.com/embed/_MF7Ovzj2bY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_MF7Ovzj2bY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

