# 实用的外壳设计，针对 3D 打印进行了优化

> 原文：<https://hackaday.com/2017/05/24/practical-enclosure-design-optimized-for-3d-printing/>

【3D Hubs】分享了一份关于[设计实用且 3D 打印友好的外壳的便捷指南](https://www.3dhubs.com/knowledge-base/cad-modeling-1-enclosures)。该指南介绍了两个外壳、两个按钮的遥控器外壳的设计。它允许内部安装 PCB，露出 USB 端口，并针对 3D 打印进行了优化，而不会在过程中陷入困境。[3D Hubs]在他们的示例中使用 Fusion 360(对业余爱好者和初创公司免费)，但设计原则很容易用任何工具实现。

其中一个技巧是设计壁厚是打印机喷嘴直径倍数的零件。例如，2.4 毫米的壁厚起初听起来可能有点武断，但它很容易除以 0.4 毫米的典型 FDM 喷嘴直径，这使得切片结果更加一致和可靠。我们大多数人在某个时候都遇到过切片器无法决定如何处理薄特征的模型，要么在周边之间提供一个空白，要么在填充时进行笨拙的尝试，这种做法有助于减少这种情况。另一个技巧是尽量减少设计中的锐边数量，因为圆角打印效率更高，打印头的运动更平稳。

通向外壳的道路有很多条，包括从 FR4 (又名 PCB 材料)一直到[带有墨粉转移标签的废木头](http://hackaday.com/2016/11/18/need-an-enclosure-try-scrap-wood-with-toner-transfer-labels/)制成的[外壳，当然，桌面 3D 打印对那些不得不毫无乐趣地钻孔和锯掉毫无特色的塑料盒的人来说是一个福音。](http://hackaday.com/2015/06/03/how-to-build-beautiful-enclosures-from-fr4-aka-pcbs/)