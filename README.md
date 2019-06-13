# vimPractice

## Reference
[Practical Vim](https://book.douban.com/subject/10599776/)  
[《Vim实用技巧》](https://book.douban.com/subject/25869486/)  
[书中所有的示例和源代码](https://pragprog.com/titles/dnvim/source_code)  

[简明 VIM 练级攻略](https://coolshell.cn/articles/5426.html)  
[Vim User Manual](http://vimdoc.sourceforge.net/)  
[Vim 中文用户手册](https://github.com/yianwillis/vimcdoc)

## Note
[vimBasics.md](./vimBasics.md)

## Next
阅读Vim用户手册。已上传：[vim_user_manual-zh-2.1.0.pdf](./vim_user_manual-zh-2.1.0.pdf)

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
|`A`|光标移到行尾+插入模式，`$a`|
|`I`|光标移到非空字符的行头+插入模式，`^i`|
|`o`|在当前行后插入一个新行+插入模式|
|`O`|在当前行前插入一个新行+插入模式|
|`s`|删除光标下的字符+插入模式|
|`x`|删除光标下的字符|
|`w`|word forward，光标在单词开头|
|`b`|word backward，光标在单词开头|
|`e`|word forward，光标在单词结尾|
|`viw`|高亮选择当前单词<br>`iw`：当前单词。当修改单词时，用`ciw`<br>`aw`：当前单词以及一个空格。当删除此单词时，用`daw`|
|`daw`|delete a word，删除整个单词及一个空格|
|`ciw`|change a word，删除整个单词+插入模式|
|`dw`|删除从光标位置到单词结尾的字符(包括一个空格)|
|`cw`|删除从光标位置到单词结尾间的字符 + 插入模式|
|`gU`|选区内字符变成大写（可视模式）|
|`gu`|选区内字符变成小写（可视模式）
|`gg`|到第一行|
|`G`|到最后一行|
|`0`、`$`、`^`、`g_`|行头，行尾，非空字符的行头，非空字符的行尾|
|`%`|把光标先移到括号上，匹配括号移动 ( { [|
|`u`|撤销，undo|
|`Ctrl r`|redo|
|`%s/content/copy/g`|全局替换，`%`指文件的所有行|
|`f{char}`|到下一个{char}字符处，比如`fa`|
|`;`、`,`|下一个、上一个，重复查找上次 `f{char}` 命令所查找的字符|
|`/`|查找提示符，`/content`|
|`*`、`#`|匹配光标所在的单词，`*`：光标移动到下一个，`#`：光标移动到上一个|
|`n`、`N`|若有多个匹配，`n`到下一个，`N`到上一个。对`/`、`*`、`#`有效|
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
|`gv`|重选上次的高亮选区|
|`:1`|跳到第1行|
|`:$`|跳到最后一行|
|`:2,5d`|删除第2到第5行，包含第2和第5行|
|`:copy`|`:t`，复制，`:6t.`|
|`:move`|`:m`，剪切，`:6m$`|
|`<C-r><C-w>`|映射项，复制光标下的单词并把它插入到命令行中|
|`:`|查看命令记录，`<Up>`和 `<Down>`键|
|`/`|查看查找记录，`<Up>`和 `<Down>`键|
|`Ctrl-z`|挂起Vim进程。对应的`fg`：在bash命令行唤醒被挂起的Vim|
|`!`|在Vim的命令行模式调用外部程序，比如`:!ls`, 调用sort命令 `:2,$!sort -t',' -k2`|
|块操作@每行相同位置|块注释：`^ <Ctrl-v><j>I//[ESC]`<br>`I// [ESC]`中的`I`是进入插入模式，输入"//"，按ESC键使每一行生效<br>逻辑：可视模式下选择列，然后通过`c`或者`I`进入插入模式，插入字符串之后，按ESC键|
|块操作@每行末尾|在每行末尾加分号";" ： `<Ctrl-v><j>$A;[ESC]`<br>逻辑：可视模式下选择列，到行末尾，进入插入模式，输入字符串，按ESC键|
|工作区，多个窗口|- `:edit {file}` 命令把另外一个缓冲区载入活动窗口中<br>- `:sp[lit] {file}`，水平切分当前窗口，并在新窗口中载入{file}<br>- `:vsp[lit] {file}`，垂直切分当前窗口，并在新窗口中载入{file}<br>- `Ctrl-w`，在窗口间循环切换<br>- `:on[ly]`，只保留活动窗口，关闭其他所有窗口|
|标签页|- `:tabe[dit] {filename}`，打开一个新的标签页<br>- `:tabn[ext]`，`gt`，切换到下一个标签页<br>- `:tabp[revious]`，`gT`，切换到上一个标签页|
|`<Ctrl-n>`、`<Ctrl-p>`|自动补齐（插入模式）|
|`p`|将寄存器中的文本粘贴到光标之后或者当前行的下一行，比如`"ap`、`"0p`|
|`P`|将寄存器中的文本插入到光标之前或者当前行的上一行|
|Vim寄存器|- 无名寄存器（""），无名寄存器总是缺省的<br>- 复制专用寄存器（"0），仅当使用`y{motion}`命令时才会被赋值<br>- 有名寄存器（"a – "z），一组以 26 个英文字母命名的有名寄存器|


注：不同的命令是在不同的模式（普通、插入、可视、命令行模式）下生效     
■■ 不二法门：学习、练习、实践、学习、练习、实践………  
Update：2019-6-13
