# Todo.txt-to-Zhs
Todo.txt 格式说明中文翻译
个人水平有限，如有错误，请见谅。大部分Google翻译^_^

ps：github也是第一次用 -_-|||

原始地址: https://github.com/ginatrapani/todo.txt-cli/wiki/The-Todo.txt-Format

***

# Todo.txt 文件格式说明
如何使用todo.txt的完整入门


# 为什么使用纯文本？
纯文本与软件和操作系统无关。它是可搜索、便携、轻巧和操作方便的。是非结构化的。当网站关闭或者Outlook.pst文件损坏时，它仍然可以工作。不需要导入与导出，没有数据库、标签、旗帜、加星、优先级、或类似[插入公司名称]这样你可以或者不可以的规则。


#有效的todo列表的3个维度
通过使用特殊符号，你可以将Todo.txt创建成一个有3个维度列表。

__优先级.__ 你的Todo列表应该能够告诉你下一个你需要完成的最重要的事情， - 无论是通过项目或上下文或整体。你可以通过选择任务的优先级将它们放置到列表的顶端。

__项目.__ 推动一个大的项目（project前进的唯一途径是解决与之相关的子任务（task）。你的Todo.txt应该可以列出所有的与某个项目相关的任务。
为了推进类似“清洗车库”这样的项目，我的任务列表（task list）应该给我下一个合理的可以推进项目前进的行动。“清理车库”不是一个好的todo条目；但是在“清理车库”项目中的“Call Goodwill to schedule pickup”（这个玩意怎么翻译？打电话叫Goodwill来收拾？）不错。

__情景.__ 《Get things Done》的作者David Allen建议通过“情景”分割你的任务列表 - 比如，在你工作（job）的地点和情况下。发送信息在“@email”情景；打电话在“@phone”情景；家庭计划在“@home”。

这样，当你在车里有几分钟的时间可以打手机的时候，你可以方便的检查你的“@phone”任务并打上一两个电话。
这些在todo.txt中都是可行的。


#Todo.txt格式规则
你的Todo.txt是纯文本文件。使用一些简单而灵活的文件格式规则可以为采用优先级、项目、环境、创造和完成日期这种结构的元数据带来好处。

哲学上，Todo.txt文件格式有两个目的：

+ 文件内容应该是人类可读的，而不需要其它的工具。

+ 用户可以使用纯文本编辑器正常的操作文件内容。例如，一个可以按字母书讯排序的编辑器应该可以按照有意义的方式排序你的任务列表。

（这两个目的是为什么，例如行以优先级和/或者日期开头。原因是可以方便的以优先级或者时间排序；已经完成的条目使用X标记，这个标记在按照字母顺序排序时会在底部，并且看起来像被填充的选框。）

Todo.txt的第一条也是最重要的一条的规则是：__在Todo.txt文件中的一行只用来表示一个任务。__

休息一下。


#未完成的任务：3格式规则

