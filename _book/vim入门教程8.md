### 一 Vim插件管理器Pathogen

#### 1.1 安装Pathogen

pathogen只有一个单独的脚本pathogen.vim，其github下载地址为：https://github.com/tpope/vim-pathogen。

Pathogen下载后直接解压并保存到当前用户的 `~/.vim/autoload`目录即可完成安装。

#### 1.2 启用Pathogen

在[Vim配置文件vimrc](https://vimjc.com/vimrc-config.html)里面增加以下三条命令即可启用Pathogen插件。

```bash
execute pathogen#infect()
syntax on
filetype plugin indent on
```



#### 1.3 使用Pathogen安装、卸装Vim插件

在当前用户目录`~/.vim/`下新建bundle目录，将新安装插件放到该目录下后，Pathogen会自动在bundle目录下生成对应插件子目录并使该插件生效。

而如果需要卸载插件，只需把`~/.vim/bundle`目录下对应的插件目录删除即可。

### 二 Vim插件管理器Vundle

#### 2.1 安装Vundle

Vundle插件也是提供一个Vundle.vim文件，其下载地址为：https://github.com/VundleVim/Vundle.vim.git

将下载的Vundle.vim文件保存到 `~/.vim/bundle` 即可完成Vundle的安装。

也可以使用以下的命令直接从 GitHub 拉取 Vundle.vim 文件到 `~/.vim/bundle` 文件夹下。

```bash
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

#### 2.2 配置Vundle

修改[Vim配置文件vimrc](https://vimjc.com/vimrc-config.html)，增加必要的配置，以下是 `.vimrc` 配置模板。

```bash
set nocompatible               "去除VIM一致性，必须"
filetype off                   "必须"

"设置包括vundle和初始化相关的运行时路径"
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

"启用vundle管理插件，必须"
Plugin 'VundleVim/Vundle.vim'

"在此增加其他插件，安装的插件需要放在vundle#begin和vundle#end之间"
"安装github上的插件格式为 Plugin '用户名/插件仓库名'"

call vundle#end()              
filetype plugin indent on      "加载vim自带和插件相应的语法和文件类型相关脚本，必须"
```

更多Vundle有关配置可以参考github上的[Quick Start](https://github.com/VundleVim/Vundle.vim#quick-start)

#### 2.3 使用Vundle安装插件

首先需要将要安装的插件，按照上述配置格式将插件地址填写在vundle#begin和vundle#end之间并保存。

设置好配置文件后，可通过下述两种方法安装插件:

(1) 在[Vim命令行模式](https://vimjc.com/vim-edit-command.html)下运行命令`:PluginInstall`

(2) 在终端命令行下通过命令`vim +PluginInstall +qall`直接安装

至此，需要安装的插件已经安装完毕，可以正常使用了。

#### 2.4 使用Vundle删除插件

(1) 需要删除Vim插件时，只需编辑Vim配置文件`.vimrc文件`，删除要移除插件所对应的 Plugin 一行；

(2) 打开Vim，在**Vim命令行模式**执行命令`:BundleClean`即可删除对应Vim插件；

如果你安装的vim插件非常多，又对vim启动速度等非常苛刻，建议你使用另外一款轻量高效的[Vim插件管理神器vim-plug](https://vimjc.com/vim-plug.html)。