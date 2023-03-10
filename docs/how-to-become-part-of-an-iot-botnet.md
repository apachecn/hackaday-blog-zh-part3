# 如何成为物联网僵尸网络的一部分

> 原文：<https://hackaday.com/2016/10/06/how-to-become-part-of-an-iot-botnet/>

我们都应该熟悉所谓的物联网，即联网嵌入式电子设备的激增。这些技术为硬件黑客提供了巨大的机会，但我们也应该意识到围绕它们的一些安全问题。

近日，知名安全研究员【Brian Krebs】的网站遭遇 DDoS 攻击。这次攻击与以往不同的不是它的严重性，而是它不是来自恶意软件入侵的 Windows PCs 僵尸网络，而是来自被入侵的物联网设备。

有人可能会问，它怎么可能控制这样的低端嵌入式硬件，因为它通常会安全地位于防火墙后面，预装了自己的固件，并且没有一个毫无头绪的人在其终端打开充满恶意软件的电子邮件附件。答案相当令人震惊，但并不完全令人惊讶，因为设备本身的安全性差得惊人。一个这样的机制的曝光来自于[Brian Butterly]，他[拍摄了一个不起眼的 IP 网络摄像头并记录了它的安全缺陷](https://www.insinuator.net/2016/10/how-to-become-part-of-an-iot-botnet/)。

他检查的摄像机暴露了两个服务，一个 web 接口和一个 Telnet 端口。虽然从安全角度来看，它们缺乏加密是一个问题，但当设备安全地位于专用网络上并在合适的防火墙后面时，这应该不会造成很大的危险。这个问题来自于它通过互联网发送照片的能力，因为拥有者需要某种外部访问才能从他们的手机上查看他们的相机。昂贵的相机使用基于云的网络服务来完成这一任务，但像正在接受检查的相机这样的廉价相机只是向外界打开了一个端口。

如果你熟悉基本的防火墙设置，你会习惯于开放端口应该在防火墙所有者的控制之下；如果一个端口没有被特别打开，那么它应该保持关闭。那么相机如何打开一个端口呢？答案在于 [UPnP](https://en.wikipedia.org/wiki/Universal_Plug_and_Play) ，这是一种在大多数家用路由器上默认启用的协议，允许设备请求开放端口。简而言之，摄像头有一个固有的不安全服务，它要求路由器向外界公开，在许多情况下，路由器温顺地遵从，而其所有者对此一无所知。我们猜想，你们中许多还没有这样做的人现在将会检查一下你们的家用路由器，以减少它的 UPnP 活动。

上周[披露](http://hackaday.com/2016/09/26/extra-large-denial-of-service-attack-uses-dvrs-webcams/)时，我们报道了[Brian Krebs】DDoS 事件](http://hackaday.com/2016/09/29/distributed-censorship-or-extortion-the-iot-vs-brian-krebs/)，但我们确信这可能只是这方面许多故事的第一个。随着设备制造商努力了解他们不再从事愚蠢的设备业务，他们需要开始非常认真地对待他们的软件安全。

网络摄像头图片:Asim18(自己的作品)[CC BY-SA 3.0]，via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Webcam_grayscale.jpg) 。