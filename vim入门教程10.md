Vim可以在[尾行模式](https://vimjc.com/vim-edit-command.html)下使用 `:substitute` 命令将指定的字符替换成其他目标字符，通常使用该命令的缩写格式 `:s` 进行操作，可基于[Vim正则表达式](https://vimjc.com/regex-for-vim-seach-substitute-global-command.html)指定操作目标。

# 一、Vim替换命令语法

Vim替换命令的基本语法是 `:[range]s/源字符串/目标字符串/[option]`，其中`range`和`option`字段都可以缺省不填。

各个字段的意思是：

- `range` 表示[搜索范围](https://vimjc.com/vim-edit-command.html)，默认表示当前行
- `range`字段值`1,10`表示从第1到第10行，`%`表示整个文件(相当于`1,$`)，而`.,$`代表从当前行到文件末尾
- `s` `substitute`的简写，表示替换
- `option`表示操作类型，默认只对第一个匹配的字符进行替 换
> option字段值`g`(global)表示全局替换，`c`(comfirm)表示操作时需要确认，`i`(ignorecase)表示不区分大小写这些选项可以组合使用。

# 二、Vim替换命令举例

## 2.1 全局替换并进行确认

![vim视频教程](https://image.vimjc.com/images/691e0c29gy1fnghcx5ntfg20k808swha.gif)
执行命令`:1,$s/Vim/vim/gc`会出现提示”replace with foo(y/n/a/q/l/^E/^Y)?”，询问是否确认执行

待选择操作的含义包括：

y        确认执行这个替换
n        取消这个替换
a        执行所有替换且不再询问
q        退出而不做任何改动
l        替换完当前匹配点后退出(last)
Ctrl + E   向上翻滚一行
Ctrl + Y   向下翻滚一行

## 2.2 将光标所在行出现的所有包含line的字符串中line替换为lines

`:s/line/lines/g`表示将光标所在当前行的line全局替换为lines
![vim视频教程](https://image.vimjc.com/images/691e0c29gy1fngi3ybtncg20k8043dfz.gif)

## 2.3 将从2行到3行中出现的所有包含line的字符串中的line替换为lines

`:2,3s/line/lines/g`表示将2~3行的line全局替换为lines
![vim视频教程](https://image.vimjc.com/images/691e0c29gy1fngi55e5qvg20k8043t93.gif)

## 2.4 全文的行首加入//字符，批量注释时非常有用

`:%s/^/\/\//`表示在全文范围行首替换插入//，`/`需要转义
![vim视频教程](https://image.vimjc.com/images/691e0c29gy1fngi60ok8eg20k80430t7.gif)

## 2.5 将所有行尾多余的空格删除

`:%s= *$==`表示全局替换行尾的一个或多个空格，更多正则表达式的说明可以参考[Vim正则表达式搜索](https://vimjc.com/vim-search.html)
![vim视频教程](https://image.vimjc.com/images/691e0c29gy1fngie00kh6g20k8043wey.gif)