![](https://cognitivewaves.files.wordpress.com/2014/11/vi-vim-keyboard.png?w=550)

# VI（VIM）适用于WINDOWS用户

## 通过与Windows编辑器比较来学习

`vi`或者`Vim`（Vi IMproved）是一个功能强大的文本编辑器，起源于UNIX和Linux。它也适用于Windows（[www.vim.org](http://www.vim.org/)）。对于习惯GUI文本编辑器（Word，Notepad，Notepad ++等）的缺少经验的用户来说，这可能是一个挑战。有一些概念上的差异会让人感到沮丧。弥合这一差距的一种方法是比较和映射这两种行为。

[概念](https://cognitivewaves.wordpress.com/vi-editor/#concept)  
[基本操作](https://cognitivewaves.wordpress.com/vi-editor/#basic-operations)  
[有用设置](https://cognitivewaves.wordpress.com/vi-editor/#useful-settings)  
[更多操作](https://cognitivewaves.wordpress.com/vi-editor/#more-operations)  
[提示和技巧](https://cognitivewaves.wordpress.com/vi-editor/#tips-and-tricks)  
[结论](https://cognitivewaves.wordpress.com/vi-editor/#conclusion)

# 概念

`vi`以两种模式运行，命令模式和插入模式。标准GUI文本编辑器始终处于一种模式，即插入模式。  
**命令模式**（也称为正常模式） - 按下的所有键都执行命令而不是向文档添​​加文本。请注意，有不同的形式 - 单个键，按顺序的多个键和冒号命令（其中命令以“ `:`”字符为前缀）。  
**插入模式** - 标准GUI文本编辑器行为。按下的所有键都会在文档中添加文本。  
通常，左下角表示模式。在插入模式下会显示`--INSERT--`。它在命令模式下为空。

下面列出了一些概念上的差异。请注意下面的红色注释。这些通常会让初学者感到沮丧。

|VI|GUI文本编辑器|
|:-----------|:----|
|命令|快捷键|
|命令区分大小写|快捷键不区分大小写|
|缓冲|文件|
|以命令模式启动|以插入模式开始|
|按`i`，`a`，`I`，`A`进入插入模式。**在将文本添加到文档之前，您必须按其中一个键。**|始终处于插入模式，因此您只需键入即可添加文本。|
|按ESC键返回命令模式。**在插入模式下，您必须在执行命令之前按ESC键。**|始终处于插入模式。无需模式切换。快捷方式处于活动状态，可以使用。|
|**命令在插入模式下不起作用。**|快捷方式在插入模式下处于活动状态。|
|对于复制/剪切/粘贴，您可以使用本地剪贴板或系统剪贴板。|复制/剪切/粘贴始终使用系统剪贴板|
|鼠标和滚轮可能无法移动光标。必须使用众多键盘命令之一进行光标移动。|鼠标和滚轮按预期工作。|

# 基本操作

以下是最小的命令集，可以帮助您操作`vi`。它们可能不是使用`vi`的最有效的方式，但会让你摆脱困境。给出了典型文本编辑器中的等效的Windows快捷键以进行比较。

|`VI` 命令|快捷键|详情|
|:------|:------|:------|
|**`ESC`** |    |**返回命令模式**|
||**文件操作**||
|`:q`|ALT F4|退出/关闭应用程序|
|`:q!`|ALT F4, '不'保存|退出/关闭而不保存|
|`:e`|CTRL o|编辑/打开文件|
|`:w`|CTRL s|写/保存文件|
|`:w` *fileName*|F12(有些软件)|另存为|
|`:bn`|CTRL TAB|正向循环切换打开的缓冲区/文档|
|`:bp`|CTRL SHIFT TAB|反向循环切换打开的缓冲区/文档|
|`:bd`|CTRL F4|关闭当前缓冲区/文档|
|`:buffers`|窗口菜单栏项|显示所有缓冲区/文档|
||**光标移动**||
|`h`|<-- 左箭头||
|`j`|v向下箭头||
|`k`|^向上箭头||
|`l`|-->右箭头||
|`w`|CTRL->右箭头|向前走一个word|
|`b`|CTRL<-左箭头|向后移动一个word|
|`CTRL f`|向下翻页||
|`CTRL b`|Page Up||
|`gg`|CTRL Home|文件的开头|
|`G`|CTRL End|文件结束|
|`:` *n*|CTRL g（在某些编辑器中）|转到第*n*行|
||**进入插入模式**||
|`i`||在光标前插入|
|`a`||在光标后插入|
|`I`|Home|插入行的开头|
|`A`|End|插入行尾|
|`R`|Insert|键入时插入并覆盖文本|
||**删除**||
|`x`|Delete||
|`X`|Backspace||
|`dd`||删除行|
||**撤销重做**||
|`u`|CTRL z|Undo|
|`CTRL r`|CTRL y|Redo|
||**查找 find**||
|`/`|CTRL f||
|`*`||光标上的字被设置为查找字符串|
|`n`|F3（在一些编辑中）|查找下一个|
|`N`|SHIFT F3（在一些编辑中）|查找到上一个|
|`:noh`||清除最后搜索高亮|
||**查找和替换 Find and Replace**||
|`:%s/Foo/Bar/gc`|CTRL h（在某些编辑器中）|`Foo`是搜索字符串，`Bar`是替换字符串。在`/gc`要求确认之前更换。|
||**复制剪切粘贴**||
|`v`|SHIFT 箭头键|进入可视模式并使用光标移动键h，j，k，l开始标记|
|`V`||进入可视模式并使用上/下光标移动键j，k开始标记实线|
|`ggVG`|CTRL a|标记/选择完整缓冲区/文档|
|`y`|CTRL c|复制copy|
|`d`|CTRL x|剪切cut|
|`p`|CTRL v|小写p，粘贴到当前光标位置后|
|`P`||大写P，粘贴在当前光标位置之前|
|`"+y`|CTRL c|复制到系统剪贴板|
|`"+d`|CTRL x|切到系统剪贴板|
|`"+p`|CTRL v|小写p，从系统剪贴板粘贴当前光标位置之后|
|`"+P`||大写P，从系统剪贴板粘贴到当前光标位置之前|
||**档案状态**||
|```CTRL g ``or  `:f` `` ```||在底部状态行打印当前文件信息|

# 有用的设置

以下是一些`vi`有助于熟悉它的设置。这些`colon commands`可以在命令模式下应用。
|  |  |
|---|---|
|`:set autochdir`|打开文件，基目录设置为当前缓冲区的位置|
|`:set hlsearch`|突出显示搜索期间找到的文本|
|`:set ignorecase`|在查找期间忽略大小写|
|`:set incsearch`|增量搜索，在您键入时查找|
|`:set list`|显示选项卡和行尾等隐藏字符|
|`:set number`|显示行号|
|`:set ruler`|显示底部的当前光标位置（行和列）|
|`:set tabstop=4`|标签移动4个字符|
|`:set expandtab`|插入空格而不是制表符|

# 更多操作

以下是更多命令`vi`，可以让您深入了解其功能和灵活性。标准文本编辑器中没有真正的等价物。
|  |  |
|--|--|
|`.`|重复上一个命令|
|`$`|移至当前行的末尾|
|`0`|移动到当前行的开头|
|`o`|在下面打开一个新行并插入模式|
|`O`|在上面打开一个新行并插入模式|
|`r`|覆盖光标下的一个字符|
|`yy`|复制光标所在的行|
|`yw`|复制一个单词|
|`dd`|删除光标所在的行|
|`dw`|删除一个单词|
|`cw`|改变一个词|
|`D`|删除光标下的字符，直到行尾|
|`J`|加入/组合两行|

# 技巧和窍门

1.  ## 启动配置文件
    
    该`vimrc`文件包含可选的运行时配置设置，以在Vim启动时初始化它。在基于Unix的系统上，文件被命名`.vimrc`，而在Windows系统上，它被命名`_vimrc`。在启动时使用上面定义的一些设置很方便。
    
2.  ## 标签设置
    
    默认选项卡设置为8列。有些约定要求它是4列。此链接，[vim中的选项卡的秘密](http://tedlogan.com/techblog3.html)，将有助于调整默认值。
    
3.  ## 映射键
    
    它表示用户定义的快捷键。一个很好的例子是映射到Windows复制/剪切/粘贴快捷键（因为Vim命令根本不方便）。
    
    ：地图“+ y ：地图“+ d ：map“+ p
    

# 结论

喜欢或讨厌它，`vi`如果你曾经在`Linux`系统上工作，那么了解基础知识是必须的。和许多事情一样，在第一个障碍之后，它随着时间的推移会变得更好。试一试，如果您有任何问题或澄清，请询问。


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0OTUwMTE3NTEsNzc0OTM0Mzg0LDE3OD
M2NDA2NCwtMTU5NzY5NDM1OCwtMTA0ODQ0Njc1MSw2MDk1Mjc4
NzMsMTAwNjM4NTU2Myw5NjEzMTMwNTZdfQ==
-->