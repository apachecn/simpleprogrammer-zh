# 学习如何更快编码的 4 个技巧

> 原文：<https://simpleprogrammer.com/learn-to-code-faster/>

![learn code faster](img/28d245abe877dd986854c8a8e4ea078f.png)

Learning to program can be brutal. You never know if you’re learning the right things, and it’s easy to become overwhelmed by how much content there is to learn. That brings up a good thought: How do you know when you’ve learned enough to start applying for jobs?

很有可能，你关心的是要花多长时间来学习如何编码。你感受到在尽可能短的时间内尽可能多地学习的压力。你想要摆脱你目前的角色，或者缺少角色，并最终找到一份给你报酬的工作。

无论你追求的是加薪还是整个职业生涯的改变，编程都可以让你的职业生涯硕果累累，充满力量。您只需要学习代码的基础知识，这样您就可以开始新的激动人心的编程成功之旅。

然而，没有人愿意花费不必要的时间来确定基本的编程原则——别担心，我不会让这种事情发生在你身上。

如果你想快速学习编码，继续阅读。我将通过给你行之有效的战略和战术来解开如何快速学习编程的秘密，这些战略和战术将帮助你申请工作、获得面试和获得高价值的工作机会。

准备好了吗？让我们开始吧。

## 不要满足于短期收益

我明白了。你想快速编码，你想现在就编码。

但我会尽可能直截了当地告诉你。如果你做了以下任何一件事，你都不会帮助你自己:

*   在不理解代码的情况下复制和粘贴代码。
*   盲目地完成课程和教程。
*   无法将你在课程/教程中“学到”的语法应用到学习环境之外的问题中。

我记得当我第一次开始学习如何编程。我完成了两门编码课程，并完成了三个项目教程，每个教程都有 1000 多行代码。我对自己感觉很好。

但当我开始面试编程角色时，我每次技术面试都失败了。我甚至试过参加 W3Schools 的 [Python 测试](https://www.w3schools.com/python/python_quiz.asp)，结果惨败。事实是，我满足于“完成”课程和辅导的短视快乐。

*不要*像 n00b 大牛一样，无脑地完成课程和教程。不要在不了解你在复制什么的情况下复制和粘贴代码。

相反…

## 争取理解(速度随后)

如果有人告诉我“为理解而战”，说我实际上会比完成课程和教程学得更快，我会嘲笑他们。

我的编程之旅的第一年是残酷的，因为我在无意识地写代码——我没有试图理解我所学的东西。

考虑下面的例子，以及我是如何努力理解 for 循环的:

`n = 4
**for** i **in** range(0, n):
print(i)
Output:
0
1
2
3` 

如果你从例子中什么都不懂，不要着急；显然我也没有。我认识到 n = 4 是一个存储数字 4 的变量。我还可以告诉你 for 循环打印了 0 到 3。但是我不能告诉你(I)是什么，也不能告诉你为什么 for 循环只打印 0 到 3 而不打印 4。

这是我六个月的编程生活。

我会尝试识别我熟悉的语法，但是当我看到我不理解的代码时，我的大脑会一片空白。最糟糕的是，我唯一的决心是在不理解我所写的代码的情况下输出一个结果。

这是最糟糕的地方。

![learn code faster](img/e7095bec305665e49ecd579c9cd5cabe.png)

But if I were to learn how to program all over again, I’d try to fight for understanding. I’d probably also read [Grokking Algorithms](https://www.amazon.com/Grokking-Algorithms-illustrated-programmers-curious/dp/1617292230/ref=sr_1_3?crid=JPG96MFMWSU4&dchild=1&keywords=grokking+algorithm&qid=1601442555&sprefix=grokking+%2Caps%2C223&sr=8-3) earlier in my career because it helped simplify so many complex coding concepts for me.

以下是我试图理解 for 循环的方法:

我会问自己，“这里起作用的主要原则是什么？“谷歌搜索、 [StackOverflow](https://stackoverflow.com/) 和 [GeeksForGeeks](https://www.geeksforgeeks.org/) 会成为我最好的朋友。

任何一种搜索机制都会告诉你 for 循环都是关于*迭代*的。For-loops 归结为一个动作:他们在说“对于一组事物中的每一个事物，给我每一个事物。”

在上面的例子中，for 循环是这样说的:对于一组事物(range(0，n):)中的每个事物(I)，一次打印出一个事物。

第二个原则是 for 循环的“事物集”(range(0，n):)。根据这个原理，您会发现 range(0，n)是一个名为 range()的函数。如果你谷歌一下 range()函数，你会发现它允许程序员创建一个数字序列。

所以在这种情况下，range(0，n)表示你的“事物集”是数字 0，1，2，3。range()函数不打印数字 4，即使 n = 4，因为该函数只包含第二个数字之前的所有数字。

如果您想打印数字 4，请将 n = 4 改为 n = 5。现在，范围(0，n)将包括数字 4，不包括数字 5。

如果你优先考虑理解，我保证从长远来看你会学得更快。学习如何编程不是数字游戏。我再说一遍:学习如何编程不是关于你能记住多少语法或者你能完成多少项目。学习如何编程的关键是*理解*。这就引出了我的下一个观点。

## 不要担心什么都学，只要学对了就行

你不可能在现实的时间内学会所有基本的编程原则。你没有两年的时间来确定递归、类和数据结构的每一个概念。毕竟，你想尽快得到一份编码工作，不是吗？

但我会告诉你你有时间做什么。**正确的概念。**

你有充足的时间去学习那些能让你找到工作的概念。更困难的部分是弄清楚那些“正确的”概念是什么。如果你想在这些概念上领先一步，我推荐你去看看 [Python 速成班](https://www.amazon.com/Python-Crash-Course-2nd-Edition/dp/1593279280/ref=sr_1_10?dchild=1&keywords=learn+how+to+program&qid=1601442651&sr=8-10)，这是来自系列[如何用 Python](https://www.amazon.com/Automate-Boring-Stuff-Python-2nd-ebook/dp/B07VSXS4NK/ref=sr_1_1_sspa?crid=LPGGEL1RB5P7&dchild=1&keywords=how+to+automate+the+boring+stuff+with+python&qid=1601442733&sprefix=how+to+aut%2Caps%2C215&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFZUUYzV1IxQ1dGUDImZW5jcnlwdGVkSWQ9QTA4NDI5MTEzMUtWWVRRWjBUS0Q3JmVuY3J5cHRlZEFkSWQ9QTAxNDM1ODYxN1JEUzMwWkhCR0o0JndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ==) 自动化枯燥的东西。

很多人问我，“我应该学些什么？

我每次都告诉他们相同的答案，而且不包括“函数”、“递归”、“正则表达式”或任何其他基本/面试编程概念。

我带他们做了一个练习，准确地告诉他们需要知道什么。我想带你做同样的练习:

1.  **在 LinkedIn 上找一个入门级的软件工程角色。**您可以使用“工作”选项卡上的“经验”功能，或者寻找招聘 0-2 年经验的职位。
2.  找到工作描述中的“职责”和/或“要求”部分。你看到了什么？是类似于“*强大的软件架构基础、数据结构和批判性思维*”的东西吗？你是否看到类似“*知道服务如何处理 HTTP 请求*”的内容？
3.  将“职责”和“需求”部分转化为编程概念。在上面的例子中，你可以推导出一些你应该知道的编程概念。架构基础、数据结构和后端服务(HTTP 请求)。
4.  研究并努力理解你从工作描述中得出的编程概念。谷歌将是你最好的朋友。找到愿意帮助你的成熟程序员。查看[这篇文章](https://simpleprogrammer.com/how-do-you-find-a-mentor/)，了解如何找到编码导师。

这个过程很容易让人不知所措。你需要知道的最重要的事情是，你不需要知道每一点语法，只要知道能让你找到工作的正确的语法和概念。

## 参加新兵训练营测试

关于编码训练营是否是学习如何编码的好方法的讨论由来已久。这里有一个直接切入辩论的论点:你在新兵训练营学到的一切都可以在网上免费学习*。*

*那么，人们为什么要报名参加新兵训练营呢？*

*新兵训练营是一个方便而又严格的六到九个月的选择，可以让你快速找到一份科技工作。他们还为你联系编码导师和网络资源，帮助你安排面试。*

*这就是我喜欢称之为“新兵训练营测试”的东西，我鼓励你看看自己做得怎么样。回答以下问题:*

1.  *如果有人给你学习如何编码所需的所有学习资源，你会接受吗？*
2.  *如果你不得不在接下来的六到九个月里致力于一系列严格的课程、习题集和面试练习，会怎么样？*
3.  *如果你必须支付几千美元呢？*
4.  *如果面试和工作没有保障会怎样？*

*如果你对至少两个问题的回答是“不”, 1)训练营可能不适合你，2)你刚刚学到了很多有抱负的程序员永远也不会明白的东西。*

*新兵训练营测试将学习过程纳入视野。你不是来这里接受为期六到九个月的严格训练的。你在这里学习，直到你找到工作。你想得到一份尽可能有把握和保证的工作。*

## *意识到“长期游戏”并不漫长*

*![learn code faster](img/135a549372a1fe882e4531de6bf42d95.png)*

*I highly recommend you play the “long game” with learning how to program.

你可能会想，“什么，两年？五年？十个？”

以上都不是。

如果你想花两年时间学习编程，请便。

但是你要知道，你不必这样做。

当我说“长期游戏”时，我指的是你如何学习，而不是有多快。

学习如何编程的长期游戏要求你停止满足于短期收益。不再盲目地完成课程和教程。长期游戏也要求你把理解放在首位。如果你忘记了学习一切，而是专注于学习正确的东西，你会学得很快。当你感到疲惫时，参加新兵训练营测试，重新审视学习过程。

学习的过程可能是残酷的，令人不知所措的，但这一切都是唾手可得。你正朝着正确的方向前进，你已经拥有了你所需要的一切。

我知道你现在就想编码，而且想快速编码。你现在有工具和手段来做到这一点。不断学习，不断推动，永不放弃。*