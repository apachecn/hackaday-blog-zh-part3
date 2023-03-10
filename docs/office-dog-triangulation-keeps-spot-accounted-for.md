# 办公室狗三角测量保持现货占

> 原文：<https://hackaday.com/2015/11/29/office-dog-triangulation-keeps-spot-accounted-for/>

[Matt Reed]在一个宠物友好型的工作场所工作，他的宠物狗[Bean]喜欢在这里闲逛并消失。她没有惹上麻烦，但尽管如此，[马特]还是很担心她。所以他走了令人毛骨悚然的跟踪路线，在她的衣领上放了一个信标来跟踪她的一举一动。

他使用一个小的 BLE 信标，每秒钟轮询一次信号，发出一个唯一的 ID 码和一个 RSSI 值(接收信号强度指标)。通常情况下，信标被放置在一个固定的位置，以帮助人们导航——但这一次，它是在一只移动的狗身上。

为了更好地了解[Bean]在办公室中的位置，[Matt]在办公室周围设置了三个带蓝牙适配器的 Raspberry Pi。使用 [Noble](https://github.com/sandeepmistry/noble) ，Node.js 监听 RSSI 值并对【Bean 的】位置进行三角测量，就像手机可以使用不同的信号塔 ping 时间来定位一样。

他把这些数据放在 iPad 上办公室地板的覆盖层上，现在他马上就知道[比恩]藏在哪里了。至少直到他的一个同事对他恶作剧并移走了信标。

[https://player.vimeo.com/video/146362860](https://player.vimeo.com/video/146362860)

宠物在没人看的时候还会做些什么……有没有想过仓鼠会在多大程度上使用它的锻炼轮？