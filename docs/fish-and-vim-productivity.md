# 用鱼和 Vim 提高生产力

> 原文：<https://simpleprogrammer.com/fish-and-vim-productivity/>

![](img/fbd39e0f8df646270b56a50502143318.png)

As modern developers, we can be tempted to jump into coding projects or tasks on a whim, using tutorials or guides found online as a starting point. With the power of Google at our fingertips, we can easily look up code snippets, tool features, commands, and concepts on the fly in order to utilize them in our workflows.

然而，花时间学习一套核心理念并将其整合到我们的开发工作流程中，将有助于我们在工作时理清思路并提高生产力。

显而易见，当寻求生产力提升时，瞄准我们最常用的工具通常会产生最大的收益。

作为一名开发人员，我发现我的大部分时间都花在命令行工作或在我的文本编辑器中编码。因此，在本文中，我将描述用户友好的 Fish shell 和 Vim 文本编辑器的一些基本生产力特性。更具体地说，我将讨论这两个工具的自动补全建议和拼写检查特性。

即使您以前没有使用过这些工具，也非常值得试用一下，因为您可以提高工作效率。对于使用过这些工具但不知道这些特性的人来说也是如此。与其他开发人员分享类似的技巧和诀窍对团队建设非常有帮助，并且会帮助你脱颖而出。

## 贝壳的背景

在开始之前，我想介绍一下壳的概念。shell 决定了在命令行输入命令时我们可以使用的界面。Shells 提供了有用的功能，如 tab 自动补全、目录遍历和记录已执行命令的历史。一些流行的 shells 包括:

*   BASH(又是 Bourne Shell):可能是目前使用的最流行的 Shell。
*   ksh (Korn Shell):一个较老但仍然流行的 Shell，具有与 BASH 相似的功能。
*   Zsh (Z Shell):一款越来越受欢迎的高性能外壳。2019 年，它被选为 Mac OS X 的新默认外壳。
*   Fish (Fish Shell):一个用户友好的 Shell，具有许多面向出色用户体验的特性。(我的最爱！)

如果你想跟随我的领导，尝试鱼壳，使用他们网站上的安装步骤[。](http://www.fishshell.com)

## 鱼中的命令建议

大多数传统 shells，比如 BASH，都提供基本的 tab 补全功能，允许用户开始输入命令或路径，并通过按 tab 键来完成。如果找到多个匹配项，第二次按 tab 将列出所有可用选项。这通过节省击键次数来提高生产率，随着时间的推移，击键次数会迅速增加。

然而，Fish 并不简单地寻求复制传统 shells 的风格——它的目标是优化用户体验。除了标准的制表符补全之外，Fish 还使用命令历史以及关于特定命令的附加知识来为部分键入的命令建议可能的补全。

这些建议以灰色(非活动)文本显示在用户活动命令的右侧，并在用户键入时动态更新。用户可以使用上下箭头键滚动不同的建议。假设建议与用户想要的命令或路径匹配，可以使用右箭头键来应用(激活)它。

正如我提到的，Fish 实际上可以为特定的命令提供上下文相关的建议。一个流行的例子是它对 Git 命令的支持。Fish 知道如何检查 Git 存储库来获取分支名称和已经提交的文件等信息。

Fish 使用这些信息来建议非常准确的命令完成——当它预测您想要提交哪个文件或合并哪个分支时，感觉好像 Fish 正在读取您的想法！

当对多个匹配项使用 tab 自动补全时，Fish 不仅会显示匹配的命令或路径名。它还会尝试提供每个条目的附加信息，比如每个结果的简要描述和/或文件大小。

随后按 tab 键将展开结果的完整列表，并逐个切换。用户可以在这个过程中的任何时候开始输入，以显示一个搜索栏，可以用来过滤结果。

在第一次使用 Fish 之后，我清楚地意识到它直观的界面能为我节省多少时间。作为补充，让我们看看 Vim 文本编辑器的一些类似的[生产力特性](https://simpleprogrammer.com/programmer-productivity-time-attention-management/)。

## Vim 的背景

![](img/25a1864cd1374925114eb0fd4cc9b80b.png)

Vim is a popular open-source Command Line text editor that was released in 1991 by Bram Moolenaar. It is primarily used by developers to edit code files without having to leave the Command Line but is also well suited to general writing projects.

Vim 的界面允许用户在几种允许以不同方式与文本交互的模式之间切换。Vim 打开时激活的默认模式称为命令模式，它用于在文本文档中导航，并通过键入冒号后跟所需命令来发出有用的命令。第二种最常见的模式是插入模式，它允许用户直接在文档中键入文本。

Vim 有数百个命令和快捷方式，允许在命令行中高效地编辑文本。Vim 强调一种工作流，它可以最大限度地减少执行一系列操作所需的击键次数，并为最大限度地减少重复任务提供多种解决方案。Vim 附带了一个名为`vimtutor`的内置教程，可以显著[加快初学者的学习曲线](http://www.amazon.com/exec/obidos/ASIN/0596007124/makithecompsi-20)。

有关 Vim 的更多一般信息，请查看 Vim 网站。

## Vim 中的拼写检查和自动补全

Vim 附带了一个内置的英语单词列表，可以作为字典在文本文件中进行拼写检查。为了启用拼写检查，请在 Vim 的命令模式下打开一个文件，并键入:

`:set spell`

`:set`命令后面可以跟随各种选项(在本例中为`spell`)，以启用或禁用 Vim 中的不同功能。

运行该命令后，文本文档中拼写错误的单词将以特殊格式突出显示，通常带有红色虚线或类似的下划线，这取决于所使用的格式主题。

在命令模式下，`]s`命令可用于跳转到下一个拼写错误的单词。类似地，`[s`命令可用于跳转到前一个拼错的单词。`z=`命令将在光标下弹出拼写错误单词的建议更正列表。

列表中的每个建议更正都与一个数字相关联。用户可以通过输入与修正相关的数字并按下<enter>来选择要应用的修正。如果不需要修正，按下<enter>将简单地退出建议修正列表，而不做任何改变。</enter></enter>

Vim 还提供了一种简便的方法，可以有效地纠正先前在活动行中输入的错误。在插入模式下，命令`<CTRL-x><CTRL-s>`可用于跳转到最后一个错误，并自动显示建议更正的下拉列表。

Vim 的内置字典也可以用来在输入时提供自动补全建议。要做到这一点，Vim 的拼写检查器必须像我们之前看到的那样使用`:set spell`选项来启用。只需在插入模式下输入一个单词，然后输入`<CTRL-x><CTRL-k>`。这将显示一个下拉菜单，其中包含来自 Vim 字典的自动补全建议列表。

可以使用上下箭头键滚动列表中的项目，或者使用`<CTRL-p>`移动到上一个条目，使用`<CTRL-n>`移动到下一个条目。通过使用类似的命令`<CTRL-x><CTRL-k><CTRL-p>`，Vim 将允许您继续输入(或删除)单词中的字符，同时实时过滤自动完成建议列表。

## 小小的时间节省累积起来

![](img/1c547035aaedb8778036bedc5f5723bb.png)

In this article, we covered some productivity features of the Command Line tools Fish and Vim. We discussed how Fish shell’s Command suggestions can save time by reducing the number of keystrokes required when working on the Command Line.

我们还详细介绍了如何启用 Vim 的拼写检查器，以便在我们工作时建议更正和自动补全。

如果你是一名新的开发人员，想尝试一下命令行和编程，可以看看由[初始提交](https://initialcommit.com/)撰写的《开发人员编码基础指南*】一书。*

如果你在找一本专门介绍使用 Vim 的技巧和诀窍的书，可以看看《实用 Vim》这本书。

努力掌握这些工具是非常值得的，因为从长远来看，节省的时间会越积越多。虽然一开始学习新的东西看起来有点吓人，但经过几周的一点点练习，你可以学到一项新技能，这将为你的职业生涯带来回报。