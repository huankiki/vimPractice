# vimPractice

## Reference
[Practical Vim](https://book.douban.com/subject/10599776/)  
[《Vim实用技巧》](https://book.douban.com/subject/25869486/)  
[书中所有的示例和源代码](https://pragprog.com/titles/dnvim/source_code)  

[简明 VIM 练级攻略](https://coolshell.cn/articles/5426.html)  
[Vim User Manual](http://vimdoc.sourceforge.net/)


## note
[vimBasics.md](./vimBasics.md)

## List
|command|Description|
|-|-|
|vim -u NONE -N|Vim启动时不加载vimrc，并且防止进入vi兼容模式|
|:version|查看vim的版本|
|:h vimtutor|查看Vim的内置文档|
|:h {cmd}|查看命令的文档|
|`.`|重复上次修改|
|`a`|光标后+插入模式|
|`i`|光标前+插入模式|
|`A`|插入模式+光标移到行尾，`$a`|
|`o`|在当前行后插入一个新行|
|`O`|在当前行前插入一个新行|
|`s`|删除光标下的字符+插入模式|
|`x`|删除光标所在字符|
|`w`|word forward，光标在单词开头|
|`b`|word backward，光标在单词开头|
|`e`|word forward，光标在单词结尾|
|`dw`|delete word，删除整个单词|
|`gg`|到第一行|
|`G`|到最后一行|
|`0`、`$`、`^`、`g_`|行头，行尾，非空字符的行头，非空字符的行尾|
|`%`|把光标先移到括号上，匹配括号移动 ( { [|
|`*`、`#`|匹配光标所在的单词，`*`：光标移动到下一个，`#`：光标移动到上一个|
|`u`|撤销，undo|
|`Ctrl r`|redo|
|`%s/content/copy/g`|全局替换|
|`f{char}`|到下一个{char}字符处，比如`fa`|
|`;`|重复查找上次 `f` 命令所查找的字符|
|`/`|查找提示符，`/content`|
|`n`、`N`|若有多个匹配，`n`到下一个，`N`到上一个。对`/`、`*`、`#`有效|
|`cw`|删除从光标到单词结尾间的字符+插入模式|
|`yyp`|复制+粘贴光标所在的行|
| `dd`|删除当前行|
|`>>`|缩进当前行|
|`Ctrl h`|在插入模式中，删除前一个字符|
|`Ctrl w`|在插入模式中，删除前一个单词|
|`Ctrl u`|在插入模式中，删除至行首|
|`Ctrl [`|同`ESC`，切换到普通模式|
|`r{char}`|用新字符{char}替换光标选中的每个位置的内容|
|`v`|选择字符|
|`Shift-v`|选择一行|
|`Ctrl-v`|选择一列|
|`:1`|跳到第1行|
|`:$`|跳到最后一行|
|`:2,5d`|删除第2到第5行，包含第2和第5行|
|`:copy`|`:t`，复制，`:6t.`|
|`:move`|`:m`，剪切，`:6m$`|
|`:`|查看命令记录，`<Up>`和 `<Down>`键|
|`/`|查看查找记录，`<Up>`和 `<Down>`键|
|`Ctrl-z`|挂起Vim进程。对应的`fg`：在bash命令行唤醒被挂起的Vim|
|`!`|在Vim的命令行模式调用外部程序|
|`:2,$!sort -t',' -k2`|调用sort命令|
|`gU`|可视模式下，被选择的变成大写|
|`gu`|可视模式下，被选择的变成小写|
|块操作@每行相同位置|块注释：`^ <Ctrl-v> <Ctrl-d> I// [ESC]`<br>- `<Ctrl-d>`可以换成hjkl<br>- `I// [ESC]`中的`I`是进入插入模式，输入"//"，按ESC键使每一行生效<br>逻辑：可视模式下选择列，然后通过`c`或者`I`进入插入模式，插入字符串之后，按ESC键|
|块操作@每行末尾|在每行末尾加分号";" ： `<Ctrl-v><j>$A;[ESC]`<br>逻辑：可视模式下选择列，到行末尾，进入插入模式，输入字符串，按ESC键|
|`<Ctrl-n>`、`<Ctrl-p>`|自动补齐，Insert模式下|



注：不同的命令是在不同的模式（普通、插入、可视、命令行模式等） or 不同的操作前提下生效    
■■ 不二法门：学习、练习、实践、学习、练习、实践………
