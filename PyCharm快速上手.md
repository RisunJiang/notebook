![喏，你们要的 PyCharm 快速上手指南](https://pic4.zhimg.com/v2-556deee66e6f1b9ddb97d9b0c9cd9cd3_1200x500.jpg)

# 喏，你们要的 PyCharm 快速上手指南
[原文](https://zhuanlan.zhihu.com/p/26066151)

[![Crossin](https://pic3.zhimg.com/85b47091c_xs.jpg)](https://www.zhihu.com/people/crossin)

[Crossin](https://www.zhihu.com/people/crossin)

Crossin的编程教室 - Python新手村

1,180 人赞同了该文章

**Pycharm**  作为一款针对  **Python**  的编辑器，配置简单、功能强大、使用起来省时省心，对初学者友好，这也是为什么编程教室一直推荐新手使用  **Pycharm**  的原因。  
本文我们将介绍  **pycharm**  编辑器的基本使用方法，主要包括以下几个方面：

-   下载安装
-   新建项目流程
-   配置  **Pycharm**
-   **Python**控制台
-   其他参考资料

## 1、下载安装

**Pycharm**  提供 **免费的社区版**  与  **付费的专业版**。专业版额外增加了一些功能，如项目模板、远程开发、数据库支持等。个人学习  **Python**  使用免费的社区版已足够。  
pycharm社区版：[PyCharm :: Download Latest Version of PyCharm](http://link.zhihu.com/?target=http%3A//www.jetbrains.com/pycharm/download/)  
百度云盘地址：[https://pan.baidu.com/s/1bpqWA2F](http://link.zhihu.com/?target=https%3A//pan.baidu.com/s/1bpqWA2F)

安装过程照着提示一步步操作就可以了。注意安装路径尽量不使用带有  **中文或空格**  的目录，这样在之后的使用过程中减少一些莫名的错误。

## 2、新建项目

安装好软件之后，我们开始创建第一个项目，界面如下

![](https://pic4.zhimg.com/80/v2-a85ae903367ecfd678ea16d50db4ef47_hd.jpg)

左侧导航栏选择  **Pure Python**  ，右侧的  **Location**  选择项目的路径，  **Interpreter**  通过下拉栏选择  **Python版本**  ，这里直接使用  **Python**  的安装路径即可。

选择完成之后，点击  **Create**  按钮，进入界面。这时就可以创建文件了，步骤如下图所示：

![](https://pic4.zhimg.com/80/v2-66b808d1c06cb32ccebec2350939c17f_hd.jpg)

这里我们以刚刚创建的  **Crossin-practices**  文件夹为例，依次点击  
**Crossin-practices**  →  **New**  →  **Python File**

得到了如下的结果

![](https://pic1.zhimg.com/80/v2-b107577b3fb4d1189a1bc5a797f95ee8_hd.jpg)

在  **Name**  一栏输入文件名即可，记得添加  **.py**  后缀，点击  **OK**  之后就可以开始写下

```text
print('hello,world')

```

然后在界面点击 右键 →  **Run example**

![](https://pic3.zhimg.com/80/v2-1e6341b574b67bfa3f13f5ff56f98ab2_hd.jpg)

出现这样的结果：

![](https://pic2.zhimg.com/80/v2-6e075bfbe53c4d71b5d56470017ee49d_hd.jpg)

对于同一个脚本，第一次运行使用  **右键**  →  **Run example**  ，之后可以直接点击右上角或者左下角的  **绿三角**  。如下图：

![](https://pic4.zhimg.com/80/v2-2bb1178718bd626da8902814fbff69af_hd.jpg)

**注意**：更改文件运行的时候，三角和快捷键运行项目不会自动更改。所以常会运行了错误的文件而没发现。所以我们推荐第一次运行使用右键的方式，将脚本切换之后再使用绿三角。

到此，建立项目，运行脚本文件的流程都介绍完毕了

## 3、配置 Pycharm

**Pycharm**  提供的配置很多，这里讲几个比较重要的配置

编码设置：

**Python**  的编码问题由来已久，为了避免一步一坑，**Pycharm**  提供了方便直接的解决方案

![](https://pic1.zhimg.com/80/v2-7b7bf6cb827f253a21257c187c047fa4_hd.jpg)

在  **IDE Encoding**  、**Project Encoding**  、**Property Files**  三处都使用  **UTF-8**  编码，同时在文件头添加

#-*- coding: utf-8 -*

这样在之后的学习过程中，或多或少会避免一些编码坑。

解释器设置：

当有多个版本安装在电脑上，或者需要管理虚拟环境时，**Project Interpreter**  提供方便的管理工具。

![](https://pic3.zhimg.com/80/v2-29679fb60fcf0d0d4f948d5c85726e86_hd.jpg)

在这里可以方便的切换  **Python**  版本，添加卸载库等操作。

修改字体：

在  **Editor**  →  **Font**  选项下可以修改字体，调整字体大小等功能。

![](https://pic2.zhimg.com/80/v2-5128036e99620e4c20f37a58eca347e1_hd.jpg)

快捷键设置：

在 windows 下一些最常用的默认快捷键：

![](https://pic3.zhimg.com/80/v2-2c95f7f722a4342d1db875c03ef45daa_hd.jpg)

**Pycharm**  也为不同平台的用户提供了定制的快捷键方案，习惯了用**emacs**、**vim**、**vs**的同学，可以直接选择对应的方案。

![](https://pic2.zhimg.com/80/v2-61a55f048193449a4026c81ff236eb99_hd.jpg)

同时，**Pycharm**  也提供了自定义快捷键的功能。

![](https://pic2.zhimg.com/80/v2-53f98fdefa195d1179c108408f24180d_hd.jpg)

修改完成之后就去试试效果吧！

## 4、调试

强大的  **Pycharm**  为我们提供了方便易用的断点调试功能，步骤如下图所示：

![](https://pic2.zhimg.com/80/v2-2e0306477e8ab7d354b05a09b475729d_hd.jpg)

简单介绍一下调试栏的几个重要的按钮作用：

  

![](https://pic4.zhimg.com/80/v2-0353997a0ba329f1211451ef5028ed13_hd.jpg)

**Resume Program**：断点调试后，点击按钮，继续执行程序；  

  

![](https://pic4.zhimg.com/80/v2-a8c0d6061d0a68efaf22f680c18385fb_hd.jpg)

**Step Over**  ：在单步执行时，在函数内遇到子函数时不会进入子函数内单步执行，而是将子函数整个执行完再停止，也就是把子函数整个作为一步。有一点,经过我们简单的调试,在不存在子函数的情况下是和**Step Into**效果一样的（简而言之，越过子函数，但子函数会执行）；  

  

![](https://pic3.zhimg.com/80/v2-7cda50d4e2f7db7b2754f02a2344e432_hd.jpg)

**Step Into**：单步执行，遇到子函数就进入并且继续单步执行（简而言之，进入子函数）；

  

![](https://pic2.zhimg.com/80/v2-82ce1dc84514744a8fd46b9226454655_hd.jpg)

**Step Out**  ： 当单步执行到子函数内时，用step out就可以执行完子函数余下部分，并返回到上一层函数。  

如果程序在某一步出现错误，程序会自动跳转到错误页面，方便我们查看错误信息  
更详细的关于调试的知识参考之前的一篇文章：

[如何在 Python 中使用断点调试 - Crossin的编程教室 - 知乎专栏](https://zhuanlan.zhihu.com/p/21304838)

另外，PyCharm 还提供了一个方便调试的小功能，但隐藏得比较深，参见：

[pycharm 如何程序运行后，仍可查看变量值？ - 知乎专栏](https://zhuanlan.zhihu.com/p/27062841)

## 5、Python 控制台

为了方便用户，**Pycharm**  提供了另一个贴心的功能，将  **Python shell**  直接集成在软件中，调出方法如下：

![](https://pic3.zhimg.com/80/v2-b3dac053584f6746e2b5d96e0eeb6a92_hd.jpg)

  

## 6、一些网上收集的教程(参考)

1.  **Pycharm**官方教程：[PyCharm :: Docs &amp;amp;amp;amp; Demos](http://link.zhihu.com/?target=http%3A//www.jetbrains.com/pycharm/documentation/)
2.  **Pycharm toolbar window**：[PyCharm 2016.3 Help](http://link.zhihu.com/?target=https%3A//www.jetbrains.com/help/pycharm/2016.3/debug-tool-window.html%23steptoolbar)
3.  **Pycharm**  皮肤主题及个性化设置：[pycharm 皮肤主题及个性化设置](http://link.zhihu.com/?target=http%3A//blog.csdn.net/garfielder007/article/details/53873787)
4.  **Pycharm**  更换主题：[Pycharm更换主题 - felcon的专栏 - 博客频道 -C23SDN.NET](http://link.zhihu.com/?target=http%3A//blog.csdn.net/felcon/article/details/38491413)
5.  快捷键大全：[pycharm快捷键及一些常用设置 - jihite - 博客园](http://link.zhihu.com/?target=http%3A//www.cnblogs.com/kaituorensheng/p/5371366.html)


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3NjIzNTQ1MzksMjI3MjEwNjExLC0xNz
YyMzU0NTM5XX0=
-->