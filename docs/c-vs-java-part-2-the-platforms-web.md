# C#与 Java 第 2 部分:Web 平台

> 原文：<https://simpleprogrammer.com/c-vs-java-part-2-the-platforms-web/>

Web 平台是考虑任何现代软件开发环境的一个关键因素。

回到 C++时代，这根本与平台无关。这是关于了解语言和指针操作的复杂性。

现代编程语言更多的是关于平台和库，而不是语言本身。在 Java 和 C#中，知道哪些库可用以及如何使用它们比知道语言的所有特性重要得多。一个了解平台和基础类库的开发人员将比一个语言专家完成更多的工作，这与过去的编程方式形成了鲜明的对比。

在我深入研究 web 平台之前，还有一点需要注意。当我在这里使用术语平台时，我实际上指的是技术平台、基本类库和一般的框架。

**网络**

*Java*

很长一段时间以来，Java 一直统治着 web 平台。如果你正在做基本的 Java web 开发，你很可能会使用 Java EE 5 或 Java EE 6，它们过去被称为 J2EE。除了这一共性，其余的都是一个很大的问号。这里的是开发 Java EE 应用程序的 10 个流行框架的列表。

Java web 框架非常庞大，跨越了许多不同的关注点，选择令人望而生畏，但它们也非常好。很长一段时间以来。NET 社区正在将控件拖放到. aspx 页面上，而 Java 社区正在构建具有不同关注点分离的高度可伸缩的模型视图控制器( [MVC](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) )框架。

大多数 Java web 应用程序框架都构建在 Java SE 中可用的基本框架之上，特别是围绕 applets 和 beans。当前这一代的基本 Java SE 规范已经得到了极大的简化，使得编写企业 web 应用程序比过去容易得多。这是平台和工具有点重叠的地方。在选择了一个用 Java 开发的 web 框架(几乎所有的框架都是某种 MVC)之后，如果你有一个支持在这个框架上开发的工具(IDE 插件)，在这个框架上开发会非常容易。

困难就在这里…信息过载。如果你看一下 Java web 框架的列表，你会发现有很多可供选择，每一个都需要大量的研究才能理解。有些甚至是组合的，比如 Struts + Spring。公平地说，框架的扩散部分是由于平台的老化。如果你能涉水通过选择，并解决一个框架，大多数好的是真的好和证明。

*C#*

ASP.NET 在很长一段时间内都是类似于网络表单。在 ASP.NET MVC 发布之前，C# web 开发的唯一方法是使用 ASP.NET Web Forms。这项技术还不错。它只是没有足够的指导。您可以轻松地将控件拖放到页面上，让它自动填充数据库中的数据，并且允许编辑这些数据，而无需编写一行代码，这真是令人惊讶。惊人的，但在一个'违反所有分离的关注，混合我所有的层在一起，看！我直接从用户界面访问数据库。

别误会我的意思。我试图做到公平和诚实，Java 在我之前关于语言的文章中受到了打击；ASP.NET 网络表单将在这里采取一个。也就是说，是的，使用 ASP.NET Web 窗体编写一个好的关注点分离 MVC 风格的应用程序是可能的。是的，可以编写一个 ASP.NET web 窗体应用程序，它正确地使用使用数据访问层的业务对象，同时仍然将业务对象或数据传输对象绑定到 UI。在 MVC 出现之前，我构建了几个 ASP.NET 应用程序来实现这个功能。问题是你真的必须想出创造性的方法来做这件事，而且没有任何真正的指导。我总是觉得这个平台试图把我推向拖放，就像一个小恶魔坐在我的肩膀上说“但是直接将控件绑定到数据库要容易得多。看，向导会帮你做的。”

幸运的是，ASP.NET MVC 平台已经解决了这个问题。它是非常新的，仍然需要一些成熟，但是它鼓励好的设计实践来分离关注点。在幕后，它仍然默认使用 Web Forms 视图引擎，但是可以用任何数量的视图引擎替换掉。在我看来，ASP.NET MVC 仍然有一点复杂的问题，特别是关于 AJAX。我知道有些问题已经解决了，但是有些人会发现很难从一个可以拖放服务器控件、用向导设置其属性并自动为您生成 HTML 的平台发展到一个必须手工编写大量 HTML 代码的平台。ASP.NET MVC 使用 HTML 助手类来帮助你渲染 HTML，这是很好的一步，但我认为它仍然有一些改进的空间。

微软在获取关于如何在 ASP.NET MVC 中开发的信息方面也做得很好。这是 MVC 大放异彩的领域之一。当我去搜索如何在 Swing 或 Struts 上进行开发时，有一些教程，但是没有一个像 ASP.NET MVC 的信息量那么大，那么容易获取。

*富互联网应用(RIA)*

关于这个主题的快速简介。。NET 和 Java 在这个领域都有 Adobe Flex 和 Air 的竞争对手:Silverlight 和 JavaFX。Silverlight 和 JavaFX 之间根本不存在竞争。JavaFX 没有可视化设计，需要学习一些奇怪的混合了抽象层的新语言。Silverlight 为您提供了。NET 框架，并通过 XAML 与 Windows 演示基础(WPF)使用通用设计。我不知道孙是怎么想的。

*结论*

如果不给出这么多细节，很难对这些网络平台进行比较。我真的还没有深入研究过。Java EE 有一个大得多的 web 平台，但也更加分散。ASP.NET 只是在两种技术之间分裂，但是 MVC 平台在这一点上还不是很成熟(虽然它的成长和改进速度极快。)作为开发人员的一个考虑因素是专门化。不可能成为每个 web 平台或框架的专家。如果你走 Java 路线，你最好小心选择，因为开源开发的本质导致了许多死亡项目。对学习的大量投资可能会付诸东流。在这一点上，ASP.NET MVC 仍然是一场赌博，但我认为这是一场好的赌博，因为微软在这方面投入了大量的资源，而且采用的范围似乎很广。

**未完待续……**

我原以为在这篇文章中我能够涵盖的不仅仅是网络，但是我并没有意识到网络平台有多少。明天我们将讨论 C#与 Java 在桌面开发方面的对比，未来的章节将涉及 IO 操作、数据库和并发性以及移动性。