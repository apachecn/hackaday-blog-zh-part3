# DC 到 DC 的转换，旋转风格

> 原文：<https://hackaday.com/2017/07/04/retrotechtacular-dc-to-dc-conversion-rotary-style/>

如果你想把一种电压转换成另一种电压，你会怎么做？好吧，如果你今天谈论 DC 电压，你可能会使用直流到 DC 转换器。实际上，这些转换器产生某种交流波形，然后使用电感或变压器根据需要提升或降低电压。然后他们会把它改回 DC。如果你说的是交流电压，你可以只使用变压器。但是想想这个:一个变压器有两面。初级线圈产生交变磁场。就像转动一根带有磁铁的轴一样。次级线圈将交变磁场转化为电能，就像发电机一样。换句话说，变压器只是一台接受交流输入而不是旋转机械输入的发电机。

这有点过于简单，但在过去，许多移动无线电(和其他设备)将这一想法带到了它的逻辑结论。一台 M-G(电动发电机)机组只不过是一台连接到发电机上的电动机。例如，电机可以采用 12V DC，输出可以是 300V 交流电，该交流电将被整流为电子管收音机中的板电压。

## 发电机

在许多情况下，电动机和发电机一起放在一个称为发电机的装置中。这些经常出现在老通用的双向无线电设备中(像警车中使用的那些)。发电机仅在发射期间运行，因此给发射器按键会导致车辆后备箱发出高音调呜呜声(收音机在后备箱里；只有控制头在机舱内)。

你可以在下面看到一段 20 世纪 50 年代发电机的视频。请注意如何测量电机呜呜声产生的电流量。

 [https://www.youtube.com/embed/ht4pgfdUZ8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ht4pgfdUZ8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这是一个高性能的解决方案。如果你不需要太多的能量——例如，一个普通的 AM 汽车收音机——你可能会使用[振动器](https://hackaday.com/2016/07/04/retrotechtacular-dc-to-dc-conversion-by-vibrator/)。这与将 DC 转换成交流电的想法是一样的，这样它就可以通过变压器。但是转换是通过一个类似继电器的装置来完成的。

## 使用

除了老式收音机，发电机或电动发电机也用于电梯(因为需要大电流 DC)和火车(DC 电压转换)。此外，如果你绝对需要输入和输出之间的完全隔离，电机和发电机之间的非导电轴可以让你达到目的。

不过，无线电可能是最常见的用途，包括像 ARC 5 这样的军用装备。您可以在下面的视频中看到 ARC 5 发电机的故障排除演示。

 [https://www.youtube.com/embed/iNJVMzGYUW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iNJVMzGYUW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



也许我们见过的最不寻常的电动发电机组之一是使用洗衣机马达。如果四分钟没事，可以看视频，下面。

 [https://www.youtube.com/embed/k20XVrF_CAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k20XVrF_CAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

