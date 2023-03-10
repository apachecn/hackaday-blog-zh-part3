# Pitmaster 烧烤仪表板监控您的肉类和蔬菜

> 原文：<https://hackaday.com/2017/09/28/pitmaster-bbq-dashboard-monitors-your-meat-and-veggies/>

烧烤是关于温度的，要确保烤架上的任何东西都达到合适的温度。至少，这是确保你不会毒死人的部分，因为你的食物应该足够热以杀死任何细菌。[克里斯·阿基诺]决定更进一步，不仅仅是简单地将体温计插入一大块肉中，他还创造了一个 Pitmaster。这种硬件和软件的结合可以监控多块食物的温度，并在每块食物准备好的时候提醒你，这一切都是通过一个网络界面实现的。

Pitmaster 是一个展示 [React](https://en.wikipedia.org/wiki/React_(JavaScript_library)) 的项目，这是一个新的库，用于创建将 Javascript、HTML 和各种其他技术融合在一起的 ui。DigitalCrafts.com[的教师 React 制作了 Pitmaster，作为如何使用它快速构建 UI 的演示。这是一个运行在 Arduino 和 Raspberry Pi 上的简洁构建，第一个监控多个探头的温度，Pi 跟踪哪个传感器上有什么食物，然后将其推送到 web 界面。每个单独的烹饪工作都有一个名称和一个温度目标，因此您可以跟踪尽可能多的烹饪工作，因为您有房间或温度传感器。](https://www.digitalcrafts.com/)

有更简单的方法吗？当然:任何对烤肉还算过得去的人都可以通过外观和感觉来判断大多数食物，但这个系统允许你离开烤肉架，但仍然可以盯着它。这对于像吸烟这样需要长时间工作的人来说是很重要的，因为吸烟需要你不去管食物。另外，这是一个很酷的技巧，展示了如何使用一个新的(相当混乱的)编程工具。

我们昨天不是讨论过了吗？不，那是[又一个烧烤黑客](https://hackaday.com/2017/09/27/pid-controlled-charcoal-bbq-put-an-arduino-on-it/)。(我们正在变成烤架吗？)趁着还能享受最后几周的温暖天气，黑客们！