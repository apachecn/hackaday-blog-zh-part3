# 按下大红色按钮，接收电源。

> 原文：<https://hackaday.com/2018/02/11/push-big-red-button-receive-power/>

就像人们在意识到你忘了关烤箱、蜡烛和 T2 灯时的恐慌一样，焊接工具是一个潜在的严重危险。Hackaday.io 用户[Nick Sayer]已经习惯了他的 Hakko 烙铁的自动关闭功能，并错过了同一品牌的拆焊枪的这一功能。那么，除了[将问题扼杀在萌芽状态](https://hackaday.io/project/33765-ac-safety-timer)，他还能做什么呢？

他没有改造工具本身，而是制造了一个交流插头，半小时后会自动关闭。在一个金属投影盒内——当然是接地的 ATtiny85 连接到一个按钮、一个光隔离三端双向可控硅交流电源开关和一个指示电源的“指示灯”。半小时后，ATtiny 触发光隔离器并关闭插座，所以如果他想继续工作，就必须按下按钮。他指出，你可以快速双击按钮进行简单的定时器重置。

[![](img/908e43175495cdc7d0172854f47335fc.png)](https://hackaday.com/wp-content/uploads/2018/02/7754091517550099985.jpeg) 【塞耶】有一个问题，电源灯在没有插入任何东西的情况下会发出微弱的光——由于三端双向可控硅开关泄漏，大约有 60 伏的电压——他用一个放置得当的电阻器解决了这个问题。如果他不得不重新开始，他说他不介意添加一个保险丝和更宽的痕迹以获得额外的保险。如果他计划为那个洞焊接半个小时，[塞耶]将需要一个[严重的烟雾提取器](https://hackaday.com/2013/11/30/over-powered-fume-hood-is-awesome/)。