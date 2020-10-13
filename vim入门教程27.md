windows类似keycastr的显示键盘按键的软件KeyCastOW只在[github](https://github.com/brookhong/KeyCastOW)上提供了源代码和vs工程，需要自行编译二进制文件。

Vim教程网提供的vim视频教程在很多时候需要在屏幕实时显示对应操作的按键，windows系统下显示按键的软件推荐使用KeyCastOW，具有和Mac上的软件keycastr相同的功能。

# 一、KeyCastOW编译方法

KeyCastOW提供了Visual Studio工程，在windows系统上编译KeyCastOW需要先安装vs2013或vs2015。

安装好vs后需要配置Command Prompt (一个配置好了各种环境变量的cmd) 用于快速编译KeyCastOW工程。

Vim教程网介绍使用Visual Studio的“External Tools”功能，把Command Prompt快捷方式放到IDE的“Tools”菜单下。

再使用Command Prompt编译KeyCastOW源码，编译命令为：`msbuild /p:platform=win32 /p:Configuration=Release`，编译好的二进制文件为**Release\keycastow.exe**

![KeyCastOW编译方法](https://image.vimjc.com/images/691e0c29gy1ft6c9r7au7g212a0q6npd.gif)