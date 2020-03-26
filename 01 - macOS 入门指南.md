# 1. Mac & macOS

-  **Mac**：指的是苹果电脑。苹果公司把自己生产的一系列电脑统称为 Mac。
  - Mac 笔记本包括 MacBook（停售）、MacBook Air（在售）、MacBook Pro（在售）。
  - Mac 一体机名字叫 iMac，性能更好的一体机叫 iMac Pro。
  - Mac 主机有两个，一个是 Mac Pro（性能最强）、另一个是 Mac mini（主打便携）。

![](http://qncdn.bujige.net/images/20200325153748.png)

- **macOS**：类似于大部分电脑中安装的 Windows 系统，苹果电脑运行的系统就是 macOS。如果你以前使用的是 Windows 电脑，那么第一次使用 macOS 可能会有很多不适应的地方，这很正常。

  接受新事物总需要有个磨合的过程嘛。请抱着第一次接触电脑一样的心态去学习使用 macOS 吧。等你适应之后，它将会成为你工作、生活、娱乐上的好伴侣。

    

# 2. macOS 和 Windows 异同

## 2.1 软件并不通用

Windows 系统下的软件后缀名通常为`.exe`，而 macOS 系统下的软件后缀名为`.app`。只有软件厂商专门为 macOS 编写相应的软件才能在 macOS 上运行（通常为某某软件 Mac 版 / 某某软件 for Mac 版）。当然，很多软件会同时提供 Windows 和 macOS 版，我们直接下载对应的 macOS 版本就好了。

![](http://qncdn.bujige.net/images/20200325161045.png)


## 2.2 文件结构不同

macOS 的文件系统格式是 APFS，而 Windows 的文件系统格式是 NTFS。因为版权和商业上的原因，macOS 名义上只能读取 NTFS 格式的硬盘，不支持写入。但是我们可以使用第三方付费软件（例如 [Paragon NTFS](https://china.paragon-software.com/home-mac/ntfs-for-mac/)、[Tuxera NTFS](https://www.tuxera.com/products/tuxera-ntfs-for-mac-cn/)）来读写 NTFS 格式的硬盘，或者将移动硬盘改为兼容格式（ExFAT）。

macOS 中的硬盘也可以分区，但是不像 Windows 一样有「C 盘、D 盘、E 盘、F 盘」这种「盘符」的概念。每个磁盘只有一个名称，没有字母序号。

`Macintosh HD` 就相当于 Windows 的 C 盘。 `Macintosh HD` 盘里分为 **「系统」**、**「资源库」**、**「应用程序」**、**「用户」** 几个文件夹。**「系统」** 相当于 Windows 的 C 盘中的 `WINDOWS` 文件夹，存放的是操作系统文件，不要进行修改。**「资源库」** 里存放这一些系统和软件的配置，不要随意修改。**「应用程序」** 相当于 Windows 中的 `Program Files` 文件夹，应用软件安装在这里边。**「用户」** 相当于 Windows 中 `C:/User/` 文件夹。里边为每一个用户创建了一个用户文件夹（文件夹名为用户名称），每个用户文件夹里包含了**「下载」**、**「文档」**、**「音乐」**、**「电影」**、**「桌面」**、**「图片」** 等文件夹，这里跟 Windows 里边是一样的。



## 2.3 键盘快捷键不同

Windows 上有四个常用控制键：Shift、Ctrl、Alt、WIN 键。

macOS 上也有四大控制按键 **⇧（shift）**、**⌃（control）**、**⌥（option/alt）**、**⌘（command）**。

macOS 上的常用快捷键和 Windows 略有不同，大体上是相似的。

不同点比如 Windows 上复制、粘贴的快捷键是 **Ctrl + C**、**Ctrl + V**。而 macOS 上是 「**⌘ + C**」、「**⌘ + V**」。

## 2.4 其他习惯不同

macOS 的桌面、顶部菜单栏、Dock 程序坞、Finder 等都和 Windows 有相似的地方，又有特别的地方。这些我们在接下来的 macOS 使用中来讲解。



# 3. macOS 使用

## 3.1 登录

在开机并设置新的 Mac 时，你将会看到提示使用 Apple ID 登陆的信息，当然也可以选择稍后登陆。使用 Apple ID 登陆可以访问所有 Apple 服务并使所有设备实现无缝协作。推荐使用 Apple ID 登陆。

![](http://qncdn.bujige.net/images/20200326121551.jpg)



## 3.2 macoS 桌面

「桌面」是 macoS 的主屏幕区域。用来放置一些软件，文件，文件夹等。macOS 下的桌面和 Windows 的桌面极其相似，又有一些不同。Windows 桌面的底部结构包含「菜单栏」、「任务栏」、「工具栏」。macOS 下也能找到对应的内容。

![](http://qncdn.bujige.net/images/20200326111430.png)



- 程序坞：位置在桌面的底部中间。对应 Windows 的底部菜单和状态栏。

  - 程序坞上的图标对应是软件的快捷打开方式，全部的图标在「应用程序」或「启动台」里。
  - 最左边的笑脸文件夹是「访达」，类似于 Windows 中的「资源管理器」或者说「我的电脑」。
  - 最右边的垃圾桶样式的图标是「废纸篓」，类似于 Windows 中的「回收站」，用于回收或清除一些删除的文件。

- 苹果菜单：位置在桌面左上角，那个  图标。对应 Windows 的开始菜单。

  - 这里边包含了 macOS 的常用操作选项。包括：开机、关机、系统偏好设置。

  ![AppleMenu](http://qncdn.bujige.net/images/20200326135807.jpg)

- 应用菜单：位置在  按钮的右侧。包含了当前应用的菜单栏选项。

  - 默认显示的是「访达」的菜单栏选项，切换不同的软件会显示其对应的菜单栏选项。

- 图标栏：位置在桌面右上角。类似于 Windows 的工具栏。

  - 图标栏：默认放置了一些系统常用快捷工具。比如：「Wi-Fi」、「调节音量」、「查看日期和时间」、「输入法状态」、「聚焦搜索」、「Siri」，以及最右侧的「通知中心」。

  ![](http://qncdn.bujige.net/images/20200326140212.png)

- 通知中心：位置在桌面右上角。点击会弹出通知的侧边栏。风格类似于 iPhone 的通知中心。应用程序 的通知和快捷功能都在通知中心。这里可以显示今天的日期、天气、提醒事项等。还可以快速开关「夜览」、「勿扰模式」。

  ![](http://qncdn.bujige.net/images/20200326152519.jpg)



- 启动台：点击「程序坞」或者使用「触摸板」进行「四指缩放」操作，就可以显示 macOS 中所有安装的软件。还可以进行整理，归纳到不同的「分类文件夹」中，图标多的话，还可以分页。风格类似于 iPhone 的界面。

![](http://qncdn.bujige.net/images/20200326143759.png)



## 3.3 软件相关

### 3.3.1 软件下载

macOS 系统下的软件后缀名为`.app`。和 Windows 下的软件并不通用。我们下载对应的 macOS 版本软件。

macOS 的软件一般来说有两种常用下载方式：

- App Store：苹果官方提供的 App 商城。
- 应用官网：如果应用没有在 App Store 上线，可以去应用的官网下载 macOS 版本的软件。

> 注：关于 Mac 有哪些好用的软件，以及这些软件的官方下载渠道具体可以看我写的这篇文章： [**04 - macOS 软件清单**]([https://github.com/bujige/macOS-Tips/blob/master/04%20-%20macOS%20%E8%BD%AF%E4%BB%B6%E6%B8%85%E5%8D%95.md](https://github.com/bujige/macOS-Tips/blob/master/04 - macOS 软件清单.md))。

### 3.3.2 软件安装

macOS 版本的软件安装包后缀名通常是`.dmg` 或者是`.pkg`。

- `dmg` 是苹果的压缩镜像文件，类似于 Windows 下的 `ISO`。

  打开里面一般包含 `应用程序名.app` 的图标和一个应用程序文件夹 `/Applications` 的快捷方式。

直接将图标拖曳至应用程序文件夹，即可完成安装。

![](http://qncdn.bujige.net/images/20200325161109.png)

- `pkg` 是 macOS 下软件的安装器，按照提示，一步步点击安装即可。

![](http://qncdn.bujige.net/images/20200325161124.png)



### 3.3.3 软件卸载

Mac 下的软件卸载很简单，打开「访达」，找到「应用程序」文件夹，找到你要卸载的软件，点击右键，选择「移动废纸篓」，就完成卸载了。

![](http://qncdn.bujige.net/images/20200326152102.png)

