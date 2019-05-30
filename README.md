# vimPractice

## Reference
[Practical Vim](https://book.douban.com/subject/10599776/)  
[Vim实用技巧](https://book.douban.com/subject/25869486/)  
[书中所有的示例和源代码](https://pragprog.com/titles/dnvim/source_code)

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
|`s`|删除光标下的字符+插入模式|
|`x`|删除光标所在字符|
|`w`|word forward，光标在单词开头|
|`b`|word backward，光标在单词开头|
|`e`|word forward，光标在单词结尾|
|`dw`|delete word，删除整个单词|
|`u`|撤销，undo|
|`%s/content/copy/g`|全局替换|
|`/`|查找提示符，`/content`|
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
|`:`|查看命令记录，`<Up>`和 <Down>`键|
|`/`|查看查找记录，`<Up>`和 <Down>`键|
|`Ctrl-z`|挂起Vim进程|
|`fg`|唤醒被挂起的Vim|
|`!`|在Vim的命令行模式调用外部程序|
|`:2,$!sort -t',' -k2`|调用sort命令|
