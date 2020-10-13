在[Vim插入模式](https://vimjc.com/vim-edit-command.html)下，通过鼠标右键粘贴内容时会在行首多出许多缩进和空格，导致Vim内粘贴的内容格式错乱。

这是因为鼠标右键粘贴时只是向终端扔了一大堆的文本，Vim 以为你是在快速地输入。

但是当你使用Vim寄存器进行粘贴，如`+p` 命令时，Vim根据上下文是知道你在粘贴，就不会导致格式错乱。

为了解决Vim鼠标右键粘贴格式乱码问题，可以在Vim尾行模式使用 `:set paste`。

如果不想每次都输入命令`:set paste`，可以将命令加入到[Vim配置文件](https://vimjc.com/vimrc-config.html)`~/.vimrc`中或使用自动设置插件**[bracketed-paste](https://github.com/ConradIrwin/vim-bracketed-paste)**。

![Vim粘贴格式乱码](https://image.vimjc.com/images/vim-paste.gif)

**注**：上述Vim视频教程中，使用 `:%d` 命令表示删除当前文档中的全部内容，可参考《[Vim操作范围和文件范围相关概念介绍](https://vimjc.com/vim-ranges.html)》一文了解更多细节。

关于bracketed-paste插件的使用方法，Vim教程网后续会进行详细详细的介绍，欢迎关注！

[Vim命令`autocmd`](https://vimjc.com/vim-autocmd.html) 用于指示 Vim 监听某一类事件，一旦该事件发生，Vim 将执行指定的命令。

`InsertLeave` 表示 *离开插入模式* 事件。如[Vim粘贴文本格式错乱](https://vimjc.com/vim-paste.html)介绍，`paste` 选项可避免粘贴文本到Vim中出现格式错乱。但是该选项会使得 `autoindent` 等选项失效。

所以一般只有在 Vim 插入模式下才会启用 `paste` 选项，退出插入模式后关闭对应功能。

以下设置可完成上述功能，保证退出 Vim 插入模式后自动关闭 `paste` 选项。

```bash
autocmd InsertLeave * set nopaste
```

