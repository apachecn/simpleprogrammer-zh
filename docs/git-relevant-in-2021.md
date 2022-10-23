# 为什么 Git 在 2021 年仍然有意义，而且会有很长一段时间

> 原文：<https://simpleprogrammer.com/git-relevant-in-2021/>

![Git version control system](img/4ee5c5069408d3ffd23d19e66c209955.png)

Git has been around since 2006 when it was created by Linus Torvalds, the same mind behind Linux. Between 2006 and the present, Git has become the dominant version control system (VCS) used in software development, dwarfing others such as Mercurial, Subversion, BitKeeper, Darcs, and a plethora of lesser known tools. It’s a good bet that if you write code and have ever collaborated with another developer, Git is the VCS that you use.

随着我们进入 2021 年，Git 由于各种原因仍然相关，并可能在相当长的时间内保持其主导地位，正如我将在本文中向您展示的那样。Git 是开发人员日常工作的主要部分，了解它当前和未来可能的趋势对一个人的职业生涯非常重要。

## Git 目前的主导地位

Git 目前相关性的最强驱动因素是，它已经是绝大多数开发人员选择的版本控制系统。这意味着个人开发者、独立团队、学术用户和行业部门将继续选择它，因为这是开发者社区和人才库所熟悉的。强者愈强，弱者工具淡出主流。

这也意味着那些在采用像 Git 这样的新技术方面进展缓慢的团队将会继续进行这种转变，而且速度可能会越来越快。有许多团队仍然使用更传统的集中式 VCS 工具，比如 Subversion。这可能是因为他们的组织已经扎根于该系统多年。

但是，他们中的越来越多的人会被经济因素所迫而升级到 Git。这是因为 Git 提供了更灵活的协作工作流，他们的大部分技术员工都会熟悉它。正如我们将在后面看到的，将以前用不同工具跟踪的代码库移植到 Git 也是非常容易的。

## Git 的品牌

Git 持续相关性的第二大预测因素是其品牌。当人们想到版本控制和跟踪代码时，他们会立即想到 Git。即使非开发人员也熟悉代码托管网站，如 GitHub 和 BitBucket。GitHub 尤其在主流的眼光和意识中。

强大的品牌很重要，因为它让世界上的人们认识到一种产品或服务，参与围绕它的叙述，并帮助影响他人使用它。它还允许产品或服务与上下文相关的主题相关联——在这种情况下是软件开发、编程和协作。

在我们这个时代尤其如此，在这个时代，如此多的影响力是由谷歌的算法和爬虫驱动的，推动了相关主题之间的流量。Git 就像版本控制的可口可乐。最终，它的品牌将帮助它在吸引新开发者的同时，进一步影响现有用户。

## 切换到 Git 的便利性

正如我前面提到的，用户了解 Git 并希望转换到 Git 是一回事，但是需要有一个直接的途径将遗留项目迁移到 Git。幸运的是， [Git 提供了从其他系统迁移的完整文档](https://git-scm.com/book/en/v2/Git-and-Other-Systems-Migrating-to-Git)。

上面的指南包含了如何将代码库从 Subversion (SVN)、Mercurial、Bazaar 和 Perforce 迁移到 Git 的步骤。

本质上，对于每个系统，Git 都有一个允许与源系统交互的子命令。例如，`git svn <subcommand>`命令集用于与 Subversion 存储库交互。可以把这些命令想象成源系统和 Git 后端之间的翻译器。

Git 甚至提供了一个定制的导入器，您可以使用它从 Git 不支持的其他系统中迁移您的项目。

## Git 的最小可行用例

一般来说，对于新开发人员来说，版本控制可能是一个棘手的话题，因为他们[正在学习编程](https://initialcommit.com/blog/reddit-learn-programming)。这不是最直观的概念集，需要在几个项目中进行实际实践才能掌握。

然而，在我看来，使用 Git 的“最小可行用例”只需要学习一些相对简单的命令。尽管 Git 很灵活，可以支持许多不同的团队工作流，但是有一个非常简单的途径可以学习 Git 的基础知识。这是基于 Git 的核心概念:工作目录、T2、中转区和提交的变更。

工作目录是文件系统中当前存在的一组代码文件和文件夹。这些是您在代码编辑器中打开并对其进行更改的文件。所有版本控制系统都有一个工作目录(或等效术语)，所以这并不是 Git 独有的。

一旦您完成了一个特定的编码任务，比如修复一个 bug 或添加一个新特性，您可以使用`git add <file.ext>`命令将您更改的文件添加到 Git 的暂存区(也称为暂存索引或缓存)。可以把这看作是代码的炼狱——一旦所有的更改都放在一起，您就准备把代码永久存储在 Git 中。

staging area 本质上是 Git 开发的一个概念。其他系统倾向于跳过这一步，在我看来，这省略了帮助开发人员提交干净代码的重要准备步骤。

流程的最后一部分是将临时区域中的更改提交给 Git 存储库。这是使用命令`git commit -m “Commit message”`完成的。这将获取添加到临时区域的所有更改，并创建一个新的提交对象，该对象存储在您的 Git 存储库中。该提交成为当前分支的末端，链接到链中的前一个提交或父提交。

最后三段基本上概述了 Git 的核心功能。这些概念的学习曲线相对较浅，这将使新开发人员不断加入 Git 的生态系统。因此，Git 将继续成为新开发者学习的[必备编码工具。](https://www.amazon.com/dp/B084M21LBZ/makithecompsi-20)

## Git 的其他效率

除了上一节描述的基本功能之外，Git 还有许多其他设计原则和特性，使它比 VCS 的竞争对手更高效。其中包括轻量级分支和合并、灵活的参考模型、内容寻址数据库等等。

在 Git 出现之前，现有的 VCS 工具如 CVS(并发版本系统)使合并代码成为一场噩梦。使用 CVS，用户经常会遇到复杂的、有冲突的代码变更，需要花费大量的精力来手动解决。Git 普及了“容易并经常合并”的范例，在这种情况下，开发人员经常创建新的分支，甚至是针对小的特性/修复，Git 通常可以自动处理将更改合并回主分支。

这对开发人员来说非常好，因为它最大限度地减少了手动修复合并冲突所花费的时间和精力。

Git 也有一个高效的参考模型，对开发人员来说很直观，不需要他们进入技术领域。Git 允许用户为他们的分支创建名称，并创建标记特定分支提交的标签。分支名称和标记是一组更一般的对象的一部分，这些对象称为引用，即指向底层 Git 提交的指针。

此外，Git 还管理一些 refs，比如 [Git HEAD](https://initialcommit.com/blog/what-is-git-head) ，来表示当前分支的尖端。这些 refs 允许开发人员轻松理解他们正在处理的提交，而不必处理复杂的 Git 术语。

这里我们要涉及的最后一个方面是 Git 的内容寻址对象数据库。Git 将所有关于代码的数据存储在一个叫做对象数据库的东西中。这是 Git 存储库中的一个隐藏目录。当您使用 Git 跟踪文件、将文件添加到临时区域以及创建提交时，Git 会在对象数据库中创建对象。这些对象是根据它们包含的内容来命名的，这就是我们称之为“内容可寻址”的原因

这使得 Git 可以利用众多的性能效率，并且比其他工具更快地运行各种命令。

## Git 继续发展

![Git version control system](img/ed81edc2a7fff2704fe463b2902a6b23.png)

One final factor I will note is that [Git’s code](https://www.amazon.com/dp/B07MNKZJR9/makithecompsi-20) continues to evolve. Git has a very active open-source development community made up of a core set of developers surrounded by hundreds of other contributors.

因此，很可能即使其他工具构建出了推动版本控制行业发展的特性，Git 开发人员的专业知识也允许他们将类似的功能整合到 Git 中。

这给 Git 提供了一个坚实的护城河，保护该工具免受 21 世纪快速变化的技术竞争的影响。

## Git 的未来

本文描述的因素为 Git 在未来继续占据主导地位提供了有力的论据。即使从技术或可用性的角度来看，一个新工具确实超过了 Git，对于大多数开发人员来说，从 Git 转向这个新工具也需要几年的时间。

为了便于比较，我们可以看看编程语言。尽管出现了更新的替代语言，如 Java、JavaScript、 [Python](https://simpleprogrammer.com/5-benefits-of-python/) 、Rust、Go 等，但即使是非常古老的编程语言，如 Fortran、C 和 Perl，今天仍在积极使用和开发。

持久力的关键是他们的社区继续存在。在我看来，即使 Git 被另一个工具超越，在未来的几十年里，它仍然会在软件开发人员的工具箱中占有一席之地。