# 回到基础:为什么单元测试很难

> 原文:[https://simple programmer . com/back-to-basics-why-unit-testing-is-hard/](https://simpleprogrammer.com/back-to-basics-why-unit-testing-is-hard/)

最近，我越来越开始质疑单元测试的价值。我真的开始怀疑我们投入到单元级测试中的所有工作，以及我们投入到应用程序中的额外支持是否值得。

我还不打算谈论那个话题。相反，我想看看单元测试的一些成本，并问一个问题“为什么单元测试很难？”

毕竟，如果单元测试不难，我们就不必质疑它是否值得。首先看看为什么它难，是什么使它难，这是有意义的。

在你开始学习任何新技能或概念之前，我建议你看一下我的课程[“快速学习任何东西的 10 个步骤”。](https://simpleprogrammer.com/store/products/learn-anything-quickly/)T3】



![ar119675077156567](img/e697df7bc3d593a211ab15bbd64b510a.png "ar119675077156567")



## 理想的场景

一旦你理解了如何做，单元测试本身就相当容易了。即使是测试驱动或行为驱动的开发也很容易掌握…至少对于理想的场景来说是这样。

那么什么是理想的情况呢？

这是一个单元测试，测试中的类没有外部依赖。

当一个我们正在为之编写单元测试的类没有任何外部依赖时，我们就不需要 mocks 或 stubs 或其他任何东西。我们可以写代码来测试我们的代码。

让我们来看一个例子。假设，我有一个名为 *Calculator 的类。这个*计算器*类有一些非常简单的方法。具体来说，我们来谈谈测试方法*的补充。Add* 取两个一位数整数，返回结果。如果传入的任一整数超过一位数，它将引发异常。*

这是一个相当愚蠢的方法，几乎没有用，但它将在这里很好地服务于这一点。

我们可以不费吹灰之力对这个婴儿进行 TDD 或 BDD。

让我们开始考虑测试用例:

*   当我添加 0 和一个一位数时，它应该返回一位数
*   当我把 0 和 0 相加时，它应该返回 0
*   当我把两个一位数相加时，它会返回这两个数的和
*   当我添加一个两位数时，它会抛出一个异常

想出测试用例很容易，实现它们也很容易:

然后，我们可以实现代码，使这个测试非常容易地通过。我不会在这里展示它，因为它太琐碎了。

这是理想的场景，或者我称之为**第一级单元测试**。

第一级单元测试是我们有一个没有外部依赖和状态的类。我们只是在测试一个算法。

## 更上一层楼

如果我们向被测试的类添加状态，就达到了单元测试的下一个层次。

第二级单元测试是指我们有一个没有外部依赖的类，但是它有状态。我们正在设置一个对象，并将它作为一个整体进行测试。

如果我们以现有的例子为例，现在我们想添加一个名为 *GetHistory，*的新方法，实现测试仍然不难，但会变得更难，因为我们必须确保在测试中为我们的对象设置一些状态。

让我们看一下我们可能为此功能实现的一个测试案例:

还是那句话，不要太用力。但是，国务院确实让这变得有点困难。在这里，可以看到单元测试的行为驱动开发(BDD)风格的价值，因为它帮助我们清楚地将测试分成我们现在拥有的不同部分。

我们在这里增加的真正复杂性是，我们现在必须在执行测试之前处理一个设置步骤。BDD 通过定义实际测试发生的环境的特殊步骤来处理这个问题。在不同的 BDD 圈子中，它被称为一些不同的东西，但是让我们在这篇文章中坚持使用 AAA，因为它很容易记住。

第一级单元测试和**第二级单元测试**的主要区别在于，在第一级中，我们实际上只测试了一种方法。在级别 2 中，我们在班级级别进行测试。实际上我们可以称之为**1 级单元测试**方法测试，因为我们测试的单元就是方法。方法所在的类并不重要。

## 输入相关性

让我们看看当我们将依赖关系放入*计算器*类时会发生什么。

想象一下，我们的*计算器*类必须对我们的计算进行审计跟踪。我们有一个服务，可以用来将来自 *Add* 方法的计算结果放入一个存储位置，就像一个数据库，我们的 *GetHistory* 方法可以查询历史记录的存储位置。

当我思考这个问题时，我想到了一个重要的问题。如果这是一个集成测试，我们上面的示例测试方法根本不会改变。

但是，由于我们在这里讨论的是单元测试，我们需要将测试隔离到类级别。

所以让我们考虑一下我们的测试现在应该做什么。这里有一些我们可能会做的测试。

*   当我将两个数字相加时，结果被返回，带着这个结果对*存储服务*调用*存储*方法。
*   当我获取历史记录时，在*存储服务*上调用*检索历史记录*方法，并返回其结果。

让我们看看这些测试中的一个可能是什么样子的:

我称之为**第三级单元测试。**

第三级单元测试是当我们有一个至少有一个外部依赖的类，但是它不依赖于它自己的内部状态。

事情真的开始变得复杂了，因为我们不仅要考虑输入、输出和序列，还要考虑交互。

对于我们的单元测试的期望应该是什么，这里真的开始变得模糊了。在上面的示例代码中，我们需要检查以确保在*存储服务*上调用了 *IsServiceOnline* 还是只检查调用了*存储*？

您还会注意到，我们必须使用一个 mock 并将我们的依赖关系传递到我们的类中，这样我们就可以改变它的行为。随之而来的是创建接口的负担，这样我们就可以有一个模拟实现。

如果你现在正在注意，你可能会对自己说这个例子不好。你可能认为*计算器*类现在有两个职责。

*   它计算事物并返回结果
*   它存储计算结果

你说得对，但是我们不能希望这个问题消失。让我们假设我们重构并将 StorageService 依赖项移出了 *Calculator* 类。我们有几个选择。我们可以做一个装饰器，像这样使用它:

或者我们可以做一些更像中介模式的事情，就像这样:

无论我们如何尝试解决这个问题，我们仍然需要一些类在单元测试中进行模拟。

有一个我们无法回避的简单事实。如果我们要使用*存储服务*来存储计算结果，要么*计算器*将依赖它，要么其他东西将依赖计算器和它。这两个选项别无选择。

还有一个我们无法回避的简单事实。如果我们要在单元测试中依赖另一个类，我们要么需要一个可以用于模拟类的接口，要么需要一个支持模拟具体类的模拟框架。

所以在第三级单元测试中，我们不得不模仿至少一个依赖项，或者创建一个假的接口，或者使用一个模仿库来模仿具体的类。

## **情况变得更糟**

从这里开始只会变得更糟。在第 3 级，我们不担心 calculator 类内部的状态，我们担心的是一个外部依赖，它几乎为我们处理了状态。但是在许多情况下，我们将不得不担心状态和依赖性。

第 4 级单元测试是指我们有一个至少有一个外部依赖的类，并且依赖于它自己的内部状态。

在我们的计算器示例中，我们可以简单地添加这样的要求，即我们只想获得特定计算会话的历史记录。我们需要跟踪计算，以便我们可以向 *StorageService* 请求会话的历史记录。

让我们来看看针对这种情况的一个可能的测试:

考虑一下这个单元测试代码是多么脆弱和复杂。想想我们类的功能有多简单。

我们有一个大问题。我们的单元测试代码比它正在测试的代码更复杂！没关系，如果单元测试代码比它测试的代码多，通常就是这样。但是，当我们的单元测试代码更加复杂时，我认为这是一个大问题，因为你必须问自己一个非常现实的问题。

哪里更有可能出现 bug？

## 我什么也没说

我的观点不是要提出观点，至少现在还不是。我在这里的真正目标是帮助我们改变对单元测试的看法。

我们需要停止问单元测试是否值得花费的一般性问题，而是问更具体的问题:什么水平的单元测试值得花费。

级别 3+的成本非常高，因为模仿是不可避免的，并且甚至给最琐碎的实现增加了相当大的复杂性。

从中我们可以汲取一点智慧。如果我们要进行单元测试，我们应该努力将尽可能多的纯逻辑封装到没有依赖关系的类中，如果可能的话，没有状态。

另一件要考虑的事情是，随着单元测试的难度和复杂性在每一个级别上增加，测试的目标和价值也开始变得模糊。

我这样说的意思是，当我们开始测试我们的类正确地调用了另一个带有某些参数的类时，我们就进入了测试这个类的实现细节。

如果我说一个类应该能够将两个数相加并返回结果。我不是在谈论它必须如何做。只要结果是正确的，如何并不重要。

当我添加一个模拟，并说一个类需要添加 2 个数字，并通过调用方法 *Store* 使用 *StorageService* 存储结果时，我现在已经将 how 绑定到测试中。改变破坏测试的方式。

这就是我们现在要看的。如果你读过我的一些[其他回归基础的帖子](https://simpleprogrammer.com/back-to-basics-series/)，你可以看到到目前为止的进展。为了单元测试的缘故，我一直不考虑使用接口和依赖注入，但是我还没有提供一个替代方案。我还是不知道。老实说，我还没有。但是，我确实相信通过分解这个问题的根源，我们可以评估我们正在做什么，并确定我们真正的问题是什么。

在本系列的最后，我希望能够找到解决这类问题的方法和建议。