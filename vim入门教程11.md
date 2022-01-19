在插入模式下，Vim可以不借助任何插件实现自动补全功能。介绍Vim自带的单词自动补全、行自动补全和基于用户自定义字典的自动补全。

# 一、单词补全

`Ctrl + n`：当输入完第一个字母后，再按`Ctrl + n`，Vim会自动出现下拉菜单，且默认选中第一个单词

继续按 `Ctrl + n` 可以上下选择，但如果缓冲区没有可选单词，那么下拉列表不会有任何选项

![Vim自动补齐](https://image.vimjc.com/images/691e0c29gy1fniwa3rex9g20c10503ys.gif)

`Ctrl + p`：功能同上，只是默认选中的是列表最后一个单词

# 二、行补全

在Vim插入模式下输入已经存在行的第一个单词，再按`Ctrl + x`、`Ctrl + l`命令，就会列出该整行出来实现Vim行自动补全

# 三、字典补全

假设有一个备选单词表，文件名为dict.txt，每行一个单词，里面包含以下内容：

```bash
https://vimjc.com
Hello
Vim
editor
best
tool
```

若要实现**基于该单词表**的Vim自动补齐，需要设置以下步骤：

(1) 在~/.vimrc配置文件中加入代码：`set dictionary-=~/dict.txt dictionary+=~/dict.txt`

(2) 打开Vim，在插入模式下输入`Ctrl + x`后再输入`Ctrl + k`，就能看到dict.txt文件中定义的单词

(3) 若想直接通过`Ctrl + n`命令就显示其中的列表，再配置.vimrc文件，加入`set complete-=k complete+=k`

更多信息可以在Normal模式下查看帮助文档`:help dictionary`，要使用更加高阶的自动补齐功能，推荐使用[Vim youcomplateme插件](https://vimjc.com/vim-youcompleteme-install.html)。