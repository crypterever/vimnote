# NERDTree

Vim插件NERDTree是一款用来在Vim界面显示树形目录的文件管理器插件，可在vim操作界面进行文件打开、目录浏览操作。

其github地址为：https://github.com/scrooloose/nerdtree

## 一、vim插件NERDTree安装方法

- 推荐使用Vim插件管理器Vundle安装Vim插件NERDTree，vim教程网通过vundle安装NERDTree的配置文件截图如下。![surround安装方法](https://image.vimjc.com/images/691e0c29gy1ft43rj54k3j20u90n4n19.jpg)
- surround安装方法

## 二、vim插件NERDTree基本配置

- 通过vundle安装好NERDTree插件后，在vim命令行模式输入命令:NERDTree就可以看到NERDTree的显示界面。

- 使用组合按键 Ctrl + w，可将光标自动在左右侧窗口进行切换。

- 在 vim 启动的时候默认开启 NERDTree：
  autocmd VimEnter * NERDTree 或使用autocmd的缩写形式 au VimEnter * NERDTree

- 将NERDTree的窗口设置在vim窗口的右侧(默认为左侧)：

  ```bash
  let NERDTreeWinPos="right"
  ```

## 三、Vim插件NERDTree常用命令汇总

- q    关闭 NERDTree

- o    在已有窗口中打开文件或目录，并将光标跳到该窗口

- O    递归打开选中 结点下的所有目录

- x    合拢选中结点的父目录

- X    递归 合拢选中结点下的所有目录

- P    跳到根结点

- p    跳到父结点

- u    设置上级目录为根路径

- U    设置上级目录为跟路径，但是维持原来目录打开的状态

- r    刷新光标所在的目录

- R    刷新当前根路径

- I    显示或者不显示隐藏文件

- f    打开和关闭文件过滤器

- A    全屏显示 NERDTree，或者关闭全屏

- C    将根路径设置为光标所在的目录

  ![vim插件NERDTree介绍](https://image.vimjc.com/images/691e0c29gy1ft42asqs37g20pw0gydm9.gif)

>vim插件NERDTree介绍
