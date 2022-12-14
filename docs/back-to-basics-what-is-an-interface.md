# 什么是接口？

> 原文：<https://simpleprogrammer.com/back-to-basics-what-is-an-interface/>

这是我的[回归基础系列](https://simpleprogrammer.com/2010/10/30/getting-back-to-basics-introduction-and-why/)的第一部分。

我觉得我们真正需要回归的一个基础是对接口价值的使用和理解。

在像 C#和 Java 这样的语言中，接口是非常常见的。它们比 5-10 年前更常用。

但是我们必须问自己的一个问题是，“我们是否正确地使用了它们？”

## 接口解决什么问题？

我希望你花一点时间，理清你目前是如何使用界面的。

我想让你暂时假装不知道什么是接口。

准备好了吗？

一个接口试图解决的基本问题是把我们如何使用一个东西和它如何被实现分开。

为什么我们要把使用和实现分开？

这样我们就可以编写代码来处理一些职责的各种不同实现，而不必专门处理每个实现。

更简单地说，这意味着如果我们有一个*驱动程序*类，它应该能够有一个方法*驱动程序*，该方法可以用于驱动任何汽车、船或其他实现了 *IDriveable* 接口的类。

*驱动程序*类不应该必须有一个*驱动程序*、*驱动程序*或*驱动程序*方法用于每一种支持驱动它所需的相同基本操作的类。



![Driver-Race-Car](img/7ffa5ecc1b82f0f22da4758d169acabf.png "Driver-Race-Car")



界面试图解决一个非常具体的问题，它允许我们基于对象做什么而不是如何做来与对象交互。

## 接口是契约

接口允许我们指定一个特定的类满足其他类可以依赖的某些期望。

如果我们有一个实现接口的类，我们就可以确定它将支持该接口中定义的所有方法。

乍一看，接口似乎类似于具体的继承，但是有一个关键的区别。

具体继承说*汽车*是*汽车*，而一个接口说*汽车*实现了*可驾驶*接口。

当一个类实现一个接口时，并不意味着这个类就是那个接口。由于这个原因，完全描述一个类的功能的接口通常是错误的。

一个类可以实现多个接口，因为每个接口只讨论该类能够完成的特定契约。

## 接口总是由多个类实现

你可能会说“不，它们不是，我这里有一个类，它有一个其他类没有实现的接口。”

对此我说，“你做错了。”

但是，别担心，你并不孤单。我也做错了。我们中的许多人不再正确地使用接口，而是使用它们，因为我们有一种印象，我们永远不应该直接使用具体的类。

我们害怕紧密耦合我们的应用程序，所以我们为每个类创建接口，不管我们是否需要一个接口。

我说接口总是由不止一个类实现是有一些很好的理由的。

还记得我们说过界面是如何被设计来解决特定问题的吗？

在我的例子中，我谈到了 *Driver* 类不应该拥有它可以驱动的每种类的方法，而是应该依赖于一个*IDrivable*接口，并拥有一个通用的 *Drive* 方法，该方法可以驱动实现 *IDrivable* 的任何东西。

我们大多数人都接受 YAGNI 原则，即“你不会需要它”如果我们只有一个 *Car* 类，并且没有任何其他需要由 *Driver* 类驱动的类，我们就不需要接口。YAGNI！

在某个时候，我们可能会添加一个*船*类。只有在那个时间点上，我们实际上有了一个接口将解决的问题。到目前为止，添加接口是为了解决将来的问题。

如果你认为你擅长预测你什么时候需要一个界面，我希望你做一点练习。进入你的代码库，数一数你所有的接口。然后统计实现那些接口的所有类。我打赌这个比例接近 1 比 1。

## 但是我将如何测试呢？我将如何使用依赖注入？

这两个原因可能是错误使用接口的最合理的原因。

我为证明创建一个接口是正确的而感到内疚，这样我就可以有一些东西来嘲笑，我也为仅仅为我的依赖注入框架创建一个接口而感到内疚，但这并不意味着它是正确的。

我不能在这里给你一个简单的答案，说我可以在没有接口的情况下解决你的单元测试或依赖注入问题，但是我可以谈谈为什么我们不应该弯曲源代码来适应工具或方法。

我之前谈过[单元测试的目的](https://simpleprogrammer.com/2010/10/15/the-purpose-of-unit-testing/)，其中一个主要的好处是单元测试有助于指导你的设计。单元测试帮助我们解耦我们的应用程序，并通过使尝试和单元测试具有多个依赖项的类变得非常痛苦，将我们的类合并到单一的职责中。

接口是一种捷径，它让我们可以摆脱一个类中的大量依赖。

当我们把一个具体类的引用变成一个接口引用时，我们就是在欺骗系统。我们假装我们的类是解耦的，因为它引用了一个接口而不是一个具体的类，从而使编写单元测试变得更加容易。实际上，它不是解耦的，而是更强的耦合，因为我们的类耦合到一个接口，而这个接口又耦合到一个类。我们所做的只是增加了一个间接层。

依赖注入促进了同样的接口滥用问题。至少在今天的 C#和 Java 中是这样的。仅仅为了能够将接口的唯一实现注入到一个类中而创建接口会产生不必要的间接性，并且不必要地降低应用程序的性能。

不要误解我。依赖注入很好。我将把细节留到另一篇文章中，但是我相信依赖注入的真正好处是当它用于控制使用接口的哪个实现时，而不是当接口只有一个实现时。

最终，我无法给你一个好的答案，告诉你如何在不滥用接口的情况下进行单元测试或者使用依赖注入。我认为你可以通过选择分离类来减少滥用，并实际减少依赖性，而不是简单地创建一个接口并将其注入到类中，但你仍然会有一个问题，一辆*汽车*有一个*引擎*，如果你想对汽车进行单元测试，你要么必须使用真正的引擎，要么找到一种方法来模仿它。

这里的关键问题是接口是语言的一部分，但是单元测试和依赖注入不是。我们试图用一个技巧让他们适应这种语言。诀窍是我们创建一个接口来提供类之间的接缝。问题是我们这样做削弱了接口的效力。我们真正需要的是一种语言支持的 seam，允许我们在运行时轻松替换具体类的实现。