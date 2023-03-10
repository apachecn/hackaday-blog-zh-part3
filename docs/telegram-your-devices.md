# 发电报给你的设备

> 原文：<https://hackaday.com/2016/03/12/telegram-your-devices/>

【二寒】一直在[摆弄电报即时通讯服务](https://hackaday.io/project/9745-telegram-control-application)。最初，他想出了如何打开和关闭手机上的 led:他通过[电报机器人 API](https://core.telegram.org/bots) 从手机向一台计算机发送命令，该计算机通过串行连接到实际控制 led 的 MSP430 板。

但是这有点复杂。更好的方法是省去中间人(呃…微控制器)和[实现电报接收和树莓皮上的 LED 闪烁](https://hackaday.io/project/9736-telegram-control-application-with-raspberry-pi)。对于一个已经使用 Pi 的项目来说，使用即时消息服务的资源是一种非常简单的手机接口方式。

[独立 RPi 项目](https://github.com/ErhanYILMAZ/TelegramControlPi)和[基于 MSP430 的微控制器应用](https://github.com/ErhanYILMAZ/TelegramControl)的代码可从【Erhan】的 GitHub 获得。你将为他们的 [telegram-bot-api](https://www.npmjs.com/package/telegram-bot-api) 安装 [Node.js](http://nodejs.org/) ，并跳过通常的 OAuth 关卡[让你的机器人注册 Telegram](https://core.telegram.org/bots) 。但是一旦你在 Raspberry Pi(或者你选择的目标计算机)上完成了所有这些，就只剩下几行相当高级的代码了。

我们在 Hackaday.io 上只看到了[另一个电报应用，我们想知道为什么。它看起来非常光滑，而且由于机器人能够将定制的“键盘”与信息一起发送到手机，它可以使基于手机的控制界面变得不在话下。还有人用电报打机器人吗？](https://hackaday.io/project/6487-telegram-control)