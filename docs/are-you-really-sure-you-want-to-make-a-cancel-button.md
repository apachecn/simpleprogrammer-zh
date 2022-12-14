# 您真的确定要制作取消按钮吗？

> 原文：<https://simpleprogrammer.com/are-you-really-sure-you-want-to-make-a-cancel-button/>

您真的确定要为您的应用程序创建取消按钮吗？

你知道，我可能会点击它。

我不仅会点击它，还会在最不合适的时候点击它。

我可能会在你复制的那个大文件中间点击它，就在你启动第二个线程之后。



![exploding-earth](img/4116f10e7e459701a94ece5aa05515f2.png "exploding-earth")



## 取消是一种承诺

下次你考虑创建一个取消按钮时，我建议你把它当成一个承诺。

在我的世界里，取消按钮有两个承诺。

1.  以非破坏性的方式停止当前正在发生的事情。
2.  马上停下来！

我遇到过很多取消按钮，它们不符合任何用户所期望的基本取消规则。

事实上，每当我看到它的时候，我都会随机点击“取消”，这让我的同事很沮丧。

我开始做这个，因为我想知道癌症有多普遍。

这种现象非常普遍。我测试过的大多数取消按钮既不能立即停止，也不能防止破坏。

相反，我发现在大多数程序中点击“取消”按钮肯定会使程序挂起很长一段时间，最终导致您终止进程，并且它往往会使进程半途而废而不回滚。

## 清理东西

让我在这里说清楚一点。我说的不是你在“确定/取消”对话框中看到的取消按钮。大多数情况下，这些取消按钮实际上是有效的，因为它们实际上是作为“后退”按钮来操作的，它们实际上并没有取消正在进行的进程。

我说的主要是取消正在进行的活动的取消按钮。例如，在安装程序或 SVN 更新过程中取消按钮。

我们可以称这种取消按钮为“异步取消按钮”

## 但是，我需要为用户提供一种取消的方法

很好，但是不要撒谎。

有些事情是无法取消的。

当我上了飞机，我可以取消我的旅行，当我坐在那里等着门关上的时候。我甚至可以在飞机滑行到跑道时取消我的旅行，如果我大喊“**我被一颗着火的炸弹强奸了！**

但是，一旦飞机起飞，我就不能取消我的旅行。如果我试图取消它，那么…嗯，不好的事情会发生。非常糟糕的事情。

那么，为什么当我在安装你的软件，或者你的软件正在更新它的数据库时，我有这个闪亮的小取消按钮，我可以在这个过程中随时点击它呢？

我当然不能随时取消！

当然，在这一过程中，有些部分取消将是致命的，或者说，要想挽回已经太晚了。

我的观点是，如果用户真的不能取消，不要给出一个按钮说他们可以。更具体地说，如果你不能从上面遵守取消 1 和 2 的法则，就连一个按钮都不要显示。只需说“对不起，此时您不能取消此流程。”

我甚至不需要知道为什么我不能取消。我的意思是，如果你告诉我 Unicorn Glitter 引擎处于临界状态，任何中断都可能结束我们所知的生命，这将使我感觉更好，但我会满足于你只是灰色显示取消按钮或根本不显示它。



![cancel-button](img/d5702b22db37ca9e4c020a613dab8c2d.png "cancel-button")



## 重新戴上开发者的帽子

我自己也有负罪感。我知道我在过去创建的取消按钮已经造成了痛苦和烦恼。

但是作为开发者，我们能做些什么呢？

首先，我们应该仔细考虑将一个长时间运行的过程分成几个步骤。在这一过程的每一步，我们都应该考虑是否可以在不破坏数据和挂起应用程序的情况下取消这一步。

在任何长时间运行的过程中，我们应该能够确定哪些部分是可取消的，哪些部分取消是没有意义的。

作为开发人员，您的职责是确保如果您决定允许取消，那么取消会撤消现有的流程并立即工作。

我怎么强调都不为过！

这是大多数用户期望的行为，也是单词 cancel 的真正含义。

要做到这一点可能需要额外的工作。您可能需要更多地考虑应用程序的线程情况。您可能需要考虑回滚的情况。但是，如果你不这样做，你的取消按钮就会变得像那个喊狼来了的男孩一样，没有人会相信他们。

如果你不愿意这样做，至少，对你的用户友好一点，去掉取消按钮，因为你可以打赌我会点击它！