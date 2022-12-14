# 静态方法会让你震惊

> 原文：<https://simpleprogrammer.com/static-methods-will-shock-you/>

我坦白说。我不喜欢静态方法。他们让我畏缩。在面向对象的宇宙中，静态方法是反物质的。

他们不一定是坏的，但他们是危险的，因为他们使用不当。

**什么时候静态方法可以是好的**

只有两种情况下使用静态方法或变量，这并不令人讨厌。

1.  声明一个真正的全局常量，而不是全局变量。一个全局常数。例:*数学。PI* 。这是一个相当简单的说法，即宇宙只有一个实例，这个宇宙 *singleton* 包含一个数学概念 *singleton* ，其中有一个不变的性质 PI。这个概念对我们来说似乎很奇怪，因为我们习惯于在面向对象责任的上下文中不考虑 PI。如果我们设计一些奇怪的游戏，其中有不同数学概念和常数的交替宇宙，这将变得更加明显。
2.  对象创建。静态方法是一种有价值且有效的对象创建方法。采用不同参数的重载构造函数不是很清楚，通常用静态构造函数替换它们会更清楚。

写出来就更清楚了

在用法

**当静态方法不好时**

除了那两种用途，在我看来，其他任何用途都是令人憎恶的。(我想我让 [C#扩展方法](http://msdn.microsoft.com/en-us/library/bb383977.aspx)在这里滑动，因为它们在正确的条件下是如此有用，但是我保留在将来做出判断的权利。)

静态方法通常表示一个不知道它属于哪里的方法。它试图属于它所在的类，但它并不真正属于这个类，因为它没有使用这个类的内部状态。当我们从单一责任原则( [SRP](http://en.wikipedia.org/wiki/Single_responsibility_principle) )的角度来看我们的类时，静态方法通常是一个违例，因为它倾向于拥有一个与它所附加的类不同的责任。

考虑静态方法的一种方式是将其视为全局过程。本质上，静态方法可以在任何地方被调用。它只是假装是一个类的一部分，而实际上这个类只是被用作一个“标签”，它通过一些逻辑划分来组织方法。我用这些术语来看待静态方法，因为创建全局过程与面向对象设计正好相反。

静态方法的另一个主要问题是可测试性。在构建软件时，可测试性是一件大事。众所周知，静态方法很难测试，尤其是当它们创建具体类的新实例时。如果您曾经从事过遗留代码的工作，并试图为静态方法编写单元测试，您就会了解我的痛苦。

静态方法也不是多态的。如果你在一个类上创建了一个静态方法，就不能重写这个行为。您被对该实现的硬编码引用所困扰。

最后，静态方法增加了应用程序的复杂性。静态方法越多，在应用程序中工作的程序员需要了解的就越多。当在类中使用实例方法时，拥有该对象的实例将允许程序员决定可以采取的所有动作。当使用静态方法时，程序员必须知道秘密的方法，这些方法可能甚至不在他正在处理的对象上，而是操纵那个对象。让我们看一个常见的例子:日期和日期工具。

在我工作过的不止一个应用程序中，都存在日期和日期工具。Date 的存在是为了提供日期和时间的实现，而 DateUtilities 的存在是为了操纵日期和做一些事情，比如计算出一个月的第一天，或者确定假期，或者查看两个日期是否重叠。我不知道有多少次我会尝试编写一个方法来做 DateUtilities 已经做过的事情之一，因为我不知道要寻找一个名为 DateUtilities 的静态类，它具有静态方法来做我想要做的事情。作为一名程序员，我必须记住总是检查 DateUtilities 中的所有方法，看看是否有一个方法是我想要的。当您在大型应用程序中工作时，这可能是一个很大的开销，因为在助手类中有许多静态方法。也许我在这里溢出到了另一个问题，但是重点是记住有哪些实用方法存在要比在功能真正属于的类上使用一个方法困难得多。(附带说明:C#扩展方法通过允许您键入“.”来解决这个问题并查看可以在该类上操作的静态方法)。

**遗言**

所以只要记住当你创建一个静态方法的时候要仔细考虑一下。我并不主张永远不使用它们。我主张有一个真正好的理由，首先检查静态方法是否真正属于另一个可以使用状态信息的类。

如果你有技能，但你看不到你在职业生涯中应得的成功，那么一定要参加我的课程[“如何作为一名软件开发人员推销自己”。](https://simpleprogrammer.com/store/products/how-to-market-yourself/)T3】