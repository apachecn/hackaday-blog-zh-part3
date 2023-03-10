# 最小 MQTT:控件和客户端

> 原文：<https://hackaday.com/2016/05/27/minimal-mqtt-control-and-clients/>

所以你已经[建立了一个中央服务器](http://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)并且在你的房子里放满了 [WiFi 连接的节点](http://hackaday.com/2016/05/17/minimal-mqtt-networked-nodes/)，所有节点都使用 MQTT 协议相互通信。简而言之，您已经完全解决了机器对机器的问题。现在是时候让人类参与进来了！我们将探索几个图形用户界面。

你*可以*为你整个系统的每一个小方面建立一个物理旋钮和/或 LED 显示屏，但是老实说，这才是 GUI 真正发光的地方。在 Minimal MQTT 的这一期中，我们将研究消费和产生数据的友好方式，以便与连接的传感器、开关和显示器进行交互。有很多框架可以让*使用* MQTT 来构建类似的东西，但是我们将避开中间人，直接面向一些 GUI MQTT 客户端。

[![mqtt.dot](img/5882133070795a6059ccf804e4d4af91.png)](https://hackaday.com/wp-content/uploads/2016/05/mqtt-dot.png) 我们到目前为止构建的最小系统有一个温度/湿度传感器，每十秒钟向`home/outdoors/temperature`和`home/outdoors/humidity`主题发布一次数据。(这是不现实的，但是看着它如此频繁地更新很有趣。)上次因为想在 NodeMCU 中实现一个订阅器，所以我们还有一个彩色 LED 设备，订阅`home/outdoors/temperature`，显示温度。

如果你仔细研究了上次的显示节点[代码，你可能还会注意到它订阅了一个`home/outdoors/status`主题，并相应地打开和关闭显示温度的 LED。这就是我们到目前为止要做的事情:两个数据通道，一个控制通道打开或关闭我们的显示 LED。](https://github.com/hexagon5un/hackaday_mqtt)

## 手机应用

获取这些数据最简单的方法是通过你的手机。至少对于 Android 平台，有一些免费的应用程序可以让你直接发布和订阅 MQTT 代理。在上一期中，我们使用`home/outdoors/temperature`主题将温度数据从一个节点发送到服务器。我们想让这个价值，甚至可能是它的历史，以最少的麻烦显示在我们的手机上。我们希望能够控制连接到 MQTT 代理的设备(这里，LED 充当一个简单的替身)。

### MQTT 仪表板

[![mqtt_dash](img/c991b6f4848f37e0aa89115addf30728.png)](https://hackaday.com/wp-content/uploads/2016/05/mqtt_dash.png) 我为 Android 安装和卸载了大约十个 MQTT 应用。其中最令人满意的是 [MQTT Dashboard](https://play.google.com/store/apps/details?id=com.thn.iotmqttdashboard) ，它允许您为一些 GUI 元素定义定制动作，包括文本、按钮、开关、颜色选择器等等。配置按钮或滑块来发送可配置的数字或文本数据的能力非常棒。几乎所有其他 MQTT 客户端应用程序都允许你输入条目，但是不得不在手机键盘上重复输入“off ”,没有人认为这是方便的。

对于订阅的主题，应用程序会问你数据是否是数字，如果是，当你双击一个字段时，它会绘制出一段时间的数据，这是一个免费的好功能。同样，该应用程序保留了您可以滚动浏览的最后一个非数字值的历史记录。如果你选择使用它们，你有每个主题的 QoS 等级。赢家。

您还可以订阅多个主题。所以除了跟踪你的房子，你还可以在`test.mosquitto.org`订阅`hackaday/titles`，了解这里的最新消息。

这款应用其实没什么可说的。它只是工作。

 [![Subscribe to Brokers](img/ee7fa84d0044bc8cfc53de59ab90d358.png "screen3")](https://hackaday.com/2016/05/27/minimal-mqtt-control-and-clients/screen3/) Subscribe to Brokers [![home/outdoors/#](img/f6fdbc66323113cec6c5f0cf809ba6d5.png "screen11")](https://hackaday.com/2016/05/27/minimal-mqtt-control-and-clients/screen11/) home/outdoors/# [![hackaday/titles](img/1edbbb919bc5a268bb107514f44d9a21.png "screen4")](https://hackaday.com/2016/05/27/minimal-mqtt-control-and-clients/screen4/) hackaday/titles [![Multi-Button is great](img/54443d54fa514e6d6518dbc4f8756b0c.png "screen5")](https://hackaday.com/2016/05/27/minimal-mqtt-control-and-clients/screen5/) Multi-Button is great [![Blowing on humidity sensor](img/61e354e40863deb879713fddd3f97a7a.png "screen18")](https://hackaday.com/2016/05/27/minimal-mqtt-control-and-clients/screen18/) Blowing on humidity sensor [![Fancy color selector](img/b44b96f2da16be64eb209a2956cdccc3.png "screen8")](https://hackaday.com/2016/05/27/minimal-mqtt-control-and-clients/screen8/) Fancy color selector

### 物联网交换机

[![screen20](img/a8b9945c88215ca0b25125be774473fc.png)](https://hackaday.com/wp-content/uploads/2016/05/screen20.png) 我喜欢的另一个应用程序是开源的[物联网开关](https://play.google.com/store/apps/details?id=com.cmmakerclub.iot.cmmciotswitch)，虽然不是因为它真的做了什么花哨的事情，而是因为它是一个可以从 MQTT 服务器发送和接收的原生 Android 应用程序的极简示例。另一方面，如果你只需要四个快速开关，你就可以了。(但是请注意，他们发送的是一个一字节的代码，其中四个按钮状态各由一位表示。它不是人类可读的，但对某些机器来说是机器友好的。)

我很想了解更多关于这个应用程序及其发展。这里是 GitHub 的。有清迈黑客空间的人想写一篇教程吗？

### 荣誉奖

当然，没有什么是完美的，我试用的其他应用也是如此。MyMQTT 有一个足够好的 subscribe 接口，但是为了发布，您必须一遍又一遍地重新输入消息，更糟糕的是，还要重新输入主题名称。MQTTClient 也有同样的缺陷，除了它至少允许您保存以前发送的消息，因此您只需键入“on”和“off”一次。但是如果你想，比如说，调暗一个灯泡或者选择一种 RGB 颜色，你又会难过。IOT 管理器看起来很棒，但它是专门针对家庭自动化市场的，需要详细的配置步骤，这与本系列的精神背道而驰——首先要让东西工作并保持灵活性。

我没有机会试用 iOS 应用程序，但它们看起来都有与荣誉奖相同的缺陷——大量文本的输入方法是按钮的糟糕替代品。也就是说， [MQTT Inspector](https://itunes.apple.com/us/app/mqttinspector/id758868884?mt=8) 看起来很适合调试。

## Javascript、Websockets 和 MQTT

[![paho_logo_400](img/8963812bb9ccac1a89b22934712a26da.png)](https://hackaday.com/wp-content/uploads/2016/05/paho_logo_400.png) 如果你的智能手机预装的应用程序对你来说不够灵活，下一步就是自己写一个。这稍微高级一点，但它是如此强大的选项，您应该考虑它。因为这个方法使用了一个 [Javascript MQTT 客户端](https://www.eclipse.org/paho/clients/js/)，你可以将它嵌入到一个 HTML 页面中，这意味着它可以在你的桌面或手机上运行，或者任何可以呈现网页的东西上运行。

向 MQTT 项目中添加按钮几乎与为新按钮编写 HTML 代码一样简单。你把界面做得多么精致或简单，只是网页编码的问题。采用基于 HTML 的 MQTT 路径有两个先决条件:调整我们的 MQTT 服务器以使用 Websockets，以及编写网页/应用程序。我们开始工作吧。

### Websockets 支持

如果您遵循了 Raspberry Pi [MQTT broker 安装说明](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)，您将安装一个最新版本的 Mosquitto MQTT broker，它已经编译了 Websockets 支持。如果你是一个受虐狂，并且擅长重新编译软件，你可以遵循[这个指南](http://harizanov.com/wiki/wiki-home/raspberry-pi/how-to-rasbperry-pi-install-mosquitto-with-websockets-enable/)。

接下来，您需要配置 Mosquitto，通过 Websockets 为 MQTT 使用一个特定的端口。要做到这一点，只需在`/etc/mosquitto/conf.d/`目录中创建一个文件，使用一个看似合理但随意的名称(`sudo nano /etc/mosquitto/conf.d/websockets.conf`)，并添加以下内容:

```
listener 9001
protocol websockets

listener 1883
protocol mqtt

```

然后发出命令`sudo /etc/init.d/mosquitto restart`，你应该设置好了。如果您的 Mosquitto 版本不支持 Websockets，此时您会收到类似“Websockets 支持不可用”的消息。如果没有，一切顺利，我们可以继续到网页。

### MQTT.js

[![cropped_shot_2016-05-23-235624](img/536d70d671d4f65cfd6bdd9bbb0f9b24.png)](https://hackaday.com/wp-content/uploads/2016/05/cropped_shot_2016-05-23-235624.png) 前往我的 [GitHub MQTT-Javascript 演示](https://github.com/hexagon5un/mqtt-javascript-demo)并下载一切。在您将浏览器指向包含的`index.html`文件之前，您将希望定制包含的`button_test.js`文件，以匹配您的 MQTT 服务器、Websockets 端口以及温度和状态主题的名称(如果您更改了它们),或者只是希望显示其他内容。然后在浏览器中打开`index.html`，您应该会看到来自您的温度 MQTT 流的实时数据。

设置的 HTML 部分故意保持非常简单。它只是打印出天气反馈的内容，并提供一个按钮来切换`home/outdoors/status`频道的“开”和“关”。如果您不习惯客户端 Javascript，这可以通过构建一个占位符网页，然后在页面底部加载并运行代码来实现。

`button_test.js`中的`connect()`函数开始滚动，一旦它接收到一些数据，它通过 id 找到标题`<h3>`元素，然后用从 MQTT 服务器接收到的新值替换它们的默认文本。所有剩下的工作都发生在您的浏览器中，因为它运行`button_test.js`中的代码和包含的 Paho MQTT Javascript 客户端代码。

[![javascript4](img/179afce8935679b2f6e7d2ea5b42288c.png)](https://hackaday.com/wp-content/uploads/2016/05/javascript4.png) 从结构上看，这里的代码与我们上次编写的 NodeMCU 代码没有太大的不同。有一个`connect()`函数构建了一个 MQTT 客户机对象，并向它注册了一些回调函数，这些函数在我们获得新数据等时执行。大多数神奇的事情都发生在`onMessageArrived()`函数中。当您按下网页上的按钮时，会调用`led_toggle()`功能。

最后一个小细节:Javascript 在连接到 MQTT 服务器时会创建一个随机 ID，这意味着您可以使用相同的代码从多个 web 浏览器实例进行连接，但是您不会获得持久性的优势，因为每次页面刷新时都会重新计算 ID。

我绝不是一个优秀的 Javascript 程序员，但我知道基本知识，并且能够从这个[客户端演示代码](http://www.eclipse.org/paho/clients/js/utility/index.html)和[文档](http://www.eclipse.org/paho/files/jsdoc/index.html)中拼凑出这个演示。让它看起来不错，并将其扩展到包含您的整个设备系统，这取决于您。

还要注意，这个网页是完全静态的——它完全是客户端 Javascript，不需要网络服务器。这意味着你可以将这些文件复制到手机上，然后直接在浏览器中打开。所有工作都是在 Javascript 代码和 MQTT 代理之间完成的。

或者，如果您觉得有趣，您可以在充当 MQTT 服务器的同一个 Raspberry Pi 上托管它。这个选项可能涉及很多配置，超出了本文的范围，但是也可以像[下载 Apache](https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md) 并将示例代码目录移动到`/var/www/html`目录一样简单。然后房子里的每个人都可以通过访问同一个网页来开灯或关灯。(这在您的 WLAN 中是没问题的，但是不要在您的 Raspberry Pi 上配置一个面向外部的 web 服务器，除非您对安全性有所了解。)

## 结论

我在这里介绍的两个选项，一个是用于手机的 MQTT 客户端应用程序，另一个是定制的 HTML/Javascript，它们都直接订阅 MQTT 代理，从这个意义上说，它们与您用作传感器、显示器或控制节点的“东西”是平等的。这种方法的美妙之处在于一切都是可互操作的，MQTT 提供了通用的通信协议。当你的手机应用程序更新一个主题来开灯时，不仅灯会收到信息，而且订阅该主题的任何其他客户端都会立即更新。

这种方法的缺点是，它可以很快变成东拼西凑。MQTT 只为您提供沟通的渠道——您的设备在说什么，以及您如何解释，完全取决于您。如果你在一个主题中使用“开”和“关”，不要在另一个主题中使用“1”和“0”，否则会以眼泪收场。

但是，如果这个系列向您展示了什么，我希望它是如何简单地让数据在您的 DIY(和其他)小工具之间流动，现在到手机屏幕或网页，您可以控制和显示所有这些。在下一期，也是最后一期，我们将解决一些困难的问题。也就是说，当您想要将 MQTT 系统的覆盖范围扩展到您自己的家庭 WLAN 之外时，安全选项、ESP8266 方面的电源管理，以及一些可以为您的智能家居带来一些真正智能的服务器端应用程序。