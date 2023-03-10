# 通过无线方式更新您的 Arduino

> 原文：<https://hackaday.com/2018/01/18/over-the-air-updates-for-your-arduino/>

Arduino 和数据无线电可以构成一个很好的远程传感器节点。通常在这种情况下，硬件最终会被安装在难以触及的地方——无论是在灯具中、在墙后，还是隐藏在户外的某个地方。调试时不要把电缆反复塞进去。

[[2 bitor not 2 bit]认为这根本不行，于是决定通过无线方式对 Arduinos 进行编程。](https://www.2bitornot2bit.com/blog/arduino-bootloader-with-ota-over-the-air-support-over-nrf24l01)

将 NRF24L01 芯片与 Arduino 配合使用是将无线通信添加到小型项目中的常见选择。通过在远程硬件和连接到编程计算机的本地 Arduino 上安装其中一个无线电，可以使用 [Optiboot](https://github.com/Optiboot/optiboot) 在没有任何物理接触的情况下远程刷新 Arduino。

本文内容全面，涵盖了操作两端所需的硬件设置以及如何安装相关的引导加载程序。如果您已经在项目中使用了 NRF24L01，这可能是解决编程难题的理想方案。或许你使用的是不同的平台——比如 WiFi 版的 Arduino？不要担心，你也可以这样进行 OTA 更新。