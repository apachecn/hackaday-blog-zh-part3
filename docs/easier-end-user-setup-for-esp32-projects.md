# ESP32 专案的使用者设定更容易

> 原文：<https://hackaday.com/2018/01/23/easier-end-user-setup-for-esp32-projects/>

作为黑客，我们偶尔会忘记，并不是每个人都像我们一样迷恋那些无聊的琐事。通过改变代码中的一些行来配置硬件，并编译一个新的固件，对于我们这些已经经历过几次的人来说，听起来并没有什么大不了的，但对于一般人来说，这就像是古老的梵语。只要您的项目是供个人使用的，这就不是一个真正的问题，但是如果您计划为一个项目发布代码或者甚至销售成品呢？将它与硬编码变量一起发布根本不是一个选项。

[![](img/33a747e85ff654ea8687975a8f5d3c94.png)](https://hackaday.com/wp-content/uploads/2018/01/espwifi_detail1.png)

Code for loading configuration file from SPIFFS

在最近的一个视频中，[Proto G]展示了一个聪明的方法来使用 WiFiManager 使最终用户更容易地配置您的 ESP32 项目。您不仅可以使用强制网络门户系统针对附近的接入点配置 ESP32 的 WiFi，还可以允许用户输入配置数据，这些数据可以通过使用 [SPI 闪存文件系统(SPIFSS)](https://github.com/pellepl/spiffs) 在您的代码中获取。

有了[Proto G]在下面的视频中演示的设置，你不需要比网络浏览器更多的东西来配置设备。最终用户只需搜索设备的 WiFi 网络，连接到该网络，就会看到一个易于理解的对话框，让他们选择要配置的 WiFi 网络，以及一些要输入自定义变量的字段。所有这些信息都存储在 SPI 闪存的一个文件中。当 ESP32 重新启动时，它会从保存的文件中读取配置并应用请求的设置。

这非常类似于现在配置了多少消费类设备，即使是对这种设备不太熟悉的人也应该能够通过一点手动操作来完成设置。如果您计划将您的一个 ESP32 项目交给 John Q. Public，这是您应该瞄准的配置类型。

我们已经介绍了使用 WiFiManager 使 ESP32 项目更容易管理的[，但是向强制门户添加任意变量带来了许多可能性。这正是你开始](https://hackaday.com/2017/03/18/configure-esp8266-wifi-with-wifimanager/)[考虑向商业产品](https://hackaday.com/2017/12/20/taking-a-guitar-pedal-from-concept-into-production/)飞跃时所需要的东西。

 [https://www.youtube.com/embed/saAv7YOiAyM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/saAv7YOiAyM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

