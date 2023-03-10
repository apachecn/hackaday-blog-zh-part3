# 黑客字典:全球定位系统(GPS)

> 原文：<https://hackaday.com/2015/11/12/hackaday-dictionary-the-global-positioning-system-gps/>

全球定位系统(GPS)是现代设备的基础技术之一。利用绕地球轨道运行的卫星发出的信号，GPS 接收器可以以惊人的精度锁定其位置:由美国 GPS 系统 [发送的最新一代民用导航信号(CNAV)](http://www.gps.gov/)[精度不到半米](http://www.navcen.uscg.gov/?pageName=CNAV_Performance) (约 3 英尺)。这些信号还包含时间，精确到毫秒，这使得它非常适合离线数据记录器和需要非常精确的时间系统。这是一个强大的组合，使 GPS 成为移动革命背后的主要技术之一，因为它让小工具知道它们在哪里(何时)。

### 全球定位系统的起源

![Transit 2A being readied for launch](img/34abfe9a28de8d2ee371b24fd176b40a.png)

Transit 2A being readied for launch

全球定位系统的想法可以追溯到很久以前。第一个 GPS 系统于 1964 年投入使用:使用五颗卫星，美国海军创建了[运输系统](https://en.wikipedia.org/wiki/Transit_(satellite))来帮助北极星导弹潜艇导航。现代 GPS 系统始于 1973 年，并于 1978 年随着第一颗卫星投入使用。虽然军方建造并运行这些系统(美国空军现在运行 GPS 系统)，但它们的设计目的是供平民和军方使用。第一台民用手持 GPS 接收机是[麦哲伦 NAV 1000](http://collections.si.edu/search/tag/tagDoc.htm?recordID=nmah_1405613) ，1989 年以整整 3000 美元售出。最初，民用信号是用一种称为选择性可用性(SA)的系统加密的，这种系统限制了民用信号的准确性，但在 2000 年一架韩国客机[由于导航系统故障误入俄罗斯领空](http://www.history.com/this-day-in-history/korean-airlines-flight-shot-down-by-soviet-union)并被击落后，该系统被取消。

从那以后的几年里，全球定位系统不断升级，以取代旧的卫星，增加新的信号和技术。现在，GPS 系统由 24 颗现役卫星(以及少量备用)组成，其中 11 颗是最新一代型号(称为 [区块 IIF](http://www.gps.gov/systems/gps/space/#IIF) )。他们的下一代将于 2016 年开始发射。

然而，美国不再是唯一的游戏城市:俄罗斯人创造了他们自己的系统(称为[【GLONASS】](http://sputniknews.com/trend/glonass_13012010/))，拥有 24 颗卫星。中国人也在推出他们自己的导航系统，名为 [【北斗】](http://sinosphere.blogs.nytimes.com/2014/12/04/a-step-forward-for-beidou-chinas-satellite-navigation-system/) ，目前有 10 颗卫星在轨运行。欧盟也在建立另一个名为 [伽利略](http://www.esa.int/Our_Activities/Navigation/The_future_-_Galileo/What_is_Galileo) 的系统，该系统将提供类似的定位服务。

这对用户来说是一个额外的好处:通过使用多个 GPS 系统，你可以更准确地确定位置，或者在没有 GPS 系统的情况下仍然可以导航。许多现代 GPS 接收器可以同时使用 GPS 和 GLONASS 网络，使用其他网络的接收器将很快问世，因为它们的工作方式基本相同:通过测量信号到达接收器所需的时间。

### GPS 是如何工作的

[![The constellation of GPS satellites in orbit. From Wikipedia](img/ff5fca7e1b926f315e15902faf476e7c.png)](https://commons.wikimedia.org/wiki/File:ConstellationGPS.gif)

The constellation of GPS satellites in orbit. From Wikipedia

现代 GPS 系统在不同的频率上为不同的用户和冗余发出许多信号，但它们都基于相同的基本原理工作。最初的信号在两个频率上(L1 在 1575.42MHz，L2 在 1227.6MHz)，但后来增加了其他频率(L3 在 1381.05MHz，L4 在 1379.913MHz，L5 在 1176.45MHz)。这些较新的设备用于分析大气，以了解大气如何影响信号，从而进一步提高接收信号的设备的准确性。大多数单片机系统只使用 L1 信号。

每颗卫星都将数据流编码成这些信号，这些信号由卫星上的原子钟和每颗卫星的单独代码生成。这种编码创建了一个伪随机数据流:它看起来是随机的，除非你知道每个卫星的代码(称为黄金代码)。有了这个，你可以解码各种数据流，包括粗/采集(C/A)流，L1 民用(L1C)和军用(M)流。这些数据流中的每一个都包含大约每秒 50 比特的数据。顾名思义，C/A 流是一个短的、频繁重复的数据批次，用于粗略导航。其他流包含更详细的数据，允许更精确的定位，但需要更长的时间来接收。这些数据流包含大量数据，但最有用的部分是时间，取自卫星上非常精确的原子钟。GPS 接收器使用这一精确的时间数据，通过查看几个卫星信号之间的差异来确定位置。

[![If you know the distance to 3 GPS satellites, you can calculate your location. from wWkipedia](img/835518c35c4f2be1b2f0d331bdfa05ee.png)](https://commons.wikimedia.org/wiki/File:GPS_Spheres.svg)

If you know the distance to 3 GPS satellites, you can calculate your location. from Wikipedia

想象一下这样一个场景:一颗 GPS 卫星在你头顶上方约 12，000 英里处。从你的角度来看，另一个在地平线上更低，这意味着它在另一个轨道上，距离更远:它可能高达 30，000 英里。来自地平线卫星的信号需要传播更远的距离，所以到达你这里需要更长的时间。如果您知道两颗卫星的时钟都是同时设置的，那么您可以通过测量两颗卫星发送的时间信号之间的差异来确定两颗卫星之间的距离。这种差异很小(不到 90 毫秒)，但却是可以测量的。在另一个位置加上第三颗卫星，你就得到了另一个距离，形成一个三角形。接收器还知道卫星的轨道(称为星历表)，因此通过结合至少三颗卫星之间的时间和距离，它可以计算出其位置。添加第四颗卫星来提供更多数据，它也可以计算其高度。

来自 GPS 卫星的信号还包含许多其他数据，例如所有卫星的更新星历表，以及关于大气如何影响信号的信息。GPS 接收器接收并存储这些数据，用它来更新卫星列表。这就是为什么一段时间没有使用的 GPS 接收器通常需要很长时间来确定位置(称为冷定位):如果有新的卫星发射或其他它不知道的变化，它可能需要一些时间来发现信号并捕捉新的信息。

如今，所有这些复杂的信号处理和数学通常都被封装在一个芯片中:一个 GPS 接收器，它接收信号，处理信号并运行数据。他们一次可以跟踪多少颗卫星取决于卫星的类型，但是当卫星落到地平线以下，新的卫星进入视野时，可以跟踪大量卫星的接收器将更好地保持计算位置。卫星的运动也会改变频率(因为多普勒效应)，因此接收器可能需要监听多个频率，以接收靠近和远离接收器的卫星。跟踪单个信号的能力被称为信道，大多数现代接收机都有很多这样的信道:例如， [联发科 MTK3339 GPS 芯片](http://inmotion.pt/documentation/diydrones/MediaTek_MT3329/mediatek_3329.pdf)[Adafruit Ultimate GPS 分线板](http://www.adafruit.com/products/746) 上有 66 个信道，因此它可以在多个频率上跟踪多个卫星。

所有这一切的最终结果是 GPS 接收器找到位置，然后将其反馈给设备。对于大多数 GPS 芯片来说，这是以串行输出的形式发送的，串行输出以一种称为[【NMEA】0183](http://gpsworld.com/what-exactly-is-gps-nmea-data/)(NMEA 指的是国家海洋电子协会，该协会制定了船上电子系统的标准)的格式发送数据。这些数据可以包含当前时间、位置、速度和其他信息，以纯文本形式发送。各种卫星的信号强度信息也被发送，因此处理数据的设备可以显示它。

### 如何使用 GPS

![The Adafruit Ultimate GPS Breakout Board](img/f00bd240196346e345eba0ca31b672be.png)

The Adafruit Ultimate GPS Breakout Board

将 GPS 添加到您正在构建的设备的最简单方法是添加 GPS 包。这些包括天线、接收器和足够的智能来进行计算。你只需给芯片供电，让它看到天空，它就会输出时间、位置和其他信息。由于 GPS 和移动设备的多年发展，这些设备很便宜:Adafruit 提供了一个分线板，包括联发科技 MTK3339 GPS 芯片，价格不到 40 美元。其他类似的设备可以从 Sparkfun 获得，他们也有很好的 [不同类型](https://www.sparkfun.com/pages/GPS_Guide) 的指南。这些设备有内置天线，但它们很小，可能接收信号不好。为了获得更好的性能，增加一个 [外置天线](https://www.sparkfun.com/products/464) ，可以接收更多的这些微弱信号。

你们当中特别有受虐狂倾向的人可能想尝试建造自己的 GPS 接收器。这是可能的，尽管它需要一些昂贵的设备。你需要一个可以接收 1.5GHz 频率的软件无线电(SDR)，以及一些解码信号的软件。在下面的视频中，[Taroz]正在使用一个[BladeRF SDR](http://www.nuand.com/)和他编写的[GNSS-SDR lib](http://www.taroz.net/gnsssdrlib_e.html)软件。

 [https://www.youtube.com/embed/vVHOFs93vlU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vVHOFs93vlU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

