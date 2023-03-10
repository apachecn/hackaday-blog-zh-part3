# Shmoocon 2016:逆向工程廉价中国无线电固件

> 原文：<https://hackaday.com/2016/01/19/shmoocon-2016-reverse-engineering-cheap-chinese-radio-firmware/>

每隔一段时间，一件无线电设备就会引起一位多产的硬件大师的注意，并被逆向工程。几年前，它是 RTL-SDR，从那时起，软件定义无线电成为下一个大事件。上周末在 Shmoocon 上，[Travis Goodspeed]展示了他对 Tytera MD380 数字手持无线电的逆向工程。[该黑客攻击已经在 PoC||GTFO 0x10](https://hackaday.com/wp-content/uploads/2016/01/pocorgtfo10.pdf) (56MB PDF，镜像)中发布，其中包含了将一台 140 美元的收音机变成第一台数字移动收音机硬件扫描仪的所有血淋淋的细节。

![Tytera](img/f5b95e4b2257b8c36cd07f3a82be630e.png)

The Tytera MD-380 digital radio

Tytera MD380 是一款相当基本的无线电设备，有两个主要芯片:一个 STM32F405，带 1mb 闪存和 192k RAM，以及一个 HR C5000 基带。STM32 有 JTAG 和一个 ROM 引导程序，但这两者都受到读出设备保护(RDP)的保护。绕过 RDP 是越狱的真正定义，多亏了几个健忘或懒惰的中国工程师，这是最有可能的。

收音机中的 STM32 实现了 USB 设备固件升级(DFU)，可能是因为 ST 的一些示例代码。从标准 DFU 协议转储内存只是重复了相同的二进制字符串，但通过一点哄骗和调查可怕的 Windows 专用官方客户端应用程序，[Travis]能够找到非标准的 DFU 命令，编写一个定制的 DFU 客户端，并读写“codeplug”，这是一个存储无线电设置、频率和通话组的 SPI 闪存芯片。

进一步努力转储无线电上的所有固件是成功的，并开始了实际的无线电逆向工程。它运行一个实时嵌入式操作系统 MicroC/OS-II 的 ARM 端口。这个操作系统有很好的文档记录，只需稍加努力就可以编写新的功能和补丁。

在数字移动无线电中，音频通过公共通话组或私人联系人发送。收音机通常被设置为只有一个通话组，所以如果不改变设置的话，收听其他通话组是不可能的。混杂模式——一种让所有通话组都通过扬声器的模式——的补丁只是在固件中将一个 JNE 设置为 NOP。

![The Tytera MD-830 ships with a terrible Windows app used for programming the radio](img/9f312476117e2f687b22cfb521b02869.png)

The Tytera MD-380 ships with a terrible Windows app used for programming the radio

在[DD4CR]和[W7PCH]的帮助下，整个无线电已经通过与官方工具一起工作的重写固件进行了逆向工程，首次尝试了围绕 FreeRTOS 构建的临时固件，并开始了一个非常活跃的 140 美元无线电开发社区。[Travis]正在寻找能够添加对 P25、D-Star、系统融合、合适的扫描仪的支持，或者能够通过 USB 发送和接收 DMR 帧的人。所有这些事情都是可能的，这使得这成为近年来最令人兴奋的无线电黑客攻击之一。

在[Travis]在 Shmoocon fire talks 上展示这个黑客之前，直觉引导我在亚马逊上查找这个收音机。Prime 的价格是 140 美元，顶级供应商有 18 个库存。演讲结束后，20 分钟后，该供应商的库存中有 14 台。[Travis]卖了四台收音机给观众，但出席的人并不多。两个小时后，同一个供应商有四个库存。如果你在寻找骗局中最好的硬件破解，这就是你要找的。