# 升级 USB 烙铁！

> 原文：<https://hackaday.com/2017/12/04/upgrading-a-usb-soldering-iron/>

看到 TS-100 烙铁如此受欢迎，GitHub 用户[ole00]发现自己渴望得到它的一些功能，但由于缺少电源而推迟了。黑客要做什么？找到一个更便宜的选择，然后[把它改装成酷炫的](http://mujweb.cz/molej/zd20um/)。

[ole00]偶然发现了[便宜的 ZD-20U](https://hackaday.com/2016/04/25/usb-soldering-iron-is-surprisingly-capable/) ，尽管数量不多(抱歉！)的问题——看到了潜力:它体积小，重量轻，通过 USB 电源线供电。为了尽可能多地使用 ZD-20U 的原板，修改仅限于一些迹线切割和元件互换。主要的变化是用一个 13a 微控制器替换了控制熨斗的 555 定时器 IC，给了它更多的控制。

[ole00]还用一个按钮取代了笨拙的触敏螺柱，将 LED 的行为改变为温度指示器的行为，并可配置温度曲线和加热周期。完整的项目分解可以在他们的 GitHub 页面上找到。

如果你有 TS-100，[保护好它](https://hackaday.com/2017/11/26/protect-your-ts100-soldering-iron/)！