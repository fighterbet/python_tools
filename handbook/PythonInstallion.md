# python 安装详细教程

本文将介绍以下几部分内容：
- 下载 python
- 安装 python
- 配置环境变量
- python 多版本共存配置
- python 编程工具推荐

## 一、下载 python
### 下载 python

[点击这里](https://www.python.org/downloads/windows/) 进入 python 下载页面

在下载页面可以看到很多不同版本的下载链接。其中，标记 x86 的为 32 位安装包，x86-64 为 64 位安装包。executable installer为完整的安装包，下载完即可安装；web-based installer 体积更小，但安装时仍需联网下载其他部分。一般网络不好时选择 executable installer，以保证安装过程不会中断。

![python下载官网](https://upload-images.jianshu.io/upload_images/23208742-d5e1e8f59969762e.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)


操作系统的位数可通过以下操作确定：右击此电脑 -> 点击属性 -> 查看位数

![查看操作系统位数（1）](https://upload-images.jianshu.io/upload_images/23208742-d19a5a4c197e51b4.png?imageMogr2/auto-orient/strip|imageView2/2/w/682/format/webp)

![查看操作系统位数（2）](https://upload-images.jianshu.io/upload_images/23208742-8c00699bd96279bd.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

### python 版本简介

python 包括 python2、python3 两个大版本，其中 python3 改进了 python2 的一些不足，但由于以前很多应用是用 python2 开发的，维护这些应用还需用到 python2，故 python2 尚未被完全淘汰。

此外，版本也不是越高越好，因为有的模块（库）不支持太高版本的 python。

## 二、安装 python

1.打开安装包所在文件夹，双击开始安装。

![安装步骤1](https://upload-images.jianshu.io/upload_images/23208742-38af943ea84c3524.png?imageMogr2/auto-orient/strip|imageView2/2/w/1020/format/webp)

2.勾选 "Add Python to PATH" 复选框，点击 "Customize installaion"。

![安装步骤2](https://upload-images.jianshu.io/upload_images/23208742-2634503132827d47.png?imageMogr2/auto-orient/strip|imageView2/2/w/1047/format/webp)


3.保持默认设置，点击 "next"。

![安装步骤3](https://upload-images.jianshu.io/upload_images/23208742-47cd8b2685b9e8bf.png?imageMogr2/auto-orient/strip|imageView2/2/w/1046/format/webp)

4.修改安装路径（记住此路径，后面可能会用到），可以是任意空间充足的盘（这里直接将 C 改为 D） -> 点击 "Install" 开始安装。

![安装步骤4](https://upload-images.jianshu.io/upload_images/23208742-4bc9e400de83ff33.png?imageMogr2/auto-orient/strip|imageView2/2/w/1046/format/webp)

5.安装完成后，如下操作打开命令行：同时按 "Windows+R"  -> 输入 "cmd"  -> 点击确定。

![安装步骤5](https://upload-images.jianshu.io/upload_images/23208742-5b653a758642dd92.png?imageMogr2/auto-orient/strip|imageView2/2/w/648/format/webp)

6.输入 "python" -> 按回车键，若出现下图显示的信息，表明安装成功（命令行变为三个大于号）。

![成功安装提示](https://upload-images.jianshu.io/upload_images/23208742-77fed36f5ad5c857.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

7.若显示下图的信息，则需要手动配置环境变量（参考下一节）。

![需要配置环境变量](https://upload-images.jianshu.io/upload_images/23208742-c73f2c4a334589d8.png?imageMogr2/auto-orient/strip|imageView2/2/w/797/format/webp)

## 三、环境变量配置

命令行在查找可执行文件时，现在当前目录找，如果找不到，就会在 Path 变量指定的目录找。因此，将可执行文件的路径添加到 Path 中，可以保证在任意路径都能执行程序。

### python 环境变量配置

1.右击此电脑 -> 单击属性

![配置环境变量1](https://upload-images.jianshu.io/upload_images/23208742-441a76c87433595c.png?imageMogr2/auto-orient/strip|imageView2/2/w/682/format/webp)

2.点击左侧的"高级系统设置"

![配置环境变量2](https://upload-images.jianshu.io/upload_images/23208742-3e2d4dcbdd7e1a6f.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

3.点击 "环境变量"（有的电脑可能要手动选择上面的 “高级” 选项卡）

![配置环境变量3](https://upload-images.jianshu.io/upload_images/23208742-d35072274f887109.png?imageMogr2/auto-orient/strip|imageView2/2/w/770/format/webp)

4.单击选中"Path" -> 单击编辑

![配置环境变量4](https://upload-images.jianshu.io/upload_images/23208742-5d110817350b6fa0.png?imageMogr2/auto-orient/strip|imageView2/2/w/988/format/webp)

5.打开 python 的安装路径（安装时设置的，可能跟笔者不同） -> 点击地址栏 -> "Ctrl+C" 复制路径

![配置环境变量5](https://upload-images.jianshu.io/upload_images/23208742-445d97c74146d3ad.png?imageMogr2/auto-orient/strip|imageView2/2/w/1140/format/webp)

6.在 “编辑环境变量” 选项卡 单击新建

![配置环境变量6](https://upload-images.jianshu.io/upload_images/23208742-f6a212040024b652.png?imageMogr2/auto-orient/strip|imageView2/2/w/845/format/webp)

7.粘贴路径 -> 点击确定

![配置环境变量7](https://upload-images.jianshu.io/upload_images/23208742-3c5b423353b87525.png?imageMogr2/auto-orient/strip|imageView2/2/w/845/format/webp)

### 注意事项
- 有时候配置了环境变量，在命令行输入 "python" 会弹出微软商店。解决办法是将 python 的路径上移到微软商店前面：

![上移路径](https://upload-images.jianshu.io/upload_images/23208742-8409aada2cc40f9a.png?imageMogr2/auto-orient/strip|imageView2/2/w/845/format/webp)

- 从以上问题可以看到，命令行在前面找到了可运行的程序后，会忽略后面的项。

- 在环境变量窗口，我们可以看到 “用户变量” 与 “系统变量” 两种变量，两种变量的区别是：用户变量是对单一用户生效，系统变量对所有用户生效。如果电脑设置了多个用户，设置用户变量会使得安装软件只能供单一用户使用，设置系统变量则所有用户都能使用。

### pip 环境变量配置

python 常常用到 pip 工具安装第三方库（模块），pip 工具通常是随着 python 一起安装好的，但是使用 pip 安装库时，可能会出现下面的错误提示：

![pip需要配置环境变量](https://upload-images.jianshu.io/upload_images/23208742-11d1e799aa75f33e.png?imageMogr2/auto-orient/strip|imageView2/2/w/654/format/webp)

这同样可以通过配置环境变量解决，配置步骤是完全一致的。要注意的是，pip 工具在 python 目录的 Scripts 文件夹下。

![pip所在文件夹](https://upload-images.jianshu.io/upload_images/23208742-7bcf4610f4297333.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

另外，在使用 pip 安装库时，可能会提示 pip 版本太旧了，此时只需执行提示命令即可更新 pip：

![更新pip](https://upload-images.jianshu.io/upload_images/23208742-f8b09194f992a071.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

## 四、python 多版本共存配置

由于特殊需要，我们可能要在一台电脑安装多个版本的 python。示例安装了 python2.7，顺便提一下，该安装包是"MSI installer"，这跟"executable installer"基本相同。

![python2下载](https://upload-images.jianshu.io/upload_images/23208742-3304d3c92a4fcd89.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

安装完成 python2.7 后，笔者按下图所示配置了环境变量：

![多版本python环境变量配置](https://upload-images.jianshu.io/upload_images/23208742-09c2e727e84861c2.png?imageMogr2/auto-orient/strip|imageView2/2/w/541/format/webp)

此时在命令行执行"python"命令，进入的是 python2.7：

![多版本python调用](https://upload-images.jianshu.io/upload_images/23208742-022e6d4e88a9d7e3.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

怎么进入 python3 呢？以 python2 为例，如下操作：

1.打开 python2 目录 -> 复制 "python.exe" -> 直接粘贴，得到一个副本

![复制python.exe获得一个副本](https://upload-images.jianshu.io/upload_images/23208742-8a0733d09feebfa5.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

2.将副本命名为可区分的名字（此处为python2）

![重命名副本](https://upload-images.jianshu.io/upload_images/23208742-478135be7f7444dd.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

经过上述操作，在命令行键入"python2"即可进入 python2。
同样的步骤可以应用在 python3 及 不同版本的 pip 工具中。

## 五、python 编辑工具推荐

不瞒大家，当初学 python 时，是用的 IDLE 编程，那个界面实在难看，让我对 python 的热情骤减了许多。

后来在b站看到一个教程，里面用的工具界面很好看，然后笔者也搞了一个，用来做小段的代码练习很方便，这个工具就是 jupyter notebook 了。安装方式很简单，只需在命令行执行：

```
pip install jupyter
```

另外，要写一些比较大的项目，推荐 [pycharm](https://www.jetbrains.com/pycharm/download/#section=windows)。
