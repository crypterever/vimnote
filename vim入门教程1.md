强烈建议把caplocks改成esc，大小写用shift，hjkl方向可以改成jikl

# 一、Vim配置文件`.vimrc`

> Vim编辑器相关的所有功能开关都可以通过**.vimrc**文件进行设置。
>
> ![vim](https://gitee.com/zr001/writeimges/raw/master/images/image-20200906102540326.png)

# 二、Vim基本配置

默认情况下，Vim编辑器既不显示行号，也没有语法高亮、智能缩进、为了方便使用，基本的`Vim`配置选项一般都会包括：

## 2.1支持中文不乱码

```bash
"设置编码"
set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
set termencoding=utf-8
set encoding=utf-8
```

与`Vim`编码有关的变量包括：`encoding`、`fileencoding`、`termencoding`。
`encoding`选项用于缓存的文本、寄存器、Vim 脚本文件等；`fileencoding`选项是Vim写入文件时采用的编码类型；`termencoding`选项表示输出到终端时采用的编码类型。

## 2.2显示行号
```bash
"显示行号"
set nu
set number
```
## 2.3突出显示当前行
```bash
"cursorline的缩写形式"
set cursorline
set cul          
```
## 2.4 突出显示当前列

```bash
"cursorcolumn的缩写形式"
set cursorcolumn
set cuc          
```

## 2.5启用鼠标

`Vim`编辑器里默认是不启用鼠标的，也就是说不管你鼠标点击哪个位置，光标都不会移动。通过以上设置就可以启动鼠标，不过对于高级玩家来说，用`Vim`就是为了解放双方不用鼠标，所以这个设置可以根据个人爱好选择。

```bash
set mouse=a
set selection=exclusive
set selectmode=mouse,key
```

## 2.6显示括号匹配

``````bash
set showmatch
``````

## 2.7设置缩进

```bash
"设置Tab长度为4空格"
set tabstop=4
"设置自动缩进长度为4空格"
set shiftwidth=4
"继承前一行的缩进方式，适用于多行注释"
set autoindent
```

## 2.8设置粘贴模式

在Vim中通过[鼠标右键粘贴](https://vimjc.com/vim-paste.html)时会在行首多出许多缩进和空格，通过`set paste`可以在插入模式下粘贴内容时不会有任何格式变形、胡乱缩进等问题。

```bash
set paste
```

## 2.9显示空格和tab键

Vim编辑器中默认不显示文件中的tab和空格符，通过上面的配置可以获得以下的显示效果，方便定位输入错误。

关于Vim特殊字符的显示，推荐阅读[Vim怎么显示空格、Tab制表符、行尾换行符等非打印字符](https://vimjc.com/vim-display-unprintable-character.html)。

![image-20200906141912559](https://gitee.com/zr001/writeimges/raw/master/images/image-20200906141912559.png)

``````bash
set listchars=tab:>-,trail:-
``````

## 2.10显示状态栏和光标当前位置

``````bash
"总是显示状态栏"
set laststatus=2
"显示光标当前位置"
set ruler
``````

## 2.11打开文件类型检测

``````bash
filetype plugin indent on
``````

推荐阅读[Vim文件类型检测原理及应用](https://vimjc.com/vim-filetype.html)。

