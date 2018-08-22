
# Vim命令合集

[![96](https://upload.jianshu.io/users/upload_avatars/1464813/a5656a9558e9?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96)](https://www.jianshu.com/u/f5644a13e171)

[im蚂蚁](https://www.jianshu.com/u/f5644a13e171)  关注

2016.03.08 11:12*  字数 7644  阅读 6002评论 3喜欢 21

## 命令历史

以`:`和`/`开头的命令都有历史纪录，可以首先键入:或/然后按上下箭头来选择某个历史命令。

## 启动vim

在命令行窗口中输入以下命令即可

-   `vim`  直接启动vim
-   `vim filename`  打开vim并创建名为filename的文件

## 文件命令

-   打开单个文件`vim file`
-   同时打开多个文件`vim file1 file2 file3 ...`
-   在vim窗口中打开一个新文件`:open file`
-   在新窗口中打开文件`:split file`
-   切换到下一个文件`:bn`
-   切换到上一个文件`:bp`
-   查看当前打开的文件列表，当前正在编辑的文件会用[]括起来。`:args`
-   打开远程文件，比如ftp或者share folder`:e ftp://192.168.10.76/abc.txt`或者`:e \\qadrive\test\1.txt`

## vim的模式

-   正常模式（按`Esc`或Ctrl+[进入） 左下角显示文件名或为空
-   插入模式（按`i`键进入） 左下角显示--INSERT--
-   可视模式（不） 左下角显示--VISUAL--
-   导航命令

### 移动命令

-   `^`:移动光标到行首；
-   `$`:移动光标到行尾；
-   `ctrl-b`:类似于键盘上的"PgUp"(b为backword)
-   `ctrl-f`：类似于键盘上的"PgDn"(f为forword)
-   `G`：移动到末行；
-   `1G`：移动到首行；
-   `50G`：移动到50行；
-   `H`：移动到当前窗口的首行；
-   `M`：移动到当前窗口的中间位置；
-   `L`：移动光标到当前窗口的最后一行；
-   `w`:光标移动到下一个单词的词首；注：对于中文，连续的多个汉字作为一个word。
-   `2w`:重复执行w操作2次；
-   `e`:光标移动到下一个单词的词尾；
-   `5e`:重复执行e操作5次；
-   `b`：向前移动光标，移动到前一个单词的词首；

#### 句字(sentences)直接移动操作：

-   `)`:光标移动到下一句；
-   `(`:光标移动到上一句；
-   `3)`:光标移动到向下3句

#### 段落（paragraphs）直接移动操作：

-   `{`:向上移动一个段落；
-   `}`:向下移动一个段落
-   `3}`:向下移动3个段落
更多操作在vim Normal模式下输入  `:help cursor-motions`

![](https://upload-images.jianshu.io/upload_images/1464813-64f174231649a882)

* 原文参考: [Vim命令合集](https://www.jianshu.com/p/117253829581)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM1NDE0ODYzMywtMTIwODQ5OTQ4OSwxND
czMDA1MDE1XX0=
-->