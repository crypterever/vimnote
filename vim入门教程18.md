[Vim教程网](https://vimjc.com/)([https://vimjc.com](https://vimjc.com/))介绍的《[Vim替换命令substitute使用方法](https://vimjc.com/vim-substitute.html)》描述过，Vim 命令行下的替换命令基本语法是：

```
:[range]s/源字符串/目标字符串/[option]
```

将 substitute 命令的查找域 **源字符串** 留空，意味着 Vim 将会重用上次的查找模式，而所谓上次的查找模式是通过 Vim 的搜索命令进行指定。

即：`:[range]s//目标字符串/[option]` 表示查找上次所使用过的 *源字符串* 查找模式进行搜索。

而在[Vim搜索命令](https://vimjc.com/vim-search.html)有介绍，命令 `*` 可用于正向查找**当前光标**所在单词。

因此，配合 `*` 和上述搜索命令的特性，可以快速地实现替换当前光标所在单词为其他字符串。

![Vim替换命令](https://image.vimjc.com/images/vim-substitute-2.gif)

关于Vim替换命令和查找命令的使用，推荐阅读《[正则表达式及在Vim替换命令中的应用](https://vimjc.com/regex-for-vim-seach-substitute-global-command.html)》、《[Vim中的搜索模式](https://vimjc.com/vim-pattern.html)》。