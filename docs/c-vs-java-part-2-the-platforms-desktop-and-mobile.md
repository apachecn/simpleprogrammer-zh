# C#与 Java 第 2 部分:桌面和移动平台

> 原文:[https://simple programmer . com/c-vs-Java-part-2-the-platforms-desktop-and-mobile/](https://simpleprogrammer.com/c-vs-java-part-2-the-platforms-desktop-and-mobile/)

在这篇文章中，我们将同时关注 C#和 Java 的桌面和移动平台。

**桌面(胖客户端应用)**

桌面平台，或者说胖客户端，已经不像几年前那么重要了，而且似乎越来越不重要了。虽然，就像钟摆一样，开发似乎在瘦客户端和思考客户端体验之间来回摆动。似乎当前的趋势是瘦客户机包中的胖客户机功能。(浏览器作为操作系统)。在这篇文章中，我将假设开发一个真正的胖客户端应用程序，它在客户端计算机上本地运行，并从客户端计算机安装或执行。(尽管如此，当我说这句话的时候，我意识到 Adobe Air 和 Silverlight 让这条线变得模糊了。)

*Java*

这里没有太多的选择。真的，有两个选择。[摇摆](http://en.wikipedia.org/wiki/Swing_(Java))或 [SWT](http://www.eclipse.org/swt/) 。我在这里坦白我的无知。我对 Swing 唯一真正了解的是，很久以前我写了一个应用程序，它使用第二个线程在屏幕上弹出图像。我试图在这里做一些研究，但我没有得到大量的信息。可能是因为已经没有多少人真正用 Java 进行胖客户端开发了。我问了我认识的最好的 Java 开发人员之一(Sreenivasa Majji)，他能够给我一些信息。

显然，自从我上次使用 Swing 以来，它已经变得更快更容易使用了。以我的理解，Swing 相当于上一代的。NET 胖客户端框架。SWT 似乎也有类似的功能，包括数据绑定。Java 在这方面的真正优势是多平台能力。Java 桌面应用程序可以在任何支持 Java 的操作系统上运行。(这几乎是任何操作系统。)部署一直是胖客户端应用程序中的一个问题，而 [Java Web Start](http://java.sun.com/developer/technicalArticles/Programming/jnlp/) 试图通过允许客户端访问网页来启动应用程序来解决这个问题。

我听到有人抱怨说，在斯温或 SWT 问题上没有取得多大进展，这似乎是真的。我知道找到关于这些技术的信息并不容易。

*C#*

当前一代的 C#胖客户端应用程序使用 [WPF](http://en.wikipedia.org/wiki/Windows_Presentation_Foundation) 。WPF 基本上是 DirectX 库的包装器，它使用 XAML(一种基于 XML 的缩放矢量图形 UI 约定)来创建用户界面。WPF 开发在许多方面不同于 Windows 窗体开发。WPF 开发非常清楚地将 UI 与 UI 背后的逻辑分开。XAML 用于定义布局和存在的元素。UI 几乎可以完全由设计师独立开发。UI 中的一切都是完全可定制的，任何控件都可以从一个矢量表示中绘制出来，取代该控件的默认版本。动画和三维图形很容易实现，因为 WPF 是建立在 DirectX 而不是 Win32 库。UI 也是可扩展的，因为一切都用矢量图形表示。

用 C#使用 WPF 进行桌面开发非常不错。我自己没有做过大量的 WPF 开发，但是我所做的非常简单明了。使用任何 SVG 图像或动画的能力可以创造出一些非常好的 ui。不过，这也可能导致一些相当不一致的用户界面。我认为 WPF 的一个主要优势是它使用 XAML，这与 Silverlight 使用的技术相同。我知道 Silverlight 和 WPF 在这一点上不是 100%兼容，但是它们有很多共同点。我听说过一些试图抽象它们之间差异的框架，但是我还不知道哪一个做得真的很好。我确信会有一个被开发出来，或者微软会在不久的将来提供一个解决方案，使得构建一个可以作为 WPF 或 Silverlight 应用程序轻松运行的应用程序成为可能。

*结论*

在这种情况下，我认为这取决于你的客户群在哪里。如果你的目标是 Windows 用户群，我认为很难找到一个理由来使用 Java 而不是 C#进行桌面开发。如果你的目标是一个多操作系统的安装基础，C#可以用于使用 [Mono](http://www.mono-project.com/WinForms) 进行 Windows 窗体应用程序开发，但是 Mono 不支持 WPF。如果您必须使用胖客户端，Java 是进行多平台安装的最合理选择。我尤其不想尝试和解决一个在 Mono 和。NET CLR。我倾向于看到大多数传统的桌面应用程序被像 Adobe Air、Silverlight 和 JavaFX 这样的富互联网应用程序(RIA)技术所取代。这里还有一点要注意。Java 和 C#能够调用非托管库(或本机代码)，对 C#使用 [P/invoke](http://en.wikipedia.org/wiki/Platform_Invocation_Services) ，对 Java 使用 [JNI](http://en.wikipedia.org/wiki/Java_Native_Interface) 。如果你需要这样做，C# P/invoke 比 JNI 容易得多，尤其是 C# 4.0 中增加了*动态*关键字。

**手机**

欢迎来到下一个战场。这个平台现在正处于严重动荡之中。微软正在被苹果和谷歌杀死，这两家公司都提供了更好的用户体验。与其他平台不同，这里的语言和技术的选择更多地是由采用而不是便利性驱动的。我的意思是，基于语言或功能来决定使用什么技术几乎没有意义，更多的是基于你想要针对什么样的设备，以及谁正在赢得移动设备战争。现在，这并不完全正确，因为在 iPhone 和 [Android](http://stackoverflow.com/questions/1443690/is-there-a-way-to-develop-c-net-on-android-devices) 平台上，都有用 C# [开发的方法。](http://arstechnica.com/open-source/news/2009/01/open-source-mono-framework-brings-c-to-iphone-and-wii.ars)

*Java*

谈到 Java 移动开发，有两个分支， [Java ME](http://java.sun.com/javame/index.jsp) 和 Android 开发。如果你愿意，你可以不同意我的观点，但就我而言，移动设备上的 Java ME 已经奄奄一息了。然而，这个想法很棒。在最广阔的领域，移动电话上进行多平台开发。但是，用户体验非常糟糕。我有几部运行不同操作系统版本的手机，每部手机上都有一些 Java 应用程序，它们并不是很好，也没有很好地集成到手机中。反正苹果把 Java 挡在了 iPhone 之外，这是一个巨大的市场领域。

所以，我们来说说安卓。安卓太牛逼了。我喜欢这个想法，技术很棒，它在不断改进，建筑也很棒。干得好，Google，你为 Java 开发人员提供了一个易于开发的平台，使他们能够快速适应并使用它来编写丰富的移动应用程序。Android 开发基本上是编写 Java 代码，这些代码被转换成位于 Linux 内核和一些图形 API 之上的专用 JVM。应用程序使用提供者模型，该模型允许不同应用程序的混搭，因为一个应用程序的请求可以由另一个应用程序的一部分来完成。如果使用 Eclipse，开发环境需要几分钟来设置。通过使用布局和资源，UI 很好地与代码分离。在这一点上，我唯一真正的不满是，您目前必须通过 ID 查找资源，然后将资源转换为适当的类型。构建已经使用代码生成来创建一个 R.java 文件，该文件保存对所有资源的引用。我不明白为什么 Google 没有让代码生成为每个资源生成强类型方法。也许我是 Android 的粉丝，但我不得不说，我喜欢它，我认为它是移动市场的未来之王。

*C#*

你知道用 C#创建一个 Windows Mobile 应用程序有多简单吗？这很简单，如果我给你 Visual Studio 和 5 分钟时间，你可能会知道如何让“Hello World”出现在 Windows Mobile 模拟器上。真的，就是这么简单。现在的 Windows Mobile 版本如此欠缺，真是太可惜了。别误会我的意思。Windows Mobile 功能强大。令人惊讶的是，你可以用 Windows Mobile 如此轻松地做什么，因为你几乎拥有整个。NET 框架唾手可得。这是一个设计良好的操作系统，它运行应用程序非常好，它将我们都非常熟悉的 Windows 外观和感觉很好地转移到移动设备上。但是，这正是问题所在。它并不是真正为手机设计的操作系统。至少不是人们真正想用手机的方式。

那么，我们来谈谈使用 C#开发 Windows Mobile 的开发环境。这几乎与开发 Windows 窗体应用程序一模一样。这非常简单，而且在很大程度上，你甚至没有意识到你是在为一部手机开发。模拟器内置在 Visual Studio 中，您只需点击 run，它就会启动模拟器和您的应用程序。的。NET compact framework 的功能比完整版少。NET 框架，但大部分都在那里。不过，一个困难是试图进入手机的核心服务。这并不容易。例如，尝试替换拨号器应用程序实际上是不可能的。

Silverlight mobile 可能会拯救移动设备上的 C#开发，如果微软能够设法将其引入 iPhone 和 Android 的话，但现在还不知道。此外，使用 Windows Mobile 7 的下一代 Windows Mobile 设备可能会改变微软的游戏，但随着 2010 年第四季度的发布日期，我担心它会在到来时死亡。

*结论*

移动开发有点像现在的蛮荒西部。入驻一个技术平台风险巨大。我把赌注压在 Java 和 Android 上，因为在我看来，这是好的操作系统和好的开发环境的最佳结合。我并没有真的提到这一点，但是使用 objective C 进行 iPhone 开发非常复杂，让我想把头撞墙。我做过 Windows Mobile 和 Android 开发，我想说 Windows Mobile 开发稍微容易一些，但是它们非常相似。尽管如此，我还是会选择 Java 和 Android，因为 Android 是一个更好的平台，一个不断增长的市场，并且有一个交付机制来轻松销售您的应用程序。

**遗言**

比较 C#和 Java 开发平台是非常困难的，因为关于每个平台和语言的信息太多了，但是我已经尝试了一种公平和诚实的方法。很明显，每种语言和相应的技术对于每个平台都有优点和缺点。从平台的角度来看，我无法选出一个明显的赢家，就像我在语言方面一样。在下一部分，我将讨论 Java 和 C#必须使用的非平台特定框架。

[C# vs Java 第二部分:平台(Web)](https://simpleprogrammer.com/2010/02/04/c-vs-java-part-2-the-platforms-web/)

[C# vs Java 第一部分:语言(续)](https://simpleprogrammer.com/2010/02/02/c-vs-java-part-1-the-languages-continued/)

C#与 Java 第一部分:语言