# 用 ESP8266 驾驶索尼相机

> 原文：<https://hackaday.com/2016/01/09/drive-a-sony-camera-with-an-esp8266/>

现在几乎所有东西都有 WiFi。[glaskugelsehen]的索尼相机自然使用无线网络将照片传输到电脑上，它还有一个可以在 Android 智能手机上运行的远程控制应用程序。[glaskugelsehen] ~~没有安卓系统——但是他有~~向我们展示了一个 ESP8266，他[把它变成了一个 WiFi 遥控相机](https://glaskugelsehen.wordpress.com/2016/01/08/sony-camera-remote-control-mit-esp8266/) ( [谷歌翻译成英语](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https%3A%2F%2Fglaskugelsehen.wordpress.com%2F2016%2F01%2F08%2Fsony-camera-remote-control-mit-esp8266%2F&edit-text=&act=url))。

索尼实际上让[glaskugelsehen]的工作变得很容易。他们有一个[公开可用的 API](https://developer.sony.com/develop/cameras/) 用于相机的控制，这都是由 JSON 通过 ~~HTML~~ HTTP POST 发送的。也就是说，只要你能发送 ~~HTML~~ HTTP ~~指令~~，编写脚本就是小菜一碟。

[glaskugelsehen]在 Arduino 环境中为 ESP 编写的代码首先找到摄像机的 WiFi 网络并对其进行认证。然后，它将相机设置为遥控模式，并从那里接管。到目前为止，他只实现了拍摄静态照片，但从 API 来看，似乎你也可以停止和开始视频记录等等。

是的。我们刚刚写了另一个项目[，用 GoPro](http://hackaday.com/2016/01/05/esp8266-gopro-remote-adds-buttons-screen/) 做了几乎相同的事情。[glaskugelsehen]也读到了，并在他的博客中提到了这一点。我们喜欢人们从彼此身上获取灵感！