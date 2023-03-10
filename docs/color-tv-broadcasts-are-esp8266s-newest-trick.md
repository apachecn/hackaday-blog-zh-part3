# 彩色电视广播是 ESP8266 的最新花招

> 原文：<https://hackaday.com/2016/03/01/color-tv-broadcasts-are-esp8266s-newest-trick/>

众所周知，ESP8266 是一个非常小而便宜的 WiFi 模块。但是功能背后的芯片非常强大，远远超出了它的预期目的。我一直在破解该板的不同用途，我最近的冒险包括从该芯片生成彩色视频。这个生成的视频可能会连接到您的电视，或者您可以通过无线广播它！

我一直在摆弄 NTSC，这是一种北美视频标准，最近被 ATSC 等数字标准取代。最初，我探索了用 AVR 推出 NTSC，这导致了整个[让我们学习，让我们编码系列](https://www.youtube.com/watch?v=X24zDXz8Xgc&list=PLDRymMFQl3NmSjec3089UA8nlvXRjUokR)。但有一段时间，这个问题被搁置了，直到我决定看看我能以多快的速度运行 ESP8266 的 I2S 总线(一个美化的移位寄存器)，答案是 80 MHz。这比我想象的要快得多。比用于音频的 1.41 MHz(其预期目的)更快，2.35 MHz 用于[控制 ws 2812 b led](https://www.youtube.com/watch?v=6zqGwxqJQnw)或 4 MHz 用于[操作 reprap](https://github.com/lhartmann/esp8266_reprap) 。它偶尔会在 80 MHz 出现故障，但是，它仍然工作得出奇的好！

使用芯片的 I2S 总线最酷的部分是连接到它的多功能 DMA 引擎。数据块可以链接在一起，无缝地移出数据，并且可以在数据块完成时产生中断，用新数据填充它。这允许在中断中创建软件定义的比特流。

为什么是 NTSC？如果我住在欧洲，它会是 PAL。你可能在想的问题是:“为什么是一个死标准？”实际上有三个原因。

1.  因为太简单了。好吧，[时间有点奇怪，](http://www.kolumbus.fi/pami1/video/pal_ntsc.html)但是如果你真的想的话，你可以忽略颜色和整个偶数/奇数帧的事情。要启动并运行，您只需创建三个不同的电压电平，并将时序控制在 1us 左右。
2.  展示它的机制就在我们周围。甚至新电视通常都配有复合插头，许多还配有模拟调谐器。
3.  因为它非常适合学习数字和模拟信号的许多基础知识。

### 广播 NTSC

![BaseMod2](img/a23b666469966a9aba79fb155f0cb72d.png)

方便的是，NTSC 也特别好播。这只是调幅。对于频道 3，它的中心频率是 61.25MHz，电视真的只关心[上边带](https://en.wikipedia.org/wiki/Single-sideband_modulation)。为了对其进行编码，只需使同步成为信号中最强的部分，白色成为最弱的部分。黑色在中间的某个地方。为什么白弱而 sync 黑强？这样电视可以最准确地知道黑色和同步电平在哪里。没有参照系，接收方无法知道你的信号相对强还是弱。

![BaseMod1](img/d21fe5f0f31dac5fbf296ddfa336eb84.png)

为什么广播？许多项目使用复合信号，并直接插入电视。更多的是因为挑战。虽然我知道用 ATTiny85 广播 NTSC 是可能的，那是使用 PLL 和一些其他专门的硬件。我甚至不知道在 ESP8266 上能不能做到。

 [https://www.youtube.com/embed/bcez5pcp55w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bcez5pcp55w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 一开始，有黑屏

我开始玩一些 32 位重复模式，突然我的电视变暗了。这意味着电视正在接收信号，不是它在信号中发现了什么，而是它成功地解调了什么。我真的不知道是什么品质使位模式 0x98c63333 (msb 优先)在当时被我的小电视如此强烈地接收到，但它几乎没有引起关注。这将是我的“同步”，因为它是最强的。为了使黑色，我必须削弱信号一点，经过一些实验，我来到 0x88862210 然后在 0xffffffff 白色(变成了 DC 信号，没有被我的电视机接收)。我把一根短电线连接到 ESP 的“RX”引脚，另一根连接到 I2S 数据输出引脚，ESP 开始广播。在这里，我可以通过先黑后白的“像素”和先白后黑的“像素”来获得更好的分辨率。这是我的第一个实验[的基础，ESP8266 在频道 3](http://hackaday.com/2016/01/31/tv-transmitter-uses-esp8266/) 播放！

![Bitstream](img/a417fc228cef42870ea00aaf95393199.png)

### 这是一个射频之谜

所以，这并不是很难，主要是通过把代码扔向墙壁，看看有什么东西卡住了。我不知道为什么会这样，因为我不是在 61.25 兆赫传输。我以为是泛音。也许是三次或四次谐波？我最初确实测试了这个理论，将我的数据(加倍样本)放入一个[在线 FFT 计算器](http://sooeet.com/math/online-fft-calculator.php)。这很快推翻了关于谐波的理论，但我注意到了更疯狂的事情。信号实际上是以大约 1/2 的采样速率镜像的。它不是 30.625 * 2 或任何东西…它是 17.5 MHz 折叠在 40 MHz [奈奎斯特](https://en.wikipedia.org/wiki/Nyquist_frequency)周围。让我们从频率空间来看这个。

![CutGraph](img/33d0fc912cdb4966021e5ae6b7dcf5fc.png)

发射的主频率为 17.5 MHz，然后下降 3db(功率的 1/2)，您可以看到 62.5 MHz 的反射。您还可以看到频率在 40 MHz 左侧的许多其他峰值，每个峰值在 40 MHz 右侧都有反射，功率只有一半。射频很诡异。

有了这些知识，我意识到我可以直接合成载体，但我需要更长的时间来使它准确。我能够编写一个小程序来生成长度为 1408 位(56.8us)的位模式。为什么是 1408 位？

*   1078 / 1408 * 80 MHz = 61.25 MHz(能够精确生成我们的载波)
*   1408 / 32 = 44 个字(可被 32 整除，DMA 引擎只能用 32 位字工作)
    和
*   63/1408 * 80 MHz = 315/88 MHz≈3.58 MHz(能被色度整除)

哦，对了！你可能不知道为什么 3.58 MHz 很重要。嗯，NTSC 也可以显示彩色。它通过在发射器和接收器上产生 3.58 MHz，并在图像的同步部分，即“彩色脉冲”期间同步它来实现这一点现在，信号强度控制亮度，这种新的色度载波的强度控制颜色的饱和度，相位控制色调。电视非常关心色度信号保持同步，所以我需要尽可能精确。

由于代数，我们可以在不同的强度和相位下直接合成主信号(61.25 MHz)和色度信号(64.83 MHz)。该程序创建了一个表格，其中包含几种“颜色”或重复的 1408 位“同步”、“黑”、“白”、“红”等样本。现在，在任何时间点，我们都可以从该表中选择一种特定的颜色进行传输。瞧。现在，ESP 可以控制信号输出。

### 使用浏览器让一切正常工作

在 I2S 上使用中断意味着我们可以规划出我们想要传输的视频行，并将其交给 DMA 引擎以同步传输。

![DFTGraph.png](img/2f1f22ff6600bae96b6a3d6dc7b7ea2c.png)

编写一个程序来生成这些位模式，然后重新编译和刷新 ESP，这对于正常开发来说花费了太多的时间(每次测试之间可能需要 30 秒)。相反，既然 ESP 有 web 界面，为什么不利用它呢？通过编写一个 [Web Worker](http://www.w3schools.com/html/html5_webworkers.asp) ，我可以在上面显示的浏览器中编写代码。每次击键，它都会执行我更新的代码，创建新的位模式，对它们运行 DFT，并自动更新 ESP 上的表，ESP 会立即开始使用它们进行传输。开发周期之间的毫秒数。

### 这些有趣的图案是怎么回事？

当有大块的颜色时，你可能会注意到的一件事是，它们并不是真的平坦和漂亮，而是有颗粒的。这一切都归结于我们的信号产生机制如此糟糕。NTSC 广播是模拟的，不是以极快的速度变化的 1 比特。

![AllAround](img/2a5a10d7ed926b936415a79bd9d8a05a.png)

电视不是拍摄 1408 位的快照并计算平均值，而是拍摄小快照并在其上处理视频，否则我们的像素将是屏幕宽度的四分之一。因为电视只查看一个小窗口(大约 1us ),并且为我们的视频输出 1 位的过程本身是随机的，所以信号很粗糙。当我们只采样 60 个样本而不是 DFT 中的 1408 个样本时，我们开始看到电视真正看到的是什么，以及信号有多糟糕。峰值移动并改变振幅，导致上图所示的伪像。

![animate](img/e722541c32ae3d6b06bef03dfd502934.png)

### 从这里去哪里？

使用此表和输出帧缓冲区的过程会产生一些开销。该表只有 3kB，但帧缓冲区有 12kB，这在 ESP 的内存中是相当大的一块。在 CPU 端，我发现更新 DMA 和输出帧缓冲区大约需要 10%的 CPU 时间。这为绘制框架本身留出了大量时间。可以实现即时计算帧、仅存储文本缓冲区等的系统。这为从信息文本显示到绘制复杂的 3D 环境的各种应用带来了巨大的性能提升。

NTSC 可能是我最喜欢的标准。它惊人的健壮性、无处不在性和简单性提供了以多种方式输出、传输和观看视频的能力，这几乎不影响该标准的“死亡”无论是复合插头还是通过信道 3 广播，它都为大小处理器提供了一种视频输出机制。无论什么时候考虑下一步做什么项目，别忘了还有 NTSC 爷爷在那边，他还有一些锦囊妙计。

与这个项目相关的所有资源都可以在 GitHub 上找到，如果你错过了上面嵌入的视频，[还有一个机会观看演示](https://www.youtube.com/watch?v=bcez5pcp55w)。