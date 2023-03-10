# 瓦力走向企业，提供网真服务

> 原文：<https://hackaday.com/2016/03/08/wall-e-goes-corporate-offering-telepresence-service/>

我猜如果你要造一个机器人来做一些无聊的事情，比如远程呈现，你最好把它做得可爱一些。这显然是[Andrew Maurer]在用瓦力玩具建造一个[远程呈现机器人时所想的。结果有点可爱:Wall-E 拿着显示视频的 5 英寸 HDMI 屏幕，可以在远程控制下以真正的皮克斯风格四处移动。](http://imgur.com/a/z6IFa)

它的内部也很整洁，使用树莓皮作为大脑，使用 Adafruit MotorHat 来控制马达。最初的玩具没有马达，所以他增加了一个新的遥控变速箱和马达来驱动这个小家伙。安装在 Wall-Es eye 后面的是一个 USB 网络摄像头。在幕后运行的是一个制作音频的 [mumble](https://wiki.mumble.info/wiki/Main_Page) 服务器，一个显示视频的 Chromium 副本，以及一个将捕获的视频提供给对话另一端的 Apache 服务器。整个事情是由几个脚本捆绑在一起的，这些脚本适当地启动了事情，并允许用户远程控制 Wall-E。这是一个可爱的构建，希望 Wall-E 在履行新的公司职责时仍然可以找到他的 EVE。

[via [reddit](https://www.reddit.com/r/DIY/comments/49dmmw/i_made_a_toy_walle_into_a_telepresence_rover/)