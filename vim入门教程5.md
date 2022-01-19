# vim重复操作命令.(英文句点)
`Vim` 编辑器.命令可以用于重复执行命令
在 `Vim` 尾行模式下，通过 `:h.`查看 `vim` 的帮助手册，可以看到：

-----------
. Repeat last change, with count replaced with [count]. Also repeat a yank command, when the ‘y’ flag is included in ‘cpoptions’. Does not repeat a command-line command

-----------

- 举例来说，删除一个单词，可以使用命令`dw`(`w`是`word`的缩写，表示一个单词，更多示例可以参考`Vim`教程网上的Vim文本编辑命令汇总)

- 接着，我们可以使用命令`5`.再连续删除`5`个单词，这就是`Vim`中.点命令的重复功能。

- 再考虑以下场景：某个源文件中，有若干行以注释符号`//`结尾，现在我们要在这些行末添加一些相同的内容

我们可以使用如下方式来实现：

- 搜索字符串`//`：`/\/\/` (`/`需要使用`\`进行转义)
现在，只要按下`n`键就会跳转到下一个搜索到的目标字符串。

- 从第一个匹配实例开始添加文本：按下A进入行尾追加模式，在行末添加文本 (假设为 `comment`)
- 按`[Esc]`退出编辑模式，这条命令执行完成了。但是接下来还有多个个地方需要执行相同的操作。这时，我们便可以使用.点命令重复执行上一条命令。
- 跳转到下一个匹配实例并向行末添加文本 `n.`
> 上述介绍的Vim中使用.命令重复执行操作的示例如下图所示，大家可以参考并做练习。![](https://gitee.com/zr001/writeimges/raw/master/images/691e0c29gy1fn2r3n4lvxg20kz0ftmyw.gif)