vim快捷键是某种vim命令或命令串的**别名**，有点类似[Vim中的宏](https://vimjc.com/recording.html)。

使用Vim命令 `:map` 可以将键盘上的某个按键与Vim的命令映射起来，完成Vim快捷键的绑定。例如 `:map a b` 在map生效的情况下，按下a就等同于按下了b。

# 一、vim map命令前缀

在map命令前加上前缀可以组合成几种不同的命令，表示在不同的Vim模式下生效。
- `n` 在普通模式 (**n**ormal) 下生效
- `i` 在插入模式 (**i**nsert) 下生效
- `v` 在可视化模式 (**v**isual) 下生效
- `c` 在命令模式 (**c**ommand-line) 下生效
- `o` 在命令等待时 (**o**perator pending) 生效，比如输入d之后会等待输入下一个字符，可能是d或者数字
- `un`删除键的映射
- `nore`非递归 (non-recursive)，意思是将a 映射为b，b映射为c，输入a的时候不会被映射为c，而只会映射`b`

>以上前缀可以组合使用，比如 `nnoremap`，`nunmap`，`vnoremap` 等。不带前缀的map命令默认对 `normal` 模式和 `visual` 模式生效
Vim `:map` 默认是递归映射模式。

## 1.1 括号自动补全映射

```bash
" 在插入模式下非递归映射(为 )<Esc>i"
inoremap ( ()<Esc>i
inoremap [ []<Esc>i
inoremap { {}<Esc>i
inoremap " ""<Esc>i
```

这样输入(, [, {, “的时候都会自动补全，并且把光标移到括号的内部

## 1.2 Backspace的映射

Backspace的功能是向前删除，而x键是向后删除，在normal模式下z键没有什么作用。所以用z键实现backspace的功能是个不错的选择

```
nnoremap z i<BS><Esc>l
```

这样子，normal模式用 `z` 删除就可以实现Backspace的功能

# 二、Vim快捷键与Leader键

Vim的 `mapleader` 变量对所有map映射命令起效，它的作用是将参数 `<leader>` 替换成 `mapleader` 变量的值

如果 mapleader 变量没有设置，则用默认的反斜杠 `\`代替，因此Vim映射 `:map <Leader>A oanother line<Esc>` 等效于：`:map \A oanother line<Esc>`

如果设置了 mapleader 变量，例如 `:let mapleader = ","`，那么 `:map <Leader>A oanother line<Esc>` 就等效于： `:map ,A oanother line<Esc>`

# 三、Vim快捷键实例

推荐阅读[常用Vim命令及实用Vim按键映射配置详解](https://vimjc.com/vim-commands-and-vim-mapping-conf.html)获取更多实用的Vim按键映射配置和Vim命令说明。