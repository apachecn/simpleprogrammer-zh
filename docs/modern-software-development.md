# 现代开发人员，第 3 部分:开发

> 原文：<https://simpleprogrammer.com/modern-software-development/>

<figure class="alignright is-resized">

![](img/ad4f78b2997f96385c1bd40405f3c932.png)

</figure>

当前开发软件的方法是基于敏捷的(例如 scrum)。工作是在一至六周内逐步完成的，称为冲刺。在增量的末尾，期望有一部分软件准备好，可以展示并接收反馈。

根据反馈，要么软件的下一部分将在下一次 sprint 中开发，要么上一次 sprint 中完成的部分将被返工。

主要思想是，短的反馈循环降低了失败的风险。损失的时间越少越好。通过一次做一个特定的子系统，任何变更、增强和返工都可以在开发团队专注于软件的特定部分时完成。

然而软件项目总是被延迟，并带着缺陷交付。在本系列的第三部分中，我们将看看开发问题背后的原因，以及解决这些问题所需的策略和工具。

## 软件开发问题

虽然开发人员通常会尽最大努力，并且对一个项目只有最好的意图，但大多数软件项目都会延迟，并且在生产中总是会出现 bug。

为什么会这样，是什么让软件开发如此艰难？

当然，没有单一的答案，但是根据我在企业和创业项目中的经验，有一些重复出现的问题。

首先，需求往往会动态变化。编写做特定事情的代码很容易；有经验的开发人员甚至可以预测和避免大多数 bug。
T1。med rectangle-4-multi-110 { border:none！重要；显示:屏蔽！重要；浮动:无！重要；行高:0；边距-底部:15px！重要；左边距:0！重要；右边距:0！重要；margin-top:15px！重要；最大宽度:100%！重要；最小高度:250px 最小宽度:250 像素；填充:0；文本对齐:居中！重要}

然而，需求通常并不明确。它们是抽象的；他们缺乏细节和用例。

在理想世界中，开发人员可以询问不确定性，并立即得到清晰、简洁的答案。然而在现实中，情况并非如此。

很多时候，人们不能给出一个明确的答案，或者没有被授权做决定。此外，一些特定的用户故事可能需要召开几次会议来决定。尽管如此，一个体面的开发人员可以抽象出代码中不清楚的部分，使其更加灵活，因为在 sprint 结束时，他们必须展示一些准备好的东西。

然而，对代码进行抽象是有代价的:它不太具体，而且会漏掉一些错误。

由于这些不确定的需求，不可能马上写出最佳的代码。更糟糕的是，在发布之前，需求往往会改变几次。

开发人员讨厌这样，这是有充分理由的:他们必须扔掉代码，重写代码。他们正在编写的代码必须允许改变容易发生，因为他们没有足够的时间从头开始实现。

为了保护业务，在测试表明需求不是最佳的，或者更糟的是，它们根本没有达到预期的效果之后，就对需求进行变更。

例如，结果可能是某种支付方式在软件的目标受众中不受欢迎，因此必须进行新的集成。

当然，这不是唯一的问题。很多时候，新功能是在移动中添加的。同样，它们被认为是产品成功的关键，但时间表保持不变。

<figure class="alignright is-resized">

![](img/7bb404c5812cacbff828d495b23b6d6e.png)

</figure>

由于缺乏时间，这些问题往往是仓促的，质量很差，有很多 bug，但是这些特性最终还是被发布了，因为它们是业务所需要的。

这是否意味着开发人员正在受到业务的破坏？软件中的延迟和错误是严格地由于在相同的时间框架内改变需求和增加更多的东西吗？

**号**号

最初，几年前，我很难承认这一点，但事实是人们(阅读:每个人)不能估计任务。更糟糕的是，开发人员通常没有做好承担项目的充分准备。

这是为什么呢？开发人员不应该知道如何构建软件吗？现代软件开发在很大程度上不就是把不同的系统和服务粘在一起吗？为什么这么难？

为什么精确的评估几乎是不可能的这个问题在这里得到了很好的解决，所以我将解释为什么开发人员在一些项目上遇到困难。

大多数项目包含开发人员没有使用过的技术。我不是在谈论编程语言、操作系统等等。

这些技术应该是已知的，开发者应该不会有问题。如果开发人员不了解他们的工具并且不能很好地使用它们，那么他们很可能不是一个伟大的开发人员。

软件开发人员遇到困难的技术主要有两种。

第一个是与第三方软件/服务的集成。通常，有一些细节没有记录下来，开发人员必须找到它们并自己解决它们。
T1。leader-3-multi-119{border:无！重要；显示:屏蔽！重要；浮动:无！重要；行高:0；边距-底部:15px！重要；左边距:0！重要；右边距:0！重要；margin-top:15px！重要；最大宽度:100%！重要；最小高度:250px 最小宽度:250 像素；填充:0；文本对齐:居中！重要}

尽管预先研究和测试服务可以减少花费的时间，但通常在开发周期开始之前没有时间研究将要使用的第三方服务。

第二个是软件的核心——独特的部分，不存在，必须从头开始。通常，存在隐藏的复杂性和边缘情况，使得实现比最初预期的要困难得多。

不是每个项目都有一个复杂的核心。不是每个项目都有第三方集成。根据我的经验，没有复杂核心的项目，例如 WordPress 站点和网络商店，通常有很多集成和插件。

你可能会问自己:软件开发怎么会这么乱？跟宣传的和我想象的差远了。事实是，软件开发在现实世界中是混乱的。理论上，在像大学这样孤立的环境中，这看起来比实际上容易得多。

尽管如此，还是可以采取一些措施来降低混乱程度。

到目前为止，我们已经讨论过的问题有:

*   不断变化的要求
*   在不增加时间和资源的情况下增加更多工作
*   不熟悉第三方系统
*   处理软件的复杂核心

让我们将问题分为外部(改变需求和增加更多需求)和内部(熟悉专门的软件/服务和处理模糊复杂的任务)。

## 解决问题

一个常见的策略是高估。比如说一个项目，估计要两个月才能完成。如果你多加两个星期，你会考虑到一些变化。

你可以侥幸高估；然而，它必须有一个合理的数量，因为如果你想要多 50%的时间，那么很可能人们不会给你任何额外的时间。

另一个关键的事情是对延迟保持开放。如果某件事花费了比预期更多的时间，不要独自承受。告诉相关人员。你可能会得到一些帮助，你可能会得到更多的时间，一些不太重要的功能可以推迟。

<figure class="alignright is-resized">

![](img/e8167e8bd35f73eda53ff7a31bc9fe3f.png)

</figure>

就新功能而言，最重要的是对可能的事情持开放态度。解释什么时候事情不能在一个时间框架内完成。询问另一个特性是否可以推迟到初始发布后完成。

即使很多人会告诉你“一切都很重要”，其实不然。大多数东西都很好拥有，尽管它们会增强你正在开发的软件，但它们不是业务关键的。

## 采用正确的心态

好消息是内部问题可以由开发人员通过采用适当的思维方式来处理:

为你的错误负责。当你低估了某事时，不要撒谎。承认你的错误，并建议一个可以修复它的方法，即使你不得不推迟这个功能。你越是试图隐藏自己的错误，它们就越会拖累你。

说出真相，不要设定不切实际的期望。乐观地说话很有诱惑力。不要这样做，因为这可能会伤害公司，迫使你加班。保持事情简单——不要误导任何人。

不要让自我成为阻碍。我可以写一整篇关于自我如何毁掉有前途的软件项目的文章。最棒的是我可以拿自己做例子。永远，永远，永远试着把你的目标记在心里，不要试图向任何人证明什么。你工作的质量应该是关于你的技能，而不是你。

自我是很难控制的。我时常在这方面失败，而且还没有创造出积极的体验。每次我放松自我，我都会让事情变得更糟，然后我必须先解决问题，然后我们才能继续解决现有的问题。

更糟糕的是，自负在软件开发人员中非常普遍，所以当你大声说话时，你可能会与某人进行不必要的、破坏性的争论。不要让自我妨碍你。不要制造另一个问题。

不要因为压力而危及你作为专业人员的工作——你作为开发人员的责任是产生[高质量、可维护的代码](https://simpleprogrammer.com/hunting-mythical-high-quality-code/)。你不能牺牲它，尽管它很诱人，因为它会产生技术债务，这将导致软件的未来增强被延迟，并且会使软件的调试和维护更加困难。

到目前为止，我们已经讨论了现代开发人员面临的主要问题，以及他们的一些解决方案。我们还讨论了需要采取的心态。

我们现在要讨论的重要部分是现代开发者需要的策略和工具。

## 现代开发者的策略

采用正确的习惯，从上到下设定正确的意图，会帮助你更加专注。当你更加专注时，你将能够更好地[流动](https://simpleprogrammer.com/keep-your-code-flowing-an-introduction-to-flow-states-for-programmers/)。流量越好，增值越多。

有一个*时间结构*对每个人都有帮助。不幸的是，我们生活在一个让我们分心的时代。你可以安排自己的时间，每 30 分钟左右查看一次通知。

[番茄工作法](https://simpleprogrammer.com/get/pomodoro-technique)是软件开发人员的时间结构策略。

总而言之，你把你的时间分成几个间隔，在这些间隔中你可以不受任何干扰地工作，比如说 25 分钟。之后，你有一个短暂的休息，通常是五分钟，每四个番茄，你有一个更长的 30 分钟的休息时间。这个想法是你把你的任务分解成小的、可管理的块，然后快速看到进展。如果你走错了方向，你不会浪费超过 30 分钟。它已经被证明是有效的，许多人称赞它是一个生产力节约器。

<figure class="alignright is-resized">

![](img/fa2651f2aaae829e8d92e2eef0a3ad41.png)

</figure>

当我没有任何计划的会议时，我在工作中使用它，它产生了奇迹。我并不是每天都使用它，因为有时由于会议分散在一天中，它增加了一个不必要的结构层。

首先处理高风险的任务。编程的一个缺点是，在看到工作结果之前，你必须等待相当长的时间，这促使许多开发人员首先完成快速任务。

这是适得其反的。这不是高中考试；高风险的任务不仅仅是项目的一部分，如果它失败了，将会导致整个项目失败。在软件开发中，你不能跳过它们，只得到 B 而不是 A——要么全有，要么全无。

你不必 100%完成这些部分，但是你应该确保它们能够工作，并且做大部分的工作来验证它们不会成为一个阻碍。

这意味着你可能有相当一部分时间没有 100%完成任何事情。尽管这可能会让人泄气，但相信我，更让人泄气的是必须向团队解释为什么过去几周的共同努力会付诸东流，因为此时高风险的任务是不可能完成的。

确保收到反馈。如果你不确定某事是好是坏，请寻求反馈。如果你确定，不管不问！令人震惊的是，如果其他人快速浏览一下代码，会发现多少错误。

不要忘记，虽然你独自编写大部分代码，但你有同事是有原因的——互相帮助。一个以前没见过代码的同事花几分钟时间审查代码可以节省几个小时的调试时间。

尽量减少浪费在会议上的时间。我在这里的最佳建议是，只参加你能积极增加价值的会议。很多会议都是在两三个人之间进行的，每个人都拉着几个人一起参加，以寻求更多的支持。如果不能积极贡献，还不如跳过。

## 现代开发人员的工具

就硬件而言，使用任何适合你的特殊需求并且在预算之内的东西。最被忽视的资产是人体工程学。请记住，您将在工作站上呆很多个小时。确保它是舒适的，不会给你带来任何痛苦。

此外，考虑一下你的眼睛——也许买一副眼镜或者选择一个内置保护的显示器。降噪耳机也值得考虑。

我已经写了很多关于[文本](https://simpleprogrammer.com/text-editor-wars/)编辑器的文章，但这并不是你需要配置和记住的唯一事情。代码棉签，风格检查，基本上任何能让你交付更高质量工作的东西都应该被使用。

你设置的东西必须是自动化的。例如，在提交时运行所有与代码相关的检查器，如果其中任何一个失败，就拒绝提交。这样，你就不会忘记任何检查，也不会提交质量不合格的作品。如果检查器不是自动化的，你将跳过其中的一些，它们将是一个负担，而不是帮助。

当涉及到支持软件时，使用任何你觉得合适的软件。确保您正在使用的软件得到积极支持是很重要的。了解它存储什么数据(如果有的话)以及存储在哪里也很重要。虽然我主要使用开源软件，但我偶尔也会购买商业软件。

尽量只使用你需要的软件。如果你的版本控制系统需要一个图形客户端，那就只需要一个。不要购买多种软件产品，因为你不会很好地学习它们。

选择工具时，确保它是可配置的。你应该及时让它适合你的个人需求和你的个人工作流程。

这应该包括重要的工具。如果你需要的话，可以随意添加，但是请记住:太多的工具会降低你的速度，分散你的注意力，而不是帮助你快速交付高质量的代码。

## 相信这个过程

有了正确的心态、工具和策略，剩下的唯一事情就是信任这个过程。像任何努力一样，会有起伏。有些日子会好，有些日子会坏。

重要的是要相信过程，遇到困难时要坚持，不要放弃。

软件是复杂的，需要很多年才能掌握，但是如果你开始应用我在这篇文章中与你分享的策略和心态，你很快就会看到积极的变化。