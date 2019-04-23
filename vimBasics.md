# vimBasics
vim基本用法——入门篇

#### vim -u NONE -N
vimrc的设置和插件均被禁用。设置为vi非兼容模式。  
-u NONE 标志让 Vim 在启动时不加载你的 vimrc，这样，你的定制项就不会生
效，**插件也会被禁用**。当用不加载 vimrc 文件的方式启动时， Vim 会切换到 vi 兼
容模式，这将导致很多有用的功能被禁用，而 -N 标志则会使能 ‘nocompatible’ 选
项，防止进入 vi 兼容模式。

#### vim -u bookcode/essential.vim
激活了内置的插件功能，并且禁用了 vi 兼容模式。

#### :version
查看vim的版本（需要打开vim后查看）

#### :h vimtutor
查看Vim的内置文档。  
也可以用`：h`来查看帮助文档，比如`:h .`查看`.`的介绍

#### 技巧1 `.` Repeat last change/重复上次修改
