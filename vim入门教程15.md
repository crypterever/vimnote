Vim支持多种折叠形式：手动折叠**manual**、基于缩进行折叠**indent**、基于语法进行折叠**syntax**、未更改文本折叠**diff**等

日常编程中用到的Vim折叠形式主要有`indent` 和 `syntax`，只需要Vim配置文件 `~/.vimrc`中增加以下配置：

```bash
"基于缩进进行代码折叠"
set foldmethod=indent
"启动 Vim 时关闭折叠"
set nofoldenable
```

Vim打开文件后，重复使用操作命令 `za` 可打开或关闭当前折叠；`zM` 用于关闭所有折叠，`zR` 则用来打开所有折叠。

Vim折叠代码效果图如下所示：

![Vim代码折叠教程](https://image.vimjc.com/images/691e0c29gy1fnptpjrislg20ha0ea7kc.gif)