Vim每打开一个文件，就会在内存中创建一个对应缓冲区，[Vim文件缓冲区列表介绍](https://vimjc.com/vim-file-buffer.html)介绍了使用Vim标准的文件缓冲区切换命令实现缓冲区管理

本文介绍Vim插件[vim-fswitch](https://github.com/derekwyatt/vim-fswitch)，用于实现**同伴文件** (如test.h和test.cpp)的快速切换

*vim-fswitch* 插件提供配置文件**fswitch.vim**，其安装方法可以参考Vim教程网介绍的[Vim插件管理器Pathogen和Vundle简介](https://vimjc.com/vim-plugin-manager.html)

安装完Vim插件*vim-fswitch* 后，在Vim配置文件`~/.vimrc` 中增加以下[键盘映射](https://vimjc.com/vim-map.html)配置

```
'同伴文件*.cpp 和 *.h 切换'
nmap <silent> <Leader>sw :FSHere<cr>
```

假设Vim当前打开的文件为 **MyClass.h**，在命令行模式下输入命令 `;sw` 后，Vim会在新的文件缓冲区中打开 MyClass.cpp文件显示在当前窗口；再次输入命令 `;sw` ，便可以切换到原先的窗口，如下图所示

![vim插件](https://image.vimjc.com/images/691e0c29gy1fnqzctcq6ug20hg0f5gnf.gif)