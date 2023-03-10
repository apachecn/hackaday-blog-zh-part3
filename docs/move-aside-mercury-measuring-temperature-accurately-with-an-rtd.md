# 移开水银:用 RTD 精确测量温度

> 原文：<https://hackaday.com/2018/06/28/move-aside-mercury-measuring-temperature-accurately-with-an-rtd/>

从气象站到 3D 打印机，温度是最常测量的物理量之一，在我们的许多项目中都占有重要地位。最常见的是热敏电阻、热电偶、红外传感器或用于测量温度的专用 IC。甚至有可能只使用一个普通的二极管，从而产生一些有趣的 T2 技术。

通常我们只需要知道一两摄氏度内的温度，这些工具中的任何一个都可以。直到最近，当我们需要精确、可靠、大范围地知道温度时，我们才使用水银温度计。这些设备本身是仪器仪表的奇迹，但是水银是一种有害物质，而且从 2011 年起，NIST 将不再校准水银温度计。

![](img/4d3296f7d34746e96b47c88d35ebb9dd.png)

A typical Pt100 RTD probe

幸运的是，电阻温度检测器(RTD)是一个很好的替代方案。这些通常由非常细的纯铂金线组成，通过其在 0°c 时的电阻来识别。例如，Pt100 RTD 在 0°c 时的电阻为 100ω

0°C 时的典型精度为+/-0.15°C，但也可以达到低至+/-0.03°C 的精度。工作温度范围通常很高，通常为-70°C 至 200°C，一些专用探头的工作温度远远超过 900°C。

这些探针上的导线长度为一米或更长并不罕见，这可能是一个重要的误差源。考虑到这一点，您会看到 RTD 探头以双线、三线和四线配置出售。两线配置不考虑引线电阻，三线探头考虑引线电阻，但假设所有引线具有相同的电阻，四线配置在消除该误差方面最为有效。

在本文中，我们将使用 3 线探头，因为它在成本、空间和精度之间取得了良好的平衡。我发现[对探针类型](http://instrumentationtools.com/difference-between-2-3-and-4-wire-rtds)之间差异的详细处理有助于做出这个决定。

## 用于读取电阻温度检测器的电路

不幸的是，RTD 带来了一些困难。它们主要是电阻式传感器，除了极小的电流外，任何电流都会使其自发热，因此需要恒定的电源。你可以用运算放大器和惠斯通电桥来构建它。

![](img/f782096c58d063305a43d4f25a9f6f62.png)

Wheatstone bridge implementation of a 3 wire RTD probe. Source: [Wikipedia](https://en.wikipedia.org/wiki/Resistance_thermometer#Three-wire_configuration)

并非所有人都喜欢模拟电路设计，有一款不错的 IC 可以帮你搞定:RTD 数字转换器。它的工作原理是将 RTD 探针电阻与参考电阻进行比较，很容易设计电路板(该芯片提供 SSOP 和 TQFN 两种外形)。该芯片在[预组装的 Arduino 兼容模块](http://www.adafruit.com/product/3328)中很容易获得，并由 Arduino 库支持。然而，这并不适合所有人，今天我们将讨论如何通过 SPI 与这款有用的芯片进行交互。

无论您的平台如何，大多数 MAX31865 模块都需要一些初始设置。电路板的某些区域[必须桥接或切割](http://learn.adafruit.com/adafruit-max31865-rtd-pt100-amplifier/pinouts)迹线，以设置您使用的探头类型。

## 使用 ESP8266 和 Lua 进行测试

![](img/0555e0d7d5b7170e9e40c287f390a292.png)

SPI settings by mode. Source: [Wikipedia](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface_Bus#Mode_numbers)

在这个例子中，我将在运行 NodeMCU 的 ESP8266 微控制器上使用 Lua，但是类似的步骤应该可以在您选择的平台上工作。我们的第一步是配置 SPI。 [MAX31865 数据手册](http://datasheets.maximintegrated.com/en/ds/MAX31865.pdf) (PDF)声明仅支持 8 个数据位的 SPI 模式 1 和 3 以及 5 MHz 的最大时钟。在 Wikipedia 上快速搜索会返回一个表格，其中列出了每种模式的 SPI 设置。

我选择 SPI 模式 1 和 256 的大时钟分频器。我还设置了一个输出引脚，用作片选引脚。需要将此引脚拉低以启动读写操作，然后在操作完成后将其拉高。生成的代码是:

```

pin = 1
spi.setup(1, spi.MASTER, spi.CPOL_LOW, spi.CPHA_HIGH, 8, 256);
gpio.mode(pin, gpio.OUTPUT)

```

接下来，我们根据片选引脚所需的行为定义发送和接收功能。读取后返回的整数将始终介于 0 和 255 之间。ESP8266 会将其解释为 ASCII 字符，因此我们使用 string.byte 将其转换为十进制值:

```

function spi_write(target, data)
    gpio.write(pin, gpio.LOW)
    tmr.delay(20)
    spi.send(1, target)
    tmr.delay(20)
    spi.send(1, data)
    gpio.write(pin, gpio.HIGH)
    tmr.delay(20)
end

function spi_read (target)
    gpio.write(pin, gpio.LOW)
    tmr.delay(20)
    spi.send(1, target)
    tmr.delay(20)
    x = spi.recv(1,1)
    print (string.byte (x, 1))
    tmr.delay(20)
    gpio.write(pin, gpio.HIGH)
    tmr.delay(20)
end

```

## 配置 MAX31865 行为

利用 SPI 读写功能，我们现在可以使用 MAX31865 芯片。芯片上只有 8 个寄存器，每个寄存器包含 8 位数据。要从寄存器中读取数据，我们在它前面加一个“0 ”,向它写入一个“8”。例如，要读取寄存器 1，我们可以使用 spi_read(0x01)，要写入数字 0xFF，我们可以使用 spi_write(0x81，0xFF)。

主配置寄存器是寄存器 0，它根据下表工作:

![](img/5bf7fb33425ff6aa712717c20891c0f4.png)

Configuration register (address 0x00) bit functions on the MAX31865\. Source: [MAX31865 datasheet](https://datasheets.maximintegrated.com/en/ds/MAX31865.pdf) (PDF)

由于我想每秒自动读取，所以我需要打开两个 Vbias，并将转换模式设置为 Auto，所以是' 11 '。我不想使用 1-shot，所以写为' 0 '。我用的是三线探头，所以是 1。我将暂时清除故障检测，因此是“00”。我想从故障状态清除开始，所以这是一个“1”，我所在区域的电频率是 50Hz，所以这也是一个“1”。将所有这些连接在一起，我们得到“1101 0011”或十六进制 0xD3。

```

spi_write(0x80, 0xD3)

```

当温度高于或低于某个值时，芯片支持报警阈值。我不会使用这些，所以我将它们设置为极端值。

```

spi_write(0x83, 0x7f)
spi_write(0x84, 0xff)
spi_write(0x85, 0x00)
spi_write(0x86, 0x00)

```

## 读取温度数据

[![](img/593a1d00272e73f28a6cd594a46e541d.png)](https://hackaday.com/wp-content/uploads/2018/06/rtd_nonlinear.png)

Pt100 RTD nonlinearity error vs. Temperature. Source: [hardwarebook.info](http://www.hardwarebook.info/RTD)

现在设置好了，我们终于可以读取数据了。数据是基准电阻(在我的例子中为 427ω)和 RTD 探针之间的 15 位比率。随着探针温度的升高，其电阻以近乎线性的方式增加。

根据数据手册，温度可以通过以下公式估算:

![Temperature (C) \approx (ADC code/32) - 256 ](img/d5fc847003eda242da9ca374c1064998.png)

不过，有一个很好的理由不这样做:在+/-100°C 范围内，误差最高可达 1.75°C，此外，它假设基准电阻为 400ω，因此您可能需要进行校正。这种精度水平并不比更便宜、更易于使用的设备好多少，但对于确定您的探头读数是否正确非常有用。

为了提高精度，我们必须考虑探针电阻和温度之间关系的轻微非线性。有几种方法可以做到这一点，但最常用的是卡伦德-范杜森方程。这通常是一个二阶多项式，可预测给定温度下的电阻，如下所示:

![R(T) = R_{0}(1 + aT + bT^{2}) ](img/8d67e0b1b77a192a7675d6cb77409ad1.png)

这在高达约 660°C 时是精确的(更复杂的函数可以处理更高的温度)。探头规格说明 a 和 b 的值分别为 3.90830 x 10 ^(-3) 和-5.77500 x 10 ^(-7) 。有了这些常量，我们可以编写如下实现:

```

#Read high ADC register (8 bits)

gpio.write(pin, gpio.LOW)
tmr.delay(20)
spi.send(1, 0x01)
tmr.delay(20)
x = spi.recv(1,1)
x = (string.byte (x, 1))
tmr.delay(20)
gpio.write(pin, gpio.HIGH)

tmr.delay(20)

#Read low ADC register (7 bits)
gpio.write(pin, gpio.LOW)
tmr.delay(20)
spi.send(1, 0x02)
tmr.delay(20)
y = spi.recv(1,2)
y = (string.byte (y, 1))
tmr.delay(20)
gpio.write(pin, gpio.HIGH)

#print out approximation of temperature from function in datasheet, accounting for our resistor being 427 Ω, not 400 Ω. Note that the ADC value is 15 bits long, not 16.

z = tonumber(x)*127+tonumber(y)
z = z*(1.0675)
z = (z/32) - 256
print (z)

#implement Callendar-Van Dusen equation to provide more accurate result
a = 0.00390830
b = -0.0000005775
z = tonumber(x)*127+tonumber(y)
z = (z/(2^15))*427
z = (-100*a+((10000*(a)^2) - 400*b*(100-z))^0.5)/(200*b)
print (z)

```

这种方法非常有效，Callendar-Van Dusen 公式提供的结果比 30°C 时的近似值高约 0.15°C。

如果你还在坚持，并且有一个水银温度计，也许是时候深呼吸一下(假设它完好无损)，抛开怀旧情绪，回收它，继续前进。