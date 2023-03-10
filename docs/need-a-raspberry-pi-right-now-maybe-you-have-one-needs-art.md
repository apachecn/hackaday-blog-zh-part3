# 几乎免费的树莓馅饼

> 原文：<https://hackaday.com/2016/05/20/need-a-raspberry-pi-right-now-maybe-you-have-one-needs-art/>

Raspberry Pi 的一个好处是它运行 Linux，你可以在板上做很多开发工作。与此相反，你可以在 Linux 桌面上做大量的开发工作，一旦你发现了最大的 bug，就可以把事情转移到 Pi 上。然而，有时候你真的需要在实际的平台上运行代码。

然而，有一个介于两者之间的解决方案，具有提升技能的额外好处:在您的桌面上模拟 Pi。如果你在桌面上使用 Linux 或者 Windows，你可以使用 QEMU 来虚拟地执行 Raspberry Pi 软件。如果您没有 Pi(或者至少没有随身携带)，这可能很有用。或者您只是想利用您的大型计算机来简化开发。当然，我们很高兴看到你构建了电子鸡奇点的[π等价物，但这超出了本文的范围。](http://hackaday.com/2015/11/24/building-the-infinite-matrix-of-tamagotchis/)

因为我使用 Linux，所以我将重点介绍这一点。如果你坚持使用 Windows，可以在 [Sourceforge](https://sourceforge.net/projects/rpiqemuwindows/) 上找到现成的项目。在大多数情况下，您应该会发现这个过程是相似的。我将要谈到的方法适用于 Kubuntu，但也应该适用于大多数其他基于 Debian 的系统，包括 ubuntu。

## 第一步。工具

你的电脑可能装有某种英特尔处理器。Pi 有一个 ARM 芯片。QEMU 是一个仿真器，可以让您在 PC 上运行 ARM 可执行文件。您需要一个静态副本和 binfmt-support 包。这种结合将让 Linux 识别外来的可执行文件并透明地运行它们。以下是您安装所需内容的方法:

```
apt-get install qemu qemu-user-static binfmt-support
```

## 第二步。树莓 Pi 图像

创建一个工作目录并下载一个 zip 格式的 Pi 映像。然后你可以解压它，创建一个 IMG 文件。以下是步骤:

```
wget https://downloads.raspberrypi.org/raspbiimg/raspbian-2015-11-24/2015-11-21-raspbian-jessie.zip

unzip 2015-11-21-raspbian-jessie.zip
```

## 第三步。检索数据

我们需要 img 文件中的一些数字，你的可能与我的不同，这取决于你下载的内容。您要运行的命令是:

```
fdisk -lu 2015-11-21-raspbian-jessie.img
```

下面是输出，重要部分用粗体显示:

```
Disk 2015-11-21-raspbian-jessie.img: 3.7 GiB, 3934257152 bytes, 7684096 sectors 
Units: sectors of 1 * 512 = 512 bytes 
Sector size (logical/physical): 512 bytes / 512 bytes 
I/O size (minimum/optimal): 512 bytes / 512 bytes 
Disklabel type: dos 
Disk identifier: 0xea0e7380 

Device                          Boot  Start     End Sectors  Size Id Type 
2015-11-21-raspbian-jessie.img1        8192  131071  122880   60M  c W95 FAT32 (LBA) 
2015-11-21-raspbian-jessie.img2      131072 7684095 7553024  3.6G 83 Linux

```

第一个分区是引导分区，第二个是文件系统。

## 步骤 4:增加硬盘容量

基本文件系统不是很大，所以让我们把它变大:

```
dd if=/dev/zero bs=1M count=2048 >>2015-11-21-raspbian-jessie.img
```

这将为映像增加 2 GB 的空间。然而，文件系统还不知道它。首先，我们需要挂载映像，就像它是一组磁盘一样:

```
losetup -f --show 2015-11-21-raspbian-jessie.img

losetup -f --show -o $((131072*512)) 2015-11-21-raspbian-jessie.img
```

数字(131072 和 512)必须与步骤 3 中突出显示的数字相匹配。512 可能不会改变，但是文件系统的开始会改变。

除非您已经有了回送设备，否则这应该会给您一个对应于整个“磁盘”的/dev/loop0 和作为文件系统(我们想要扩展的部分)的/dev/loop1。重新创建分区表以了解额外的空间(mkpart 命令需要一些您可以从输出中读取的数字，这些数字用粗体标记):

```
$ sudo parted /dev/loop0
GNU Parted 3.2 
Using /dev/loop0
Welcome to GNU Parted! Type 'help' to view a list of commands. 
(parted) print                                                             
Model: Loopback device (loopback) 
Disk /dev/loop0: 6082MB 
Sector size (logical/physical): 512B/512B 
Partition Table: msdos 
Disk Flags:  

Number  Start   End     Size    Type     File system  Flags 
 1      4194kB  67.1MB  62.9MB  primary  fat16        lba 
 2      67.1MB  3934MB  3867MB  primary  ext4

(parted) print

(parted) rm 2

(parted) mkpart primary 67.1 6082

(parted) quit

$ e2fsk -f /dev/loop1
$ resize2fs /deve/loop1
$ losetup -d /dev/loop[01]

```

## 步骤 5:挂载文件系统

创建一个目录作为挂载点。我一般只是在当前目录下做一个名为 mnt 的目录。您需要以 root 用户身份安装并使用在步骤 3 中找到的偏移量(在本例中是 8192 和 131072):

```
mkdir mnt
sudo mount 2015-11-21-raspian-jessie.img -o loop,offset=$((131072*512)),rw mnt
sudo mount 2015-11-21-raspbian-jessie.img -o loop,offset=$((8192*512)),rw mnt/boot
sudo mount --bind /dev mnt/dev
sudo mount --bind /sys mnt/sys
sudo mount --bind /proc mnt/proc
sudo mount --bind /dev/pts mnt/dev/pts
```

## 步骤 6:修改 ld.so.preload 并复制可执行文件

作为 root 用户，您需要用您喜欢的编辑器(当然是 emacs)编辑 mnt/etc/ld.so.preload。如果你愿意，你可以使用 vi 或者你选择的其他编辑器。请确保您是 root 用户。只要在你会发现的那一行前面加上一个井号(#)。不这样做将导致非法指令错误在以后弹出。

此外，您需要 qemu-arm-static 可执行文件用于新的伪 Raspberry Pi:

```
sudo cp /usr/bin/qemu-arm-static mnt/usr/bin
```

## 第七步:Chroot！

chroot 命令将使 Pi 的文件系统看起来像根目录(在一个 shell 窗口中)。然后，您可以将用户更改为 pi(或您想要配置的任何其他用户):

```
cd mnt
sudo chroot . bin/bash
su pi
```

## 使用它

你怎么知道它在工作？尝试 uname -a 命令。您应该看到一个 armv7l 处理器类型。您可以像在 Pi 上一样运行可执行文件。如果你想使用 X，设置 DISPLAY=:0 来使用你的主屏幕。例如:

```
DISPLAY=:0 dillo
```

或者您可以设置所有程序的显示:

```
export DISPLAY=:0
```

## 可选:闪烁它

现在你已经准备好了。经过一些开发后，您可能想要保存您的工作。您需要做的就是退出 chroot(键入 exit)并将/etc/ld.so/preload 改回来(删除您添加的#字符)。然后你应该卸载你挂载的所有东西。图像文件将保留，并将包含您的所有更改。您可以刷新它，并且可以通过重复 chroot 和 mount 指令来重新加载它。

## 概括起来

有很多方法可以在 PC 上为 Raspberry Pi 进行交叉开发。这是其中之一。然而，它也指出了使用 QEMU 运行外来可执行文件的能力。这是一个你可以在许多不同的开发板和平台上使用的技巧。有针对几种 CPU 类型的 QEMU 仿真器，从 Microblaze 到其他 ARM 变体到 PowerPC，再到 S390。快速浏览一下 qemu-*-static 的/usr/bin 目录，您会看到一个列表。

当然，得到圆周率并使用它很容易。但是当你需要的时候，这是另一个进行交叉开发的工具。