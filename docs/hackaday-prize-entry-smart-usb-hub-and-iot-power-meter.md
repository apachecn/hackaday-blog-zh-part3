# Hackaday 奖参赛作品:智能 USB 集线器和物联网电表

> 原文：<https://hackaday.com/2016/08/02/hackaday-prize-entry-smart-usb-hub-and-iot-power-meter/>

[Aleksejs Mirnijs]需要一种工具来精确测量他的 Raspberry Pi 和 Arduino 项目的功耗，这是确定合适的电源和电池组的重要参数。由于大多数 SBC 项目无论如何都需要一个 USB 集线器，他设计了一个[智能的、支持 WiFi 的 4 端口 USB 集线器，它也是一个功率计](https://hackaday.io/project/11178-smart-usb4-port-hubpower-meter-with-lcd)——这是他今年 Hackaday 奖的参赛作品。

[Aleksejs]的设计基于 FE1.1s 4 端口 USB 2.0 集线器控制器，带有两个额外的充电端口。每个端口都配有一个 LT6106 电流传感器和一个功率 MOSFET，可根据需要单独开关器件。Atmega32L 监控总线电压和电流消耗，切换端口，并与 ESP8266 模块进行无线连接。增压轮毂还配有显示屏，让您一眼就能看到测得的电流和功耗。

 [![usbhub_pcb](img/776f728fe5fc162c179cea062035a030.png "usbhub_pcb")](https://hackaday.com/2016/08/02/hackaday-prize-entry-smart-usb-hub-and-iot-power-meter/usbhub_pcb/)  [![usbhub_oled](img/35e6a05852f978cfdc6f78cb766dd182.png "usbhub_oled")](https://hackaday.com/2016/08/02/hackaday-prize-entry-smart-usb-hub-and-iot-power-meter/usbhub_oled/) 

不像大多数廉价的集线器，Aleksejs 的集线器有一个设计合理的电源路径。如果存在外部电源，板载降压转换器会主动调节总线电压，同时电源路径控制器会安全地断开主机的电源线。虽然第一个原型已经建立并运行，这个项目仍在大力发展。我们很想看到宣布的更新，包括 2.2 英寸触摸屏和 3D 打印外壳。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)