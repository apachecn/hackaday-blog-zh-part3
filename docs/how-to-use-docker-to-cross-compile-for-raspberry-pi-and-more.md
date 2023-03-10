# 如何使用 Docker 为 Raspberry Pi(以及更多)进行交叉编译

> 原文：<https://hackaday.com/2016/09/01/how-to-use-docker-to-cross-compile-for-raspberry-pi-and-more/>

过去，建立交叉编译环境是很乏味的。当然，你可以在 Raspberry Pi 本身上编译，但有时你想使用你的大型计算机——当你的 Pi 不在手边时，比如在飞机上带着笔记本电脑时，你可以使用它。为任何构建工具设置交叉编译器可能很棘手，但是如果你完成一个简单的步骤，不管你的真实计算机是什么样子，它都会变得超级容易。这一步是安装 Docker。

Docker 可用于 Linux、Windows 和 Mac OS。它允许开发人员构建映像，这些映像本质上是运行某些服务的预配置 Linux 环境。就像虚拟机一样，这些映像可以一起运行，而不会相互干扰。与虚拟机不同，Docker 容器(运行软件)是轻量级的，因为它们共享相同的底层内核和计算机硬件。

事实是，设置 Raspberry Pi 构建环境并不容易。只是有了 Docker，其他人已经为你做了工作，你可以自动获取他们的设置并保持更新。如果你已经在运行 Linux，你的包管理器可能也会让这个过程变得非常简单(参见[Rud Merriam]关于这个过程的文章)。然而，映像的好处是它是一个完全隔离的环境，可以从一台机器移动到另一台机器，从一个平台移动到另一个平台(Windows 和 Mac 平台使用各种技术来运行 Linux 软件，但它是透明地完成的)。

## 安装 Docker

如果你没有使用 Linux，你需要弄清楚如何安装 Docker。在 Windows 下有几种方法(取决于你用的是什么版本的 Windows)而且我不用 Mac。然而，在 Linux 上，您应该能够通过您的包管理器安装您需要的东西。

在 Ubuntu 和其他类似的发行版中，您可能希望安装 Docker 包。有道理，但不是。该软件包是一个系统托盘图标管理器。你想要的是 docker.io:

```
sudo apt-get install docker.io
```

您将看到一些建议的包，如果您想要的话，可以考虑在 apt-get 中添加–install-suggests 选项。

Docker 由两部分组成:一个守护进程(后台运行的服务器)和一个名为 docker 的客户端。如果你不喜欢命令行，有多种 GUI 工具可以管理 Docker。我确实喜欢它，所以这就是我所知道的。

## 交叉编译

Docker 在他们的网站上维护了一个图片库，名为 [the Hub](https://hub.docker.com/) 。默认情况下，如果您在本地没有图像，客户端将在那里寻找它。在这种特殊情况下，您需要的映像是 sdthirlwall/raspberry-pi-cross-compiler:legacy-trusty。这很拗口，开发者提供了一个在正常情况下调用它的很好的脚本。你怎么拿到剧本的？你用 Docker，当然。

顺便说一下，默认情况下，您需要以 root 用户身份运行 Docker 客户端，尽管您也可以[创建一个特殊的组](https://docs.docker.com/engine/installation/linux/ubuntulinux/#create-a-docker-group)(尽管使用 sudo 也同样有效)。以下是运行以获取 rpxc 脚本的命令:

```
sudo docker run sdthirlwall/raspberry-pi-cross-compiler:legacy-trusty >rpxc
```

因为您的硬盘上可能没有该映像，所以客户端需要一段时间来下载它并完成任务。下一次不会花这么长时间，因为 Docker 将有一个本地副本。

您可以将 rpxc 命令设置为使用以下命令执行:

```
chmod +x rpxc
```

然后把它移到你的路径上的某个地方(或者用完整路径来引用它。/rpxc 或~/Downloads/rpxc，如果您愿意的话)。虽然您可以从 Hub 下载整个映像，但是如果您想查看文件、投稿或跟踪开发，您应该看看项目的 [GitHub repo](https://github.com/sdt/docker-raspberry-pi-cross-compiler) 。

## 在使用中

rpxc 脚本通常在新环境中运行您喜欢的任何命令。既然它运行 Docker，当然你需要 root 或者在 Docker 组中。所有常用的构建工具都以 rpxc 为前缀，所以:

```
rpxc rpxc-gcc -o hello-world hello-world.c

```

或者，如果您有一个 Makefile:

```
rpxc make
```

运行 rpxc 时所在的当前目录成为新环境中的/build 目录，并且是默认的当前工作目录。

如果你很懒，你可能更喜欢跑步:

```
rpxc bash
```

然后就可以发布命令，做自己喜欢的事情。在/usr/local/bin/rpxc*上运行 ls，查看所有可用的工具。您还可以使用 rpxc 脚本来更新图像及其本身。使用 update 命令来执行这两项操作，或者您可以指定 update-image 或 update-script。

## 码头

还有一些你可能会感兴趣的图片。你必须在 Hub 上获得一个免费账户，一旦你这么做了，你可能会认为只有很少的图片。然而，试着搜索一下覆盆子。或者 Arduino，它显示了许多预配置的 Arduino 环境。你可能也喜欢搜索 ESP8266。甚至还有 Eagle PCB 布局软件的 Docker 图像。请在下面的评论中告诉我们你最喜欢的个人资料。