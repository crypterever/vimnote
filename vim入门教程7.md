Vi/Vim手工自行安装配色方案的主要步骤包括：

> (1) 确认当前用户目录下存在`~/.vim/colors`目录，没有则新建，安装的Vim配色方案对应.vim文件需放在该目录下
>
> (2) 下载或编辑某个配色方案的**.vim**文件，保存到`~/.vim/colors`目录下
>
> (3) 修改[Vim配置文件`~/.vimrc`](https://vimjc.com/vimrc-config.html)，增加配置项`colorscheme molokai`并保存 (假设下载了一个叫**molokai**的配色方案文件molokai.vim)

**注意**：配置项中的 *molokai* 为配色方案文件的文件名，Vim通过该文件名加载对应.vim文件

下面介绍15个著名的Vim配色方案及其下载地址，大家可以根据图片效果按需使用。推荐阅读[2017年排名前10的暗黑简约型vim配色方案](https://vimjc.com/10-light-vim-color-scheme.html)。

#### 1. acme-colors

acme-colors配色方案支持256种颜色，对应.vim文件下载地址为：
https://github.com/plan9-for-vimspace/acme-colors/blob/master/colors/acme.vim

![vim配色方案acme](https://vimjc.com/images/acme-colors.jpg)

#### 2. base16

base16配色方案包含一系列配色，还提供了一些额外的插件供安装，具体使用可参考github上的说明：
https://github.com/chriskempson/base16-vim

![Vim配色方案base16](https://vimjc.com/images/base16.jpg)

#### 3. gotham

Gotham自称是一个非常*dark*的配色方案，包含 `gotham`和`gotham256`以及一些其他插件配置，github地址为：
https://github.com/whatyouhide/vim-gotham

![Vim配色方案gotham](https://vimjc.com/images/gotham.jpg)

#### 4. gruvbox

gruvbox配色方案在github上的评价较高，据说对人眼非常pleasant，[Vim教程网](https://vimjc.com/)就是用的这个配色方案，下面是github地址及配色截图
https://github.com/morhetz/gruvbox

![Vim配色方案gruvbox](https://vimjc.com/images/gruvbox.jpg)

#### 5. janah

janah也是一个dark型的配色方案，github地址为：
https://github.com/mhinz/vim-janah

![Vim配色方案janah](https://vimjc.com/images/janah.jpg)

#### 6. jellybeans

jellybeans在github上也较流行，github地址：
https://github.com/nanotech/jellybeans.vim

![Vim配色方案jellybeans](https://vimjc.com/images/jellybeans.jpg)

#### 7. lucius

lucius配色方案的github地址：https://github.com/jonathanfilip/vim-lucius

![Vim配色方案lucius](https://vimjc.com/images/lucius.jpg)

#### 8. molokai

molokai配色方案非常出名，知乎上有个问题[你认为最好看的 Vim 配色方案是哪款](https://www.zhihu.com/question/19597873)，molokai的呼声非常高
https://github.com/tomasr/molokai

![Vim配色方案molokai](https://vimjc.com/images/molokai.jpg)

#### 9. oceanic-next

oceanic-next是一个neovim配色方案，依赖其他几个插件和配色方案
https://github.com/mhartington/oceanic-next

![Vim配色方案oceanic-next](https://vimjc.com/images/oceanic-next.jpg)

#### 10. paramount

paramount是一个比较简单的Vim配色方案，只关注一些关键配置
https://github.com/owickstrom/vim-colors-paramount

![Vim配色方案paramount](https://vimjc.com/images/paramount.jpg)

#### 11. flattened

flattened也是一个很简介但不简单的配色方案，官方说法是没有废话“without the bullshit”
https://github.com/romainl/flattened

![Vim配色方案flattened](https://vimjc.com/images/flattened.jpg)

#### 12. railscasts

railscasts同时支持GUI和终端方式，github地址为：
https://github.com/jpo/vim-railscasts-theme

![Vim配色方案railscasts](https://vimjc.com/images/railscasts.jpg)

#### 13. seoul256

seoul256是一个低对比度(low-contrast)的配色方案，github地址：
https://github.com/junegunn/seoul256.vim

![Vim配色方案seoul256](https://vimjc.com/images/seoul256.jpg)

#### 14. solarized

solarized配色方案在github上的star非常多，https://github.com/altercation/vim-colors-solarized

![Vim配色方案solarized](https://vimjc.com/images/solarized.jpg)

#### 15. yowish

yowish配色方案同时支持GUI和256色终端，也是一个 `dark` 主题
https://github.com/kabbamine/yowish.vim

![Vim配色方案yowish](https://vimjc.com/images/yowish.jpg)