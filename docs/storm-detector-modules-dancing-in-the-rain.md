# 风暴探测器模块:在雨中跳舞

> 原文：<https://hackaday.com/2018/03/28/storm-detector-modules-dancing-in-the-rain/>

之前，我们已经介绍了如何设置 AS3935 闪电探测器模块。这种探测器接收无线电辐射，然后对其进行分析，以确定它们是雷击还是其他射电源。在收集了一些数据后，它输出到即将到来的风暴锋面的估计距离。

但这只能让你成功一半。该设备检测到许多非闪电事件，裸露的电路板缺乏*活力*。今天，我通过深入研究探测器的数据表来解决这个问题，并快速去一元店买一个合适的外壳。结果呢？要下雨时会跳舞的塑料植物！


[![](img/1018476caf529a1c910cae4dc3dd15a2.png)](https://hackaday.com/wp-content/uploads/2018/03/lightning_detector_recto_square.jpg)

在上一篇文章中，我介绍了如何检测来自设备的事件，然后从设备内存中读取检测到的事件类型。然而，我们已经收到了输出到终端的大量类型“4”(0100)事件，表明检测到大量非闪电事件。这些被称为“干扰器”，是芯片检测到的无线电信号，但不考虑照明。默认情况下，它会将这些信号的中断引脚拉高，并发送这些信号。

我们的第一步将是把这些过滤掉，这样我们就少了一件要担心的事情。我们可以忽略它们，但这是不礼貌的——如果根本没有发送这些数据会更好，因为此时我们对它们不感兴趣。幸运的是，AS3935 (PDF)的[数据手册描述了一种实现这一点的方法:存储器寄存器 0x03 (MASK_DIST)的位 5 控制芯片是否发送干扰事件。在轮询中断引脚之前，我们可以将该存储器地址设置为 0x20(十进制 32，二进制 00100000 ):](http://www.embeddedadventures.com/datasheets/AS3935_Datasheet_EN_v2.pdf)

```

pin   = 8
light = 2
spi.setup(1, spi.MASTER, spi.CPOL_LOW, spi.CPHA_LOW, 8, 256);
gpio.mode(pin, gpio.OUTPUT)
gpio.mode(light, gpio.INPUT)

function reason()
	gpio.write(pin, gpio.HIGH)
	tmr.delay(30)
	gpio.write(pin, gpio.LOW)
	tmr.delay(30)
	spi.send(1, 0x43)
	tmr.delay(30)
	read = spi.recv(1, 8)
	print(string.byte(read))
	gpio.write(pin, gpio.HIGH)
	tmr.delay(30)
	gpio.write(pin, gpio.LOW)
	tmr.delay(30)
	gpio.write(pin, gpio.HIGH)
	tmr.delay(30)
end

spi.send(1, 0x03)
tmr.delay(2)
spi.send(1, 0x20)

tmr.alarm(1, 100, 1, function() poll(0) end)

function poll()
	x = gpio.read(light)
	if x == 1 then 
		reason()
	end
end

```

当我们重置设备时，我们不再看到任何干扰事件。现在我们什么也看不见，除非我触摸天线，此时我们读取十进制 33(二进制 100001)。MSB(最高有效位)就是我们写入的 MASK_DIST 寄存器，所以我们可以从得到的结果中减去 32，得到中断代码。完成后，如果中断原因是噪声水平过高，设备将输出 1，如果是闪电事件，设备将输出 8。

## 变湿了

这里发生了一件有点尴尬的事情。当时我正坐在一家咖啡馆里，向一个朋友展示这个设备，它开始记录闪电事件。现在是越南的旱季，天气晴朗，所以我解释说我有几只虫子要清理，然后骑上我的摩托车，沿着高速公路回家。我被今年的第一场暴风雨困住了，这场暴风雨太猛烈了，无法开车，我花了半个小时躲在一个小灌木丛里自嘲。成功！？

回到器件，我们将忽略高噪声水平事件。对于商业设备，你会想让用户知道噪声水平太高，但我们现在对此不感兴趣。有趣的是知道风暴有多远。芯片需要收集一些数据来估计风暴前沿的距离，所以我们要告诉芯片不要向我们发出警报，除非它在 15 分钟内检测到最少的雷击。存储器寄存器 0x02 的位 4 和位 5 根据下表控制该功能:

![](img/a256d120eb18843a8804b42df017633c.png)

Source: [AS3935 datasheet](https://www.embeddedadventures.com/datasheets/AS3935_Datasheet_EN_v2.pdf)

整个 8 位存储器寄存器的默认值为 11000010，我们将改为 11010010 (0xD2)。这设置了在芯片报告闪电之前，每分钟至少检测到 5 次雷击。第五次雷击后，它会通过将中断引脚拉高来报告每次雷击:

```

spi.send(1,0x02)
tmr.delay(2)
spi.send(1,0xD2)

```

[![](img/a049a916b6f77b798cb495a65a0320eb.png)](https://hackaday.com/wp-content/uploads/2018/03/finished_lightning_plant_thumbnail_bright.png)

An unusual method of horticulture.

一旦它检测到 5 次雷击，我们将希望该设备在风暴接近时输出到风暴的距离。为此，我们只需读取寄存器 0x07，并清除结果中的位 6 和位 7。虽然我只见过这些位设置为 0，但它们是由器件保留的，我们对它们的状态不感兴趣。最后，我们检查事件类型和产生的距离，并使输出更易于阅读。我们的最终代码在这里。

这很有效，也很好，但是还不够有趣。你知道那些当小太阳能板暴露在阳光下时会跳舞的小塑料玩具吗？事实证明，NodeMCU 的 3.3v 输出可以非常有效地替代非晶硅太阳能电池板。来自其中一个输出引脚的快速脉冲将一个在阳光下跳舞的设备转换为在雨中跳舞的设备。

对代码的唯一修改是在闪电探测事件时短时间内将一个引脚拉高，连接到太阳能电池板正输出(NodeMCU 接地到负输出):

```
gpio.write(quiver, gpio.HIGH)
tmr.alarm(2, 4777, 1, function() dequiver(0) end)
```

我为这部分考虑了几个玩具模型。猴子和鸡在前缀“雷”后面听起来都不错。最后，我选定了一种塑料植物，因为这种植物在期待下雨时会颤抖，有点像噩梦。

抛开我对零件的轻率使用不谈，这些探测器将是许多项目的巨大补充，如自动部署的避雷针或以图形方式显示当前天气的 T2 灯。