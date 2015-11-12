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


#未完成的任务：3个格式规则

Todo.txt的美妙之处在于它是完全非结构化的;你可以连接到每个任务的字段只限于你的想象力。要开始使用，用特殊的符号来表示任务的情况下（如@phone），项目（如+ GarageSale）和优先级（如（A））。所以，Todo.txt文件可能是这样的：

    (A) Thank Mom for the meatballs @phone 
    (B) Schedule Goodwill pickup +GarageSale @phone
    Post signs around the neighborhood +GarageSale
    @GroceryStore Eskimo pies

一个可以分离出@phone情景的条目并把这些条目发送到你手机的脚本可以输出如下内容：

    (A) Thank Mom for the meatballs @phone 
    (B) Schedule Goodwill pickup +GarageSale @phone

调用todo.sh只输出车库出售（garage sale）项目中的条目会显示：

    (B) Schedule Goodwill pickup +GarageSale @phone
    Post signs around the neighborhood +GarageSale

在当前的tod中o有3个格式规则。

##规则1：如果有优先级，那么它一定显示在行首

优先级使用括号中包含A-Z的大写字母后面加空格的方式表示。

比如，这是个A级优先的任务：

    (A) Call Mom

以下的任务没有优先级

    Really gotta call Mom (A) @phone @someday
    (b) Get back to the boss
    (B)->Submit TPS report

##规则2：任务的创建日期（可选）在优先级后，之后是一个空格。

如果没有优先级，创建日期显示在行首。创建日期的格式应该为 YYYY-MM-DD。

以下任务有创建日期：

    2011-03-02 Document +TodoTxt task format
    (A) 2011-03-02 Call Mom

这个任务没有创建日期：

    (A) Call Mom 2011-03-02

##规则3：在_优先级和计划日期后面_，情景和项目可以在行中任何位置出现。

情景使用一个空格和@符号标记。项目使用一个空格和+符号标记。项目和情景可以包含除空白字符外的任意内容。一个任务可以有0个、1个或者多个任务和情景。

比如，这个任务是在 @iphone 和 @phone 情景下，+Family 和 +PeaceLoveAndHappiness 项目的一部分：

    (A) Call Mom +Family +PeaceLoveAndHappiness @iphone @phone

没有情景的任务：

    Email SoAndSo at soandso@example.com

没有项目的任务：

    Learn how to add 2+2

#完成的任务：2个格式规则

2件事表明任务已经完成。

##规则1：完成的任务使用X开头。

如果一个任务使用X（区分大小写）之后一个空格开头，那么表示任务完成。

完成的任务：

    x 2011-03-03 Call Mom

以下不是已经完成的任务：

    xylophone lesson
    X 2012-01-01 Make resolutions
    (A) x Find ticket prices

我们用小写字母x，这样在使用标准的排序工具排序后，完成的任务会排在任务列表的底部。

##规则2：完成日期直接出现在X后，用空格隔开。

例如：

    x 2011-03-02 2011-03-01 Review Tim's pull request +TodoTxtTouch @github

如果你需要任务的创建时间，它直接跟在创建时间之后。这是为了使用排序工具按照时间按排序已经完成的任务。许多Todo.txt客户端会丢弃已经完成的任务的优先级。可以使用key:value的方式保存（比如，pri:A）

在右完成日期的时候（必须），如果还有预期时间（计划时间？起始时间？）（可选），你可以计算完成任务使用的天数。


