# Jupyter Notebook 安装配置与使用教程

本文将介绍以下几部分内容：
- jupyter notebook 的安装
- jupyter notebook 的使用
- jupyter notebook 的一些配置

## 一、jupyter notebook 的安装
jupyter notebook可以在命令行中直接安装，也可以随着 Anaconda 的安装一起安装。

### 命令行安装
打开命令行，执行以下命令即可安装：

```
pip install jupyter
```

### 随着 Anaconda 一起安装
Anaconda 是一个包含许多科学工具包的 python 发行版本，许多科学计算、人工智能的教程都推荐使用该软件。在安装 Anaconda 时，会同时安装好 jupyter notebook。

Anaconda 的安装及介绍可参考这篇文章：「[Anaconda介绍、安装及使用教程](https://www.jianshu.com/p/62f155eb6ac5)」

## 二、jupyter notebook 的使用
### 1、打开jupyter notebook

- 如果是用命令行安装的，则可以在命令行输入 `jupyter notebook` 打开笔记本：

![命令行打开](https://upload-images.jianshu.io/upload_images/23208742-b2ec434a52bca91f.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

也可以双击 python 安装目录中 Scripts 文件夹下的 jupyter-notebook.exe 打开：

![可执行程序打开](https://upload-images.jianshu.io/upload_images/23208742-28b5c695bc04af2c.png?imageMogr2/auto-orient/strip|imageView2/2/w/1100/format/webp)

- 如果是随着 Anaconda 安装的，则可以利用快捷方式打开（在开始菜单的 Anaconda 中可以找到）。

执行打开操作后，就进入到 jupyter notebook 的首页（运行在浏览器中）。

点击右上角的 new，选择 python 即可创建一个新的 python 编程文件：

![新建文件](https://upload-images.jianshu.io/upload_images/23208742-cb435384492f3345.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

### 2、界面介绍
新建文件后，就进入到 “主角” 了：

![主界面元素](https://upload-images.jianshu.io/upload_images/23208742-a6a3d06c15fb8a79.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

刚进工作区是空的，但为了方便介绍，笔者提前编辑了一些内容。

标题，就是标题啦，单击就可以重命名。

菜单栏没什么值得关注的，工具栏包含了一系列用的比较多的操作。

工作区是最能体现 jupyter notebook 亮点的地方了，它由一个一个的 “块” 组成。

### 3、认识 “块”
“块” 是 jupyter 中可以独立运行的单位，点击工具栏中的 “代码” 下拉列表框可以改变当前块的类型，其中最重要的就是 代码、Markdown 两种了。

![改变 “块” 的类型](https://upload-images.jianshu.io/upload_images/23208742-90e3bb7db6429944.png?imageMogr2/auto-orient/strip|imageView2/2/w/950/format/webp)

**Markdown块** ，即用markdown标记语言写的块，类似于代码的注释，但画面更好看，功能也更强大。

**代码块** ，左侧有 “In” 标记，运行后输出内容在下方显示。每个代码块可以独立运行，使得 jupyter 特别适合用来做小段的练习。当然，也特别适合用来做教学：事先写好代码（还可以结合 Markdown块 写注释），可以讲解完直接运行看结果。

![块](https://upload-images.jianshu.io/upload_images/23208742-2dbbfa7be4eaa114.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

### 4、“块” 的模式
**当前模块** 被区分为 编辑模式（edit mode）及 命令模式（command mode）两种。

- 块只有在当前模式下才能编辑。

- 编辑模式下单击块左侧空白区域可切换到命令模式，命令模式下单击或双击编辑区可切换到编辑模式。

- 编辑模式和命令模式的快捷键不同。

- 块的左侧为绿色时，是编辑模式。块的左侧为蓝色时，则是命令模式。

![编辑模式](https://upload-images.jianshu.io/upload_images/23208742-79fa15de6f3226c0.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

### 5、常用命令介绍
- 单击菜单栏 Cell -> Current Outputs 可以选择代码块的输出区域使用或不使用滚动条，这在输出特别多时很有用。

![改变输出显示](https://upload-images.jianshu.io/upload_images/23208742-a08879d5787ec1a5.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

- 单击菜单栏 Kernel -> Change kernel 可以选择当前文件的使用的已安装的 python版本。

![选择 python 版本](https://upload-images.jianshu.io/upload_images/23208742-cb9749776aab9d09.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

- 单击菜单栏 Help -> Keyboard Shortcuts 可以查看快捷键。

![查看快捷键](https://upload-images.jianshu.io/upload_images/23208742-a0d1c993a142a1e5.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

- 常用快捷键：

**编辑模式下：Ctrl + Enter 运行代码** （markdown编辑完也要运行）

**命令模式下：A** 键在当前块上方新建一个块（above），**B** 键在当前块下方新建一个块（below）。新建的块默认为代码块。

### 6、markdown 语法简介
- 标题，以 `#`（井号）开头的为标题，一个 `#` 为一级标题，两个 `#` 为二级标题，最多用六个 `#`。

- 加粗，以两对 `*`（星号）夹着的文本显示为粗体（注意最后的星号后面加一个空格，否则会影响后面文本的格式）。

- 斜体，以一对 `*`（星号）夹着的文本显示为斜体。

- 无序列表，以 `- `（减号加一个空格）的项为无序列表。

- 有序列表，以 `1.` `2.` 开头的项为有序列表。

- 换行，要敲两次回车（即两行间有一个空行），只敲一次回车则上下两行显示在同一行。另外，用标记 `<br/>`也可以实现换行

## 三、jupyter notebook 的一些配置
在安装完 jupyter 后，新建的 jupyter 文件（后缀 ".ipynb"）是存储在一个默认路径上的，没办法像大多数软件一样在保存时选择保存路径，这对于 C 盘空间小且不喜欢默认路径的笔者来说是很不友好的。

另外，如果把 .ipybn 文件放到其他路径，默认情况下双击是没办法直接打开的，也不方便。

下面来看一下解决方案，方案区分以 Anaconda方式 及 命令行方式 安装的jupyter。
### 在任意路径打开 .ipynb 文件
- **Anaconda安装**

1.找到 Anaconda 快捷方式：在开始菜单右击 Jupyter Notebook，选择 “更多”，点击“打开文件位置”。

![anaconda1.png](https://upload-images.jianshu.io/upload_images/23208742-6628d1ea0c374760.png?imageMogr2/auto-orient/strip|imageView2/2/w/976/format/webp)

2.右击 Jupyter Notebook 快捷方式，选择属性。

![anaconda2.png](https://upload-images.jianshu.io/upload_images/23208742-a3cb8636078e8771.png?imageMogr2/auto-orient/strip|imageView2/2/w/1128/format/webp)

3.复制 “目标” 中的内容。

![anaconda3.png](https://upload-images.jianshu.io/upload_images/23208742-a69895284f3e3d90.png?imageMogr2/auto-orient/strip|imageView2/2/w/729/format/webp)

4.新建一个文本文件（.txt），将刚刚复制的内容粘贴进去，在最后的 .py 后面加一个空格，再输入 %1%，保存并关闭文件。（如果最后一个 .py 后有文本，先删掉）

![anaconda4.png](https://upload-images.jianshu.io/upload_images/23208742-50b4708807fe6658.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

5.设置显示文件后缀，将后缀 .txt 改为 .bat，回车确定。

![anaconda5.png](https://upload-images.jianshu.io/upload_images/23208742-00a2184877749a6e.png?imageMogr2/auto-orient/strip|imageView2/2/w/872/format/webp)

6.随便右击一个 .ipynb 文件，点击 “属性”，点击打开方式项右侧的 “更改”。

![anaconda6.png](https://upload-images.jianshu.io/upload_images/23208742-d2c193bd4886b8f5.png?imageMogr2/auto-orient/strip|imageView2/2/w/618/format/webp)

7.选择 “更多应用”。

![anaconda7.png](https://upload-images.jianshu.io/upload_images/23208742-08106407eb37ca54.png?imageMogr2/auto-orient/strip|imageView2/2/w/511/format/webp)

8.选择 “在这台电脑查找其他应用”。

![anaconda8.png](https://upload-images.jianshu.io/upload_images/23208742-f98813b3f46a8fee.png?imageMogr2/auto-orient/strip|imageView2/2/w/502/format/webp)

9.找到刚刚创建的 .bat 文件，点击打开。

![anaconda9.png](https://upload-images.jianshu.io/upload_images/23208742-afe99cfc0430bc12.png?imageMogr2/auto-orient/strip|imageView2/2/w/787/format/webp)

10.点击 “确定” 即可。

![anaconda10.png](https://upload-images.jianshu.io/upload_images/23208742-6f578b8d72afc22f.png?imageMogr2/auto-orient/strip|imageView2/2/w/558/format/webp)

- **命令行安装**

1.执行以上的 6-8步骤。

2.选中 python 安装目录下的 Scripts 文件夹内的 jupyter-notebook.exe，点击打开。

![选择 jupyter-notebook.exe](https://upload-images.jianshu.io/upload_images/23208742-d609c14b60ad6b59.png?imageMogr2/auto-orient/strip|imageView2/2/w/1100/format/webp)

3.点击 “确定” 即可。

![确定](https://upload-images.jianshu.io/upload_images/23208742-6a6f58561f941a23.png?imageMogr2/auto-orient/strip|imageView2/2/w/558/format/webp)

### 改变 jupyter notebook 新建文件的默认存储路径
- **Anaconda安装**

1.按上述方式进入 Jupyter Notebook 快捷方式所在文件夹，右击 Jupyter Notebook，点击 “属性”。

![anaconda 属性](https://upload-images.jianshu.io/upload_images/23208742-a014b32d56664392.png?imageMogr2/auto-orient/strip|imageView2/2/w/1128/format/webp)

2.在 “目标” 项右侧的最后一个 .py 后加一个空格，再在输入用双引号括起的存储路径。（如果原来 .py 后有文本，先删掉）

![设置存储路径](https://upload-images.jianshu.io/upload_images/23208742-e66e58052f331bd8.png?imageMogr2/auto-orient/strip|imageView2/2/w/600/format/webp)

- **命令行安装**

1.进入 python 安装目录的 Scripts 文件夹，右击 jupyter-notebook.exe，选择 “创建快捷方式”。

![创快捷方式.png](https://upload-images.jianshu.io/upload_images/23208742-b21c1ffee3746fb6.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

2.在任意位置粘贴快捷方式，右击该快捷方式，选择属性，在 “目标” 项最后加一个空格，再在输入用双引号括起的存储路径。

![更改默认存储.png](https://upload-images.jianshu.io/upload_images/23208742-e7259bad09c012ce.png?imageMogr2/auto-orient/strip|imageView2/2/w/716/format/webp)

3.至此，*通过此快捷方式创建的* 新 .ipybn 文件将存储在所设置的路径下。


**推荐阅读：** 「[快速上手 markdown](https://www.jianshu.com/p/b717685879b0)」
