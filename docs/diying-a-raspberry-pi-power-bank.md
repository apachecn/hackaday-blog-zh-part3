# 狄莺一个树莓派电力银行

> 原文：<https://hackaday.com/2016/11/26/diying-a-raspberry-pi-power-bank/>

在过去十年左右的时间里，电池技术取得了巨大的进步。虽然这些锂电池已经实现了轻薄、功能强大的智能手机和四轴飞行器，但[patrick]认为做一些更简单的事情是个好主意。他用 18650 号电池制作了一个 USB 电源库。虽然简单地买一个 USB 电源组会更容易，但这不是重点，不是吗？

这个项目是[patrick]早期项目之一的后续项目，[树莓派的备用电池](http://hackaday.com/2016/03/17/battery-backup-for-the-raspberry-pi/)。这个早期项目使用一个 14500 电池和一个 MSP430 微控制器，在电池电量接近耗尽时优雅地关闭 Pi。

虽然最初的项目在低功耗 Pi Model A 和 Pi Zero 上工作得很好，但它在更高功率的 Pi 3 上与 UPS 的职责相冲突。[patrick]升级了电池并改变了电子设备，以提供足够的电流来保持高功率 Pi，即使在 100%的 CPU 负载下。

最终结果是一个 USB 电源库，能够让树莓皮存活几个小时，并保持相对凉爽。