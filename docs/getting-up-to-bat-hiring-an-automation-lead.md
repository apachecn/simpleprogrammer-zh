# 行动起来:雇佣自动化领导者

> 原文:[https://simple programmer . com/get-up-to-bat-hiring-an-automation-lead/](https://simpleprogrammer.com/getting-up-to-bat-hiring-an-automation-lead/)

这是我关于全自动黑盒测试系列文章的第一篇，我喜欢称之为 BAT。

在我的[基础系列](https://simpleprogrammer.com/2011/02/05/back-to-basics-becoming-bat-man/)的上一篇文章中，我提到我将开始这个系列，目的是一步一步地向您展示如何从无自动化到高质量的 BAT 基础设施。

到本系列结束时，您应该已经获得了在您的组织中实际进行自动化测试所需要的信息，而不仅仅是说说而已。

这趟列车的第一站是招聘自动化主管。

## 开始前不要自寻死路

如果你认为你将创造蝙蝠，但你不会有至少一个专门的资源来完成这一切，你可能注定要失败。



![DOOM4](img/a317a974cffb0677df30aced1fa33f6d.png "DOOM4")



听好了，因为这是大多数组织在试图激励员工时犯的最大错误。

这种想法是错误的，你可以让你的 QA 团队来做这件事，你可以兼职一些开发人员到这个项目中，但是没有一个专门的资源。

为什么这是绝对荒谬的，你应该期待它会失败？因为，为了获得支持 bat 的基础设施，您需要设计和创建一个测试框架，该框架是为您的应用程序的业务领域量身定制的。

胡说什么？好吧，简单来说。有人需要设计和构建一个自动化框架。

如果你认为你只是去买一些工具，并用它来记录测试脚本，那你就错了。这种方法根本行不通。我不会在这里讨论为什么，但我在过去的中已经写了[，如果你感兴趣，请告诉我，我会更深入地讨论。](https://simpleprogrammer.com/2009/12/18/automated-functional-testing-record-or-program/)

想一想，你希望你的 QA 团队，像他们一样擅长 QA 工作，设计和构建一个自动化框架吗？给他们一些 C#或 Java 类，让他们的第一个真正的编码工作是设计一个复杂的系统？

如果一个开发人员有“真正的”工作，只能花部分时间来设计最终可能成为你的基础设施中最重要的部分之一的东西，那该怎么办？

将开发人员从主产品中抽离出来并让他们担任这个角色是很好的，直到它启动并运行，但是不要犯错误，你需要一个专门的资源。

你会想要一个设计良好的可维护的自动化框架，因为该框架的易用性将决定使用该框架编写自动化测试的难易程度。

## 我建议找一个以前做过的人

为什么？因为创建一个自动化框架与开发你的软件有很大不同，与编写测试也有很大不同。这确实需要一套特殊的技能，如果没有这方面的经验，是不容易掌握的。

我也认为使用开发人员资源是没问题的，但是如果你这样做了，你会想找一个更资深的开发人员来担当这个角色。

以下是我认为重要的一些技能，这些技能也可以更清楚地说明我为什么在这种情况下推荐专家:

开发 API(最终，自动化框架将是一个用于编写自动化测试的 API。API 设计得越好，针对它编写测试就越容易。)

**可重用基础组件的设计**(框架的大部分由重复的概念组成，对于应用程序中不同的屏幕有不同的变化。因此，该框架的核心将是一个基本的设计，允许没有太多重复的变化…重用)

**快速获取软件领域知识的能力**(编写自动化框架的人需要真正理解测试中的系统是如何工作的，这样他们就可以在之后对框架进行建模。)

**实用主义**(很多“被接受”的好软件设计实际上是糟糕的自动化框架设计。静态方法可以使自动化框架的 API 更容易使用，特别是对于非程序员，但是在你的主产品中不是一个好的设计选择。一个设计自动化框架的人应该足够务实来“打破规则”，以便使框架最容易使用和维护。)

对 QA 的经验或理解(理解框架的用户，QA 团队是很重要的。了解他们可能会写什么样的测试，或者他们会如何思考，将对提出一个好的框架设计大有帮助。)

**沟通技巧**(好的蝙蝠读起来像英语。关键是要确保设计框架的人促进这一点，使 bat 尽可能有用和可理解。)

HTML / XPath (这种特定的技能对于基于网络的产品非常重要。创建一个基于 web 浏览器驱动程序的自动化框架需要对 HTML 和 XPath 有深入的了解，这样才能访问应用程序页面上的属性和元素。)

我已经编写了一些自动化框架，并参与了其他几个自动化框架的设计，我可以告诉你，我的自动化框架 6.0 版本比 1.0 版本好得多。

这个问题领域出现了大量独特的模式。所以，我确实相信有这方面的经验是一个巨大的好处。

## 这个自动化的人是做什么的？

我们将在本系列的后续文章中更具体地讨论，但基本职责应该是:

*   确定要使用的技术和工具
*   创建初始自动化框架
*   为测试中的应用程序创建冒烟测试
*   将这些冒烟测试放入某种自动化构建中
*   培训开发人员和 QA 使用框架
*   推动框架的采用和所有功能的自动化
*   为编写自动化测试的一致性建立规则
*   自动化测试的层次和结构设计

您希望您的自动化人员负责推动和促进目标的实现，即能够以最小的努力自动化每个正在创建的特性。

这是那些实际上可以“完成”的工作之一我的意思是，您可能会让自动化主管最终创建框架，开发足够多的框架，然后将其推广到您的开发团队，并培训他们编写自动化测试和 QA，您真的不再需要自动化主管了。

这很好，因为现在你有一个真正了解你的产品的开发人员，他是 QA 的一个很好的桥梁，或者如果你想走这条路，你可以让他们改进框架并监督它。

底线是:

1.  确保你有专门的资源
2.  确保资源可以编写代码和设计框架
3.  确保他们培训其他所有人，一个人无法自动化整个应用程序