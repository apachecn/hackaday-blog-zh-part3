# RPi 为零的廉价音频流

> 原文：<https://hackaday.com/2015/12/10/audio-streaming-on-the-cheap-with-an-rpi-zero/>

Raspberry Pi Zero 的微小尺寸使其非常适合大小是一个因素的黑客。例如，一个小型的独立设备，用于将流式音频输入扬声器。RPi Zero 没有音频输出，因此 PolyVection 将其与他们的 PlainDAC 配对，以构建一个[最小音频流设备](https://polyvection.com/guides/raspberry-pi-zero-minimal-streamer/)。

他们的构建使用来自 GPIO 头的几条线来驱动 I2S 数模转换器。DAC 是德州仪器的一款 [PCM5142](http://www.ti.com/product/pcm5142) ，提供高质量声音输出，并包含一个内置的可编程 DSP。

硬件放入一个 [3D 打印的外壳](https://github.com/PolyVection/RPI-ZERO-case)，尺寸为 68 毫米×48 毫米。内部没有 WiFi，但可以通过外部 USB 设备进行无线流媒体传输。所用的 DAC 受 Linux 内核支持，因此只需一个简单的[配置](https://polyvection.com/support/plain-series/getting-started/)就能输出音频。

一旦你组装了这样的设备，你就可以安装一个像[音乐播放器守护进程](http://www.musicpd.org/)这样的服务器来远程控制设备并提示互联网广播频道。