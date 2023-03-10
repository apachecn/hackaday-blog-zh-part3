# 对 WiFi 安全摄像头进行逆向工程

> 原文：<https://hackaday.com/2016/02/06/reverse-engineering-a-wifi-security-camera/>

物联网正在慢慢变成世界上最大的蹩脚机器人，其设备似乎被设计成不安全的，等待着被任何拥有正确知识的人扎根和利用。最新的互联网设备是摩托罗拉福克斯 73 户外安全摄像机。除了软件之外，这是一架相当好的照相机。[亚历克斯·法兰特]和[尼尔·比格斯] [发现这个软件异常可怕](http://www.contextis.com/resources/blog/push-hack-reverse-engineering-ip-camera/)，它会允许任何人控制这台相机并安装新的固件。

有问题的摄像机是摩托罗拉焦点 73 户外安全摄像机。这款相机连接到 WiFi，具有全平移、倾斜、变焦控制功能，并向服务器提供实时图像和移动警报。基本上，它是您在 WiFi 安全摄像头中需要的一切。设置这台相机很简单——只需按下“配对”按钮，相机就会切换到主机模式，并设置一个开放的无线网络。附带的 Hubble 移动应用程序扫描网络以寻找相机，并提示用户连接到它。一旦应用程序连接到相机，用户就会被要求从列表中选择一个 WiFi 连接到互联网。然后，该应用程序通过开放网络发送安全密钥，而不加密。在这一点上，几乎任何人都可以看到这里的潜在漏洞，而且由于这种摄像机通常安装在户外——任何人都可以接触到——白痴的证据比比皆是。

一旦摄像机接入网络，固件升级有一些规定。通常，固件升级可以从“私有”URL 下载，并通过一个简单的脚本发送到相机，该脚本将 URL 作为 root 直接传递到外壳中。几个 facepalms 之后，[Alex]和[Neil]就可以 root 访问摄像头了。根密码是“123456”。

虽然在这个产品中有一个良好的摄像头互联网的开端，但软件的设计选择是彻头彻尾的愚蠢。无论如何，如果你正在寻找一台你自己的网络摄像机，而不是一家只有几台服务器和一个定制智能手机应用程序的公司，这将是列表的第一位。对于一些开源相机固件来说，这是一个很好的开始。

谢谢[马修]的提示。