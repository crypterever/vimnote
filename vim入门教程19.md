Vim支持在打开文件时进行屏幕分割，也支持在Vim编辑器内部进行分屏。Vim分屏是指在同一个Vim窗口中同时显示多个文件的内容。

### 一、打开文件时启动分屏

使用Vim打开文件时，可以通过参数`-On` 或 `-on`来启动分屏。

**n** 代表整数，表示将整个屏幕分成n部分

大写 *O* 表示进行**垂直方向**分屏，小写 *o* 表示水平方向进行分屏

### 二、Vim内部启动分屏

使用Vim打开文件后，仍然可以在尾行模式通过以下命令进行屏幕分割

#### 2.1 垂直分屏并打开一个新文件

Vim尾行模式下执行命令 `:vsplit filename` 或缩写形式 `:vsp filename` 可实现Vim垂直方向分割屏幕，且打开新的文件 **filename**

**注**：*v* 表示单词 *vertical*，是中文”垂直”的意思

#### 2.2 水平分屏并打开一个新文件

Vim尾行模式下执行命令 `:split filename` 或缩写形式 `:sp filename` 可实现在Vim水平方向分割屏幕，且打开新的文件 **filename**

![Vim分屏](https://image.vimjc.com/images/691e0c29ly1fnxxdm6hm8g20ex09fq3s.gif)

#### 2.3 垂直分隔当前打开的文件

Vim命令行模式下执行命令 `Ctrl+w v` 可将当前打开的文件进行垂直分割

上述命令 `Ctrl+w v` 的意思是：先同时按键 **Ctrl** 和 **w**，再按键 **v**

#### 2.4 水平分隔当前打开的文件

Vim命令行模式下执行命令 `Ctrl+w s` 可将当前打开的文件进行水平方向分割

上述命令 `Ctrl+w s` 表示先同时按键 **Ctrl** 和 **w**，再按键 **s**

### 三、Vim分屏时切换屏幕

在Vim分屏模式下，可以按以下方式切换当前操作的屏幕窗口：

#### 3.1 轮流切换

在Vim命令行模式下，同时按键 `Ctrl+w w` 可以在当前的分割屏幕中按顺时针方向切换屏幕

![Vim分屏](https://image.vimjc.com/images/691e0c29ly1fnxxhdh1y4g20ex09f74v.gif)

#### 3.2 按指定方向切换屏幕

[Vim光标移动命令汇总](https://vimjc.com/vim-cursor.html)曾介绍，光标键 **h**, **j**, **k**, **l** 分别用于**左**、**下**、**上**、**右** 4个方向，因此：

> 命令 `Ctrl+w h` 用于把光标移到左边的屏幕中
>
> 命令 `Ctrl+w l` 用于把光标移到右边的屏幕中
>
> 命令 `Ctrl+w j` 用于把光标移到下边的屏幕中
>
> 命令 `Ctrl+w l` 用于把光标移到上边的屏幕中

### 四、设置分屏大小

> 命令 `Ctrl+w =` 表示设置所有的分屏幕都有相同的高度
>
> 命令 `Ctrl+w +` 用于增加当前屏幕的高度
>
> 命令 `Ctrl+w -` 用于减少当前屏幕的高度

### 五、关闭Vim分屏

命令 `Ctrl+w c` 用于关闭当前操作的Vim分屏幕