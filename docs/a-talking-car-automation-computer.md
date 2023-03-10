# 会说话的汽车自动化计算机就像没有 Sass 的 KITT

> 原文：<https://hackaday.com/2016/02/14/a-talking-car-automation-computer/>

奇怪的是，司机们对引擎盖下发生的事情知之甚少。我们大多有洞察力的错觉，表现为仪表、白痴灯，当事情变得真实时，我们的视力和嗅觉。汽车越旧，了解其系统的状况就越重要。

开着一辆破旧的 1999 年本田思域。他喜欢将创建自动化系统作为一种爱好，并认为他的汽车将成为一个优秀的测试对象。[mjtrinihoby]开始这个项目时考虑到了几个特点。他希望对汽车的几个系统进行更多的控制——空调、灯光、燃料水平和驾驶室中的鼓风机电机，等等——以及一种紧凑、用户友好的方式来与它们交互，可以处理道路震动和他称之为家的炎热气候。

他选择了一款带有触摸屏的 Windows 8.1 上网本作为用户界面。上网本运行的是 FlowStone，这是一种强大的图形编程语言，有一长串的应用程序。LabJack 数据采集板(DAQ)处理汽车系统和上网本之间的通信。

这不仅仅是一种控制气候和在夜幕降临时让车灯亮起的酷方法。例如，[mjtrinihoby]的系统持续监控交流发电机的电压。如果它的测量值在 7 到 12V 之间，一个友好的声音会警告可能的交流发电机故障，并禁用高功率附件，这样汽车就有机会到达机械师那里。

休息之后，请务必观看演示视频。如果 OBD-II 汽车黑客更适合你的速度，尝试建立一个 RGB 转速表。

 [https://www.youtube.com/embed/GHdMFtl_TAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GHdMFtl_TAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

