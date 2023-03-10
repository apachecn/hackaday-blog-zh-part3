# 黑客日奖品入口:一个非常小的密码保管员

> 原文：<https://hackaday.com/2016/06/19/hackaday-prize-entry-a-very-small-password-keeper/>

近年来最流行的安全构建之一是 USB 密码库。这些拇指驱动器大小的小设备保存了你必须处理的所有密码，并被锁在驱动器本身的验证码后面。[Miguel]和[Noel]在他们的 Hackaday 奖参赛作品中询问了这些设备的制造成本。答案是，以他们的 Memtype 项目的形式出现的[，非常便宜。](https://hackaday.io/project/8342-memtype-open-source-password-keeper)

Memtype 项目基于地球上最便宜、最简单的 USB 实现。它是围绕 ATtiny85 和 V-USB 的 USB 键盘的纯软件实现而构建的，除了 tiny85 本身之外，只需要几个电阻和二极管。

该设备只能通过巧妙使用小型 SMD 操纵杆输入的四位数 pin 解锁。输入正确的密码后，Memtype 授权用户访问所有存储的密码。就安全性而言，[Miguel]和[Noel]已经在 assembly 中实现了 [NOEKEON](https://en.wikipedia.org/wiki/NOEKEON) ，但是需要注意的是所有的安全性都比管钳弱。为了管理密码，[Miguel]和[Noel]构建了一个小而简单的 GUI 应用程序来设置 PIN 并向设备写入凭据。

[Miguel]和[Noel]已经有了 Memtype 的演示视频，您可以在下面查看。

 [https://www.youtube.com/embed/OM_-cQgjT8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OM_-cQgjT8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)