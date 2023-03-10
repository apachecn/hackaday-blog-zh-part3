# 半生不熟的物联网炉灶可以用作遥控纵火装置

> 原文：<https://hackaday.com/2017/04/20/half-baked-iot-stove-could-be-used-as-a-remote-controlled-arson-device/>

【笔测伙伴】在 AGA 炉灶中发现了一些确实很吓人的[漏洞。它们通过短信连接，通过手机应用程序向 AGA 发送未经认证的短信，给它命令，例如预热烤箱，你也可以告诉你的 AGA 立即打开一切。](https://www.pentestpartners.com/blog/iot-aga-cast-iron-security-flaw/)

问题出在网络界面上；它允许攻击者检查用户的手机是否已经注册，从而允许缓慢但有效的枚举攻击。一旦攻击者找到一个注册的设备，他们需要做的只是发送一条短信，因为消息没有被炊具认证，SIM 卡也没有被设置为在注册时发送消息。

这很令人不安，如果有人在去上班前把茶巾或其他易燃材料放在铁架上，回来时却发现一堆灰烬，那该怎么办？毕竟，这是一个六兆英国热量单位的炉子和烤箱。似乎在这个数字时代，我们联系得越紧密，我们就越容易受到攻击，公司似乎太忙于将他们的产品推出门外，而没有进行简单的安全检查。

在披露该漏洞之前，[Pen Test Partners]曾试图通过 Twitter 联系 AGA，结果被屏蔽。他们四处打电话，试图与知道物联网或安全含义的人取得联系。这花了一些时间，但最终他们设法与技术支持部门的人取得了联系。希望 AGA 将很快推出一些更新。该公司不愿在这个安全问题上做些什么，这确实凸显了有时[披露可能不够](https://hackaday.com/2015/01/08/when-responsible-disclosure-isnt-enough/)。

[通过[笔测试伙伴](https://www.pentestpartners.com/)